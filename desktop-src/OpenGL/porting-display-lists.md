---
title: Portieren von Anzeigelisten
description: Die OpenGL-Implementierung von Anzeigelisten ähnelt der Iris GL-Implementierung, mit zwei Ausnahmen in OpenGL können Sie anzeigen Listen nicht bearbeiten, nachdem Sie Sie erstellt haben, und Sie können keine Funktionen aus Anzeigelisten aufrufen.
ms.assetid: 617e19ff-6a55-4f7c-b229-075cdee8f1cf
keywords:
- IRIS GL portieren, Anzeigen von Listen
- Portieren von IRIS GL, Anzeigen von Listen
- Portieren auf OpenGL von IRIS GL, Anzeigen von Listen
- OpenGL-Portierung von IRIS GL, Anzeigen von Listen
- Anzeigen von Listen, Portieren von IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461000e6d785f0d03bbbc8f738eba60768bc5d74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309451"
---
# <a name="porting-display-lists"></a>Portieren von Anzeigelisten

Die OpenGL-Implementierung von Anzeigelisten ähnelt der Iris GL-Implementierung mit zwei Ausnahmen: in OpenGL können Sie anzeigen Listen nicht bearbeiten, nachdem Sie Sie erstellt haben, und Sie können keine Funktionen aus Anzeigelisten aufrufen.

Da Sie Funktionen nicht innerhalb von Anzeigelisten bearbeiten oder aufrufen können, haben diese IRIS GL-Funktionen in OpenGL keine Entsprechung:

-   **editobj**
-   **objdelete**, **objinsert** und **objreplace**
-   **maketag**, **Gentag**, **ISTAG** und **Delta Tag**
-   **callfunc**

In IRIS GL verwenden Sie die Funktionen **makeobj** und **closeobj** , um Anzeigelisten zu erstellen. In OpenGL verwenden Sie " [**glnewlist**](glnewlist.md) " und " [**glendlist**](glendlist.md)".

In der folgenden Tabelle sind die Funktionen der Iris GL-Anzeigeliste mit den entsprechenden OpenGL-Funktionen aufgelistet.



| IRIS GL-Funktion | OpenGL-Funktion                                                      | Bedeutung                                                       |
|------------------|----------------------------------------------------------------------|---------------------------------------------------------------|
| **makeobj**      | **glnewlist**                                                        | Erstellt eine neue Anzeigeliste.                                   |
| **closeobj**     | **glendlist**                                                        | Signalisiert das Ende der Anzeigeliste.                                  |
| **czuweisung**      | [**glCallList**](glcalllist.md), [ **glcalllists**](glcalllists.md) | Führt die Anzeigeliste oder Listen aus.                               |
| **isobj**        | [**glislist**](glislist.md)                                         | Testet, ob die Anzeigeliste vorhanden ist.                             |
| **Delta-**       | [**gldelta etelists**](gldeletelists.md)                               | Löscht eine zusammenhängende Gruppe von Anzeigelisten.                    |
| **genobj**       | [**glgenlists**](glgenlists.md)                                     | Generiert die angegebene Anzahl von zusammenhängenden leeren Anzeigelisten. |



 

Dieses Thema enthält Informationen zu den folgenden Themen.

-   [Portieren der BBOX2-Funktion](porting-the-bbox2-function.md)
-   [Portieren von bearbeiteten anzeigen Listen](porting-edited-display-lists.md)
-   [Einen Beispielport einer Anzeigeliste](a-sample-port-of-a-display-list.md)

 

 




