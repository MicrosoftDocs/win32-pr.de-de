---
title: Abrufen von Zustandsinformationen
description: Abrufen von Zustandsinformationen
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL, Zustandsinformationen
- OpenGL, Zustandsvariablen
- Zustandsinformationen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfac92233e971104fd4d343970a9ecc79496ed54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709719"
---
# <a name="obtaining-state-information"></a>Abrufen von Zustandsinformationen

OpenGL verwaltet viele Zustandsvariablen, die sich auf das Verhalten vieler Funktionen auswirken. Einige dieser Variablen verfügen über spezialisierte Abfragefunktionen.



|                                          |                                                    |                                                          |
|------------------------------------------|----------------------------------------------------|----------------------------------------------------------|
| [**glgetclipplane**](glgetclipplane.md) | [**glgetpixelmap**](glgetpixelmap.md)             | [**glgetteximage**](glgetteximage.md)                   |
| [**glgetlight**](glgetlight.md)         | [**glgetpolygonstippel**](glgetpolygonstipple.md) | [**glgettexlevelparameter**](glgettexlevelparameter.md) |
| [**glgetmap**](glgetmap.md)             | [**glgettex-v**](glgettexenv.md)                 | [**glgettexparameter**](glgettexparameter.md)           |
| [**glgetmaterial**](glgetmaterial.md)   | [**glgettexgen**](glgettexgen.md)                 |                                                          |



 

Um den Wert anderer Zustandsvariablen zu erhalten, verwenden Sie je nach Bedarf " [**glgetbooleanv**](glgetbooleanv.md)", " [**glgetdoublev**](glgetdoublev.md)", " [**glgetfloatv**](glgetfloatv.md)" oder " [**glgetintegerv**](glgetintegerv.md)". Weitere Informationen zur Verwendung dieser Funktionen finden Sie unter [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) . Andere Abfragefunktionen, die Sie verwenden möchten, sind " [**glgeterror**](glgeterror.md)", " [**glgetstring**](glgetstring.md)" und " [**glisenabled**](glisenabled.md)". (Weitere Informationen zu Funktionen im Zusammenhang mit der Fehlerbehandlung finden Sie unter [Behandeln von Fehlern](handling-errors.md) ). Verwenden Sie zum Speichern und Wiederherstellen von Gruppen von Zustandsvariablen [**glpushatpub**](glpushattrib.md) und [**glpopatpub**](glpopattrib.md).

-   [Verwenden der Abfragefunktionen](using-the-query-functions.md)
-   [Fehlerbehandlung](error-handling.md)
-   [OpenGL-Fehler Codes](opengl-error-codes.md)
-   [Speichern und Wiederherstellen von Sätzen von Zustandsvariablen](saving-and-restoring-sets-of-state-variables.md)
-   [OpenGL-Zustandsvariablen](opengl-state-variables.md)
-   [Referenz zu Zustandsinformationen](state-information-reference.md)

 

 




