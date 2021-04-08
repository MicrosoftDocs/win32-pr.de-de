---
title: ICM_DRAW Meldung (VFW. h)
description: Mit der ICM \_ Draw-Nachricht wird ein renderingertreiber benachrichtigt, um einen Datenrahmen zu dekomprimieren und auf dem Bildschirm zu zeichnen.
ms.assetid: eceb42c6-d91a-45b7-98dc-e0944df3e558
keywords:
- ICM_DRAW-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0840c6df2c69f4d3e45600cf8599c214b36200a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741169"
---
# <a name="icm_draw-message"></a><span data-ttu-id="7fb02-104">ICM- \_ Zeichnungs Meldung</span><span class="sxs-lookup"><span data-stu-id="7fb02-104">ICM\_DRAW message</span></span>

<span data-ttu-id="7fb02-105">Mit der **ICM \_ Draw** -Nachricht wird ein renderingertreiber benachrichtigt, um einen Datenrahmen zu dekomprimieren und auf dem Bildschirm zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="7fb02-105">The **ICM\_DRAW** message notifies a rendering driver to decompress a frame of data and draw it to the screen.</span></span>


```C++
ICM_DRAW 
wParam = (DWORD) (LPVOID) &icdraw; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a><span data-ttu-id="7fb02-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fb02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fb02-107"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="7fb02-107"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="7fb02-108">Zeiger auf eine [**icdraw**](/windows/desktop/api/Vfw/ns-vfw-icdraw) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7fb02-108">Pointer to an [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7fb02-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="7fb02-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="7fb02-110">Größe von [**icdraw**](/windows/desktop/api/Vfw/ns-vfw-icdraw)(in Bytes).</span><span class="sxs-lookup"><span data-stu-id="7fb02-110">Size, in bytes, of [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fb02-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7fb02-111">Return Value</span></span>

<span data-ttu-id="7fb02-112">Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="7fb02-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fb02-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7fb02-113">Remarks</span></span>

<span data-ttu-id="7fb02-114">Wenn das icdraw- \_ updateflag im **dwFlags** -Member von [**icdraw**](/windows/desktop/api/Vfw/ns-vfw-icdraw)festgelegt wird, ist der zum Zeichnen verwendete Bildschirm ungültig und muss aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7fb02-114">If the ICDRAW\_UPDATE flag is set in the **dwFlags** member of [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw), the area of the screen used for drawing is invalid and needs to be updated.</span></span> <span data-ttu-id="7fb02-115">Der Umfang der Aktualisierung hängt vom Inhalt des **lpdata** -Members ab.</span><span class="sxs-lookup"><span data-stu-id="7fb02-115">The extent of updating depends on the contents of the **lpData** member.</span></span>

<span data-ttu-id="7fb02-116">Wenn **lpdata** **null** ist, sollte der Treiber das gesamte Ziel Rechteck mit dem aktuellen Bild aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7fb02-116">If **lpData** is **NULL**, the driver should update the entire destination rectangle with the current image.</span></span> <span data-ttu-id="7fb02-117">Wenn der Treiber eine Kopie des Abbilds in einem Offscreen-Puffer verwaltet, kann diese Meldung fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="7fb02-117">If the driver maintains a copy of the image in an off-screen buffer, it can fail this message.</span></span> <span data-ttu-id="7fb02-118">Wenn **lpdata** nicht **null** ist, sollte der Treiber die Daten zeichnen und sicherstellen, dass das gesamte Ziel aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7fb02-118">If **lpData** is not **NULL**, the driver should draw the data and make sure the entire destination is updated.</span></span>

<span data-ttu-id="7fb02-119">Wenn das icdraw- \_ hurryup-Flag in **dwFlags** festgelegt ist, möchte die aufrufende Anwendung, dass der Treiber so schnell wie möglich fortgesetzt werden kann. möglicherweise wird der Bildschirm nicht sogar aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fb02-119">If the ICDRAW\_HURRYUP flag is set in **dwFlags**, the calling application wants the driver to proceed as quickly as possible, possibly not even updating the screen.</span></span>

<span data-ttu-id="7fb02-120">Wenn das icdraw- \_ vorab-Flag in **dwFlags** festgelegt ist, handelt es sich bei diesem Videoframe um vorläufige Informationen, die nach Möglichkeit nicht angezeigt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="7fb02-120">If the ICDRAW\_PREROLL flag is set in **dwFlags**, this video frame is preliminary information and should not be displayed if possible.</span></span> <span data-ttu-id="7fb02-121">Wenn z. b. "Play" von Frame 10 gestartet werden soll und Frame 0 der nächste vorherige Keyframe ist, haben die Rahmen 0 bis 9 das icdraw- \_ vorab Zeichen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7fb02-121">For example, if play is to start from frame 10, and frame 0 is the nearest previous key frame, frames 0 through 9 will have ICDRAW\_PREROLL set.</span></span>

<span data-ttu-id="7fb02-122">Wenn Sie möchten, dass der Treiber Daten in einen Puffer dekomprimieren soll, senden Sie die [**ICM \_ dekomprimieren**](icm-decompress.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="7fb02-122">If you want the driver to decompress data into a buffer, send the [**ICM\_DECOMPRESS**](icm-decompress.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fb02-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7fb02-123">Requirements</span></span>



| <span data-ttu-id="7fb02-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7fb02-124">Requirement</span></span> | <span data-ttu-id="7fb02-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7fb02-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fb02-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7fb02-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7fb02-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fb02-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7fb02-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7fb02-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7fb02-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fb02-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7fb02-130">Header</span><span class="sxs-lookup"><span data-stu-id="7fb02-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fb02-131"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fb02-131"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fb02-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fb02-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fb02-133">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="7fb02-133">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="7fb02-134">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="7fb02-134">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





