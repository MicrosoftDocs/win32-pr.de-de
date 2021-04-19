---
description: 'Sprite-Flags, die der Sprite-Zeichnungs-API mitteilen, wie Sie sich Verhalten. Diese werden an ID3DX10Sprite:: begin übermittelt.'
ms.assetid: 734096e6-1482-479c-b287-a77a4695487c
title: D3DX10_SPRITE_FLAG-Enumeration (D3DX10Core. h)
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
ms.openlocfilehash: 21ba4f035b43b1a002b014909fb4d0a02a64d1e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361236"
---
# <a name="d3dx10_sprite_flag-enumeration"></a>D3dx10 \_ Sprite- \_ Flag-Enumeration

Sprite-Flags, die der Sprite-Zeichnungs-API mitteilen, wie Sie sich Verhalten. Diese werden an [**ID3DX10Sprite:: begin**](id3dx10sprite-begin.md)übermittelt.

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

<span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**D3dx10 \_ Sprite- \_ Sortier \_ Textur**
</dt> <dd>

Sortieren Sie die Sprites anhand der Textur vor dem Rendering, damit viele Sprites mit derselben Textur vorhanden sind, in denen alle diese Sprites gleichzeitig gerendert werden, wodurch die Leistung verbessert wird.

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3dx10 \_ Sprite- \_ Sortier \_ Tiefe \_ zurück \_ in den \_ Vordergrund**
</dt> <dd>

Sortieren Sie die Sprites von hinten nach oben, sodass die weiter Weg von der Kamera zuerst gezeichnet werden.

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**D3dx10 \_ Sprite- \_ Sortier \_ Tiefe \_ vor \_ dem \_ Hintergrund**
</dt> <dd>

Sortieren Sie die Sprites von vorne nach hinten, sodass diese an der Kamera näher gezeichnet werden.

</dd> <dt>

<span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3dx10 \_ Sprite- \_ Speicher \_ Zustand**
</dt> <dd>

Speichert den Zustand, sodass, wenn [**ID3DX10Sprite:: End**](id3dx10sprite-end.md) aufgerufen wird, der Zustand so wieder hergestellt wird, wie er vor dem Aufruf von [**ID3DX10Sprite:: begin**](id3dx10sprite-begin.md) aufgerufen wurde.

</dd> <dt>

<span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**D3dx10 \_ Sprite- \_ Adressaten \_**
</dt> <dd>

Ruft die adressf für alle Texturen auf, wenn Sie an [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md)weitergegeben werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Nachdem eine Front-to-Back-oder Back-to-Front-Sortierung durchgeführt wurde, wird automatisch eine sekundäre Sortierung nach Textur durchgeführt. Dies ist hilfreich, wenn sich viele Sprites mit derselben Textur auf derselben Ebene befinden, z. b. beim Zeichnen der Benutzeroberfläche in einem Spiel.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




