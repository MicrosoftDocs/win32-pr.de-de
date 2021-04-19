---
title: Verwenden der Abfragefunktionen
description: Verwenden der Abfragefunktionen
ms.assetid: 5f874a0e-77c0-4009-a18f-a852d7ffe891
keywords:
- OpenGL, Abfragefunktionen
- Abfragefunktionen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14804b260451d4b51b0146b1cb2f796ba6b6778e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341859"
---
# <a name="using-the-query-functions"></a>Verwenden der Abfragefunktionen

Es gibt vier Abfragefunktionen zum Abrufen einfacher Zustandsvariablen und eine zum bestimmen, ob ein bestimmter Zustand aktiviert oder deaktiviert ist:

-   [**glgetbooleanv**](glgetbooleanv.md)
-   [**glgetintegerv**](glgetintegerv.md)
-   [**glgetfloatv**](glgetfloatv.md)
-   [**glgetdoublev**](glgetdoublev.md)
-   [**glisenabled**](glisenabled.md)

Die Prototypen für die Abfragefunktionen lauten wie folgt:

**void** **glgetbooleanv**(**GLenum** *PName* , **glboolean \*** *para* Metern);

**void** **glgetintegerv**(**GLenum** *PName* , **glint \*** *para* Metern);

**void** **glgetfloatv**(**GLenum** *PName* , **glfloat \*** *para* Metern);

**void** **glgetdoublev**(**GLenum** *PName* , **gldouble \*** *para* );

Die Abfragefunktionen erhalten die Statusvariablen "Boolean", "Integer", "Floating-Point" oder "Double Precision". Der *PName* -Parameter ist eine symbolische Konstante, die die zurück zugebende Zustands Variable angibt, und *params* ist ein Zeiger auf ein Array vom Typ, in dem die zurückgegebenen Daten abgelegt werden sollen. Die möglichen Werte für " *PName* " sind in den [OpenGL-Zustandsvariablen](opengl-state-variables.md)aufgeführt. Eine Typkonvertierung wird ausgeführt, wenn die gewünschte Variable als angeforderter Datentyp zurückgegeben werden muss.

Der Prototyp für " [**glisenabled**](glisenabled.md) " ist:

**Glboolean** - **glisenabled**(GLenum- *Cap* );

Wenn der durch *Cap* angegebene Modus aktiviert ist, gibt " **glisenabled** " den Wert "GL true" zurück \_ . Wenn der durch *Cap* angegebene Modus deaktiviert ist, gibt " **glisenabled** " den Wert "GL false" zurück \_ . Die möglichen Werte für *Cap* sind unter [OpenGL-Zustandsvariablen](opengl-state-variables.md)aufgeführt.

Bei anderen spezialisierten Funktionen werden bestimmte Zustandsvariablen zurückgegeben. Informationen dazu, wann diese Funktionen verwendet werden sollten, finden Sie unter OpenGL-Zustandsvariablen und im *OpenGL-Referenzhandbuch*. Weitere Informationen zur Fehlerbehandlung von OpenGL und zur Funktion " **glgeterror** " finden Sie unter [Fehlerbehandlung](error-handling.md).

Die Funktionen, die bestimmte Zustandsvariablen zurückgeben, lauten wie folgt:

-   [**glgetclipplane**](glgetclipplane.md)
-   [**glgeterror**](glgeterror.md)
-   [**glgetlight**](glgetlight.md)
-   [**glgetmap**](glgetmap.md)
-   [**glgetmaterial**](glgetmaterial.md)
-   [**glgetpixelmap**](glgetpixelmap.md)
-   [**glgetpolygonstippel**](glgetpolygonstipple.md)
-   [**glgetstring**](glgetstring.md)
-   [**glgettex-v**](glgettexenv.md)
-   [**glgettexgen**](glgettexgen.md)
-   [**glgetteximage**](glgetteximage.md)
-   [**glgettexlevelparameter**](glgettexlevelparameter.md)
-   [**glgettexparameter**](glgettexparameter.md)

 

 




