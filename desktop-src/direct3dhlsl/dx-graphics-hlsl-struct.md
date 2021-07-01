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
ms.openlocfilehash: 89435e9c8757d2e732bc6237b02a508d3af4b4db
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119095"
---
# <a name="struct-type"></a>Strukturtyp

Verwenden Sie die folgende Syntax, um eine -Struktur mitHILFE von HLSL zu deklarieren.

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

Der Membertyp mit einer optionalen Zeilengröße (*R*) x Spalte (*C*) Arraygröße. Eine -Struktur enthält mindestens ein -Element. Wenn sie mehr als ein Element enthält, sind alle Elemente vom gleichen Typ. Die Anzahl der Zeilen und Spalten sind ganze Zahlen ohne Vorzeichen zwischen 1 und einschließlich 4.

</dd> <dt>

<span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*Membername*
</dt> <dd>

Eine ASCII-Zeichenfolge, die den Membernamen eindeutig identifiziert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein Interpolationsmodifizierer kann für jeden Struktur member oder für ein Argument für eine Pixel-Shaderfunktion angegeben werden. Wenn ein Modifizierer an beiden Stellen angezeigt wird, überstimmt der modifizierer outside (der Modifizierer für Das Pixel-Shaderargument) den Inside-Modifizierer (den Strukturmodifizierer).

Beim Kompilieren eines Shaders oder Effekts packt der Shadercompiler Strukturmitglieder gemäß [HLSL-Füllregeln.](dx-graphics-hlsl-packing-rules.md)

### <a name="interpolation-modifiers-introduced-in-shader-model-4"></a>In Shadermodell 4 eingeführte Interpolationsmodifizierer

Vertex-Shader-Ausgaben, die für Pixel-Shadereingaben verwendet werden, werden linear interpoliert, um während der Rasterung Pixelwerte zu erhalten. Verwenden Sie zum Festlegen der Interpolationsmethode einen der folgenden Werte, die in [Shadermodell 4](dx-graphics-hlsl-sm4.md) oder höher unterstützt werden. Der Modifizierer wird bei jeder Vertex-Shaderausgabe ignoriert, die nicht als Pixel-Shadereingabe verwendet wird.



| Interpolationsmodifizierer | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Lineare**             | Interpolieren zwischen Shadereingaben; **linear** ist der Standardwert, wenn kein Interpolationsmodifizierer angegeben ist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Schwerpunkt**           | Interpolieren Zwischen Stichproben, die sich innerhalb des abgedeckten Bereichs des Pixels befinden (dies erfordert möglicherweise extrapolierte Endpunkte von einem Pixelcenter). Die Schwerpunkt-Stichprobenentnahme kann das Antialiasing verbessern, wenn ein Pixel teilweise abgedeckt ist (auch wenn der Pixelmittelpunkt nicht abgedeckt ist). Der **Schwerpunktmodifizierer** muss entweder mit dem **linearen** modifizierer oder **noperspective-Modifizierer** kombiniert werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **nointerpolation**    | Interpolieren Sie nicht .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **noperspective**      | Führen Sie während der Interpolation keine Perspektivkorrektur durch. Der **modifizierer noperspective** kann mit dem Modifizierer **"schwerpunkt"** kombiniert werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Beispiel**             | **Verfügbar in Shadermodell 4.1 und höher** Interpolieren Sie an der Beispielposition und nicht in der Pixelmitte. Dies bewirkt, dass der Pixel-Shader pro Stichprobe und nicht pro Pixel ausgeführt wird. Eine weitere Möglichkeit, die Ausführung pro Beispiel zu verursachen, ist eine Eingabe mit semantic [SV \_ SampleIndex,](dx-graphics-hlsl-semantics.md)die das aktuelle Beispiel angibt. Nur die  Eingaben mit angegebenem Beispiel (oder Eingabe von SV SampleIndex) unterscheiden sich zwischen Shaderaufrufen im Pixel, während andere Eingaben, die keine Modifizierer angeben (z. B. wenn Sie Modifizierer für verschiedene Eingaben mischen), weiterhin in der Pixelmitte \_ interpolieren. Sowohl der Shaderaufruf als auch der Tiefen-/Schablonentest erfolgen für jedes abgedeckte Beispiel im Pixel. Dies wird manchmal als *Supersampling bezeichnet.* Im Gegensatz dazu wird der Pixel-Shader in Ermangelung eines Beispielhäufigkeitsaufrufs, der als *Multisampling* bezeichnet wird, einmal pro Pixel aufgerufen, unabhängig davon, wie viele Stichproben abgedeckt sind, während Tiefen-/Schablonentests mit Stichprobenhäufigkeit durchgeführt werden. Beide Modi bieten entsprechende Edge-Antialiasing. Die Übersampling-Methode bietet jedoch eine bessere Schattierungsqualität, indem der Pixel-Shader häufiger aufruft.<br/> |



 

<dl> 1. Bei Verwendung eines int/uint-Typs ist **nointerpolation** die einzige gültige Option.  
</dl>

Interpolationsmodifizierer können auf Strukturmitglieder oder [Funktionsargumente oder](dx-graphics-hlsl-function-parameters.md)beides angewendet werden.

## <a name="examples"></a>Beispiele

Im Folgenden finden Sie einige Beispielstrukturdeklarationen.


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

 

 





