---
title: Befehle zum Portieren von Bildschirmen und Puffern
description: OpenGL ersetzt eine Vielzahl von CLEAR-Funktionen für IRIS GL (zclear, aclear, sclear und so weiter) durch eine einzelne Funktion, glClear. Geben Sie genau an, was Sie löschen möchten, indem Sie Masken an glClear übergeben.
ms.assetid: 52ba503d-e412-4815-a039-a039b41327f4
keywords:
- IRIS GL-Portierung, Clear-Funktionen
- Portieren von IRIS GL,Clear-Funktionen
- Portieren von IRIS GL zu OpenGL, Löschen von Funktionen
- OpenGL-Portierung von IRIS GL, Clear-Funktionen
- Clear-Funktionen
- IRIS GL-Portierung, Befehle zum Löschen des Bildschirms
- Portieren von IRIS GL, Befehle zum Löschen des Bildschirms
- Portieren von IRIS GL zu OpenGL, Befehle zum Löschen des Bildschirms
- OpenGL-Portierung über IRIS GL, Befehle zum Löschen des Bildschirms
- Befehle zum Löschen des Bildschirms
- IRIS GL-Portierung, Befehle zum Löschen von Puffern
- Portieren von IRIS GL,Befehle zum Löschen von Puffern
- Portieren von IRIS GL zu OpenGL, Befehle zum Löschen von Puffern
- OpenGL-Portierung über IRIS GL, Befehle zum Löschen von Puffern
- Befehle zum Löschen von Puffern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbff0fed3472fd4374605cb96dbae845998c0ba2d8ce488420f9b4c6895a07c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794875"
---
# <a name="porting-screen-and-buffer-clearing-commands"></a>Befehle zum Portieren von Bildschirmen und Puffern

OpenGL ersetzt eine Vielzahl von clear-Funktionen von IRIS **GL** **(zclear, aclear,** **sclear** und so weiter) durch eine einzelne Funktion, [**glClear**](glclear.md).  Geben Sie genau an, was Sie löschen möchten, indem Sie Masken an **glClear übergeben.**

Beachten Sie beim Portieren von Bildschirm- und Pufferbefehlen folgende Punkte:

-   OpenGL verwaltet das Löschen von Farben getrennt vom Zeichnen von Farben mit Aufrufen wie [**glClearColor**](glclearcolor.md) und [**glClearIndex.**](glclearindex.md) Achten Sie darauf, dass Sie vor dem Löschen die klare Farbe für jeden Puffer festlegen.
-   Anstatt einen von mehreren unterschiedlich benannten clear-Aufrufen zu verwenden, löschen Sie jetzt mehrere Puffer mit einem Aufruf, [**glClear,**](glclear.md)durch **OR,** indem Sie Puffermasken zusammen verwenden. So wird **z. B. "clear"** durch Folgendes ersetzt:

    ``` syntax
    glClear( GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT )
    ```

-   IRIS GL verweist auf den Polygonausschnitt und die Farb-Schreibmaske. OpenGL ignoriert den Polygonausschnitt, verweist aber auf die Farb-Schreibmaske. (Die **funktion "clear"** ignoriert sowohl den Polygonausschnitt als auch die Farb-Schreibmaske.)

In der folgenden Tabelle sind die verschiedenen CLEAR-Funktionen von IRIS GL mit den entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Aufruf         | OpenGL-Aufruf                                                               | Bedeutung                                           |
|----------------------|---------------------------------------------------------------------------|---------------------------------------------------|
| **acbuf**(AC \_ CLEAR) | **glClear**( \_ GL BUFFERM \_ BUFFER BIT \_ )                                     | Löschen Sie den Akkumulationspuffer.                    |
|                      | **glClearColor**                                                          | Legen Sie die RGBA-Klarfarbe fest.                         |
|                      | **glClearIndex**                                                          | Legen Sie den Clear-Color-Index fest.                        |
| **Löschen**            | **glClear**( GL \_ COLOR BUFFER BIT \_ \_ )                                     | Löschen Sie den Farbpuffer.                           |
|                      | **glClearDepth**                                                          | Geben Sie den eindeutigen Wert für den Tiefenpuffer an.     |
| **zclear**           | **glClear**( GL \_ DEPTH BUFFER BIT \_ \_ )                                     | Löschen Sie den Tiefenpuffer.                           |
| **-100000000**          | **glClear**( GL \_ COLOR BUFFER BIT GL DEPTH BUFFER BIT \_ \_ \| \_ \_ \_ )<br/> | Löschen Sie den Farbpuffer und den Tiefenpuffer.      |
|                      | **glClearAccum**                                                          | Geben Sie klare Werte für den Akkumulationspuffer an. |
|                      | **glClearStencil**                                                        | Geben Sie den unverankerten Wert für den Schablonenpuffer an.   |
| **sclear**           | **glClear**( GL \_ STENCIL \_ BUFFER BIT \_ )                                   | Löschen Sie den Schablonenpuffer.                         |



 

Wenn Ihr IRIS GL-Code sowohl **gclear** als auch **sclear verwendet,** können Sie sie in einem einzigen **glClear-Aufruf** kombinieren. kann die Leistung Ihres Programms verbessern.

 

 





