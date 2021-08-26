---
title: D3DX11_CHANNEL_FLAG-Enumeration (D3DX11tex.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt. Diese Flags werden von Funktionen verwendet, die auf einem oder mehreren Kanälen in einer Textur arbeiten.
ms.assetid: 058a0a1e-3c1b-4397-a41a-2e47d878cd92
keywords:
- D3DX11_CHANNEL_FLAG-Enumeration Direct3D 11
- LPD3DX11_CHANNEL_FLAG Enumerationszeiger Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_CHANNEL_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45f8142d34235a151638e1043928521666f2d1751319ee785d22b92004a14421
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028310"
---
# <a name="d3dx11_channel_flag-enumeration"></a>D3DX11 \_ CHANNEL \_ FLAG-Enumeration

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt.

 

Diese Flags werden von Funktionen verwendet, die auf einem oder mehreren Kanälen in einer Textur arbeiten.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX11_CHANNEL_FLAG { 
  D3DX11_CHANNEL_RED        = (1 << 0),
  D3DX11_CHANNEL_BLUE       = (1 << 1),
  D3DX11_CHANNEL_GREEN      = (1 << 2),
  D3DX11_CHANNEL_ALPHA      = (1 << 3),
  D3DX11_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX11_CHANNEL_FLAG, *LPD3DX11_CHANNEL_FLAG;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**D3DX11 \_ CHANNEL \_ RED**
</dt> <dd>

Gibt an, dass der rote Kanal verwendet werden soll.

</dd> <dt>

<span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**D3DX11 \_ CHANNEL \_ BLUE**
</dt> <dd>

Gibt an, dass der blaue Kanal verwendet werden soll.

</dd> <dt>

<span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**D3DX11 \_ CHANNEL \_ GREEN**
</dt> <dd>

Gibt an, dass der grüne Kanal verwendet werden soll.

</dd> <dt>

<span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**D3DX11 \_ CHANNEL \_ ALPHA**
</dt> <dd>

Gibt an, dass der Alphakanal verwendet werden soll.

</dd> <dt>

<span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**D3DX11 \_ CHANNEL \_ LUMINANCE**
</dt> <dd>

Gibt die Leuchtdichte der roten, grünen und blauen Kanäle an, die verwendet werden sollen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





