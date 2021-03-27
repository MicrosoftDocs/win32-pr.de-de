---
title: HLSL-Shader-Modell 6,4
description: Beschreibt die Machine Learning-systeminternen Funktionen, die dem HLSL-Shadermodell 6,4 hinzugefügt werden.
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 10e74b268243ab059c2d0945887a6d429d40bb53
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103869644"
---
# <a name="hlsl-shader-model-64"></a>HLSL-Shader-Modell 6,4

Beschreibt die Machine Learning-systeminternen Funktionen, die dem HLSL-Shadermodell 6,4 hinzugefügt werden.

## <a name="shader-model-64"></a>Shadermodell 6,4
Diese systeminternen Funktionen sind ein erforderliches/unterstütztes Feature von Shader-Modell 6,4. Folglich ist keine separate Funktionalitäts bitüberprüfung erforderlich, außer die Sicherstellung der Verwendung von Shader-Modell 6,4. Der unterstützte mindestclient für diese Routinen ist Windows 10, Version 1903.

## <a name="shading-language-intrinsics"></a>Intrinsische Funktionen für Schattierungs Sprache

### <a name="unsigned-integer-dot-product-of-4-elements-and-accumulate"></a>Ganzzahlige Dot-Product ohne Vorzeichen von vier Elementen und Kumulierung
```syntax
uint32 dot4add_u8packed(uint32 a, uint32 b, uint32 acc); // ubyte4 a, b;
```
 
Eine 4-dimensionale Ganzzahl ohne Vorzeichen mit dem Wert hinzufügen. Multipliziert jedes entsprechende Paar von 8-Bit-int-Bytes ohne Vorzeichen in den beiden Eingabe-DWords und fasst die Ergebnisse in den 32-Bit-Integer-Akkumulator (ohne Vorzeichen) zusammen. Diese Anweisung funktioniert innerhalb einer einzelnen 32-Bit-weiten SIMD-Strecke. Die Eingaben werden auch als 32-Bit-Mengen angenommen.
 
### <a name="signed-integer-dot-product-of-4-elements-and-accumulate"></a>Ganzzahlige Dot-Product mit Vorzeichen von vier Elementen und Kumulierung
```syntax
int32 dot4add_i8packed(uint32 a, uint32 b, int32 acc); // signed byte4 a, b;
```

Eine 4-dimensionale Ganzzahl mit Vorzeichen und einem Wert von "Add". Multipliziert jedes entsprechende Paar von 8-Bit-int-Bytes mit Vorzeichen in den beiden Eingabe-DWords und fasst die Ergebnisse in den 32-Bit-integerakkumulator mit Vorzeichen um. Diese Anweisung funktioniert innerhalb einer einzelnen 32-Bit-weiten SIMD-Strecke. Die Eingaben werden auch als 32-Bit-Mengen angenommen.
 
### <a name="single-precision-floating-point-2-element-dot-product-and-accumulate"></a>Gleit Komma Wert mit einfacher Genauigkeit 2-Element Dot-Product und ansammeln
```syntax
float dot2add( half2 a, half2 b, float acc );
```

Ein zweidimensionales Gleit Komma-Punkt-Product von half2 Vektoren mit Add. Multipliziert die Elemente der zwei Gleit Komma Eingabe-Vektoren mit halber Genauigkeit und fasst die Ergebnisse in den 32-Bit-Float-Akkumulator um. Diese Anweisungen werden innerhalb einer einzelnen 32-Bit-weiten SIMD-Spur betrieben. Die Eingaben sind 16-Bit-Mengen, die in denselben Bereich verpackt sind.

Dies wird im featurebit mit niedriger Genauigkeit behandelt (gibt an, dass die systemeigene Hälfte und die kurze Unterstützung vorhanden sind).

### <a name="sv_shadingrate"></a>SV_ShadingRate
```syntax
uint shadingRate : SV_ShadingRate
```

Eine ganze Zahl ohne Vorzeichen, die die Anzahl der Ziel Pixel darstellt, die bei jedem Aufruf des Pixel-Shaders geschrieben werden. Gültige Werte gehören zum Satz von Enumerationswerten [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).

Dieser System Wert ist auf Plattformen verfügbar, die [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) oder höher sind. Sie kann von höchstens einer der Scheitelpunkt-oder Geometrie-shaderphasen geschrieben werden. Sie kann aus der Pixel-Shader-Stufe gelesen werden. Weitere Informationen finden Sie unter [Variable-Rate-Schattierung](../direct3d12/vrs.md).