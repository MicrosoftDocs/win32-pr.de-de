---
title: Portieren von Farb-, Schattierungs-und beschreibe-Code
description: Portieren von Farb-, Schattierungs-und beschreibe-Code
ms.assetid: ffcf33b2-c3b8-4e89-9c2f-085b98cbb496
keywords:
- IRIS GL portieren, Farbe
- Portieren von IRIS GL, Color
- Portieren auf OpenGL von IRIS GL, Color
- OpenGL-Portierung von IRIS GL, Color
- IRIS GL portieren, Schattierung
- Portieren von IRIS GL, Schattierung
- Portieren auf OpenGL von IRIS GL, Schattierung
- OpenGL-Portierung von IRIS GL, Schattierung
- IRIS GL portieren, Write-Ask
- Portieren von IRIS GL, Write temask
- Portieren auf OpenGL von IRIS GL, Write temask
- OpenGL-Portierung von IRIS GL, Write temask
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8bc35986bc0f9d7076411fecbd9c1fa5d7bfbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708466"
---
# <a name="porting-color-shading-and-writemask-code"></a>Portieren von Farb-, Schattierungs-und beschreibe-Code

Beachten Sie beim Portieren von Farb-, Schattierungs-und beschreibe-Code in OpenGL die folgenden Punkte:

-   Obwohl Sie Farb Zuordnungs Indizes mit der OpenGL-Funktion " [glindex](glindex-functions.md) " festlegen können, verfügt OpenGL nicht über eine Funktion zum Laden von Farb Zuordnungs Indizes.
-   Farbwerte werden in ihren Datentyp normalisiert. (Informationen zu Farbwerten finden Sie unter [glcolor](glcolor-functions.md)).
-   Es gibt keine einfache Entsprechung für **CPack**.
-   Sie müssen möglicherweise Code, der die **c** -oder **Color** -Funktionen enthält, in [**glclearcolor**](glclearcolor.md) oder [**glclearindex**](glclearindex.md) anstelle von **glcolor** oder **glindex** übersetzen.
-   Die RGBA-Schreibweise wird für jede Komponente angewendet, aber nicht für jedes Bit.
-   IRIS GL bietet definierte Farb Konstanten: schwarz, blau, rot, grün, Magenta, Cyan, gelb und weiß. OpenGL bietet diese Konstanten nicht.

Dieses Thema enthält Informationen zu den folgenden Themen.

-   [Portieren von Farb aufrufen](porting-color-calls.md)
-   [Portieren von Schattierungs Modellen](porting-shading-models.md)

 

 




