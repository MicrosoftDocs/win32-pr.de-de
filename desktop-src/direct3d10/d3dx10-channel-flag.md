---
description: Diese Flags werden von Funktionen verwendet, die auf einem oder mehrere Kanäle in einer Textur arbeiten.
ms.assetid: 54ecb39a-a36e-43bb-bb51-78b7375716d8
title: D3DX10_CHANNEL_FLAG -Enumeration (D3DX10Tex.h)
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
ms.openlocfilehash: 4b29cbb958b2aa8af02000fc62d4d3a848c2efba585bd927674c9ceca9d65d9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634960"
---
# <a name="d3dx10_channel_flag-enumeration"></a>D3DX10 \_ CHANNEL \_ FLAG-Enumeration

Diese Flags werden von Funktionen verwendet, die auf einem oder mehrere Kanäle in einer Textur arbeiten.

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

<span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**D3DX10 \_ CHANNEL \_ RED**
</dt> <dd>

Gibt an, dass der rote Kanal verwendet werden soll.

</dd> <dt>

<span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**D3DX10 \_ CHANNEL \_ BLUE**
</dt> <dd>

Gibt an, dass der blaue Kanal verwendet werden soll.

</dd> <dt>

<span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**D3DX10 \_ CHANNEL \_ GREEN**
</dt> <dd>

Gibt an, dass der grüne Kanal verwendet werden soll.

</dd> <dt>

<span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**D3DX10 \_ CHANNEL \_ ALPHA**
</dt> <dd>

Gibt an, dass der Alphakanal verwendet werden soll.

</dd> <dt>

<span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**\_D3DX10-KANAL-LUDOMINANZ \_**
</dt> <dd>

Gibt die Luminaces der roten, grünen und blauen Kanäle an, die verwendet werden sollen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Tex.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Enumerationen](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




