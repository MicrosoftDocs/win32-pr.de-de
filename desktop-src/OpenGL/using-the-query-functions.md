---
title: Verwenden der Abfragefunktionen
description: Verwenden der Abfragefunktionen
ms.assetid: 5f874a0e-77c0-4009-a18f-a852d7ffe891
keywords:
- OpenGL, Abfragefunktionen
- Abfragefunktionen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e3e883bdf8730dac7b1a8e07448b771109bef0ac5ec2246411703e8f841a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776480"
---
# <a name="using-the-query-functions"></a>Verwenden der Abfragefunktionen

Es gibt vier Abfragefunktionen zum Abrufen einfacher Zustandsvariablen und eine zum Bestimmen, ob ein bestimmter Zustand aktiviert oder deaktiviert ist:

-   [**glGetBooleanv**](glgetbooleanv.md)
-   [**glGetIntegerv**](glgetintegerv.md)
-   [**glGetFloatv**](glgetfloatv.md)
-   [**glGetDoublev**](glgetdoublev.md)
-   [**glIsEnabled**](glisenabled.md)

Die Prototypen für die Abfragefunktionen sind:

**void** **glGetBooleanv**(**GLenum** *pname* , **GLboolean \** _ _params* );

**void** **glGetIntegerv**(**GLenum** *pname* , **GLint \** _ _params* );

**void** **glGetFloatv**(**GLenum** *pname* , **GLfloat \** _ _params* );

**void** **glGetDoublev**(**GLenum** *pname* , **GLdouble \** _ _params* );

Die Abfragefunktionen rufen boolesche, ganzzahlige, Gleitkomma- oder Doppeltgenauigkeitszustandsvariablen ab. Der *pname-Parameter* ist eine symbolische Konstante, die die zurückzugebende Zustandsvariable angibt, und *params* ist ein Zeiger auf ein Array des angegebenen Typs, in dem die zurückgegebenen Daten enthalten sein sollen. Die möglichen Werte für *pname* sind unter [OpenGL-Statusvariablen](opengl-state-variables.md)aufgeführt. Bei Bedarf wird eine Typkonvertierung ausgeführt, um die gewünschte Variable als angeforderten Datentyp zurückzugeben.

Der Prototyp für [**glIsEnabled**](glisenabled.md) lautet:

**GLboolean** **glIsEnabled**(GLenum *cap* );

Wenn der durch *cap* angegebene Modus aktiviert ist, gibt **glIsEnabled** GL \_ TRUE zurück. Wenn der durch *cap* angegebene Modus deaktiviert ist, gibt **glIsEnabled** GL \_ FALSE zurück. Die möglichen Werte für *cap* sind unter [OpenGL-Statusvariablen](opengl-state-variables.md)aufgeführt.

Andere spezialisierte Funktionen geben bestimmte Zustandsvariablen zurück. Informationen zur Verwendung dieser Funktionen finden Sie unter OpenGL State Variables (OpenGL-Zustandsvariablen) und *openGL Reference Manual (OpenGL-Referenzhandbuch).* Weitere Informationen zur Fehlerbehandlungsfunktion von OpenGL und zur **glGetError-Funktion** finden Sie unter [Fehlerbehandlung.](error-handling.md)

Die Funktionen, die bestimmte Zustandsvariablen zurückgeben, sind:

-   [**glGetClipPlane**](glgetclipplane.md)
-   [**glGetError**](glgeterror.md)
-   [**glGetLight**](glgetlight.md)
-   [**glGetMap**](glgetmap.md)
-   [**glGetMaterial**](glgetmaterial.md)
-   [**glGetPixelMap**](glgetpixelmap.md)
-   [**glGetPolygonStipple**](glgetpolygonstipple.md)
-   [**glGetString**](glgetstring.md)
-   [**glGetTexEnv**](glgettexenv.md)
-   [**glGetTexGen**](glgettexgen.md)
-   [**glGetTexImage**](glgetteximage.md)
-   [**glGetTexLevelParameter**](glgettexlevelparameter.md)
-   [**glGetTexParameter**](glgettexparameter.md)

 

 




