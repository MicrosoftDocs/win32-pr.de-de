---
title: IDWriteTextLayout3-Schnittstelle
description: Stellt einen TextBlock dar, nachdem er vollständig analysiert und formatiert wurde. | IDWriteTextLayout3-Schnittstelle
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
keywords:
- IDWriteTextLayout3 Interface Direct Write
- IDWriteTextLayout3 Interface Direct Write, beschrieben
topic_type:
- apiref
api_name:
- IDWriteTextLayout3
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78a7a9203245939e40b522e0ef5998be0764085a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355146"
---
# <a name="idwritetextlayout3-interface"></a><span data-ttu-id="a485c-106">IDWriteTextLayout3-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a485c-106">IDWriteTextLayout3 interface</span></span>

<span data-ttu-id="a485c-107">Stellt einen TextBlock dar, nachdem er vollständig analysiert und formatiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a485c-107">Represents a block of text after it has been fully analyzed and formatted.</span></span>

## <a name="members"></a><span data-ttu-id="a485c-108">Member</span><span class="sxs-lookup"><span data-stu-id="a485c-108">Members</span></span>

<span data-ttu-id="a485c-109">Die **IDWriteTextLayout3** -Schnittstelle erbt von [**IDWriteTextLayout2**](idwritetextlayout2.md).</span><span class="sxs-lookup"><span data-stu-id="a485c-109">The **IDWriteTextLayout3** interface inherits from [**IDWriteTextLayout2**](idwritetextlayout2.md).</span></span> <span data-ttu-id="a485c-110">**IDWriteTextLayout3** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a485c-110">**IDWriteTextLayout3** also has these types of members:</span></span>

-   [<span data-ttu-id="a485c-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="a485c-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a485c-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="a485c-112">Methods</span></span>

<span data-ttu-id="a485c-113">Die **IDWriteTextLayout3** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a485c-113">The **IDWriteTextLayout3** interface has these methods.</span></span>



| <span data-ttu-id="a485c-114">Methode</span><span class="sxs-lookup"><span data-stu-id="a485c-114">Method</span></span>                                                          | <span data-ttu-id="a485c-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a485c-115">Description</span></span>                                                                                                                                                                                                                                                          |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a485c-116">**GetLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="a485c-116">**GetLineMetrics**</span></span>](idwritetextlayout3-getlinemetrics.md)     | <span data-ttu-id="a485c-117">Ruft die Eigenschaften der einzelnen Zeilen ab.</span><span class="sxs-lookup"><span data-stu-id="a485c-117">Retrieves properties of each line.</span></span><br/>                                                                                                                                                                                                                        |
| [<span data-ttu-id="a485c-118">**GetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="a485c-118">**GetLineSpacing**</span></span>](idwritetextlayout3-getlinespacing.md)     | <span data-ttu-id="a485c-119">Ruft Informationen zum Zeilenabstand ab.</span><span class="sxs-lookup"><span data-stu-id="a485c-119">Gets line spacing information.</span></span><br/>                                                                                                                                                                                                                            |
| [<span data-ttu-id="a485c-120">**Invalidatelayout**</span><span class="sxs-lookup"><span data-stu-id="a485c-120">**InvalidateLayout**</span></span>](idwritetextlayout3-invalidatelayout.md) | <span data-ttu-id="a485c-121">Macht das Layout ungültig und erzwingt, dass das Layout neu gemessen wird, bevor die Metriken oder Zeichnungsfunktionen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a485c-121">Invalidates the layout, forcing layout to remeasure before calling the metrics or drawing functions.</span></span> <span data-ttu-id="a485c-122">Dies ist hilfreich, wenn sich die Position einer Schriftart ändert und das Layout neu gezeichnet werden soll, oder wenn die Größe eines Clients idschreiteinlineobject-Änderungen implementiert hat.</span><span class="sxs-lookup"><span data-stu-id="a485c-122">This is useful if the locality of a font changes, and layout should be redrawn, or if the size of a client implemented IDWriteInlineObject changes.</span></span> <br/> |
| [<span data-ttu-id="a485c-123">**SetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="a485c-123">**SetLineSpacing**</span></span>](idwritetextlayout3-setlinespacing.md)     | <span data-ttu-id="a485c-124">Zeilenabstand festlegen.</span><span class="sxs-lookup"><span data-stu-id="a485c-124">Set line spacing.</span></span><br/>                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="a485c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a485c-125">Requirements</span></span>



| <span data-ttu-id="a485c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a485c-126">Requirement</span></span> | <span data-ttu-id="a485c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a485c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a485c-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a485c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a485c-129">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a485c-129">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="a485c-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a485c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a485c-131">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a485c-131">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="a485c-132">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="a485c-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="a485c-133">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="a485c-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="a485c-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a485c-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="a485c-135"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a485c-135"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a485c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a485c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a485c-137"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a485c-137"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a485c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a485c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a485c-139">**IDWriteTextLayout2**</span><span class="sxs-lookup"><span data-stu-id="a485c-139">**IDWriteTextLayout2**</span></span>](idwritetextlayout2.md)
</dt> </dl>

 

 





