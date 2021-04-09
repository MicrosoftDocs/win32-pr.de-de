---
title: ICM_DRAW_BEGIN Meldung (VFW. h)
description: Mit der ICM \_ Draw \_ Begin-Meldung wird ein renderingertreiber benachrichtigt, um das Zeichnen von Daten vorzubereiten.
ms.assetid: e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8
keywords:
- ICM_DRAW_BEGIN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db7b9e20a0b0621038e1c7e092a871a6727566cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956971"
---
# <a name="icm_draw_begin-message"></a><span data-ttu-id="42249-104">ICM- \_ Zeichnungs \_ anfangs Nachricht</span><span class="sxs-lookup"><span data-stu-id="42249-104">ICM\_DRAW\_BEGIN message</span></span>

<span data-ttu-id="42249-105">Mit der **ICM \_ Draw \_ Begin** -Meldung wird ein renderingertreiber benachrichtigt, um das Zeichnen von Daten vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="42249-105">The **ICM\_DRAW\_BEGIN** message notifies a rendering driver to prepare to draw data.</span></span>


```C++
ICM_DRAW_BEGIN 
wParam = (DWORD) (LPVOID) &icdrwBgn; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a><span data-ttu-id="42249-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="42249-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42249-107"><span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwbgn*</span><span class="sxs-lookup"><span data-stu-id="42249-107"><span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwBgn*</span></span>
</dt> <dd>

<span data-ttu-id="42249-108">Zeiger auf eine [**icdrawbegin**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) -Struktur, die das Eingabeformat enthält.</span><span class="sxs-lookup"><span data-stu-id="42249-108">Pointer to an [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="42249-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="42249-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="42249-110">Größe von **icdrawbegin**(in Bytes).</span><span class="sxs-lookup"><span data-stu-id="42249-110">Size, in bytes, of **ICDRAWBEGIN**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42249-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42249-111">Return Value</span></span>

<span data-ttu-id="42249-112">Gibt ICERR \_ OK zurück, wenn der Treiber das Zeichnen der Daten auf den Bildschirm auf die angegebene Art und Weise unterstützt, oder andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="42249-112">Returns ICERR\_OK if the driver supports drawing the data to the screen in the specified manner and format, or an error code otherwise.</span></span> <span data-ttu-id="42249-113">Folgende Fehler Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="42249-113">Possible error values include the following.</span></span>



| <span data-ttu-id="42249-114">Wert</span><span class="sxs-lookup"><span data-stu-id="42249-114">Value</span></span>               | <span data-ttu-id="42249-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="42249-115">Meaning</span></span>                                                                       |
|---------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="42249-116">ICERR \_ badformat</span><span class="sxs-lookup"><span data-stu-id="42249-116">ICERR\_BADFORMAT</span></span>    | <span data-ttu-id="42249-117">Ein Eingabe-oder Ausgabeformat wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42249-117">Input or output format is not supported.</span></span>                                      |
| <span data-ttu-id="42249-118">ICERR \_ NotSupported</span><span class="sxs-lookup"><span data-stu-id="42249-118">ICERR\_NOTSUPPORTED</span></span> | <span data-ttu-id="42249-119">Der Treiber wird nicht direkt auf den Bildschirm gezeichnet oder unterstützt diese Meldung nicht.</span><span class="sxs-lookup"><span data-stu-id="42249-119">Driver does not draw directly to the screen or does not support this message.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="42249-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42249-120">Remarks</span></span>

<span data-ttu-id="42249-121">Wenn Sie möchten, dass der Treiber Daten in einen Puffer dekomprimiert, senden Sie die [**ICM \_ dekomprimieren \_ Begin**](icm-decompress-begin.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="42249-121">If you want the driver to decompress data into a buffer, send the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="42249-122">Die **ICM \_ Draw- \_ Begin** -und [**ICM \_ Draw \_**](icm-draw-end.md) -Meldungen werden nicht geschachtelt.</span><span class="sxs-lookup"><span data-stu-id="42249-122">The **ICM\_DRAW\_BEGIN** and [**ICM\_DRAW\_END**](icm-draw-end.md) messages do not nest.</span></span> <span data-ttu-id="42249-123">Wenn der Treiber den **ICM- \_ Zeichnen- \_ Anfang** erhält, bevor die Dekomprimierung mit dem **ICM- \_ Zeichnungs \_ Ende** beendet wird, sollte die Dekomprimierung mit neuen Parametern neu gestartet</span><span class="sxs-lookup"><span data-stu-id="42249-123">If your driver receives **ICM\_DRAW\_BEGIN** before decompression is stopped with **ICM\_DRAW\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="42249-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42249-124">Requirements</span></span>



| <span data-ttu-id="42249-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42249-125">Requirement</span></span> | <span data-ttu-id="42249-126">Wert</span><span class="sxs-lookup"><span data-stu-id="42249-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="42249-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42249-127">Minimum supported client</span></span><br/> | <span data-ttu-id="42249-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42249-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="42249-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42249-129">Minimum supported server</span></span><br/> | <span data-ttu-id="42249-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42249-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="42249-131">Header</span><span class="sxs-lookup"><span data-stu-id="42249-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="42249-132"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="42249-132"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42249-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42249-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42249-134">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="42249-134">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="42249-135">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="42249-135">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





