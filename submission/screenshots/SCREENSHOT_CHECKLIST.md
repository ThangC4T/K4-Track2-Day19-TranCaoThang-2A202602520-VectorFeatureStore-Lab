# Screenshot Checklist

Open the rendered HTML files in this folder and capture the visible output cells below.

Core rubric:
- `01_embeddings_index.html`: capture `Indexed: 1000 vectors`, keyword top-5, and paraphrase top-5.
- `02_hybrid_search_rrf.html`: capture Precision@10 table and slice table by query type.
- `03_search_api_benchmark.html`: capture API response sample and latency table/PASS line.
- `04_feast_feature_store.html`: capture Feast apply/materialize output, online lookup latency, and PIT join dataframe.

Advanced evidence:
- `05_filtered_search.html`: recall/selectivity table and over-fetch ladder.
- `06_agent_retrieval.html`: strategy comparison table, trace/reflection, and `build_context()` output.
- `07_semantic_cache.html`: threshold sweep and tenant leak/fix demo.
- `08_feature_engineering.html`: leakage table, PIT vs latest, and on-demand feature output.

Suggested filenames after you capture:
- `nb1_index_top5.png`
- `nb2_precision_slices.png`
- `nb3_api_latency.png`
- `nb4_feast_online_pit.png`
- optional advanced: `nb5_filtered.png`, `nb6_agent.png`, `nb7_cache.png`, `nb8_features.png`
