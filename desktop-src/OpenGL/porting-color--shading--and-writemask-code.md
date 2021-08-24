---
title: Portieren von Farbe, Schattierung und Schreibmaskencode
description: Portieren von Farbe, Schattierung und Schreibmaskencode
ms.assetid: ffcf33b2-c3b8-4e89-9c2f-085b98cbb496
keywords:
- IRIS GL-Portierung, Farbe
- Portieren von IRIS GL, Farbe
- Portieren von IRIS GL zu OpenGL, Farbe
- OpenGL-Portierung von IRIS GL, Farbe
- IRIS GL-Portierung, Schattierung
- Portieren von IRIS GL, Schattierung
- Portieren von IRIS GL zu OpenGL, Schattierung
- OpenGL-Portierung von IRIS GL,Schattierung
- IRIS GL-Portierung, Schreibmaske
- Portieren von IRIS GL, Schreibmaske
- Portieren von IRIS GL zu OpenGL, Schreibmaske
- OpenGL-Portierung von IRIS GL, Schreibmaske
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9d3fcb9cf47b45b4b1174cb20e3259dbb883c2fd0414d255a418c52b50fa28e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485780"
---
# <a name="porting-color-shading-and-writemask-code"></a>Portieren von Farbe, Schattierung und Schreibmaskencode

Beachten Sie beim Portieren von Farbe, Schattierung und Schreiben von Textmaskencode in OpenGL die folgenden Punkte:

-   Obwohl Sie Farbzuordnungsindizes mit der OpenGL [glIndex-Funktion](glindex-functions.md) festlegen können, verfügt OpenGL nicht über eine Funktion zum Laden von Farbzuordnungsindizes.
-   Farbwerte werden auf ihren Datentyp normalisiert. (Informationen zu Farbwerten finden Sie unter [glColor](glcolor-functions.md).
-   Es gibt keine einfache Entsprechung für **cpack**.
-   Möglicherweise müssen Sie Code, der die **c-** oder **color-Funktionen** enthält, in [**glClearColor**](glclearcolor.md) oder [**glClearIndex**](glclearindex.md) anstelle von **glColor** oder **glIndex** übersetzen.
-   Die RGBA-Schreibmaske gilt für jede Komponente, jedoch nicht für jedes Bit.
-   IRIS GL stellt definierte Farbkonstanten bereit: BLACK, BLUE, RED, GREEN, MAGENTA, CYAN, YELLOW und WHITE. OpenGL stellt diese Konstanten nicht bereit.

Dieses Thema enthält Informationen zu folgendem Thema.

-   [Portieren von Farbaufrufen](porting-color-calls.md)
-   [Portieren von Schattierungsmodellen](porting-shading-models.md)

 

 




