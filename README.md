# IdeaPlotter: Steam map

A phone-friendly map of Steam games. Each dot is a game. Games with similar store text sit close together, and colours show clusters of related games. Tap a dot to see the game, its five closest neighbours and a link to its Steam store page.

Open the map: https://brbselling.github.io/ideaplotter/

Current build: `sample2000-bf16`, 2000 games, built 2026-10-26 11:03 CET.

How it is made: each game's name, top tags, genres, play modes and store descriptions are embedded with Qwen3-Embedding-0.6B. Clusters come from Louvain clustering on a 10-nearest-neighbour graph, and the 2D layout comes from UMAP. Only names, Steam app IDs, cluster labels and map points are published here.

## Data

Steam Games Dataset by [Fronkon Games](https://github.com/FronkonGames), commit 6a31fcb, from [Hugging Face](https://huggingface.co/datasets/FronkonGames/steam-games-dataset), released under the MIT licence. It was collected from the Steam API and Steam Spy. Game names and store pages belong to their owners.
