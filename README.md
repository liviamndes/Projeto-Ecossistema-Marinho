# 🌊 Marine Ecosystem Simulation

Uma simulação robusta de um ecossistema marinho desenvolvida em **Java**, demonstrando a aplicação prática de Padrões de Projeto (**Design Patterns**) para modelar interações biológicas complexas, cadeias alimentares e eventos ambientais.

## 🧠 Sobre o Projeto

Este projeto simula a vida no Oceano Pacífico, gerenciando diversas entidades biológicas. O foco principal é a arquitetura de software, utilizando padrões para resolver problemas de hierarquia e notificação de eventos.

### 🎯 Objetivos
* Simular interações tróficas (Predador vs. Presa).
* Gerenciar grupos de animais e indivíduos de forma unificada.
* Reagir a eventos ambientais (como poluição ou mudança de temperatura) em tempo real.

---

## 🛠️ Padrões de Projeto Utilizados

O núcleo do sistema foi construído sobre dois padrões clássicos:

### 1. Composite Pattern (Padrão Composite)
Utilizado para tratar animais individuais (**Folhas**) e grupos de animais (**Compositores**) de maneira uniforme.
* **Aplicação:** O `Habitat` pode enviar comandos como `simulateMovement()` para uma única Baleia ou para um Cardume inteiro de Salmões sem saber a diferença.
* **Classes Chave:** `EcosystemEntity` (Componente), `Animal` (Folha), `AnimalGroup` (Compositor).

### 2. Observer Pattern (Padrão Observador)
Utilizado para o sistema de eventos ambientais.
* **Aplicação:** O `Habitat` atua como o **Sujeito**. Quando ocorre
* **Classes Chave:** `HabitatSubject`, `HabitatObserver`, `Condition`.

---

## 🚀 Como Executar

### Pré-requisitos
* Java JDK 17 ou superior.
* Uma IDE (VS Code, Eclipse, IntelliJ) ou Terminal.

### Passos
1.  Clone o repositório:
    ```bash
    git clone [https://github.com/SEU_USUARIO/ecossistema-java-patterns.git](https://github.com/liviamndes/Projeto-Ecossistema-Marinho.git)
    ```
2.  Navegue até a pasta do código:
    ```bash
    cd ecot12-projetofinal
    ```
3.  Compile e execute a classe `Main.java`.

---

## 📸 Exemplo de Saída (Simulação)

```text
=============================================
   ECOSYSTEM SIMULATION: STARTING
=============================================
Creating Habitat: Pacific Ocean... 
Creating individual animals (Leaves)...

*** Habitat population complete. All animals and groups have been added. ***

=============================================
   PHASE 1: OBSERVER PATTERN (Pollution Event)
=============================================
Blue Whale is affected by ocean noise pollution. This noise disrupts its complex communication (Structured Low-Frequency) and migration patterns.
Humpback Whale is affected by ocean noise pollution. This noise disrupts its complex communication (Highly Complex Melodies) and migration patterns.
Orca is affected by ocean noise pollution. This noise disrupts its complex communication (Complex Pod Dialects) and migration patterns.     
--- The group 'Dolphin Pod' received an alert. Notifying members... ---
Bottlenose Dolphin may ingest plastic, which affects over 56% of cetaceans and can cause digestive blockages, malnutrition, or death.       
Pacific White-Sided Dolphin may ingest plastic, which affects over 56% of cetaceans and can cause digestive blockages, malnutrition, or death.
Mako Shark may suffer from bioaccumulation of heavy metals and ingest plastic waste, affecting its health and survival.
Great White Shark may suffer from bioaccumulation of heavy metals and ingest plastic waste, affecting its health and survival.
Clownfish suffers from local pollution in its territory.
--- The group 'Salmon School' received an alert. Notifying members... ---
Pollution in this area is critical for Pacific Salmon, as it disrupts its vital migratory route.
Pollution in this area is critical for Pacific Salmon, as it disrupts its vital migratory route.
Pollution in this area is critical for Pacific Salmon, as it disrupts its vital migratory route.
Pollution in this area is critical for Pacific Salmon, as it disrupts its vital migratory route.
Pollution in this area is critical for Pacific Salmon, as it disrupts its vital migratory route.
Dungeness Crab is highly sensitive to pollution, which clogs its 'Gills'.
Lined Shore Crab is highly sensitive to pollution, which clogs its 'Gills'.
Ochre Sea Star is suffocating. Pollution is damaging its delicate 'Skin Gills (Papulae)'.
Bat Star is suffocating. Pollution is damaging its delicate 'Skin Gills (Papulae)'.
--- The group 'Jellyfish Bloom' received an alert. Notifying members... ---
Moon Jelly is sensitive to pollution, as it absorbs toxins via 'Diffusion'.
Pacific Sea Nettle is sensitive to pollution, as it absorbs toxins via 'Diffusion'.
Crystal Jelly is sensitive to pollution, as it absorbs toxins via 'Diffusion'.
Giant Pacific Octopus is affected by chemical pollutants, which may impair its immune system and increase mortality.
Dumbo Octopus is affected by chemical pollutants, which may impair its immune system and increase mortality.
Mimic Octopus is affected by chemical pollutants, which may impair its immune system and increase mortality.
Green Sea Turtle (which breathes with 'Pulmonary') surfaces more often to breathe, avoiding the polluted water.
Loggerhead Sea Turtle (which breathes with 'Pulmonary') surfaces more often to breathe, avoiding the polluted water.

* Octopus -> Crab *
Giant Pacific Octopus uses its camouflage to ambush Dungeness Crab.   
It swiftly captures the prey using its 8 tentacles and strong suction cups.
Dungeness Crab is attacked by Giant Pacific Octopus and attempts to defend itself with its claws.        

* Sea Turtle -> Jellyfish *        
Loggerhead Sea Turtle slowly approaches and consumes the Moon Jelly.  
Moon Jelly is attacked by Loggerhead Sea Turtle!
It defends itself with its stinging tentacles (Severity: Mild).       

* Shark -> Sea Turtle *
Great White Shark uses electroreception to detect Green Sea Turtle.   
Great White Shark then attacks using its tactic: Breach Ambush!       
Green Sea Turtle is attacked by Great White Shark!
Its hard shell (5.0cm thick) provides excellent protection.
However, the predator's powerful jaws may be able to break the shell. 

* Starfish -> Crab *
Ochre Sea Star slowly crawls over Lined Shore Crab and begins to pry it open with its tube feet.
Lined Shore Crab is attacked by Ochre Sea Star and attempts to defend itself with its claws.

* Orca -> Dolphin *
Orca uses its Complex Pod Dialects to coordinate an attack on Bottlenose Dolphin.
Bottlenose Dolphin is eaten by Orca

* Shark -> Salmon *
Mako Shark uses electroreception to detect Pacific Salmon.
Mako Shark then attacks using its tactic: Speed Ambush!
Pacific Salmon is eaten by Mako Shark

* Sea Turtle -> Orca (Impossible Hunt)*
HUNT FAILED: Loggerhead Sea Turtle is not an active hunter or does not hunt Orca.

*** Special Behavior: Whale Songs ***
Orca begins to sing, performing its Complex Pod Dialects song.        
Blue Whale begins to sing, performing its Structured Low-Frequency song.
Humpback Whale begins to sing, performing its Highly Complex Melodies song.

=============================================
   PHASE 3: COMPOSITE PATTERN (Simulations)
=============================================

--- [FEEDING SIMULATION] in Pacific Ocean ---
Blue Whale uses its filter mechanism to filter krill and plankton, fueling its massive size (up to 190000.0 kg).
Humpback Whale uses its filter mechanism to filter krill and plankton, fueling its massive size (up to 40000.0 kg).
Orca hunts or scavenges other animals.
--- The group 'Dolphin Pod' begins to feed. ---
Bottlenose Dolphin uses echolocation at 130000.0 Hz to locate fish and squid.
Pacific White-Sided Dolphin uses echolocation at 125000.0 Hz to locate fish and squid.
Mako Shark consumes prey using strong jaws and its sharp teeth.       
Great White Shark consumes prey using strong jaws and its sharp teeth.
Clownfish feeds on algae, plankton, or small invertebrates depending on species.
--- The group 'Salmon School' begins to feed. ---
Pacific Salmon feeds on algae, plankton, or small invertebrates depending on species.
Pacific Salmon feeds on algae, plankton, or small invertebrates depending on species.
Pacific Salmon feeds on algae, plankton, or small invertebrates depending on species.
Pacific Salmon feeds on algae, plankton, or small invertebrates depending on species.
Pacific Salmon feeds on algae, plankton, or small invertebrates depending on species.
Ochre Sea Star everts its stomach to externally digest prey, like mussels or clams.
Bat Star feeds on organic particles (detritus) from the ocean floor.  
--- The group 'Jellyfish Bloom' begins to feed. ---
Moon Jelly captures plankton and small fish using its stinging tentacles.
Pacific Sea Nettle captures plankton and small fish using its stinging tentacles.
Crystal Jelly captures plankton and small fish using its stinging tentacles.
Giant Pacific Octopus uses its 8 powerful tentacles and beak to eat crustaceans (like Crabs) and mollusks.
Dumbo Octopus uses its 8 powerful tentacles and beak to eat crustaceans (like Crabs) and mollusks.       
Mimic Octopus uses its 8 powerful tentacles and beak to eat crustaceans (like Crabs) and mollusks.       
Loggerhead Sea Turtle occasionally consumes jellyfish or small marine animals.

--- [MOVEMENT SIMULATION] in Pacific Ocean ---
Blue Whale propels its massive body (up to 190000.0 kg) using powerful tail flukes.
Humpback Whale propels its massive body (up to 40000.0 kg) using powerful tail flukes.
Orca propels its massive body (up to 9000.0 kg) using powerful tail flukes.
--- The group 'Dolphin Pod' is moving as a unit. ---
Bottlenose Dolphin swims quickly and gracefully, using its tail fluke and fins to navigate.
Pacific White-Sided Dolphin swims quickly and gracefully, using its tail fluke and fins to navigate.     
Mako Shark swims constantly to stay afloat, relying on its large, oily liver for buoyancy.
Great White Shark swims constantly to stay afloat, relying on its large, oily liver for buoyancy.        
Clownfish swims using its fins and adjusts buoyancy with its swim bladder.
--- The group 'Salmon School' is moving as a unit. ---
Pacific Salmon swims using its fins and adjusts buoyancy with its swim bladder.
Pacific Salmon is a migratory species and travels long distances.     
Pacific Salmon swims using its fins and adjusts buoyancy with its swim bladder.
Pacific Salmon is a migratory species and travels long distances.     
Pacific Salmon swims using its fins and adjusts buoyancy with its swim bladder.
Pacific Salmon is a migratory species and travels long distances.     
Pacific Salmon swims using its fins and adjusts buoyancy with its swim bladder.
Pacific Salmon is a migratory species and travels long distances.     
Pacific Salmon swims using its fins and adjusts buoyancy with its swim bladder.
Pacific Salmon is a migratory species and travels long distances.     
Ochre Sea Star slowly moves using its tube feet, which are part of its 'Radial' body plan.
Bat Star slowly moves using its tube feet, which are part of its 'Radial' body plan.
--- The group 'Jellyfish Bloom' is moving as a unit. ---
Moon Jelly drifts with the current, pulsing its 'Medusa' bell to move.
Pacific Sea Nettle drifts with the current, pulsing its 'Medusa' bell to move.
Crystal Jelly drifts with the current, pulsing its 'Medusa' bell to move.
Crystal Jelly emits a soft bioluminescent glow in the dark ocean.     
Giant Pacific Octopus propels itself using jet propulsion, or crawls along the seabed using its 8 tentacles.
Dumbo Octopus propels itself using jet propulsion, or crawls along the seabed using its 8 tentacles.     
Mimic Octopus propels itself using jet propulsion, or crawls along the seabed using its 8 tentacles.     
Loggerhead Sea Turtle swims gracefully using its large SWIMMINGPADDLES.
It can dive to impressive depths, reaching up to 500.0 meters.        

--- [REPRODUCTION SIMULATION] in Pacific Ocean ---
Blue Whale reproduces via internal fertilization and has a gestation period of 335 days.
Humpback Whale reproduces via internal fertilization and has a gestation period of 330 days.
Orca reproduces via internal fertilization and has a gestation period of 517 days.
--- It is breeding season for the group 'Dolphin Pod'. ---
Bottlenose Dolphin reproduces via internal fertilization and has a gestation period of 365 days.
Pacific White-Sided Dolphin reproduces via internal fertilization and has a gestation period of 365 days.
Mako Shark reproduces via internal fertilization; some species give live birth.
Great White Shark reproduces via internal fertilization; some species give live birth.
Clownfish reproduces through external fertilization, releasing eggs in the water.
--- It is breeding season for the group 'Salmon School'. ---
Pacific Salmon reproduces through external fertilization, releasing eggs in the water.
Pacific Salmon reproduces through external fertilization, releasing eggs in the water.
Pacific Salmon reproduces through external fertilization, releasing eggs in the water.
Pacific Salmon reproduces through external fertilization, releasing eggs in the water.
Pacific Salmon reproduces through external fertilization, releasing eggs in the water.
Ochre Sea Star reproduces sexually by releasing gametes into the water.
It can also reproduce asexually, as its body can regenerate from fragments.
Bat Star reproduces sexually by releasing gametes into the water.     
It can also reproduce asexually, as its body can regenerate from fragments.
--- It is breeding season for the group 'Jellyfish Bloom'. ---        
Moon Jelly alternates between sexual and asexual reproduction depending on its life stage.
Pacific Sea Nettle alternates between sexual and asexual reproduction dependingmales usually die shortly after mating.
Loggerhead Sea Turtle reproduces sexually.
It migrates hundreds of kilometers back to its home: Temperate and Tropical Beaches.
It crawls ashore to dig a nest in the sand and lay its eggs.

=============================================
   SIMULATION COMPLETE
=============================================
