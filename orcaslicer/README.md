# Profils OrcaSlicer — CR-10 (2017) modifiée

Profils utilisateur d'OrcaSlicer 2.4.x pour une CR-10 2017 (MKS Gen L, BLTouch,
double Z, bowden), utilisés avec ce firmware Marlin.

- `machine/CR-10 BLTouch.json` : machine (G-code de démarrage avec `G34`, `G29`).
  L'adresse OctoPrint (`print_host`) et la clé d'API sont **volontairement vides** :
  à renseigner dans Orca après import.
- `process/CR-10 0.20mm.json` : processus 0.20 mm (supports désactivés, accélération 500).
- `filament/eSUN PETG.json` : 240 °C, plateau 75 °C, débit max 8 mm³/s, K=1,5, rétraction 2 mm.
- `filament/eSUN PLA Matte Rainbow.json` : 220 °C, plateau 60 °C, débit max 7,5 mm³/s,
  K=0,9, rétraction 1,5 mm, flow ratio 1,03.

Ils héritent de profils système Orca (« MyMarlin », « Generic PETG/PLA @System »).
Import : Fichier → Importer → Importer la configuration, ou copie dans
`<config Orca>/user/default/{machine,process,filament}`.
