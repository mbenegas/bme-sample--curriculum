# bme-sample--curriculum

graph TD
    %% Year 1
    subgraph Year_1 [Year 1]
        BME100[BME 100: Intro to Profession]
        CS104[CS 104: Intro to Programming]
        MATH151[MATH 151: Calculus I]
        CHEM124[CHEM 124: Chemistry I]
        MATH152[MATH 152: Calculus II]
        CHEM125[CHEM 125: Chemistry II]
        PHYS123[PHYS 123: Physics I Mechanics]
    end

    %% Year 2
    subgraph Year_2 [Year 2]
        CHEM235[CHEM 235: Organic Chem I]
        ECE211[ECE 211: Circuit Analysis I]
        MATH252[MATH 252: Diff Equations]
        MMAE202[MMAE 202: Mechanics of Solids]
        PHYS221[PHYS 221: Physics II E&M]
        BIOL115[BIOL 115: Human Biology]
        MATH251[MATH 251: Multivariate Calc]
        BME315[BME 315: Instr. Lab]
    end

    %% Year 3
    subgraph Year_3 [Year 3]
        BME453[BME 453: Quant Physiology]
        BME301[BME 301: Bio-Fluids]
        CHE202[CHE 202: Material Energy Bal]
        ECE308[ECE 308: Signals & Systems]
        BME422[BME 422: Math Methods]
        BIOL403[BIOL 403: Biochemistry]
        BME310[BME 310: Biomaterials]
        BME335[BME 335: Thermo of Living Sys]
        BME320[BME 320: Fluids Lab]
        BME405[BME 405: Physio Lab]
    end

    %% Year 4
    subgraph Year_4 [Year 4]
        BME418[BME 418: Reaction Kinetics]
        BME482[BME 482: Mass Transport]
        BME419[BME 419: Design Concepts I]
        BME433[BME 433: BME Statistics]
        BME420[BME 420: Design Concepts II]
        BME424[BME 424: Quant Cell/Tissue Engr]
    end

    %% Connections (Prerequisites)
    MATH151 --> MATH152
    MATH152 --> MATH251
    MATH152 --> MATH252
    MATH151 --> PHYS123
    CHEM124 --> CHEM125
    
    %% Physics & Engineering Core
    PHYS123 --> PHYS221
    PHYS123 --> MMAE202
    MATH152 --> MMAE202
    MATH152 --> ECE211
    PHYS221 --> ECE211
    ECE211 --> ECE308
    ECE211 --> BME315

    %% Chemistry & Bio Core
    CHEM125 --> CHEM235
    CHEM125 --> CHE202
    CHEM235 --> BIOL403
    BIOL115 --> BIOL403
    BIOL115 --> BME453
    
    %% BME Core Streams
    MMAE202 --> BME301
    MATH252 --> BME301
    BME301 --> BME320
    
    CHE202 --> BME335
    BME335 --> BME418
    
    MATH252 --> BME453
    BME453 --> BME405
    
    %% Advanced Transport & Tissue
    BME301 --> BME482
    BME335 --> BME482
    BME482 --> BME424
    BME453 --> BME424
    
    %% Design & Math
    MATH252 --> BME422
    MATH251 --> BME433
    ECE308 --> BME419
    BME453 --> BME419
    BME419 --> BME420

    %% Biomaterials
    CHEM125 --> BME310
