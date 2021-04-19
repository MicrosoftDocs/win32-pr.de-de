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
# <a name="d3dx10_sprite_flag-enumeration"></a><span data-ttu-id="78243-104">D3dx10 \_ Sprite- \_ Flag-Enumeration</span><span class="sxs-lookup"><span data-stu-id="78243-104">D3DX10\_SPRITE\_FLAG enumeration</span></span>

<span data-ttu-id="78243-105">Sprite-Flags, die der Sprite-Zeichnungs-API mitteilen, wie Sie sich Verhalten.</span><span class="sxs-lookup"><span data-stu-id="78243-105">Sprite flags that tell the sprite drawing API how to behave.</span></span> <span data-ttu-id="78243-106">Diese werden an [**ID3DX10Sprite:: begin**](id3dx10sprite-begin.md)übermittelt.</span><span class="sxs-lookup"><span data-stu-id="78243-106">These are passed into [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="78243-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="78243-107">Syntax</span></span>


```C++
typedef enum D3DX10_SPRITE_FLAG { 
  D3DX10_SPRITE_SORT_TEXTURE              = 0x01,
  D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT  = 0x02,
  D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK  = 0x04,
  D3DX10_SPRITE_SAVE_STATE                = 0x08,
  D3DX10_SPRITE_ADDREF_TEXTURES           = 0x10
} D3DX10_SPRITE_FLAG, *LPD3DX10_SPRITE_FLAG;
```



## <a name="constants"></a><span data-ttu-id="78243-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="78243-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="78243-109"><span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**D3dx10 \_ Sprite- \_ Sortier \_ Textur**</span><span class="sxs-lookup"><span data-stu-id="78243-109"><span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**D3DX10\_SPRITE\_SORT\_TEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="78243-110">Sortieren Sie die Sprites anhand der Textur vor dem Rendering, damit viele Sprites mit derselben Textur vorhanden sind, in denen alle diese Sprites gleichzeitig gerendert werden, wodurch die Leistung verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="78243-110">Sort the sprites by texture before rendering so that when there are many sprites with the same texture that texture all of those sprites will be rendered at the same time, thereby improving performance.</span></span>

</dd> <dt>

<span data-ttu-id="78243-111"><span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3dx10 \_ Sprite- \_ Sortier \_ Tiefe \_ zurück \_ in den \_ Vordergrund**</span><span class="sxs-lookup"><span data-stu-id="78243-111"><span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3DX10\_SPRITE\_SORT\_DEPTH\_BACK\_TO\_FRONT**</span></span>
</dt> <dd>

<span data-ttu-id="78243-112">Sortieren Sie die Sprites von hinten nach oben, sodass die weiter Weg von der Kamera zuerst gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="78243-112">Sort the sprites from back to front to that those farther away from the camera will be drawn first.</span></span>

</dd> <dt>

<span data-ttu-id="78243-113"><span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**D3dx10 \_ Sprite- \_ Sortier \_ Tiefe \_ vor \_ dem \_ Hintergrund**</span><span class="sxs-lookup"><span data-stu-id="78243-113"><span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**D3DX10\_SPRITE\_SORT\_DEPTH\_FRONT\_TO\_BACK**</span></span>
</dt> <dd>

<span data-ttu-id="78243-114">Sortieren Sie die Sprites von vorne nach hinten, sodass diese an der Kamera näher gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="78243-114">Sort the sprites from front to back so that those closer to the camera will be drawn first.</span></span>

</dd> <dt>

<span data-ttu-id="78243-115"><span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3dx10 \_ Sprite- \_ Speicher \_ Zustand**</span><span class="sxs-lookup"><span data-stu-id="78243-115"><span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3DX10\_SPRITE\_SAVE\_STATE**</span></span>
</dt> <dd>

<span data-ttu-id="78243-116">Speichert den Zustand, sodass, wenn [**ID3DX10Sprite:: End**](id3dx10sprite-end.md) aufgerufen wird, der Zustand so wieder hergestellt wird, wie er vor dem Aufruf von [**ID3DX10Sprite:: begin**](id3dx10sprite-begin.md) aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="78243-116">Saves the state so that when [**ID3DX10Sprite::End**](id3dx10sprite-end.md) is called, it will restore the state to the way it was before [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) was called.</span></span>

</dd> <dt>

<span data-ttu-id="78243-117"><span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**D3dx10 \_ Sprite- \_ Adressaten \_**</span><span class="sxs-lookup"><span data-stu-id="78243-117"><span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**D3DX10\_SPRITE\_ADDREF\_TEXTURES**</span></span>
</dt> <dd>

<span data-ttu-id="78243-118">Ruft die adressf für alle Texturen auf, wenn Sie an [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md)weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="78243-118">Calls AddRef on all of the textures when they are passed into [**ID3DX10Sprite::DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78243-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78243-119">Remarks</span></span>

<span data-ttu-id="78243-120">Nachdem eine Front-to-Back-oder Back-to-Front-Sortierung durchgeführt wurde, wird automatisch eine sekundäre Sortierung nach Textur durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="78243-120">After a front-to-back or back-to-front sort is done, it will automatically do a secondary sort by texture.</span></span> <span data-ttu-id="78243-121">Dies ist hilfreich, wenn sich viele Sprites mit derselben Textur auf derselben Ebene befinden, z. b. beim Zeichnen der Benutzeroberfläche in einem Spiel.</span><span class="sxs-lookup"><span data-stu-id="78243-121">This is helpful for when there are many sprites with the same texture all on the same plane, such as when drawing the user interface in a game.</span></span>

## <a name="requirements"></a><span data-ttu-id="78243-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78243-122">Requirements</span></span>



| <span data-ttu-id="78243-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78243-123">Requirement</span></span> | <span data-ttu-id="78243-124">Wert</span><span class="sxs-lookup"><span data-stu-id="78243-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78243-125">Header</span><span class="sxs-lookup"><span data-stu-id="78243-125">Header</span></span><br/> | <dl> <span data-ttu-id="78243-126"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="78243-126"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78243-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78243-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78243-128">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="78243-128">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




