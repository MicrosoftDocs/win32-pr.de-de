---
title: Transformieren von Koordinaten
description: Die OpenGL Utility Library (GLU) stellt mehrere häufig verwendete Matrix Transformations Funktionen bereit.
ms.assetid: 9ca32be8-3bc0-4fca-a58c-69a4800c3c55
keywords:
- OpenGL-Hilfsprogramm (GLU), Matrix Transformations Funktionen
- GLU (OpenGL-Hilfsprogramm), Matrix Transformations Funktionen
- Matrix Transformations Funktionen OpenGL
- OpenGL-Hilfsprogramm (GLU), Transformieren von Koordinaten
- GLU (OpenGL-Hilfsprogramm), Transformieren von Koordinaten
- Transformieren von Koordinaten OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a5a58c723dcccfc54ce2f47a01710133ccc30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713937"
---
# <a name="transforming-coordinates"></a>Transformieren von Koordinaten

Die OpenGL Utility Library (GLU) stellt mehrere häufig verwendete Matrix Transformations Funktionen bereit. Sie können einen zweidimensionalen orthografischen Anzeigebereich mit [**gluOrtho2D**](gluortho2d.md), ein Standardmäßiges perspektivisches Ansichts Volume mithilfe von " [**gluperspective**](gluperspective.md)" oder ein Ansichts Volume einrichten, das auf einem angegebenen Punkt mit " [**glulookat**](glulookat.md)" zentriert ist. Jede dieser Funktionen erstellt die gewünschte Matrix und wendet sie mit [**glmultmatrix**](glmultmatrix.md)auf die aktuelle Matrix an.

Die Funktion " [**glupickmatrix**](glupickmatrix.md) " vereinfacht die Auswahl einer Auswahl Matrix, indem eine Matrix erstellt wird, die das Zeichnen auf einen kleinen Bereich des Viewports einschränkt. Wenn Sie die Szene nach dem Anwenden dieser Matrix im Auswahlmodus erneut Renderen, werden alle Objekte, die in der Nähe des Cursors gezeichnet werden, ausgewählt, und die Informationen zu Ihnen werden im Auswahl Puffer gespeichert. Weitere Informationen zum Auswahlmodus finden Sie unter "Auswahl und Feedback durchführen" Auswahl [und Feedback](performing-selection-and-feedback.md).

Um zu ermitteln, an welcher Stelle im Fenster ein Objekt gezeichnet wird, verwenden Sie " [**gluproject**](gluproject.md)", das die angegebenen Objekt Koordinaten " *objX*", " *objy*" und " *objz* " mithilfe von *modelmatrix*, *projmatrix* und *Viewport* in Fenster Koordinaten konvertiert. Das Ergebnis wird in *Winx*, *Winy* und *Winz* gespeichert. Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert "GL \_ true". Wenn die Funktion fehlschlägt, ist der Rückgabewert "GL \_ false".

Die Funktion " [**gluunproject**](gluunproject.md) " führt die umgekehrte Konvertierung durch: Sie transformiert die angegebenen Fenster Koordinaten *Winx*, *Winy* und *Winz* in Objekt Koordinaten mithilfe von *modelmatrix*, *projmatrix* und *Viewport*. Das Ergebnis wird in *objX*, *objy* und *objz* gespeichert. Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert "GL \_ true". Wenn die Funktion fehlschlägt, ist der Rückgabewert "GL \_ false".

 

 




