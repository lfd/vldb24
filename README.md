# Quantum-Inspired Digital Annealing for Join Ordering

This repository contains code and data artifacts for "Quantum-Inspired Digital Annealing for Join Ordering", submitted to VLDB 2024.

## Project Structure

DigitalAnnealing.py and SimulatedAnnealing.py contain code for our experimental analysis, using Scripts/ProblemGenerator.py to load query data, where we consider (1) query graphs extracted from standard benchmarks (SQLite [1], TPC-H [2], TPC-DS [3], LDBC [4], Join Order Benchmark [5]), (2) synthetic chain, star and cycle queries, generated in accordance to the classic method by Steinbrunn et al. [6], using generation code by Trummer [7], and (3) synthetic tree queries by Neumann and Radke [8]. Data for all queries can be found in ExperimentalAnalysis/Problems. 

Scripts/QUBOGenerator.py constructs JO-QUBO encodings based on our novel formulation method, allowing their deployment on the Fujitsu Digital Annealer [9]. Finally, Scripts/Postprocessing.py contains code for reading out join orders from each annealing solution obtained by the annealing device. Raw annealing results for all queries can be found in ExperimentalAnalysis/Data.

## References

[1] Richard D Hipp. 2020. SQLite. https://www.sqlite.org/index.htm

[2] Transaction Processing Performance Council. 2023. TPC Benchmark H. https:
//www.tpc.org

[3] Transaction Processing Performance Council. 2023. TPC Benchmark DS. https:
//www.tpc.org

[4] Renzo Angles, Peter Boncz, Josep-Lluis Larriba-Pey, Irini Fundulaki, Thomas
Neumann, Orri Erling, Peter Neubauer, Norbert Martínez-Bazan, Venelin Kotsev,
and Ioan Toma. 2014. The Linked Data Benchmark Council: A graph and RDF
industry benchmarking effort. ACM SIGMOD Record 43 (05 2014), 27–31. https:
//doi.org/10.1145/2627692.2627697

[5] Viktor Leis, Bernhard Radke, Andrey Gubichev, Atanas Mirchev, Peter Boncz,
Alfons Kemper, and Thomas Neumann. 2018. Query optimization through the
looking glass, and what we found running the join order benchmark. The VLDB
Journal 27 (2018), 643–668.

[6] Michael Steinbrunn, Guido Moerkotte, and Alfons Kemper. 1997. Heuristic and
randomized optimization for the join ordering problem. The VLDB journal 6
(1997), 191–208.

[7] Immanuel Trummer. 2016. Query Optimizer Library. https://github.com/itrummer/query-optimizer-lib

[8] Thomas Neumann and Bernhard Radke. 2018. Adaptive Optimization of Very
Large Join Queries. In Proceedings of the 2018 International Conference on Manage-
ment of Data (Houston, TX, USA) (SIGMOD ’18). Association for Computing Ma-
chinery, New York, NY, USA, 677–692. https://doi.org/10.1145/3183713.3183733

[9] Fujitsu Limited. 2023. Fujitsu Digital Annealer - solving large-scale combinatorial optimization problems instantly. https://www.fujitsu.com/emeia/services/business-services/digital-annealer/what-is-digital-annealer/
