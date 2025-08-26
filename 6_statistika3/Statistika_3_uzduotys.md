# Statistika – 3 paskaita: Užduotys (be sprendimų)

Dataset'ai: `tips` ir `penguins` (`seaborn.load_dataset`)

## A. Tikimybės (tips)
1. Apskaičiuokite P(tip > 5). Pavaizduokite `total_bill` histogramą (20 binų) ir pažymėkite vertikalią liniją ties 30.
2. Apskaičiuokite P(smoker == 'Yes'). Patikrinkite nepriklausomumą: ar P(tip > 5 ∩ smoker) ≈ P(tip > 5) * P(smoker)?
3. Apskaičiuokite sąlyginę tikimybę P(tip > 5 | day ∈ {Sat, Sun}). Palyginkite su P(tip > 5 | day ∈ {Thur, Fri}).
4. Sudarykite dvimatę dažnių lentelę `smoker` × `day`. Iš jos ranka (naudodami skaičius) įvertinkite P(smoker='Yes' | day='Sun').

## B. Kodavimas (tips)
5. Sukurkite one-hot/dummy kintamuosius stulpeliams: `sex`, `smoker`, `day`, `time`. Paaiškinkite, kada naudotumėte `drop_first=True`.
6. Susikurkite `tip_rate = tip / total_bill`. Pagal kvantiles sukurkite ordinal kintamąjį `service_level`: Low/Medium/High. Priskirkite 1/2/3.
7. Pavaizduokite `tip_rate` dėžės diagramą (boxplot) pagal `smoker`. Ką pastebite?

## C. Sąlyginės tikimybės ir Bayeso intuicija (penguins)
8. Išvalykite trūkstamas reikšmes. Apskaičiuokite P(species='Adelie').
9. Apskaičiuokite P(flipper_length_mm > 200) ir P(Adelie | flipper_length_mm > 200).
10. Pavaizduokite `flipper_length_mm` histogramą. Kurioje zonoje dažniau pasitaiko `Gentoo`?
11. Sukurkite `size_class` pagal `body_mass_g` kvantiles: Low/Medium/High (ordinal 1/2/3). Pavaizduokite bar diagramą.

## D. ML ryšys: Naive Bayes (penguins)
12. Užkoduokite `island` ir `sex` (one-hot), sujunkite su skaitiniais požymiais. Tikslas: `species`.
13. Padalinkite į train/test (25% test, stratify=y). Su `GaussianNB` išmokykite modelį.
14. Pateikite klasifikacijos ataskaitą, konfuzijos matricą. Parodykite pirmų 5 įrašų prognozių tikimybes.
15. Intuicija: atrinkite 5 įrašus su `flipper_length_mm > 210`, parodykite jų prognozių tikimybes. Ką pastebite?
