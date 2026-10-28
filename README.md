# DnD Dice Reader

Vak: Image Processing

Een image processing-project dat DnD-dobbelstenen (d4 t/m d20) herkent en afleest via een camera, met OpenCV.

## Groepsleden

- [Junhao Johnny](https://github.com/junhao-johnny-lin)
- [Nick Driessen](https://github.com/TheEarthsMoon)

## Doel

Dit project is een programma dat via een camera een worp met DnD-dobbelstenen inleest. Het programma detecteert elke dobbelsteen op de afbeelding, bepaalt het type (d4, d6, d8, d10, d12 of d20) en leest de bovenste waarde af. Per steen wordt de waarde teruggegeven, en het totaal van de worp wordt berekend.

Het project is bewust gefocust op image processing. Hardware en gebruikersinterface blijven minimaal: een laptop met camera en een effen ondergrond volstaan. De nadruk ligt op het ontwerpen, vergelijken en meten van de processing-pipeline.

Dit project is geschreven zodat iemand het kan gebruiken als startpunt voor een eigen project: per processing-stap leggen we uit waarom we een methode gekozen hebben, hoe goed ze werkt (met meetbare waarden) en welke alternatieven we overwogen hebben.

## Pipeline in het kort

1. Preprocessing (grijswaarden, ruisreductie, belichtingscorrectie)
2. Segmentatie van de stenen
3. Type-herkenning (d4, d6, d8, d10, d12, d20, d100)
4. Waarde aflezen (ogen tellen bij d6, cijfers herkennen bij de overige stenen)
5. Evaluatie op een eigen, gelabelde dataset

## Demo

> Nog in te vullen: GIF of video van het programma in werking, plus een voorbeeld van een invoerafbeelding en het resultaat.

```
Voorbeeld van de verwachte uitvoer:
Worp: d6 = 4, d8 = 7, d20 = 15  ->  totaal = 26
```

## Inhoud van deze repository

| Document | Inhoud |
|---|---|
| [README.md](README.md) | Doel, demo en interne links (dit bestand) |
| [OPSTELLING.md](OPSTELLING.md) | Wat hebben we geprobeerd, waarom en hoe? Gekozen methodes en overwogen alternatieven per stap |
| [RESULTATEN.md](RESULTATEN.md) | Hoe hebben we geëvalueerd en wat zijn de resultaten? Meetwaarden per stap en per omstandigheid |

## Vereisten en installatie

- Python 3
- OpenCV, NumPy, scikit-learn
- Optioneel: Tesseract of PyTorch voor de vergelijking met machine-learning-methodes

```
pip install opencv-python numpy scikit-learn
```

## Gebruik

> Nog in te vullen zodra het programma bestaat (commando om het programma te starten met een afbeelding of met de camera).

## Benodigde materialen

- Set DnD-dobbelstenen (liefst meerdere sets met verschillende kleuren en stijlen)
- Webcam of smartphone, eventueel met statief
- Effen ondergrond (dobbelbak of vilt) voor de basisopstelling, plus andere ondergronden voor robuustheidstests
- Laptop met Python, OpenCV, NumPy en scikit-learn
