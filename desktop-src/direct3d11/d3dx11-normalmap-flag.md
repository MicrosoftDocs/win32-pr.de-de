---
title: D3DX11_NORMALMAP_FLAG -Enumeration (D3DX11tex.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Normale Kartenoptionen. Sie können eine beliebige Anzahl dieser Flags mithilfe einer bitweise OR-Operation kombinieren.
ms.assetid: cc9c8a54-be1e-4594-8274-9955562a6fa8
keywords:
- D3DX11_NORMALMAP_FLAG-Enumeration Direct3D 11
- LPD3DX11_NORMALMAP_FLAG-Enumerationszeiger Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_NORMALMAP_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbea7c787ac2e2aa7d988e052e2ca548a49a338c9b9f981ce73d51c40e0b4edd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300649"
---
# <a name="d3dx11_normalmap_flag-enumeration"></a>D3DX11 \_ NORMALMAP \_ FLAG-Enumeration

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Normale Kartenoptionen. Sie können eine beliebige Anzahl dieser Flags mithilfe einer bitweise OR-Operation kombinieren.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX11_NORMALMAP_FLAG { 
  D3DX11_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX11_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX11_NORMALMAP_MIRROR             = (3 << 16),
  D3DX11_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX11_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX11_NORMALMAP_FLAG, *LPD3DX11_NORMALMAP_FLAG;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**D3DX11 \_ NORMALMAP \_ MIRROR \_ U**
</dt> <dd>

Gibt an, dass Pixel vom Rand der Textur auf der U-Achse gespiegelt und nicht umrandet werden sollen.

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11 \_ NORMALMAP \_ MIRROR \_ V**
</dt> <dd>

Gibt an, dass Pixel vom Rand der Textur auf der V-Achse gespiegelt und nicht umrandet werden sollen.

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**D3DX11 \_ NORMALMAP \_ MIRROR**
</dt> <dd>

Identisch mit D3DX11 \_ NORMALMAP \_ MIRROR U \_ \| D3DX11 \_ NORMALMAP MIRROR \_ \_ V.

</dd> <dt>

<span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11 \_ NORMALMAP \_ INVERTSIGN**
</dt> <dd>

Invertiert die Richtung der einzelnen Normalen.

</dd> <dt>

<span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**D3DX11 \_ NORMALMAP \_ COMPUTE \_ OCCLUSION**
</dt> <dd>

Berechnet den Okklusionsbegriff pro Pixel und codiert ihn in das Alpha. Ein Alphawert von 1 bedeutet, dass das Pixel nicht verdeckt wird, und ein Alpha von 0 bedeutet, dass das Pixel vollständig verdeckt ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Flags werden von [**D3DX11ComputeNormalMap verwendet.**](d3dx11computenormalmap.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





