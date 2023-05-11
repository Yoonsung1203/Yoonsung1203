## section1

[test](README.md)

<a href=README.md>test2</a>

## section2

```mermaid
  flowchart TB
    subgraph Total["Methylome Pipeline"]
      direction TB
      subgraph WS1["Installation"]
        direction TB
        W1["install_methylseq_required_R_packages"]
        click W1 href "http://www.github.com"
        B[an important <br><br> <ul> <li>app : <a href='http://google.com'>link</a></li> <li>option1 : hello</li> </ul>]
      end
      subgraph WS2[" "]
        direction LR
        subgraph WS2Loop["Extract CpG Table"]
          direction TB
          W2[<a href=./README.md>makedirs_for_bismark_result</a>]-->W3["fastpQCPairedEndTrimming"]
          W3-->W4["mapping_sequence_by_bismark"]
          W4-->W5["deduplication_by_bismark"]
          W5-->W6["methylation_extract_by_bismark"]
          W6-->W7["makedirectories_for_methyl_cpg_min"]
          W7-->W8["convert_CpGReport_to_methyl_cpg_min"]
          W8-->W9["pair_mereged_methyl_cpg_min"]
        end
        subgraph WS2LoopVariable["Loop"]
          direction TB
          WS2Var1[<ul><li>a</li><li>b</li></ul>]
        end
        WS2Loop-.-WS2LoopVariable
      end
      subgraph WS3["MetaTable Processing"]
        direction TB
        W10["add_file_path_to_metatable"]-->W11["get_metatable_of_control_sample"]
        W11-->W12["get_metatable_of_case_sample"]
      end
      subgraph WS4["DMP Analysis"]
        direction TB
        W13["extract_DMP"]
      end
      subgraph WS5["PCA Analysis"]
        direction TB
        W14["run_PCA_analysis_for_methyl"]
      end
      subgraph WS6["Volcano Plot"]
        direction TB
        W15["draw_methyl_volcano_plot"]
      end
      WS1-->WS2
      WS2-->WS4
      WS3-->WS4
      WS3-->WS5
      WS2-->WS5
      WS4-->WS6
    end
```
