---
title: Portieren von Anzeigelisten
description: Die OpenGL-Implementierung von Anzeigelisten ähnelt der IRIS GL-Implementierung. Mit zwei Ausnahmen in OpenGL können Sie Anzeigelisten nicht mehr bearbeiten, nachdem Sie sie erstellt haben, und Sie können keine Funktionen aus Anzeigelisten aufrufen.
ms.assetid: 617e19ff-6a55-4f7c-b229-075cdee8f1cf
keywords:
- IRIS GL-Portierung, Anzeigelisten
- Portieren von IRIS GL, Anzeigelisten
- Portieren von IRIS GL zu OpenGL, Anzeigen von Listen
- OpenGL-Portierung von IRIS GL, Anzeigelisten
- Anzeigelisten,Portieren von IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858f1f3be180b3ef09c81bb8d61b18705fc9485742d7384562eecff142f4bfb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117980802"
---
# <a name="porting-display-lists"></a>Portieren von Anzeigelisten

Die OpenGL-Implementierung von Anzeigelisten ähnelt der IRIS GL-Implementierung mit zwei Ausnahmen: In OpenGL können Sie Anzeigelisten nicht mehr bearbeiten, nachdem Sie sie erstellt haben, und Sie können keine Funktionen aus Anzeigelisten aufrufen.

Da Sie Funktionen nicht in Anzeigelisten bearbeiten oder aufrufen können, weisen diese IRIS GL-Funktionen in OpenGL keine Entsprechung auf:

-   **editobj**
-   **objdelete,** **objinsert** und **objreplace**
-   **maketag,** **gentag,** **istag** und **deltag**
-   **callfunc**

In IRIS GL verwenden Sie die Funktionen **makeobj** und **closeobj,** um Anzeigelisten zu erstellen. In OpenGL verwenden Sie [**glNewList**](glnewlist.md) und [**glEndList.**](glendlist.md)

In der folgenden Tabelle sind die IRIS GL-Anzeigelistenfunktionen mit ihren entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion | OpenGL-Funktion                                                      | Bedeutung                                                       |
|------------------|----------------------------------------------------------------------|---------------------------------------------------------------|
| **makeobj**      | **glNewList**                                                        | Erstellt eine neue Anzeigeliste.                                   |
| **closeobj**     | **glEndList**                                                        | Signalisiert das Ende der Anzeigeliste.                                  |
| **callobj**      | [**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md) | Führt Anzeigelisten aus.                               |
| **isobj**        | [**glIsList**](glislist.md)                                         | Testet das Vorhandensein von Anzeigelisten.                             |
| **delobj**       | [**glDeleteLists**](gldeletelists.md)                               | Löscht zusammenhängende Gruppen von Anzeigelisten.                    |
| **genobj**       | [**glGenLists**](glgenlists.md)                                     | Generiert die angegebene Anzahl zusammenhängender leerer Anzeigelisten. |



 

Dieses Thema enthält Informationen zu folgendem Thema.

-   [Portieren der bbox2-Funktion](porting-the-bbox2-function.md)
-   [Portieren bearbeiteter Anzeigelisten](porting-edited-display-lists.md)
-   [Beispielport einer Anzeigeliste](a-sample-port-of-a-display-list.md)

 

 




