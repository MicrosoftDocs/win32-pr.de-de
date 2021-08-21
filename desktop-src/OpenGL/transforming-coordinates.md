---
title: Transformieren von Koordinaten
description: Die OpenGL-Hilfsprogrammbibliothek (GLU) bietet mehrere häufig verwendete Matrixtransformationsfunktionen.
ms.assetid: 9ca32be8-3bc0-4fca-a58c-69a4800c3c55
keywords:
- OpenGL-Hilfsprogramm (GLU), Matrixtransformationsfunktionen
- GLU (OpenGL-Hilfsprogramm), Matrixtransformationsfunktionen
- Matrixtransformationsfunktionen OpenGL
- OpenGL-Hilfsprogramm (GLU), Transformieren von Koordinaten
- GLU (OpenGL-Hilfsprogramm), Transformieren von Koordinaten
- Transformieren von Koordinaten OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3c2e4f8c0dd9540e8ba7963640072ebf44997cf9d99e807f31914ddf8eed4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553570"
---
# <a name="transforming-coordinates"></a>Transformieren von Koordinaten

Die OpenGL-Hilfsprogrammbibliothek (GLU) bietet mehrere häufig verwendete Matrixtransformationsfunktionen. Sie können einen zweidimensionalen orthografischen Anzeigebereich mit [**gluOrtho2D,**](gluortho2d.md)ein standardmäßiges Perspektivansichtsvolumen mithilfe von [**gluPerspective**](gluperspective.md)oder ein Ansichtsvolumen einrichten, das mit [**gluLookAt**](glulookat.md)auf einem angegebenen Augenpunkt zentriert ist. Jede dieser Funktionen erstellt die gewünschte Matrix und wendet sie mit [**glMultMatrix**](glmultmatrix.md)auf die aktuelle Matrix an.

Die [**gluPickMatrix-Funktion**](glupickmatrix.md) vereinfacht die Auswahl einer Auswahlmatrix, indem eine Matrix erstellt wird, die das Zeichnen auf einen kleinen Bereich des Viewports beschränkt. Wenn Sie die Szene im Auswahlmodus erneut rendern, nachdem diese Matrix angewendet wurde, werden alle Objekte ausgewählt, die in der Nähe des Cursors gezeichnet werden, und Informationen zu ihnen werden im Auswahlpuffer gespeichert. Weitere Informationen zum Auswahlmodus finden Sie unter "Durchführen von Auswahl und Feedback" [Durchführen von Auswahl und Feedback.](performing-selection-and-feedback.md)

Um zu bestimmen, wo im Fenster ein Objekt gezeichnet wird, verwenden Sie [**gluProject,**](gluproject.md)das die angegebenen Objektkoordinaten *objx,* *objy* und *objz* mithilfe von *modelMatrix,* *projMatrix* und *viewport* in Fensterkoordinaten konvertiert. Das Ergebnis wird in *winx*, *winy* und *winz gespeichert.* Wenn die Funktion erfolgreich ist, ist der Rückgabewert GL \_ TRUE. Wenn die Funktion fehlschlägt, ist der Rückgabewert GL \_ FALSE.

Die [**gluUnProject-Funktion**](gluunproject.md) führt die umgekehrte Konvertierung aus: Sie transformiert die angegebenen Fensterkoordinaten *winx,* *winy* und *winz* mithilfe von *modelMatrix,* *projMatrix* und *Viewport* in Objektkoordinaten. Das Ergebnis wird in *objx*, *objy* und *objz gespeichert.* Wenn die Funktion erfolgreich ist, ist der Rückgabewert GL \_ TRUE. Wenn die Funktion fehlschlägt, ist der Rückgabewert GL \_ FALSE.

 

 




