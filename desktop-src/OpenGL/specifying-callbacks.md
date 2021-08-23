---
title: Angeben von Rückrufen
description: Sie können bis zu fünf Rückruffunktionen für ein Mosaik angeben.
ms.assetid: b49a8400-8111-450d-a2d7-c313a898a213
keywords:
- OpenGL-Hilfsprogramm (GLU), Angeben von Rückruffunktionen
- GLU (OpenGL-Hilfsprogramm), Angeben von Rückruffunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e57a5f961a980f20451f594fa59885eda99d1e2de94a55fbfd2abd4b8301b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553780"
---
# <a name="specifying-callbacks"></a>Angeben von Rückrufen

Sie können bis zu fünf Rückruffunktionen für ein Mosaik angeben. Alle Funktionen, die Sie nicht angeben, werden während des Mosaiks nicht aufgerufen, und Sie erhalten keine Informationen, die sie möglicherweise zurückgegeben haben. Sie geben die Rückruffunktionen mit [*gluTessCallback an.*](glutess.md)

Die **gluTessCallback-Funktion** ordnet die Rückruffunktion *fn* dem Mosaikobjekt *tessobj zu.* Der Typ des Rückrufs wird durch den Parametertyp *bestimmt,* der **GLU \_ BEGIN,** **GLU EDGE \_ \_ FLAG,** **GLU \_ VERTEX,** **GLU \_ END** oder **GLU ERROR \_ sein kann.** Die fünf möglichen Rückruffunktionen verfügen über die folgenden Prototypen.



| Rückruffunktion   | Prototyp                                    |
|---------------------|----------------------------------------------|
| **GLU \_ BEGIN**      | **void** **begin**(**GLenum-Typ** );       |
| **\_ \_ GLU-EDGEFLAG** | **void** **edgeFlag**(**GLboolean**_flag_ ); |
| **GLU \_ VERTEX**     | **void** **vertex**(**void \* \data* );     |
| **\_GLU-ENDE**        | **void** **end**( *void* );                  |
| **\_GLU-FEHLER**      | **void** **error**(**GLenum**_errno_ );      |



 

Um eine Rückruffunktion zu ändern, rufen Sie [*gluTessCallback*](glutess.md) mit der neuen Funktion auf. Um eine Rückruffunktion zu beseitigen, ohne sie durch eine neue zu ersetzen, übergeben Sie **gluTessCallback** einen NULL-Zeiger für die entsprechende Funktion.

Während das Mosaik fortgesetzt wird, werden die Rückruffunktionen ähnlich wie die OpenGL-Funktionen [**glBegin,**](glbegin.md) [glEdgeFlag,](gledgeflag-functions.md) [glVertex](glvertex-functions.md)und [**glEnd**](glend.md)aufgerufen.

Die **GLU \_ BEGIN-Rückruffunktion** wird mit einem von drei möglichen Parametern aufgerufen:

-   GL \_ TRIANGLE \_ FAN
-   GL \_ TRIANGLE \_ STRIP
-   \_GL-DREIECKE

Nach dem Aufruf der **GLU \_ BEGIN-Rückruffunktion** und vor dem Aufruf der Rückruffunktion, die **GLU \_ END** zugeordnet ist, wird eine Kombination der **GLU \_ \_ EDGE-FLAG-** und **GLU \_ VERTEX-Rückrufe** aufgerufen. Die zugeordneten Scheitelzeichen und Kantenflags werden genau so interpretiert, wie sie sich in OpenGL zwischen **glBegin**(GL \_ TRIANGLE \_ FAN), **glBegin**(GL TRIANGLE STRIP) oder \_ \_ **glBegin**(GL TRIANGLES ) und dem entsprechenden \_ **glEnd befinden.**

Da Kantenflags in einem Dreiecksfächer oder Dreiecksstreifen keinen Sinn ergeben, wird der **GLU \_ BEGIN-Rückruf** nur mit GL TRIANGLES aufgerufen, wenn eine Rückruffunktion dem **GLU \_ EDGE \_ FLAG** zugeordnet **\_ ist.** Die **GLU \_ EDGE \_ FLAG-Rückruffunktion** funktioniert analog zur OpenGL [glEdgeFlag-Funktion.](gledgeflag-functions.md)

Wenn während des Mosaiks ein Fehler auftritt, wird die Fehlerrückruffunktion aufgerufen. Der Fehlerrückruffunktion wird eine GLU-Fehlernummer übergeben. Sie können eine Zeichenfolge abrufen, die den Fehler mit der [**gluErrorString-Funktion**](gluerrorstring.md) beschreibt.

 

 




