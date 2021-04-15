---
title: Angeben von Rückrufen
description: Sie können bis zu fünf Rückruf Funktionen für ein Mosaik angeben.
ms.assetid: b49a8400-8111-450d-a2d7-c313a898a213
keywords:
- OpenGL-Hilfsprogramm (GLU), angeben von Rückruf Funktionen
- GLU (OpenGL-Hilfsprogramm), angeben von Rückruf Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6086448cf6f4a71ea6a49359d5656f12f613d760
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516029"
---
# <a name="specifying-callbacks"></a>Angeben von Rückrufen

Sie können bis zu fünf Rückruf Funktionen für ein Mosaik angeben. Alle Funktionen, die Sie nicht angeben, werden im Mosaik Prozess nicht aufgerufen, und Sie erhalten keine Informationen, die Sie möglicherweise zurückgegeben haben. Sie geben die Rückruf Funktionen mit " [*glutesscallback*](glutess.md)" an.

Die Funktion " **glutesscallback** " verknüpft die Rückruffunktion " *FN* " mit dem Mosaik Objekt " *tessobj*". Der Typ des Rückrufs wird durch den *Parametertyp* bestimmt, der z. b. " **glu \_ Begin**", " **glu \_ Edge \_ Flag** **", " \_** **glu \_ Scheitel** Punkt" oder " **glu- \_ Fehler**" sein kann. Die fünf möglichen Rückruf Funktionen verfügen über die folgenden Prototypen.



| Rückruffunktion   | Prototyp                                    |
|---------------------|----------------------------------------------|
| **Glu \_ Anfang**      | **void** **Begin**(**GLenum * * *-Typ* );       |
| **Glu \_ Edge- \_ Flag** | **void** **edgeflag**(**glboolean * * *-Flag* ); |
| **Glu- \_ Scheitelpunkt**     | **void** **Scheitel** Punkt (**void \* * * *-Daten* );     |
| **Glu \_ Ende**        |  **Ende beenden**( *void* );                  |
| **Glu- \_ Fehler**      | **void** - **Fehler**(**GLenum * * * errno* );      |



 

Um eine Rückruffunktion zu ändern, rufen Sie mit der neuen Funktion " [*glutesscallback*](glutess.md) " auf. Um eine Rückruffunktion auszuschließen, ohne Sie durch eine neue zu ersetzen, **übergeben Sie** für die entsprechende Funktion einen NULL-Zeiger.

Wenn das Mosaik Vorgang fortgesetzt wird, werden die Rückruf Funktionen ähnlich wie die OpenGL-Funktionen " [**glBegin**](glbegin.md)", " [gledgeflag](gledgeflag-functions.md)", " [glVertex](glvertex-functions.md)" und " [**glEnd**](glend.md)" aufgerufen.

Die **glu \_ Begin** -Rückruffunktion wird mit einem von drei möglichen Parametern aufgerufen:

-   GL- \_ Dreiecks \_ Lüfter
-   GL- \_ Dreiecks \_ Streifen
-   GL- \_ Dreiecke

Nach dem Aufrufen der Funktion " **glu \_ Begin** Callback" und vor dem Aufrufen der mit dem " **glu \_ End**" verknüpften Rückruffunktion wird eine Kombination aus dem glu-edgeflag und dem **glu \_ Vertex** -Rückrufe aufgerufen. **\_ \_** Die zugeordneten Scheitel Punkte und edgeflags werden genau so interpretiert, wie Sie in OpenGL zwischen **glBegin**(GL- \_ Dreieck- \_ Lüfter), **glBegin**(GL- \_ Dreiecks \_ Streifen) oder **glBegin**(GL \_ -Dreiecke **)** und dem passenden **glEnd** liegen.

Da edgeflags in einem Dreiecks Lüfter oder einem Dreiecks Streifen keinen Sinn ergeben, wird der **glu \_ Begin** -Rückruf nur mit **GL- \_ Dreiecke** aufgerufen, wenn eine Rückruffunktion mit einem glu-edgeflag verknüpft ist. **\_ \_** Die Funktion " **glu \_ Edge \_ Flag** Callback" funktioniert analog zur OpenGL [gledgeflag](gledgeflag-functions.md) -Funktion.

Wenn während des Mosaik Fehlers ein Fehler auftritt, wird die Fehler Rückruffunktion aufgerufen. An die Fehler Rückruffunktion wird eine glu-Fehlernummer übermittelt. Sie können eine Zeichenfolge abrufen, in der der Fehler mit der Funktion " [**gluerrorstring**](gluerrorstring.md) " beschrieben wird.

 

 




