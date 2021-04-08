---
title: STM_SETIMAGE Meldung (Winuser. h)
description: Eine Anwendung sendet eine STM \_ SetImage-Nachricht, um ein neues Bild einem statischen Steuerelement zuzuordnen.
ms.assetid: d3e7c5d4-f621-40f6-9558-7fb699e8b489
keywords:
- Windows-Steuerelemente für STM_SETIMAGE Meldung
topic_type:
- apiref
api_name:
- STM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27c4f9c216d2e987727a1e2fa9bc6de12a823d52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949547"
---
# <a name="stm_setimage-message"></a><span data-ttu-id="1926e-104">STM- \_ abtimage-Nachricht</span><span class="sxs-lookup"><span data-stu-id="1926e-104">STM\_SETIMAGE message</span></span>

<span data-ttu-id="1926e-105">Eine Anwendung sendet eine **STM \_ SetImage** -Nachricht, um ein neues Bild einem statischen Steuerelement zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="1926e-105">An application sends an **STM\_SETIMAGE** message to associate a new image with a static control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1926e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1926e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1926e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1926e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1926e-108">Gibt den Typ des Bilds an, das dem statischen Steuerelement zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1926e-108">Specifies the type of image to associate with the static control.</span></span> <span data-ttu-id="1926e-109">Dieser Parameter kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="1926e-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="1926e-110">Wert</span><span class="sxs-lookup"><span data-stu-id="1926e-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="1926e-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1926e-111">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="1926e-112"><dt>**Bild \_ Bitmap**</dt></span><span class="sxs-lookup"><span data-stu-id="1926e-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl>                | <span data-ttu-id="1926e-113">Bitmap.</span><span class="sxs-lookup"><span data-stu-id="1926e-113">Bitmap.</span></span><br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <span data-ttu-id="1926e-114"><dt>**Bild \_ Cursor**</dt></span><span class="sxs-lookup"><span data-stu-id="1926e-114"><dt>**IMAGE\_CURSOR**</dt></span></span> </dl>                | <span data-ttu-id="1926e-115">Hand.</span><span class="sxs-lookup"><span data-stu-id="1926e-115">Cursor.</span></span><br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <span data-ttu-id="1926e-116"><dt>**Image- \_ enhmetafile**</dt></span><span class="sxs-lookup"><span data-stu-id="1926e-116"><dt>**IMAGE\_ENHMETAFILE**</dt></span></span> </dl> | <span data-ttu-id="1926e-117">Erweiterte Metadatei.</span><span class="sxs-lookup"><span data-stu-id="1926e-117">Enhanced metafile.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="1926e-118"><dt>**Bild \_ Symbol**</dt></span><span class="sxs-lookup"><span data-stu-id="1926e-118"><dt>**IMAGE\_ICON**</dt></span></span> </dl>                      | <span data-ttu-id="1926e-119">Angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1926e-119">Icon.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="1926e-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1926e-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1926e-121">Handle für das Bild, das dem statischen Steuerelement zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1926e-121">Handle to the image to associate with the static control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1926e-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1926e-122">Return value</span></span>

<span data-ttu-id="1926e-123">Der Rückgabewert ist ein Handle für das Bild, das zuvor dem statischen Steuerelement zugeordnet ist, sofern vorhanden. Andernfalls ist der Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="1926e-123">The return value is a handle to the image previously associated with the static control, if any; otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1926e-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1926e-124">Remarks</span></span>

<span data-ttu-id="1926e-125">Zum Zuordnen eines Bilds zu einem statischen Steuerelement muss das Steuerelement über den richtigen Stil verfügen.</span><span class="sxs-lookup"><span data-stu-id="1926e-125">To associate an image with a static control, the control must have the proper style.</span></span> <span data-ttu-id="1926e-126">In der folgenden Tabelle wird der für jeden Bildtyp benötigte Stil angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1926e-126">The following table shows the style needed for each image type.</span></span>



| <span data-ttu-id="1926e-127">Imagetyp</span><span class="sxs-lookup"><span data-stu-id="1926e-127">Image type</span></span>         | <span data-ttu-id="1926e-128">Stil des statischen Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="1926e-128">Static control style</span></span> |
|--------------------|----------------------|
| <span data-ttu-id="1926e-129">Bild \_ Bitmap</span><span class="sxs-lookup"><span data-stu-id="1926e-129">IMAGE\_BITMAP</span></span>      | <span data-ttu-id="1926e-130">SS- \_ Bitmap</span><span class="sxs-lookup"><span data-stu-id="1926e-130">SS\_BITMAP</span></span>           |
| <span data-ttu-id="1926e-131">Bild \_ Cursor</span><span class="sxs-lookup"><span data-stu-id="1926e-131">IMAGE\_CURSOR</span></span>      | <span data-ttu-id="1926e-132">SS- \_ Symbol</span><span class="sxs-lookup"><span data-stu-id="1926e-132">SS\_ICON</span></span>             |
| <span data-ttu-id="1926e-133">Image- \_ enhmetafile</span><span class="sxs-lookup"><span data-stu-id="1926e-133">IMAGE\_ENHMETAFILE</span></span> | <span data-ttu-id="1926e-134">SS-" \_ enhmetafile"</span><span class="sxs-lookup"><span data-stu-id="1926e-134">SS\_ENHMETAFILE</span></span>      |
| <span data-ttu-id="1926e-135">Bild \_ Symbol</span><span class="sxs-lookup"><span data-stu-id="1926e-135">IMAGE\_ICON</span></span>        | <span data-ttu-id="1926e-136">SS- \_ Symbol</span><span class="sxs-lookup"><span data-stu-id="1926e-136">SS\_ICON</span></span>             |



 

> [!IMPORTANT]
>
> <span data-ttu-id="1926e-137">In Version 6 der Win32-Steuerelemente von Microsoft war eine Bitmap, die an ein statisches Steuerelement mithilfe der STM-ablaufnachricht übergeben wurde, dieselbe Bitmap, die von einer nachfolgenden **STM \_** -ablaufsnachricht zurückgegeben wurde. **\_**</span><span class="sxs-lookup"><span data-stu-id="1926e-137">In version 6 of the Microsoft Win32 controls, a bitmap passed to a static control using the **STM\_SETIMAGE** message was the same bitmap returned by a subsequent **STM\_SETIMAGE** message.</span></span> <span data-ttu-id="1926e-138">Der Client ist dafür verantwortlich, jede Bitmap zu löschen, die an ein statisches Steuerelement gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="1926e-138">The client is responsible to delete any bitmap sent to a static control.</span></span>
>
> <span data-ttu-id="1926e-139">Wenn in Windows XP die in der STM-ablaufmeldungs Meldung über gegebene Bitmap Pixel mit einem Alpha Wert ungleich 0 (null) enthält, nimmt das statische Steuerelement eine Kopie der Bitmap an. **\_**</span><span class="sxs-lookup"><span data-stu-id="1926e-139">With Windows XP, if the bitmap passed in the **STM\_SETIMAGE** message contains pixels with nonzero alpha, the static control takes a copy of the bitmap.</span></span> <span data-ttu-id="1926e-140">Diese kopierte Bitmap wird von der nächsten **STM- \_ logtimage** -Nachricht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1926e-140">This copied bitmap is returned by the next **STM\_SETIMAGE** message.</span></span> <span data-ttu-id="1926e-141">Der Client Code kann die an das statische Steuerelement übergebenen Bitmaps unabhängig nachverfolgen, aber wenn er die von **STM \_ SetImage** -Nachrichten zurückgegebenen Bitmaps nicht überprüft und freigibt, werden die Bitmaps kompromittiert.</span><span class="sxs-lookup"><span data-stu-id="1926e-141">The client code may independently track the bitmaps passed to the static control, but if it does not check and release the bitmaps returned from **STM\_SETIMAGE** messages, the bitmaps are leaked.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1926e-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1926e-142">Requirements</span></span>



| <span data-ttu-id="1926e-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1926e-143">Requirement</span></span> | <span data-ttu-id="1926e-144">Wert</span><span class="sxs-lookup"><span data-stu-id="1926e-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1926e-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1926e-145">Minimum supported client</span></span><br/> | <span data-ttu-id="1926e-146">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1926e-146">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1926e-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1926e-147">Minimum supported server</span></span><br/> | <span data-ttu-id="1926e-148">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1926e-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1926e-149">Header</span><span class="sxs-lookup"><span data-stu-id="1926e-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="1926e-150"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="1926e-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1926e-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1926e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1926e-152">**STM \_ GetImage**</span><span class="sxs-lookup"><span data-stu-id="1926e-152">**STM\_GETIMAGE**</span></span>](stm-getimage.md)
</dt> </dl>

 

 





