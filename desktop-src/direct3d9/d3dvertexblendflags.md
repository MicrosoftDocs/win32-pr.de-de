---
description: Definiert Flags, die verwendet werden, um die Anzahl oder Matrizen zu steuern, die das System beim Ausführen der Vertexmischung mit mehreren Matrizen anwendet.
ms.assetid: 5314f455-ce5f-4ff5-81fc-d3dffc8705b7
title: D3DVERTEXBLENDFLAGS-Enumeration (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBLENDFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: ecc7f99e26088ff03b626604279bffe5c64ddb82b95a6f6219b637b3fce5a59b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527304"
---
# <a name="d3dvertexblendflags-enumeration"></a>D3DVERTEXBLENDFLAGS-Enumeration

Definiert Flags, die verwendet werden, um die Anzahl oder Matrizen zu steuern, die das System beim Ausführen der Vertexmischung mit mehreren Matrizen anwendet.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DVERTEXBLENDFLAGS { 
  D3DVBF_DISABLE   = 0,
  D3DVBF_1WEIGHTS  = 1,
  D3DVBF_2WEIGHTS  = 2,
  D3DVBF_3WEIGHTS  = 3,
  D3DVBF_TWEENING  = 255,
  D3DVBF_0WEIGHTS  = 256
} D3DVERTEXBLENDFLAGS, *LPD3DVERTEXBLENDFLAGS;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**D3DVBF \_ DISABLE**
</dt> <dd>

Deaktivieren der Vertexmischung; wenden Sie nur die vom [**D3DTS \_ WORLDMATRIX-Makro**](d3dts-worldmatrix.md) festgelegte Weltmatrix an, wobei der Indexwert für den Transformationszustand 0 ist.

</dd> <dt>

<span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF \_ 1WEIGHTS**
</dt> <dd>

Aktivieren Sie die Vertexmischung zwischen den beiden Matrizen, die vom [**D3DTS \_ WORLDMATRIX-Makro**](d3dts-worldmatrix.md) festgelegt werden, wobei der Indexwert für die Transformationszustände 0 und 1 ist.

</dd> <dt>

<span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF \_ 2WEIGHTS**
</dt> <dd>

Aktivieren Sie die Vertexmischung zwischen den drei Matrizen, die vom [**D3DTS \_ WORLDMATRIX-Makro**](d3dts-worldmatrix.md) festgelegt werden, wobei der Indexwert für die Transformationszustände 0, 1 und 2 ist.

</dd> <dt>

<span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF \_ 3WEIGHTS**
</dt> <dd>

Aktivieren Sie die Vertexmischung zwischen den vier Matrizen, die vom [**D3DTS \_ WORLDMATRIX-Makro**](d3dts-worldmatrix.md) festgelegt werden, wobei der Indexwert für die Transformationszustände 0, 1, 2 und 3 ist.

</dd> <dt>

<span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**\_D3DVBF-TWEENING**
</dt> <dd>

Die Vertexmischung erfolgt mithilfe des Werts, der D3DRS \_ TWEENFACTOR zugewiesen ist.

</dd> <dt>

<span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF \_ 0WEIGHTS**
</dt> <dd>

Verwenden Sie eine einzelne Matrix mit einer Gewichtung von 1,0.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Member dieses Typs werden mit dem D3DRS \_ VERTEXBLEND-Renderzustand verwendet.

Die Geometriemischung (Multimatrix vertex blending) erfordert, dass Ihre Anwendung ein Scheitelpunktformat verwendet, das für jeden Scheitelpunkt Überblendungsgewichtungen (Betaversionen) hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> <dt>

[**D3DTS \_ WORLD**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ WORLDn**](d3dts-worldn.md)
</dt> <dt>

[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
