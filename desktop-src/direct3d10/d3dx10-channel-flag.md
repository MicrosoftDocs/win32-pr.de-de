---
description: Diese Flags werden von Funktionen verwendet, die auf einem oder mehreren Kanälen in einer Textur arbeiten.
ms.assetid: 54ecb39a-a36e-43bb-bb51-78b7375716d8
title: D3DX10_CHANNEL_FLAG-Enumeration (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_CHANNEL_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: f21958ab964a70116a551c0cb8dadbce6db88f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355636"
---
# <a name="d3dx10_channel_flag-enumeration"></a>D3dx10 \_ - \_ kanalflag-Enumeration

Diese Flags werden von Funktionen verwendet, die auf einem oder mehreren Kanälen in einer Textur arbeiten.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_CHANNEL_FLAG { 
  D3DX10_CHANNEL_RED        = (1 << 0),
  D3DX10_CHANNEL_BLUE       = (1 << 1),
  D3DX10_CHANNEL_GREEN      = (1 << 2),
  D3DX10_CHANNEL_ALPHA      = (1 << 3),
  D3DX10_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX10_CHANNEL_FLAG, *LPD3DX10_CHANNEL_FLAG;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**D3dx10 \_ Kanal \_ rot**
</dt> <dd>

Gibt an, dass der rote Kanal verwendet werden soll.

</dd> <dt>

<span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**D3dx10 \_ Kanal \_ blau**
</dt> <dd>

Gibt an, dass der blaue Kanal verwendet werden soll.

</dd> <dt>

<span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**D3dx10 \_ Kanal \_ grün**
</dt> <dd>

Gibt an, dass der grüne Kanal verwendet werden soll.

</dd> <dt>

<span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**D3dx10 \_ Channel \_ Alpha**
</dt> <dd>

Gibt an, dass der Alphakanal verwendet werden soll.

</dd> <dt>

<span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**D3dx10 \_ Kanal- \_ Leuchtkraft**
</dt> <dd>

Gibt an, dass die leuchtenden der roten, grünen und blauen Kanäle verwendet werden sollen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




