---
title: ICM_DRAW_REALIZE Meldung (VFW. h)
description: Mit der ICM \_ Draw- \_ Meldung wird ein renderingerber benachrichtigt, seine Zeichnungs Palette beim Zeichnen zu erkennen. Sie können diese Nachricht explizit oder mithilfe des icdraw-/-Makros senden.
ms.assetid: 501540cd-41e2-4f80-abf8-2ec2179970a9
keywords:
- ICM_DRAW_REALIZE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd054c16caae55cba25c30098337e54b0ec4b681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391826"
---
# <a name="icm_draw_realize-message"></a><span data-ttu-id="cba47-105">ICM \_ Draw- \_ Nachricht erkennen</span><span class="sxs-lookup"><span data-stu-id="cba47-105">ICM\_DRAW\_REALIZE message</span></span>

<span data-ttu-id="cba47-106">Mit der **ICM \_ Draw \_** -Meldung wird ein renderingerber benachrichtigt, seine Zeichnungs Palette beim Zeichnen zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="cba47-106">The **ICM\_DRAW\_REALIZE** message notifies a rendering driver to realize its drawing palette while drawing.</span></span> <span data-ttu-id="cba47-107">Sie können diese Nachricht explizit oder mithilfe des [**icdraw-**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) /-Makros senden.</span><span class="sxs-lookup"><span data-stu-id="cba47-107">You can send this message explicitly or by using the [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) macro.</span></span>


```C++
ICM_DRAW_REALIZE 
wParam = (DWORD_PTR) (UINT_PTR) (HDC) hdc; 
lParam = (DWORD_PTR) (BOOL) fBackground; 
```



## <a name="parameters"></a><span data-ttu-id="cba47-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cba47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cba47-109"><span id="hdc"></span><span id="HDC"></span>*HDC*</span><span class="sxs-lookup"><span data-stu-id="cba47-109"><span id="hdc"></span><span id="HDC"></span>*hdc*</span></span>
</dt> <dd>

<span data-ttu-id="cba47-110">Handle für den DC, der zum realisieren der Palette verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cba47-110">Handle to the DC used to realize the palette.</span></span>

</dd> <dt>

<span data-ttu-id="cba47-111"><span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*f-Hintergrund*</span><span class="sxs-lookup"><span data-stu-id="cba47-111"><span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*</span></span>
</dt> <dd>

<span data-ttu-id="cba47-112">Hintergrundflag.</span><span class="sxs-lookup"><span data-stu-id="cba47-112">Background flag.</span></span> <span data-ttu-id="cba47-113">Geben Sie **true** an, um die Palette als Hintergrundaufgabe zu erkennen, oder **false** , um die Palette im Vordergrund zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="cba47-113">Specify **TRUE** to realize the palette as a background task or **FALSE** to realize the palette in the foreground.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cba47-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cba47-114">Return Value</span></span>

<span data-ttu-id="cba47-115">Gibt ICERR \_ OK zurück, wenn die Zeichnungs Palette realisiert wird, oder ICERR wird \_ nicht unterstützt, wenn die Palette, die den entkomprimierten Daten zugeordnet ist, erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="cba47-115">Returns ICERR\_OK if the drawing palette is realized or ICERR\_UNSUPPORTED if the palette associated with the decompressed data is realized.</span></span>

## <a name="remarks"></a><span data-ttu-id="cba47-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cba47-116">Remarks</span></span>

<span data-ttu-id="cba47-117">Treiber müssen auf diese Nachricht nur reagieren, wenn sich die Zeichnungs Palette von der dekomprimierten Palette unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="cba47-117">Drivers need to respond to this message only if the drawing palette is different from the decompressed palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="cba47-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cba47-118">Requirements</span></span>



| <span data-ttu-id="cba47-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cba47-119">Requirement</span></span> | <span data-ttu-id="cba47-120">Wert</span><span class="sxs-lookup"><span data-stu-id="cba47-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cba47-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cba47-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cba47-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cba47-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cba47-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cba47-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cba47-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cba47-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cba47-125">Header</span><span class="sxs-lookup"><span data-stu-id="cba47-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cba47-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="cba47-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cba47-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cba47-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cba47-128">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="cba47-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="cba47-129">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="cba47-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





