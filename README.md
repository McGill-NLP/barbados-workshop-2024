# Barbados Workshop 2024
Clone of [Barbados Workshop 2023](https://barbadosworkshop.com).

## Updating the Participant List
Download the CSV from [here](https://docs.google.com/spreadsheets/d/1zUCSJKIWzERRMTZmbDy8JefsXfzf-1k8Y6v86XSDfTo/edit#gid=278216229).
Run the following command:
```bash
python3 scripts/load_participant.py \
    --input_file data/participant.csv \
    --output_file participant.html
```
This script checks whether an image exists in `assets/participants` for each participant.
Each image should use the naming scheme `{first_name}_{last_name}.*` where `first_name` and `last_name` are all lowercase (and correspond to a record in the CSV).
Last names consisting of multiple words are delimited by `-`.

## Build
GitHub pages points to the `main` branch. Any new commits to this branch will trigger a deployment.
