---
title: Portieren von greset
description: OpenGL ersetzt die IRIS GL-Funktion greset durch die Funktionen glPushAttrib und glPopAttrib.
ms.assetid: 348e8b18-4f12-45d1-a4d2-6533a983236b
keywords:
- IRIS GL-Portierung,Zustandsvariablen
- Portieren von IRIS GL,Zustandsvariablen
- Portieren von IRIS GL zu OpenGL, Zustandsvariablen
- OpenGL-Portierung von IRIS GL, Zustandsvariablen
- Zustandsvariablen
- IRIS GL-Portierung, greset-Funktion
- Portieren von IRIS GL, greset-Funktion
- Portieren von IRIS GL,greset-Funktion zu OpenGL
- OpenGL-Portierung von IRIS GL,greset-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5a48c09e7078f3eccd316de9cb86872d61343aabfa0faf60fbe5af2bef218c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936148"
---
# <a name="porting-greset"></a>Portieren von greset

OpenGL ersetzt die IRIS GL-Funktion **greset** durch die Funktionen [**glPushAttrib**](glpushattrib.md) und [**glPopAttrib.**](glpopattrib.md) Verwenden Sie diese Funktionen, um Gruppen von Zustandsvariablen zu speichern und wiederherzustellen. Beispiel:

``` syntax
void glPushAttrib( GLbitfield mask );
```

In diesem Beispiel wird ein bitweises OR von symbolischen Konstanten angenommen, das angibt, welche Gruppen von Zustandsvariablen auf einen Attributstapel gepusht werden sollen. Jede Konstante bezieht sich auf eine Gruppe von Zustandsvariablen. Die folgende Tabelle zeigt die Attributgruppen mit ihren entsprechenden symbolischen Konstantennamen. Eine vollständige Liste der OpenGL-Zustandsvariablen, die den einzelnen Konstanten zugeordnet sind, finden Sie unter [**glPushAttrib**](glpushattrib.md).



| attribute                       | Konstante                  |
|---------------------------------|---------------------------|
| Akkumulationspuffer–Clear-Wert | GL \_ ACCUM \_ BUFFER \_ BIT    |
| Farbpuffer                    | GL \_ COLOR \_ BUFFER \_ BIT    |
| Aktuell                         | GL \_ CURRENT \_ BIT          |
| Tiefenpuffer                    | GL \_ DEPTH \_ BUFFER \_ BIT    |
| enable                          | GL \_ ENABLE \_ BIT           |
| Bewerter                      | EGL \_ VAL \_ BIT             |
| Nebel                             | GL \_ ÜBER \_ BIT              |
| GL \_ LIST \_ BASE-Einstellung          | GL \_ LIST \_ BIT             |
| Hinweisvariablen                  | GL \_ HINT \_ BIT             |
| Beleuchtungsvariablen              | GL \_ LIGHTING \_ BIT         |
| Linienzeichnungsmodus               | GL \_ LINE \_ BIT             |
| Pixelmodusvariablen            | GL \_ PIXEL \_ MODE \_ BIT      |
| Punktvariablen                 | GL \_ POINT \_ BIT            |
| polygon                         | GL \_ POLYGON \_ BIT          |
| Polygonstipple                 | GL \_ POLYGON \_ STIPPLE \_ BIT |
| Schere                         | GL \_ SCISSOR \_ BIT          |
| Schablonenpuffer                  | GL \_ STENCIL \_ BUFFER \_ BIT  |
| Struktur                         | GL \_ TEXTURE \_ BIT          |
| Transformieren                       | GL \_ TRANSFORM \_ BIT        |
| Viewport                        | GL \_ VIEWPORT \_ BIT         |
|                                 | GL \_ ALL \_ ATTRIB \_ BITS     |



 

Rufen Sie einfach [**glPopAttrib**](glpopattrib.md)auf, um die Werte der Zustandsvariablen auf die werte wiederherzustellen, die mit dem letzten [**glPushAttrib**](glpushattrib.md)gespeichert wurden. Die Variablen, die Sie nicht gespeichert haben, bleiben unverändert. Der Attributstapel hat eine endliche Tiefe von mindestens 16.

 

 




