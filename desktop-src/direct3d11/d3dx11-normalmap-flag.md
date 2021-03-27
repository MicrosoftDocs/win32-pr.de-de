---
title: D3DX11_NORMALMAP_FLAG-Enumeration (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Normale Karten Optionen. Sie können eine beliebige Anzahl dieser Flags mit einer bitweisen OR-Operation kombinieren.
ms.assetid: cc9c8a54-be1e-4594-8274-9955562a6fa8
keywords:
- D3DX11_NORMALMAP_FLAG-Enumeration Direct3D 11
- LPD3DX11_NORMALMAP_FLAG enumerationszeiger Direct3D 11
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
ms.openlocfilehash: 37f5d9669370e6df03d783ae1cb82a5eeb5a9142
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219700"
---
# <a name="d3dx11_normalmap_flag-enumeration"></a>Bibliothek d3dx11 \_ normalmap- \_ Flag-Enumeration

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Normale Karten Optionen. Sie können eine beliebige Anzahl dieser Flags mit einer bitweisen OR-Operation kombinieren.

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

<span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**Bibliothek d3dx11 \_ normalmap- \_ Spiegelung \_ U**
</dt> <dd>

Gibt an, dass die Pixel außerhalb des Kanten der Textur auf der U-Achse gespiegelt und nicht mit wvergewaltigt versehen werden sollen.

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**Bibliothek d3dx11 \_ normalmap- \_ Spiegelung \_ V**
</dt> <dd>

Gibt an, dass die Pixel außerhalb des Kanten der Textur auf der V-Achse gespiegelt und nicht mit wvergewaltigt versehen werden sollen.

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**Bibliothek d3dx11 \_ normalmap- \_ Spiegelung**
</dt> <dd>

Identisch mit Bibliothek d3dx11 \_ normalmap- \_ Spiegelung \_ U \| Bibliothek d3dx11 \_ normmap- \_ Spiegelung \_ V.

</dd> <dt>

<span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**Bibliothek d3dx11 \_ normalmap \_ invertsign**
</dt> <dd>

Kehrt die Richtung der einzelnen normalen um.

</dd> <dt>

<span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**Bibliothek d3dx11 \_ normalmap \_ Compute- \_ oksion**
</dt> <dd>

Berechnet den Okklusions Begriff pro Pixel und codiert ihn in das Alpha. Ein Alpha von 1 bedeutet, dass das Pixel in keiner Weise verdeckt wird, und ein Alpha von 0 bedeutet, dass das Pixel vollständig verdeckt ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Flags werden von [**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md)verwendet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Enumerationen](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





