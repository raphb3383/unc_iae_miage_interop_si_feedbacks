# ❔ Donnnées

```sql
CREATE TABLE feedback_sessions (
    session_date DATE NOT NULL,
    id_etudiant_gh varchar NOT NULL,
    duree_heures INT NOT NULL,
    niko_niko varchar check (niko_niko in ('VERT', 'JAUNE', 'ROUGE')),
    fdbck_clarte_explications integer CHECK (fdbck_clarte_explications BETWEEN 1 AND 5),
    fdbck_utilite_concepts integer CHECK (fdbck_utilite_concepts BETWEEN 1 AND 5),
    fdbck_difficulte_percue integer CHECK (fdbck_difficulte_percue BETWEEN 1 AND 5),
    fdbck_suggestions_amelioration varchar(50),
    fdbck_impact_progression integer CHECK (fdbck_impact_progression BETWEEN 1 AND 5),
    fdbck_confiance_atteinte_objectif_professionnel integer CHECK (fdbck_confiance_atteinte_objectif_professionnel BETWEEN 1 AND 5),
    fdbck_ce_que_j_ai_prefere varchar(50),
    fdbck_commentaires_supplementaires varchar(50),
    PRIMARY KEY (session_date, id_etudiant_gh)
);
```
