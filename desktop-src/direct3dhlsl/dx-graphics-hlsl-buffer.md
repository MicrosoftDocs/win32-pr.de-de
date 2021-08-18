---
title: Puffertyp
description: Verwenden Sie die folgende Syntax, um eine Puffervariable zu deklarieren.
ms.assetid: f21f0de5-58e3-466b-97bb-e4e7efa9cc1c
keywords:
- Puffertyp HLSL
topic_type:
- apiref
api_name:
- Buffer Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78d0b452a387ed1d4bf750062963996d0248fa249954a99be581118560866123
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120344"
---
# <a name="buffer-type"></a>Puffertyp

Verwenden Sie die folgende Syntax, um eine Puffervariable zu deklarieren.



| Buffer<*Type* >  *Name*; |
|------------------------------|



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Puffer**
</dt> <dd>

Erforderliches Schlüsselwort.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Typ*
</dt> <dd>

Einer der [Skalar-,](dx-graphics-hlsl-scalar.md) [Vektor-](dx-graphics-hlsl-vector.md)und [matrixbasierten](dx-graphics-hlsl-matrix.md) HLSL-Typen. Sie können eine Puffervariable mit einer Matrix deklarieren, solange sie in 4 32-Bit-Mengen passt. Sie können also `Buffer<float2x2>` schreiben. Ist `Buffer<float4x4>` jedoch zu groß, und der Compiler generiert einen Fehler.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Namen*
</dt> <dd>

Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.

</dd> </dl>

## <a name="example"></a>Beispiel

Hier ist ein Beispiel für eine Pufferdeklaration aus der Datei PipesGS.fx im [PipesGS-Beispiel](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).


```
Buffer<float4> g_Buffer;
```



Daten werden mithilfe einer überladenen Version der systeminternen [**Funktion Load**](dx-graphics-hlsl-to-load.md) HLSL aus einem Puffer gelesen, die einen Eingabeparameter (einen ganzzahligen Index) akzeptiert. Auf einen Puffer wird wie ein Array von Elementen zugegriffen. Daher liest dieses Beispiel das zweite Element.


```
float4 bufferData = g_Buffer.Load( 1 );
```



Verwenden Sie [die Streamausgabephase,](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) um Daten in einen Puffer ausausgaben.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 