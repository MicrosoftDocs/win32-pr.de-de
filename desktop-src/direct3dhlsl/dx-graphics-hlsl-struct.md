---
title: Strukturtyp
description: Strukturtyp
ms.assetid: 896030b0-07cd-41bd-8c94-e173eabc81dd
keywords:
- Strukturtyp HLSL
topic_type:
- apiref
api_name:
- Struct Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b050a60911212a550433c5cc961a12ea52209b268330739c2f73158bf8fe1063
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068140"
---
# <a name="struct-type"></a>Strukturtyp

Verwenden Sie die folgende Syntax, um eine Struktur mit HLSL zu deklarieren.

Strukturname { \[ *InterpolationModifier* \] *Type* \[ *R* x *C* \] *MemberName*;     ... };



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Namen*
</dt> <dd>

Eine ASCII-Zeichenfolge, die den Strukturnamen eindeutig identifiziert.

</dd> <dt>

<span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]
</dt> <dd>

Optionaler Modifizierer, der einen Interpolationstyp angibt. Weitere Informationen finden Sie im Abschnitt [Hinweise](#remarks).

</dd> <dt>

<span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Typ* \[ *R* x *C*\]
</dt> <dd>

Der Membertyp mit einer optionalen Zeilengröße *(R*) x Spalte (*C*) Arraygröße. Eine -Struktur enthält mindestens ein -Element. Wenn es mehr als ein Element enthält, sind die Elemente alle vom gleichen Typ. Die Anzahl der Zeilen und Spalten ist ganze Zahlen ohne Vorzeichen zwischen 1 und 4 einschließlich.

</dd> <dt>

<span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*Membername*
</dt> <dd>

Eine ASCII-Zeichenfolge, die den Membernamen eindeutig identifiziert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein Interpolationsmodifizierer kann für jeden Strukturmember oder für ein Argument für eine Pixelshaderfunktion angegeben werden. Wenn an beiden Stellen ein Modifizierer angezeigt wird, überschreibt der äußere Modifizierer (der Pixelshaderargumentmodifizierer) den Inside-Modifizierer (den Strukturmodifizierer).

Beim Kompilieren eines Shaders oder Effekts packt der Shadercompiler Strukturmember gemäß [den HLSL-Komprimierungsregeln.](dx-graphics-hlsl-packing-rules.md)

### <a name="interpolation-modifiers-introduced-in-shader-model-4"></a>Im Shadermodell 4 eingeführte Interpolationsmodifizierer

Vertex-Shaderausgaben, die für Pixel-Shadereingaben verwendet werden, werden linear interpoliert, um während der Rasterung Pixelwerte abzurufen. Um die Interpolationsmethode festzulegen, verwenden Sie einen der folgenden Werte, die im [Shadermodell 4](dx-graphics-hlsl-sm4.md) oder höher unterstützt werden. Der Modifizierer wird bei jeder Vertex-Shaderausgabe ignoriert, die nicht als Pixel-Shadereingabe verwendet wird.



| Interpolationsmodifizierer | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Lineare**             | Interpolieren zwischen Shadereingaben; **linear** ist der Standardwert, wenn kein Interpolationsmodifizierer angegeben wird.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Schwerpunkt**           | Interpolieren zwischen Stichproben, die sich innerhalb des abgedeckten Bereichs des Pixels befinden (dies kann eine Extrapolierung von Endpunkten aus einem Pixelmittelpunkt erfordern). Schwerpunktstichproben können das Antialiasing verbessern, wenn ein Pixel teilweise abgedeckt ist (auch wenn die Pixelmitte nicht abgedeckt ist). Der **Schwerpunktmodifizierer** muss entweder mit dem **linearen** oder **noperspective-Modifizierer** kombiniert werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Nointerpolation**    | Interpolieren Sie nicht .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **noperspective**      | Führen Sie während der Interpolation keine perspektivische Korrektur aus. Der **Noperspective-Modifizierer** kann mit dem Schwerpunktmodifizierer kombiniert werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Beispiel**             | **Verfügbar im Shadermodell 4.1 und höher** Interpolieren Sie an der Stichprobenposition und nicht in der Pixelmitte. Dies bewirkt, dass der Pixelshader pro Stichprobe und nicht pro Pixel ausgeführt wird. Eine weitere Möglichkeit, die Ausführung pro Stichprobe zu verursachen, besteht darin, eine Eingabe mit [semantischem SV \_ SampleIndex](dx-graphics-hlsl-semantics.md)zu erhalten, die das aktuelle Beispiel angibt. Nur die Eingaben mit der angegebenen **Stichprobe** (oder die Eingabe sv \_ sampleIndex) unterscheiden sich zwischen Shaderaufrufen im Pixel, während andere Eingaben, die keine Modifizierer angeben (z. B. wenn Sie Modifizierer für verschiedene Eingaben kombinieren), weiterhin in der Pixelmitte interpolieren. Sowohl der Pixel-Shaderaufruf als auch die Tiefen-/Schablonentests werden für jede abgedeckte Stichprobe im Pixel durchgeführt. Dies wird manchmal als *Supersampling* bezeichnet. Im Gegensatz dazu wird der Pixelshader bei fehlendem Samplinghäufigkeitsaufruf, der als *Multisampling* bezeichnet wird, einmal pro Pixel aufgerufen, unabhängig davon, wie viele Stichproben abgedeckt werden, während Tiefen-/Schablonentests bei der Stichprobenhäufigkeit erfolgen. Beide Modi bieten entsprechende Edge-Antialiasing. Supersampling bietet jedoch eine bessere Schattierungsqualität, indem der Pixelshader häufiger aufgerufen wird.<br/> |



 

<dl> 1. Bei Verwendung eines int/uint-Typs ist die einzige gültige Option **nointerpolation**.  
</dl>

Interpolationsmodifizierer können auf Strukturmember, [Funktionsargumente](dx-graphics-hlsl-function-parameters.md)oder beides angewendet werden.

## <a name="examples"></a>Beispiele

Hier sind einige Beispielstrukturdeklarationen.


```
struct struct1
{
  int    a;
}
```



Diese Deklaration enthält ein Array.


```
struct struct2
{
  int    a;
  float  b;
  int4x4 iMatrix;
}
```



Diese Deklaration enthält einen Interpolationsmodifizierer.


```
struct In
{
  centroid float2 Texcoord;
};
```



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





