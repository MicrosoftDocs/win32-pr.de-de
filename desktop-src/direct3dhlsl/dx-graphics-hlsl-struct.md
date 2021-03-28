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
ms.openlocfilehash: 416c14c18fa1d0b76f4d13b609b895b0c64c2594
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104992903"
---
# <a name="struct-type"></a>Strukturtyp

Verwenden Sie die folgende Syntax, um eine Struktur mithilfe von HLSL zu deklarieren.



|                                                                                           |
|-------------------------------------------------------------------------------------------|
| Struktur *Name*{ \[ *interpolationmodifier* \] *Type* \[ *R* x *C* \] *Mitgliedschaft Name*;     ... }; |



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Benennen*
</dt> <dd>

Eine ASCII-Zeichenfolge, die den Namen der Struktur eindeutig identifiziert.

</dd> <dt>

<span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*Interpolationmodifier*\]
</dt> <dd>

Optionaler Modifizierer, der einen Interpolationstyp angibt. Weitere Informationen finden Sie im Abschnitt [Hinweise](#remarks).

</dd> <dt>

<span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Typ* \[ *R* x *C*\]
</dt> <dd>

Der Elementtyp mit einer optionalen Row (*R*) x Column (*C*)-Array Größe. Eine-Struktur enthält mindestens ein Element. Wenn Sie mehr als ein Element enthält, sind die Elemente alle vom gleichen Typ. Die Anzahl von Zeilen und Spalten ist eine ganze Zahl ohne Vorzeichen zwischen 1 und 4 einschließlich.

</dd> <dt>

<span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*Membername*
</dt> <dd>

Eine ASCII-Zeichenfolge, die den Elementnamen eindeutig identifiziert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein interpolationsmodifizierer kann für beliebige Strukturmember oder für ein Argument einer Pixel-Shader-Funktion angegeben werden. Wenn ein Modifizierer an beiden Stellen angezeigt wird, überschreibt der äußere Modifizierer (der Pixelshader-argumentmodifizierer) den in-Modifizierer (Strukturmodifizierer).

Wenn ein Shader oder ein Effekt kompiliert wird, packt der Shader-Compiler Strukturelemente gemäß den [HLSL-Verpackungs Regeln](dx-graphics-hlsl-packing-rules.md).

### <a name="interpolation-modifiers-introduced-in-shader-model-4"></a>Im Shader-Modell 4 eingeführte Interpolations Modifizierer

Vertex-Shader-Ausgaben, die für Pixel-shadereingaben verwendet werden, werden linear interpoliert, um bei der rasterisierung pro Pixel-Werte zu erhalten. Verwenden Sie zum Festlegen der Interpolationsmethode einen der folgenden Werte, die in [Shadermodell 4](dx-graphics-hlsl-sm4.md) oder höher unterstützt werden. Der-Modifizierer wird für jede Vertexshader-Ausgabe ignoriert, die nicht als Pixel-Shadereingabe verwendet wird.



| Interpolations Modifizierer | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AK**             | Interpolieren zwischen shadereingaben; " **linear** " ist der Standardwert, wenn kein Interpolations Modifizierer angegeben ist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Schwerpunkt**           | Interpolieren Sie zwischen Stichproben, die sich im abgedeckten Bereich des Pixels befinden (Dies erfordert möglicherweise das extrapolieren von Endpunkten von einem Pixel Center). Die Centroid-Stichprobenentnahme kann das Antialiasing verbessern, wenn ein Pixel teilweise abgedeckt wird (selbst wenn das Pixel Center nicht abgedeckt ist). Der **Schwerpunkt** -Modifizierer muss entweder mit dem **linearen** oder dem **noperktiven** -Modifizierer kombiniert werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **nointerpolations**    | Nicht interpolieren.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **noperer**      | Führen Sie während der Interpolations Zeit keine perspektivische Korrektur durch. Der **noperspemodifizierer** kann mit dem **Schwerpunkt** -Modifizierer kombiniert werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Blutprobe**             | **Verfügbar im Shader-Modell 4,1 und** höher Interpolieren Sie an einer Beispiel Position statt im Pixel Center. Dies bewirkt, dass der Pixelshader pro-Stichprobe anstatt pro Pixel ausgeführt wird. Eine andere Möglichkeit, die Ausführung pro Stichprobe zu verursachen, besteht darin, eine Eingabe mit [Semantik SV \_ sampleindex](dx-graphics-hlsl-semantics.md)zu haben, die das aktuelle Beispiel angibt. Nur die Eingaben mit angegebenem **Beispiel** (bzw. das Einfügen von SV \_ sampleindex) unterscheiden sich zwischen shaderaufrufen im Pixel, während andere Eingaben, die keine Modifizierern angeben (z. b. Wenn Sie Modifizierern für verschiedene Eingaben mischen), immer noch im Pixel Center interpolieren. Sowohl der Pixelshader-Aufruf als auch der tiefen-/Schablone-Test erfolgt für jedes abgedeckte Beispiel im Pixel. Dies wird manchmal als *Supersampling* bezeichnet. Im Gegensatz dazu wird der Pixelshader beim Fehlen von Sample Frequency-aufrufen, die als *mehrfach Stichprobe* bezeichnet werden, einmal pro Pixel aufgerufen, unabhängig davon, wie viele Stichproben abgedeckt werden, während tiefe-/Schablone-Tests bei der Stichproben Häufigkeit stattfinden. Beide Modi bieten äquivalente Edge-Antialiasing. Supersampling bietet jedoch eine bessere Schattierungs Qualität, indem der Pixelshader häufiger aufgerufen wird.<br/> |



 

<dl> 1.Wenn ein int/uint-Typ verwendet wird, ist die einzige gültige Option **nointerpolation.**  
</dl>

Interpolations Modifizierer können auf Strukturmember oder [Funktionsargumente](dx-graphics-hlsl-function-parameters.md)oder beides angewendet werden.

## <a name="examples"></a>Beispiele

Hier sind einige Beispiel Struktur Deklarationen.


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



Diese Deklaration enthält einen Interpolations Modifizierer.


```
struct In
{
  centroid float2 Texcoord;
};
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





