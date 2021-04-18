---
description: Diese Flags werden verwendet, um zu steuern, wie D3DX10ComputeNormalMap normale Zuordnungen generiert. Eine beliebige Anzahl dieser Flags kann in beliebiger Kombination oder zusammengefasst werden.
ms.assetid: 307936c1-3137-41fe-8bea-7a82e6db0867
title: D3DX10_NORMALMAP_FLAG-Enumeration (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_NORMALMAP_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: c4b6962561007fbc3e64b471c045e98b2f8328b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355025"
---
# <a name="d3dx10_normalmap_flag-enumeration"></a>D3dx10 \_ normalmap- \_ Flag-Enumeration

Diese Flags werden verwendet, um zu steuern, wie [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) normale Zuordnungen generiert. Eine beliebige Anzahl dieser Flags kann in beliebiger Kombination oder zusammengefasst werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_NORMALMAP_FLAG { 
  D3DX10_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX10_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX10_NORMALMAP_MIRROR             = (3 << 16),
  D3DX10_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX10_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX10_NORMALMAP_FLAG, *LPD3DX10_NORMALMAP_FLAG;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3dx10 \_ normalmap- \_ Spiegelung \_ U**
</dt> <dd>

Gibt an, dass die Pixel außerhalb des Kanten der Textur auf der U-Achse gespiegelt und nicht mit wvergewaltigt versehen werden sollen.

</dd> <dt>

<span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3dx10 \_ normalmap- \_ Spiegelung \_ V**
</dt> <dd>

Gibt an, dass die Pixel außerhalb des Kanten der Textur auf der V-Achse gespiegelt und nicht mit wvergewaltigt versehen werden sollen.

</dd> <dt>

<span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**D3dx10 \_ normalmap- \_ Spiegelung**
</dt> <dd>

Identisch mit d3dx10 \_ normalmap- \_ Spiegelung \_ U \| d3dx10 \_ normmap- \_ Spiegelung \_ V.

</dd> <dt>

<span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3dx10 \_ normalmap \_ invertsign**
</dt> <dd>

Kehrt die Richtung der einzelnen normalen um.

</dd> <dt>

<span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**D3dx10 \_ normalmap \_ Compute- \_ oksion**
</dt> <dd>

Berechnet den Okklusions Begriff pro Pixel und codiert ihn in das Alpha. Ein Alpha von 1 bedeutet, dass das Pixel in keiner Weise verdeckt wird, und ein Alpha von 0 bedeutet, dass das Pixel vollständig verdeckt ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




