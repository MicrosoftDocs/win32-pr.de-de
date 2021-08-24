---
description: Sprite-Flags, die der Sprite-Zeichnungs-API mitteilen, wie sich verhalten soll. Diese werden an ID3DX10Sprite::Begin übergeben.
ms.assetid: 734096e6-1482-479c-b287-a77a4695487c
title: D3DX10_SPRITE_FLAG-Enumeration (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 53b2c7965beaeb2976e88d38f5af90d546f644b6d4879964c23b2166cd51b19b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634940"
---
# <a name="d3dx10_sprite_flag-enumeration"></a>D3DX10 \_ SPRITE \_ FLAG-Enumeration

Sprite-Flags, die der Sprite-Zeichnungs-API mitteilen, wie sich verhalten soll. Diese werden an [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md)übergeben.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_SPRITE_FLAG { 
  D3DX10_SPRITE_SORT_TEXTURE              = 0x01,
  D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT  = 0x02,
  D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK  = 0x04,
  D3DX10_SPRITE_SAVE_STATE                = 0x08,
  D3DX10_SPRITE_ADDREF_TEXTURES           = 0x10
} D3DX10_SPRITE_FLAG, *LPD3DX10_SPRITE_FLAG;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**D3DX10 \_ SPRITE \_ SORT \_ TEXTURE**
</dt> <dd>

Sortieren Sie die Sprites vor dem Rendern nach Textur, sodass bei vielen Sprites mit der gleichen Textur alle diese Sprites gleichzeitig gerendert werden, wodurch die Leistung verbessert wird.

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3DX10 \_ SPRITE \_ SORT \_ DEPTH \_ BACK \_ TO \_ FRONT**
</dt> <dd>

Sortieren Sie die Sprites von zurück nach vorne so, dass diejenigen, die weiter von der Kamera entfernt sind, zuerst gezeichnet werden.

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**D3DX10 \_ SPRITE \_ SORT \_ DEPTH \_ FRONT \_ TO \_ BACK**
</dt> <dd>

Sortieren Sie die Sprites von vorn nach zurück, sodass diejenigen, die näher an der Kamera sind, zuerst gezeichnet werden.

</dd> <dt>

<span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3DX10 \_ SPRITE \_ SAVE \_ STATE**
</dt> <dd>

Speichert den Zustand, sodass der Zustand beim Aufruf von [**ID3DX10Sprite::End**](id3dx10sprite-end.md) so wiederhergestellt wird, wie er vor dem Aufruf von [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) war.

</dd> <dt>

<span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**D3DX10 \_ SPRITE \_ ADDREF \_ TEXTURES**
</dt> <dd>

Ruft AddRef für alle Texturen auf, wenn sie an [**ID3DX10Sprite::D rawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md)übergeben werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Nachdem eine Front-to-Back- oder Back-to-Front-Sortierung durchgeführt wurde, wird automatisch eine sekundäre Sortierung nach Textur durchgeführt. Dies ist hilfreich, wenn viele Sprites mit der gleichen Textur auf derselben Ebene vorhanden sind, z. B. wenn die Benutzeroberfläche in einem Spiel gezeichnet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Enumerationen](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




