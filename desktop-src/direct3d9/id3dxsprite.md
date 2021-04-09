---
description: Die ID3DXSprite-Schnittstelle stellt eine Reihe von Methoden bereit, die das Zeichnen von Sprites mithilfe von Microsoft Direct3D vereinfachen.
ms.assetid: ccf34fac-91a7-4734-bc62-aedaf4d66522
title: ID3DXSprite-Schnittstelle (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3703132cd8a0f7744119d9b8cb5d9d48f260094c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870135"
---
# <a name="id3dxsprite-interface"></a><span data-ttu-id="a8e5b-103">ID3DXSprite-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a8e5b-103">ID3DXSprite interface</span></span>

<span data-ttu-id="a8e5b-104">Die ID3DXSprite-Schnittstelle stellt eine Reihe von Methoden bereit, die das Zeichnen von Sprites mithilfe von Microsoft Direct3D vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-104">The ID3DXSprite interface provides a set of methods that simplify the process of drawing sprites using Microsoft Direct3D.</span></span>

## <a name="members"></a><span data-ttu-id="a8e5b-105">Member</span><span class="sxs-lookup"><span data-stu-id="a8e5b-105">Members</span></span>

<span data-ttu-id="a8e5b-106">Die **ID3DXSprite** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-106">The **ID3DXSprite** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a8e5b-107">**ID3DXSprite** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a8e5b-107">**ID3DXSprite** also has these types of members:</span></span>

-   [<span data-ttu-id="a8e5b-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="a8e5b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a8e5b-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="a8e5b-109">Methods</span></span>

<span data-ttu-id="a8e5b-110">Die **ID3DXSprite** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-110">The **ID3DXSprite** interface has these methods.</span></span>



| <span data-ttu-id="a8e5b-111">Methode</span><span class="sxs-lookup"><span data-stu-id="a8e5b-111">Method</span></span>                                                | <span data-ttu-id="a8e5b-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8e5b-112">Description</span></span>                                                                                                                                                                                                                  |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8e5b-113">**Starten**</span><span class="sxs-lookup"><span data-stu-id="a8e5b-113">**Begin**</span></span>](id3dxsprite--begin.md)                   | <span data-ttu-id="a8e5b-114">Bereitet ein Gerät zum Zeichnen von Sprites vor.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-114">Prepares a device for drawing sprites.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="a8e5b-115">**Draw**</span><span class="sxs-lookup"><span data-stu-id="a8e5b-115">**Draw**</span></span>](id3dxsprite--draw.md)                     | <span data-ttu-id="a8e5b-116">Fügt der Liste der im Batch verarbeiteten Sprites ein Sprite hinzu.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-116">Adds a sprite to the list of batched sprites.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="a8e5b-117">**ENDE**</span><span class="sxs-lookup"><span data-stu-id="a8e5b-117">**End**</span></span>](id3dxsprite--end.md)                       | <span data-ttu-id="a8e5b-118">Ruft [**ID3DXSprite:: Flush**](id3dxsprite--flush.md) auf und stellt den Gerätezustand vor dem Aufrufen von [**ID3DXSprite:: begin**](id3dxsprite--begin.md) wieder her.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-118">Calls [**ID3DXSprite::Flush**](id3dxsprite--flush.md) and restores the device state to how it was before [**ID3DXSprite::Begin**](id3dxsprite--begin.md) was called.</span></span><br/>                                            |
| [<span data-ttu-id="a8e5b-119">**Leerung**</span><span class="sxs-lookup"><span data-stu-id="a8e5b-119">**Flush**</span></span>](id3dxsprite--flush.md)                   | <span data-ttu-id="a8e5b-120">Erzwingt, dass alle Batch-Sprites an das Gerät übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-120">Forces all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="a8e5b-121">Gerätezustände verbleiben nach dem letzten [**ID3DXSprite:: begin**](id3dxsprite--begin.md)-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-121">Device states remain as they were after the last call to [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span> <span data-ttu-id="a8e5b-122">Die Liste der im Batch verarbeiteten Sprites wird dann gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-122">The list of batched sprites is then cleared.</span></span><br/> |
| [<span data-ttu-id="a8e5b-123">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="a8e5b-123">**GetDevice**</span></span>](id3dxsprite--getdevice.md)           | <span data-ttu-id="a8e5b-124">Ruft das Gerät ab, das dem Sprite-Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-124">Retrieves the device associated with the sprite object.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="a8e5b-125">**GetTransform**</span><span class="sxs-lookup"><span data-stu-id="a8e5b-125">**GetTransform**</span></span>](id3dxsprite--gettransform.md)     | <span data-ttu-id="a8e5b-126">Ruft die Sprite-Transformation ab.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-126">Gets the sprite transform.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="a8e5b-127">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="a8e5b-127">**OnLostDevice**</span></span>](id3dxsprite--onlostdevice.md)     | <span data-ttu-id="a8e5b-128">Verwenden Sie diese Methode, um alle Verweise auf Videospeicher Ressourcen freizugeben und alle stateblocks zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-128">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="a8e5b-129">Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder ein Gerät zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-129">This method should be called whenever a device is lost or before resetting a device.</span></span><br/>                              |
| [<span data-ttu-id="a8e5b-130">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="a8e5b-130">**OnResetDevice**</span></span>](id3dxsprite--onresetdevice.md)   | <span data-ttu-id="a8e5b-131">Verwenden Sie diese Methode, um Ressourcen erneut abzurufen und den Anfangszustand zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-131">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="a8e5b-132">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="a8e5b-132">**SetTransform**</span></span>](id3dxsprite--settransform.md)     | <span data-ttu-id="a8e5b-133">Legt die Sprite-Transformation fest.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-133">Sets the sprite transform.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="a8e5b-134">**SetWorldViewLH**</span><span class="sxs-lookup"><span data-stu-id="a8e5b-134">**SetWorldViewLH**</span></span>](id3dxsprite--setworldviewlh.md) | <span data-ttu-id="a8e5b-135">Legt die linke Seite "World-View Transform" für ein Sprite fest.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-135">Sets the left-handed world-view transform for a sprite.</span></span> <span data-ttu-id="a8e5b-136">Ein Aufrufe dieser Methode ist vor dem abgleichen oder Sortieren von Sprites erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-136">A call to this method is required before billboarding or sorting sprites.</span></span><br/>                                                                                 |
| [<span data-ttu-id="a8e5b-137">**SetWorldViewRH**</span><span class="sxs-lookup"><span data-stu-id="a8e5b-137">**SetWorldViewRH**</span></span>](id3dxsprite--setworldviewrh.md) | <span data-ttu-id="a8e5b-138">Legt die von rechts ausgebene World-View-Transformation für ein Sprite fest.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-138">Sets the right-handed world-view transform for a sprite.</span></span> <span data-ttu-id="a8e5b-139">Ein Aufrufe dieser Methode ist vor dem abgleichen oder Sortieren von Sprites erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-139">A call to this method is required before billboarding or sorting sprites.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="a8e5b-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8e5b-140">Remarks</span></span>

<span data-ttu-id="a8e5b-141">Die **ID3DXSprite** -Schnittstelle wird durch Aufrufen der [**D3DXCreateSprite**](d3dxcreatesprite.md) -Funktion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-141">The **ID3DXSprite** interface is obtained by calling the [**D3DXCreateSprite**](d3dxcreatesprite.md) function.</span></span>

<span data-ttu-id="a8e5b-142">Die Anwendung ruft in der Regel zuerst [**ID3DXSprite:: begin**](id3dxsprite--begin.md)auf und ermöglicht so die Kontrolle über den Geräte Rendering, die Alpha Mischung und die Sprite-Transformation und-Sortierung.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-142">The application typically first calls [**ID3DXSprite::Begin**](id3dxsprite--begin.md), which allows control over the device render state, alpha blending, and sprite transformation and sorting.</span></span> <span data-ttu-id="a8e5b-143">Nennen Sie dann für jedes Sprite, das angezeigt werden soll, [**ID3DXSprite::D RAW**](id3dxsprite--draw.md).</span><span class="sxs-lookup"><span data-stu-id="a8e5b-143">Then for each sprite to be displayed, call [**ID3DXSprite::Draw**](id3dxsprite--draw.md).</span></span> <span data-ttu-id="a8e5b-144">**ID3DXSprite::D RAW** kann wiederholt aufgerufen werden, um eine beliebige Anzahl von Sprites zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-144">**ID3DXSprite::Draw** can be called repeatedly to store any number of sprites.</span></span> <span data-ttu-id="a8e5b-145">Um die Batch Verarbeitung für das Gerät anzuzeigen, müssen Sie [**ID3DXSprite:: End**](id3dxsprite--end.md) oder [**ID3DXSprite:: Flush**](id3dxsprite--flush.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-145">To display the batched sprites to the device, call [**ID3DXSprite::End**](id3dxsprite--end.md) or [**ID3DXSprite::Flush**](id3dxsprite--flush.md).</span></span>

<span data-ttu-id="a8e5b-146">Der LPD3DXSPRITE-Typ wird als Zeiger auf die **ID3DXSprite** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="a8e5b-146">The LPD3DXSPRITE type is defined as a pointer to the **ID3DXSprite** interface.</span></span>


```
typedef interface ID3DXSprite ID3DXSprite;
typedef interface ID3DXSprite *LPD3DXSPRITE;
```



## <a name="requirements"></a><span data-ttu-id="a8e5b-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8e5b-147">Requirements</span></span>



| <span data-ttu-id="a8e5b-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8e5b-148">Requirement</span></span> | <span data-ttu-id="a8e5b-149">Wert</span><span class="sxs-lookup"><span data-stu-id="a8e5b-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e5b-150">Header</span><span class="sxs-lookup"><span data-stu-id="a8e5b-150">Header</span></span><br/>  | <dl> <span data-ttu-id="a8e5b-151"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8e5b-151"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a8e5b-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a8e5b-152">Library</span></span><br/> | <dl> <span data-ttu-id="a8e5b-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8e5b-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a8e5b-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8e5b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8e5b-155">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a8e5b-155">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
