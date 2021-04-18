---
title: Portieren von IRIS GL Get-Funktionen
description: 'IRIS GL \ 0034; Get \ 0034; Funktionen haben folgende Form:'
ms.assetid: 5bd6aa13-b41d-4f89-91dc-cc47481ac7b7
keywords:
- IRIS GL Porting, Get Functions
- Portieren von IRIS GL, Get Functions
- Portieren auf OpenGL von IRIS GL, Get Functions
- OpenGL-Portierung von IRIS GL, Get Functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594b12bb1738846b98d33137dd8b623f0405ec40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340436"
---
# <a name="porting-iris-gl-get-functions"></a>Portieren von IRIS GL Get-Funktionen

Die "Get"-Funktionen von IRIS GL haben folgende Form:

``` syntax
int getthing();
```

und

``` syntax
int getthings( int *a, int *b);
```

Der Iris GL-Code umfasst wahrscheinlich Get-Funktionsaufrufe, die etwa wie folgt aussehen:

``` syntax
thing = getthing(); 
if (getthing() == THING) { /* some stuff here */ } 
getthings (&a, &b);
```

In OpenGL verwenden Sie einen der folgenden vier Arten von [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) -Funktionen anstelle der entsprechenden IRIS GL Get-Funktionen:

-   **glgetbooleanv**
-   **glgetintegerv**
-   **glgetfloatv**
-   **glgetdoublev**

Die Funktionen haben die folgende Syntax:

``` syntax
glGet<Datatype>v( value, *data );
```

der *Wert* ist vom Typ " **GLenum** ", und die Daten sind vom Typ " **gldatatype**". Wenn Sie " **glget** " und einen anderen Typ als den erwarteten Typ zurückgeben, wird der Typ entsprechend konvertiert. Eine umfassende Liste der Parameter für **glget** finden Sie unter [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).

 

 




