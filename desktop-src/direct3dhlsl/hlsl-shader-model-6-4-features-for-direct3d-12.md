---
title: HLSL-Shadermodell 6.4
description: Beschreibt die systeminternen Machine Learning-Eigenschaften, die dem HLSL-Shadermodell 6.4 hinzugefügt wurden.
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 5e161d77439eef63547d92fcc4f47e3185ac798141d20017d7e7102ee86a38cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511834"
---
# <a name="hlsl-shader-model-64"></a>HLSL-Shadermodell 6.4

Beschreibt die systeminternen Machine Learning-Eigenschaften, die dem HLSL-Shadermodell 6.4 hinzugefügt wurden.

## <a name="shader-model-64"></a>Shadermodell 6.4
Diese systeminternen Funktionen sind ein erforderliches/unterstütztes Feature des Shadermodells 6.4. Daher ist keine separate Funktionsbitüberprüfung erforderlich, über die Verwendung des Shadermodells 6.4 hinaus. Der mindestens unterstützte Client für diese Routinen ist Windows 10 Version 1903.

## <a name="shading-language-intrinsics"></a>Intrinsische Schattierungssprache

### <a name="unsigned-integer-dot-product-of-4-elements-and-accumulate"></a>Ganze Zahl ohne Vorzeichen Dot-Product 4 Elemente und Accumulate
```syntax
uint32 dot4add_u8packed(uint32 a, uint32 b, uint32 acc); // ubyte4 a, b;
```
 
Ein vierdimensionales ganzzahliges Ganzzahlprodukt ohne Vorzeichen mit add. Multipliziert jedes entsprechende Paar von 8-Bit-Int-Bytes ohne Vorzeichen in den beiden Eingabe-DWORDs und summiert die Ergebnisse in den 32-Bit-Akkumulator für ganze Zahlen ohne Vorzeichen. Diese Anweisung wird innerhalb einer einzelnen 32-Bit-Breiten-SIMD-Spur betrieben. Es wird auch davon ausgegangen, dass es sich bei den Eingaben um 32-Bit-Mengen handelt.
 
### <a name="signed-integer-dot-product-of-4-elements-and-accumulate"></a>Ganze Zahl mit Vorzeichen Dot-Product 4 Elementen und Accumulate
```syntax
int32 dot4add_i8packed(uint32 a, uint32 b, int32 acc); // signed byte4 a, b;
```

Ein vierdimensionales ganzzahliges Punktprodukt mit Vorzeichen mit Add. Multipliziert jedes entsprechende Paar von signierten 8-Bit-Int-Bytes in den beiden Eingabe-DWORDs und summiert die Ergebnisse in den 32-Bit-Akkumulator für ganze Zahlen mit Vorzeichen. Diese Anweisung wird innerhalb einer einzelnen 32-Bit-Breiten-SIMD-Spur betrieben. Es wird auch davon ausgegangen, dass es sich bei den Eingaben um 32-Bit-Mengen handelt.
 
### <a name="single-precision-floating-point-2-element-dot-product-and-accumulate"></a>Single Precision Floating Point 2-Element-Dot-Product und Accumulate
```syntax
float dot2add( half2 a, half2 b, float acc );
```

Ein zweidimensionales Gleitkomma-Punktprodukt von half2-Vektoren mit Add. Multipliziert die Elemente der beiden Gleitkommaeingabevektoren mit halber Genauigkeit und summiert die Ergebnisse in den 32-Bit-Float-Akkumulator. Diese Anweisungen werden innerhalb einer einzelnen 32-Bit-Breiten-SIMD-Spur betrieben. Die Eingaben sind 16-Bit-Mengen, die in derselben Spur gepackt sind.

Dies wird unter dem Featurebit mit niedriger Genauigkeit abgedeckt (was darauf hinweist, dass native Hälfte und kurze Unterstützung vorhanden sind).

### <a name="sv_shadingrate"></a>SV_ShadingRate
```syntax
uint shadingRate : SV_ShadingRate
```

Eine ganze Zahl ohne Vorzeichen, die angibt, wie viele Zielpixel bei jedem Aufruf des Pixel-Shaders geschrieben werden. Gültige Werte gehören zu einem Satz von Enumerationswerten [D3D12_SHADING_RATE.](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate)

Dieser Systemwert ist auf Plattformen verfügbar, [die](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) D3D12_VARIABLE_SHADING_RATE_TIER_2 oder höher sind. Sie kann aus mindestens einer Der Scheitelpunkt- oder Geometrie-Shaderstufen geschrieben werden. Sie kann aus der Pixel-Shaderphase gelesen werden. Weitere Informationen finden Sie unter [Variable Rate Shading (Schattierung variabler Rate).](../direct3d12/vrs.md)