---
title: D3DX11_CHANNEL_FLAG-Enumeration (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Diese Flags werden von Funktionen verwendet, die auf einem oder mehreren Kanälen in einer Textur arbeiten.
ms.assetid: 058a0a1e-3c1b-4397-a41a-2e47d878cd92
keywords:
- D3DX11_CHANNEL_FLAG-Enumeration Direct3D 11
- LPD3DX11_CHANNEL_FLAG enumerationszeiger Direct3D 11
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
ms.openlocfilehash: d2e3097552637ce96663671dda443684ebda2b65
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394254"
---
# <a name="d3dx11_channel_flag-enumeration"></a>Bibliothek d3dx11 \_ - \_ kanalflag-Enumeration

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

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

<span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**Bibliothek d3dx11 \_ Kanal \_ rot**
</dt> <dd>

Gibt an, dass der rote Kanal verwendet werden soll.

</dd> <dt>

<span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**Bibliothek d3dx11 \_ Kanal \_ blau**
</dt> <dd>

Gibt an, dass der blaue Kanal verwendet werden soll.

</dd> <dt>

<span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**Bibliothek d3dx11 \_ Kanal \_ grün**
</dt> <dd>

Gibt an, dass der grüne Kanal verwendet werden soll.

</dd> <dt>

<span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**Bibliothek d3dx11 \_ Channel \_ Alpha**
</dt> <dd>

Gibt an, dass der Alphakanal verwendet werden soll.

</dd> <dt>

<span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**Bibliothek d3dx11 \_ Kanal- \_ Leuchtkraft**
</dt> <dd>

Gibt an, dass die leuchtenden der roten, grünen und blauen Kanäle verwendet werden sollen.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Enumerationen](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





