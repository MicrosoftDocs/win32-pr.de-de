---
title: Portieren von IRIS GL Get-Funktionen
description: 'IRIS GL \ 0034;get \ 0034; -Funktionen haben die folgende Form:'
ms.assetid: 5bd6aa13-b41d-4f89-91dc-cc47481ac7b7
keywords:
- IRIS GL-Portierung, Get-Funktionen
- Portieren von IRIS GL,Get-Funktionen
- Portieren von IRIS GL zu OpenGL, Abrufen von Funktionen
- OpenGL-Portierung von IRIS GL,Get-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfe9159e0207198fa94959729bd0c95439bb91b5dd55a8a1f9adf3b048d7bb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485560"
---
# <a name="porting-iris-gl-get-functions"></a>Portieren von IRIS GL Get-Funktionen

IRIS GL-Get-Funktionen haben die folgende Form:

``` syntax
int getthing();
```

und

``` syntax
int getthings( int *a, int *b);
```

Ihr IRIS GL-Code enthält wahrscheinlich Get-Funktionsaufrufe, die in etwa wie folgt aussehen:

``` syntax
thing = getthing(); 
if (getthing() == THING) { /* some stuff here */ } 
getthings (&a, &b);
```

In OpenGL verwenden Sie eine der folgenden vier Typen von [**glGet-Funktionen**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) anstelle der entsprechenden IRIS GL get-Funktionen:

-   **glGetBooleanv**
-   **glGetIntegerv**
-   **glGetFloatv**
-   **glGetDoublev**

Die Funktionen weisen die folgende Syntax auf:

``` syntax
glGet<Datatype>v( value, *data );
```

dabei ist *value* vom Typ **GLenum** und data vom Typ **GLdatatype.** Wenn Sie **glGet** aufrufen und einen anderen Typ als den erwarteten Typ zurückgibt, wird der Typ entsprechend konvertiert. Eine vollständige Liste der **glGet-Parameter** finden Sie unter [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).

 

 




