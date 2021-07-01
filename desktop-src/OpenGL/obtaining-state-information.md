---
title: Abrufen von Zustandsinformationen
description: Abrufen von Zustandsinformationen
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL,Zustandsinformationen
- OpenGL,Zustandsvariablen
- 'Zustandsinformationen: OpenGL'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8329fd34fc68122be8d63e4dc28756f88faf7797
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120685"
---
# <a name="obtaining-state-information"></a>Abrufen von Zustandsinformationen

OpenGL verwaltet viele Zustandsvariablen, die sich auf das Verhalten vieler Funktionen auswirken. Einige dieser Variablen verfügen über spezielle Abfragefunktionen.

:::row:::
    :::column:::
        [**glGetClipPlane**](glgetclipplane.md)
    :::column-end:::
    :::column:::
        [**glGetPixelMap**](glgetpixelmap.md)
    :::column-end:::
    :::column:::
        [**glGetTexImage**](glgetteximage.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**glGetLight**](glgetlight.md)
    :::column-end:::
    :::column:::
        [**glGetPolygonStipple**](glgetpolygonstipple.md)
    :::column-end:::
    :::column:::
        [**glGetTexLevelParameter**](glgettexlevelparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**glGetMap**](glgetmap.md)
    :::column-end:::
    :::column:::
        [**glGetTexEnv**](glgettexenv.md)
    :::column-end:::
    :::column:::
        [**glGetTexParameter**](glgettexparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**glGetMaterial**](glgetmaterial.md)
    :::column-end:::
    :::column:::
        [**glGetTexGen**](glgettexgen.md)
    :::column-end:::
    :::column:::

    :::column-end:::
:::row-end:::

Verwenden Sie [**glGetBooleanv,**](glgetbooleanv.md) [**glGetDoublev,**](glgetdoublev.md) [**glGetFloatv**](glgetfloatv.md)oder [**glGetIntegerv,**](glgetintegerv.md)um den Wert anderer Zustandsvariablen zu erhalten. Informationen zur Verwendung dieser Funktionen finden Sie unter [**glGet.**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) Weitere Abfragefunktionen, die Sie möglicherweise verwenden möchten, sind [**glGetError,**](glgeterror.md) [**glGetString**](glgetstring.md)und [**glIsEnabled.**](glisenabled.md) (Weitere [Informationen zu Funktionen im Zusammenhang](handling-errors.md) mit der Fehlerbehandlung finden Sie unter Behandeln von Fehlern.) Verwenden Sie [**glPushAttrib**](glpushattrib.md) und [**glPopAttrib,**](glpopattrib.md)um Sätze von Zustandsvariablen zu speichern und wiederherzustellen.

-   [Verwenden der Abfragefunktionen](using-the-query-functions.md)
-   [Fehlerbehandlung](error-handling.md)
-   [OpenGL-Fehlercodes](opengl-error-codes.md)
-   [Speichern und Wiederherstellen von Sätzen von Zustandsvariablen](saving-and-restoring-sets-of-state-variables.md)
-   [OpenGL-Zustandsvariablen](opengl-state-variables.md)
-   [Referenz zu Zustandsinformationen](state-information-reference.md)

 

 




