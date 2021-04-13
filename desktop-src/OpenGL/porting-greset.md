---
title: Portieren von greset
description: OpenGL ersetzt die Iris GL-Funktion "greset" durch die Funktionen "glpushatpub" und "glpopatpub".
ms.assetid: 348e8b18-4f12-45d1-a4d2-6533a983236b
keywords:
- IRIS GL portieren, Zustandsvariablen
- Portieren von IRIS GL, Zustandsvariablen
- Portieren auf OpenGL von IRIS GL, Zustandsvariablen
- OpenGL-Portierung von IRIS GL, Zustandsvariablen
- Zustandsvariablen
- IRIS GL Porting, greset-Funktion
- Portieren von IRIS GL, greset-Funktion
- Portieren auf OpenGL von IRIS GL, greset-Funktion
- OpenGL-Portierung von IRIS GL, greset-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078482f47dcaf7fd5f84605e2e0fa32d0cf14729
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388490"
---
# <a name="porting-greset"></a>Portieren von greset

OpenGL ersetzt die Iris GL-Funktion " **greset**" durch die Funktionen " [**glpushatpub**](glpushattrib.md) " und " [**glpopatpub**](glpopattrib.md)". Verwenden Sie diese Funktionen, um Gruppen von Zustandsvariablen zu speichern und wiederherzustellen. Beispiel:

``` syntax
void glPushAttrib( GLbitfield mask );
```

In diesem Beispiel wird eine bitweise OR-Eigenschaft von symbolischen Konstanten angenommen, die angibt, welche Gruppen von Zustandsvariablen in einem Attribut Stapel abgelegt werden. Jede Konstante verweist auf eine Gruppe von Zustandsvariablen. In der folgenden Tabelle werden die Attribut Gruppen mit den entsprechenden symbolischen Konstanten Namen angezeigt. Eine komplette Liste der OpenGL-Zustandsvariablen, die den einzelnen Konstanten zugeordnet sind, finden Sie unter [**glpushatfferb**](glpushattrib.md).



| Attribut                       | Konstante                  |
|---------------------------------|---------------------------|
| Wert für Kumulations Puffer Clear | GL- \_ Accum- \_ Puffer \_ Bit    |
| Farb Puffer                    | GL- \_ Farb \_ Puffer \_ Bit    |
| Aktuell                         | GL \_ Aktuelles \_ Bit          |
| tiefen Puffer                    | GL- \_ Tiefe- \_ Puffer \_ Bit    |
| enable                          | GL \_ enable \_ Bit           |
| Auswertungen                      | EGL- \_ Val- \_ Bit             |
| Nebel                             | GL \_ - \_ nebelbit              |
| \_ \_ Basis Einstellung der GL-Liste          | GL- \_ Listen \_ Bit             |
| Hinweis Variablen                  | GL- \_ Hinweis \_ Bit             |
| Beleuchtungs Variablen              | GL- \_ Beleuchtungs \_ Bit         |
| Zeilen Zeichnungsmodus               | GL \_ - \_ linienbit             |
| Pixel Modus-Variablen            | GL- \_ Pixel \_ Modus- \_ Bit      |
| Punkt Variablen                 | GL \_ - \_ punktbit            |
| polygon                         | GL- \_ Polygon- \_ Bit          |
| Polygon-Stippel                 | GL- \_ Polygon- \_ Stippel \_ Bit |
| Scheren                         | GL- \_ Scheren- \_ Bit          |
| Schablone-Puffer                  | GL- \_ Schablone- \_ Puffer \_ Bit  |
| Struktur                         | GL- \_ Textur \_ Bit          |
| Transformieren                       | GL- \_ Transform- \_ Bit        |
| Viewport                        | GL- \_ \_ viewportbit         |
|                                 | GL \_ alle \_ attrb- \_ Bits     |



 

Um die Werte der Zustandsvariablen wiederherzustellen, die mit dem letzten [**glpushatpub**](glpushattrib.md)gespeichert wurden, nennen Sie einfach " [**glpopatpub**](glpopattrib.md)". Die Variablen, die Sie nicht gespeichert haben, bleiben unverändert. Der Attribut Stapel hat eine endliche Tiefe von mindestens 16.

 

 




