---
title: Portieren von Bildschirm-und Puffer Lösch Befehlen
description: OpenGL ersetzt eine Reihe von IRIS GL Clear-Funktionen (z. b. zclear, aclear, sClear usw.) durch eine einzelne Funktion, glClear. Geben Sie genau an, was Sie löschen möchten, indem Sie Masken an glClear übergeben.
ms.assetid: 52ba503d-e412-4815-a039-a039b41327f4
keywords:
- IRIS GL portieren, Löschen von Funktionen
- Portieren von IRIS GL, Löschen von Funktionen
- Portieren auf OpenGL von IRIS GL, Clear Functions
- OpenGL-Portierung von IRIS GL, Clear Functions
- Funktionen löschen
- IRIS GL Porting, Befehle zum Löschen von Bildschirmen
- portieren aus IRIS GL, Befehle zum Löschen von Bildschirmen
- Portieren auf OpenGL von IRIS GL, Befehle zum Löschen von Bildschirmen
- OpenGL-Portierung von IRIS GL, Befehle zum Löschen von Bildschirmen
- Bildschirm Lösch Befehle
- IRIS GL Porting, Befehle zum Löschen von Puffern
- Portieren von IRIS GL, Puffer Lösch Befehle
- Portieren von IRIS gl auf OpenGL, Puffer Lösch Befehle
- OpenGL-Portierung von IRIS GL, Puffer Lösch Befehle
- Puffer Lösch Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53566c9fe14922f3965133cef9e30cbea4548b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341463"
---
# <a name="porting-screen-and-buffer-clearing-commands"></a>Portieren von Bildschirm-und Puffer Lösch Befehlen

OpenGL ersetzt eine Reihe von IRIS GL **Clear** -Funktionen (z. b. **zclear**, **aclear**, **sClear** usw.) durch eine einzelne Funktion, [**glClear**](glclear.md). Geben Sie genau an, was Sie löschen möchten, indem Sie Masken an **glClear** übergeben.

Beachten Sie die folgenden Punkte, wenn Sie Bildschirm-und Puffer Befehle portieren:

-   Bei OpenGL wird das Löschen von Farben getrennt von Zeichnungs Farben mit aufrufen wie " [**glclearcolor**](glclearcolor.md) " und " [**glclearindex**](glclearindex.md)" beibehalten. Stellen Sie sicher, dass Sie die klar Farbe für jeden Puffer vor dem Löschen festlegen.
-   Anstatt einen von mehreren unterschiedlichen benannten Clear-aufrufen zu verwenden, löschen Sie nun mehrere Puffer mit einem Aufruf, einem [**glClear**](glclear.md)- **oder** -up-Puffer Masken. Beispielsweise wird " **czclear** " durch Folgendes ersetzt:

    ``` syntax
    glClear( GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT )
    ```

-   IRIS GL verweist auf den Polygon Stippel und die Farb schreibfrage. OpenGL ignoriert den Polygon-Stippel, verweist jedoch auf die Farb schreibfrage. (Die Funktion " **czclear** " ignoriert sowohl den Polygon Stippel als auch die Farb schreibfrage.)

In der folgenden Tabelle werden die verschiedenen "IRIS GL Clear"-Funktionen mit ihren entsprechenden OpenGL-Funktionen aufgelistet.



| IRIS GL-Befehl         | OpenGL-Befehl                                                               | Bedeutung                                           |
|----------------------|---------------------------------------------------------------------------|---------------------------------------------------|
| **acbuf**(AC \_ Clear) | **glClear**(GL- \_ Accum- \_ Puffer \_ Bit)                                     | Löschen Sie den Akkumulations Puffer.                    |
|                      | **glclearcolor**                                                          | Legen Sie die RGBA-Clear-Farbe fest.                         |
|                      | **glclearindex**                                                          | Legen Sie den Clear-Color-Index fest.                        |
| **Löschen**            | **glClear**(GL- \_ Farb \_ Puffer \_ Bit)                                     | Löschen Sie den Farb Puffer.                           |
|                      | **glcleartiefe**                                                          | Geben Sie den undeutlichen Wert für den tiefen Puffer an.     |
| **zclear**           | **glClear**(GL- \_ Tiefe- \_ Puffer \_ Bit)                                     | Löschen Sie den tiefen Puffer.                           |
| **czclear**          | **glClear**(GL- \_ Farb \_ Puffer Bit-GL- \_ \| \_ tiefen \_ Puffer \_ Bit)<br/> | Löschen Sie den Farb Puffer und den tiefen Puffer.      |
|                      | **glclearaccum**                                                          | Geben Sie eindeutige Werte für den Akkumulations Puffer an. |
|                      | **glclearstencil**                                                        | Geben Sie den undeutlichen Wert für den Schablonen Puffer an.   |
| **sClear**           | **glClear**(GL- \_ Schablone- \_ Puffer \_ Bit)                                   | Löschen Sie den Schablonen Puffer.                         |



 

Wenn Ihr IRIS GL-Code sowohl **gclear** als auch **sClear** verwendet, können Sie diese in einem einzelnen **glClear** -Befehl kombinieren. kann die Leistung des Programms verbessern.

 

 





