---
title: Struktur der Schnittmengen Attribute
description: Eine in HLSL deklarierte Struktur, die Treffer Attribute für Dreiecks Schnittstellen mit fester Funktion oder an einem Achsen ausgerichteten Begrenzungsfeld für die prozedurale Schnittmenge darstellt.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f1dd8fee7371f81dd538b6ea6622f22e3bfd3d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "106365220"
---
# <a name="intersection-attributes-structure"></a>Struktur der Schnittmengen Attribute 

Eine in HLSL deklarierte Struktur, die Treffer Attribute für Dreiecks Schnittstellen mit fester Funktion oder an einem Achsen ausgerichteten Begrenzungsfeld für die prozedurale Schnittmenge darstellt.

## <a name="fixed-function-triangle-intersection"></a>Dreiecks Schnittmenge mit fester Funktion

Die folgende Struktur wird in HLSL deklariert, um Treffer Attribute für Dreiecks Schnittstellen mit fester Funktion darzustellen:


```
struct BuiltInTriangleIntersectionAttributes
{
    float2 barycentrics;
};
```

[Alle Treffer](any-hit-shader.md) -und [nächsten Treffer](closest-hit-shader.md) -Shader, die mithilfe von Dreiecks Schnittstellen mit fester Funktion aufgerufen wurden, müssen diese Struktur für Treffer Attribute verwenden. Bei den Attributen a0, a1 und a2 für die 3 Scheitel Punkte eines Dreiecks ist "barycentrics. x" die Gewichtung für a1 und barycentrics. y ist die Gewichtung für a2.  Die APP kann z. b. wie folgt interpolieren: a = a0 + barycentrics. x * (a1-a0) + baryzentrics. y * (a2 – a0).

## <a name="axis-aligned-bounding-box-for-procedural-primitive-intersection"></a>Achsen gerichtetes Begrenzungsfeld für prozedurale Schnittmenge

Wenn Achsen ausgerichtete Begrenzungs Felder für Schnittmengen mit prozeduralen primitiven verwendet werden, wird ein Schnittstellen-Shader ausgelöst.  Dieser Shader stellt dem [**reporthit**](reporthit-function.md) -Befehl eine benutzerdefinierte Schnittmengen-Attribut Struktur bereit.  Alle Treffer-und nächsten Treffer-Shader, die in derselben Treffer Gruppe mit diesem schnittsshader gebunden sind, müssen dieselbe Struktur für Treffer Attribute verwenden, auch wenn auf die Attribute nicht verwiesen wird.  Die maximale Attribut Struktur Größe beträgt 32 Bytes und wird als **Maximale \_ Attribut Größe von D3D12 Raytracing \_ \_ \_ \_ in \_ Byte** definiert.


