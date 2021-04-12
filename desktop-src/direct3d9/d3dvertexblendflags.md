---
description: Definiert Flags, die verwendet werden, um die Anzahl oder Matrizen zu steuern, die das System beim Ausführen von multimatrix-Vertex-Blending anwendet
ms.assetid: 5314f455-ce5f-4ff5-81fc-d3dffc8705b7
title: D3DVERTEXBLENDFLAGS-Enumeration (D3D9Types. h)
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
ms.openlocfilehash: 0b4d22740a9ad06a9848dc7649d62ac06d37a056
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354736"
---
# <a name="d3dvertexblendflags-enumeration"></a>D3DVERTEXBLENDFLAGS-Enumeration

Definiert Flags, die verwendet werden, um die Anzahl oder Matrizen zu steuern, die das System beim Ausführen von multimatrix-Vertex-Blending anwendet

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

<span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**D3DVBF \_ Deaktivieren**
</dt> <dd>

Vertex-Blending deaktivieren; wenden Sie nur die Weltmatrix an, die vom [**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md) -Makro festgelegt wird, wobei der Indexwert für den Transformations Status 0 ist.

</dd> <dt>

<span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF \_ 1 Gewichtungen**
</dt> <dd>

Aktivieren Sie die Vertex-Mischung zwischen den beiden Matrizen, die durch das [**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md) -Makro festgelegt wurden, wobei der Indexwert für die Transformations Zustände 0 und 1 ist.

</dd> <dt>

<span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF \_ 2 Gewichtungen**
</dt> <dd>

Aktivieren Sie die Vertex-Vermischung zwischen den drei Matrizen, die durch das [**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md) -Makro festgelegt sind, wobei der Indexwert für die Transformations Zustände 0, 1 und 2 ist.

</dd> <dt>

<span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF \_ 3gewichtungen**
</dt> <dd>

Aktivieren Sie die vertexmischung zwischen den vier Matrizen, die durch das [**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md) -Makro festgelegt werden, wobei der Indexwert für die Transformations Zustände 0, 1, 2 und 3 ist.

</dd> <dt>

<span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**D3DVBF- \_ twiening**
</dt> <dd>

Die Vertex-Mischung erfolgt mithilfe des Werts, der D3DRS \_ tweumfactor zugewiesen ist.

</dd> <dt>

<span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF \_ 0gewichtungen**
</dt> <dd>

Verwenden Sie eine einzelne Matrix mit einer Gewichtung von 1,0.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Member dieses Typs werden mit dem D3DRS \_ vertexblend-Rendering-Zustand verwendet.

Geometrie Mischung (multimatrix-Vertex-Blending) erfordert, dass Ihre Anwendung ein Scheitelpunkt Format verwendet, das für jeden Scheitelpunkt über Mischungs-Gewichtungen (Beta) verfügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> <dt>

[**D3DTS \_ Welt**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ worldn**](d3dts-worldn.md)
</dt> <dt>

[**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
