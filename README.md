# TimeTable Generator Using Genetic Algorithm

This project aims to generate an optimal timetable for educational institutions using a Genetic Algorithm. The system handles multiple constraints, ensuring a conflict-free and efficient scheduling process. The algorithm is designed to create a timetable that accommodates professors, courses, sections, rooms, and timeslots while respecting hard and soft constraints.

## Dataset Generation

Dataframes were created for the following entities:
- **Professors**
- **Courses**
- **Rooms**
- **Sections**
- **Timeslots**
- **Days**

Each entity is encoded to simplify the process of chromosome generation for the Genetic Algorithm.

## Chromosome Generation

The timetable is represented as a chromosome, consisting of encoded and detailed data for each section, course, professor, room, day, and timeslot. Each chromosome is created by random selection, ensuring that no conflicts arise (e.g., no double-booking of rooms or professors).

## Fitness Calculation

The fitness function evaluates each chromosome by applying penalties for rule violations (e.g., scheduling conflicts, room capacity issues). The goal is to minimize the penalty to zero, which represents a perfect timetable.

### Hard Constraints
- Classes must be scheduled in free rooms.
- A professor cannot teach two classes at the same time.
- A section cannot be in two different rooms simultaneously.
- Room capacity must be sufficient for the section.
- Courses must have two lectures per week, not on the same or adjacent days.

### Soft Constraints
- Theory classes should be scheduled in the morning, while lab sessions should be in the afternoon.
- Teachers/students should not need to traverse multiple floors for consecutive classes.

## Genetic Algorithm

The Genetic Algorithm consists of the following steps:
1. **Population Generation**: A population of chromosomes is generated.
2. **Selection**: Chromosomes are selected based on their fitness.
3. **Crossover and Mutation**: Selected chromosomes undergo crossover and mutation to create new offspring.
4. **Fitness Evaluation**: The new population is evaluated, and the process repeats until an optimal solution is found.

## Output

The best solution is stored in a text file, and detailed daily timetables are generated for each day of the week (Monday through Friday). The timetables are printed and written to a file for easy visualization.

## How to Run
1. Clone the repository.
2. Run the main script to generate the timetable.
3. View the output timetables in the generated text file.


