---
title: Struktur von Schnittmengenattributen
description: Eine -Struktur, die in HLSL deklariert ist, um Trefferattribute für dreieckige Schnittpunkte fester Funktionen oder einen achsenbündigen Begrenzungsbereich für prozedurale primitive Schnittmenge zu darstellen.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: fea10edb8402f07431d488ff9d28d1de539259e51bc1893d20e76e8f4cc3cdab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528118"
---
# <a name="intersection-attributes-structure"></a>Struktur von Schnittmengenattributen 

Eine -Struktur, die in HLSL deklariert ist, um Trefferattribute für dreieckige Schnittpunkte fester Funktionen oder einen achsenbündigen Begrenzungsbereich für prozedurale primitive Schnittmenge zu darstellen.

## <a name="fixed-function-triangle-intersection"></a>Feste Funktionsdreieck-Schnittmenge

Die folgende Struktur wird in HLSL deklariert, um Trefferattribute für die Dreieckskreuzung fester Funktion zu darstellen:


```
struct BuiltInTriangleIntersectionAttributes
{
    float2 barycentrics;
};
```

[Alle Treffer- und](any-hit-shader.md) [nächstgelegenen Treffer-Shader,](closest-hit-shader.md) die mit einer Dreiecksschnittmenge fester Funktionen aufgerufen werden, müssen diese Struktur für Trefferattribute verwenden. Bei den Attributen a0, a1 und a2 für die drei Scheitelungen eines Dreiecks ist barycentrics.x die Gewichtung für a1 und barycentrics.y die Gewichtung für a2.  Die App kann beispielsweise interpolieren, indem sie folgendes vorzieht: a = a0 + barycentrics.x * (a1-a0) + barycentrics.y* (a2 – a0).

## <a name="axis-aligned-bounding-box-for-procedural-primitive-intersection"></a>Achsenbündig ausgerichtetes Begrenzungsfeld für prozedurale primitive Schnittmenge

Wenn achsenbündig ausgerichtete Begrenzungsfelder für die Schnittmenge mit prozeduralen Primitiven verwendet werden, wird ein Schnittpunkt-Shader ausgelöst.  Dieser Shader bietet eine benutzerdefinierte Schnittmengenattributstruktur für den [**ReportHit-Aufruf.**](reporthit-function.md)  Alle Treffer- und nächstgelegenen Treffer-Shader, die in derselben Treffergruppe mit diesem Schnittpunkt-Shader gebunden sind, müssen dieselbe Struktur für Trefferattribute verwenden, auch wenn nicht auf die Attribute verwiesen wird.  Die maximale Größe der Attributstruktur beträgt 32 Byte, definiert als **D3D12 \_ RAYTRACING \_ MAX ATTRIBUTE SIZE IN \_ \_ \_ \_ BYTES.**


