---
title: Puffertyp
description: Verwenden Sie die folgende Syntax, um eine Puffer Variable zu deklarieren.
ms.assetid: f21f0de5-58e3-466b-97bb-e4e7efa9cc1c
keywords:
- Pusl-Puffertyp
topic_type:
- apiref
api_name:
- Buffer Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e36030f3dd31f1bdada238e89c1048e4971cd45c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039190"
---
# <a name="buffer-type"></a>Puffertyp

Verwenden Sie die folgende Syntax, um eine Puffer Variable zu deklarieren.



| Puffer< >  *Typname*; |
|------------------------------|



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Ert**
</dt> <dd>

Erforderliches Schlüsselwort.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Sorte*
</dt> <dd>

Einer der Typen [skalare](dx-graphics-hlsl-scalar.md), [Vector](dx-graphics-hlsl-vector.md)und some [Matrix](dx-graphics-hlsl-matrix.md) HLSL. Sie können eine Puffer Variable mit einer Matrix deklarieren, solange Sie in 4 32-Bit-Mengen passt. Daher können Sie schreiben `Buffer<float2x2>` . Aber `Buffer<float4x4>` ist zu groß, und der Compiler generiert einen Fehler.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Benennen*
</dt> <dd>

Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.

</dd> </dl>

## <a name="example"></a>Beispiel

Im folgenden finden Sie ein Beispiel für eine Puffer Deklaration aus der Datei "pipesgs. FX" in [pipesgs Sample](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).


```
Buffer<float4> g_Buffer;
```



Daten werden aus einem Puffer mithilfe einer überladenen Version der systeminternen [**Load**](dx-graphics-hlsl-to-load.md) HLSL-Funktion gelesen, die einen Eingabeparameter (einen ganzzahligen Index) annimmt. Auf einen Puffer wird wie ein Array von Elementen zugegriffen. Daher wird in diesem Beispiel das zweite Element gelesen.


```
float4 bufferData = g_Buffer.Load( 1 );
```



Verwenden Sie die [Stream-Output-Phase](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) , um Daten in einen Puffer auszugeben.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 