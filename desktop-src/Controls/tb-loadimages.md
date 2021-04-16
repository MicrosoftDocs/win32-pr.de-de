---
title: TB_LOADIMAGES Meldung (kommstrg. h)
description: Lädt System definierte Schaltflächen Bilder in die Bildliste eines Symbolleisten-Steuer Elements.
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- Windows-Steuerelemente für TB_LOADIMAGES Meldung
topic_type:
- apiref
api_name:
- TB_LOADIMAGES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0ba6bf75855a0b81ac56438489d7eced3d589
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478090"
---
# <a name="tb_loadimages-message"></a><span data-ttu-id="4f60d-104">TB- \_ loadimages-Nachricht</span><span class="sxs-lookup"><span data-stu-id="4f60d-104">TB\_LOADIMAGES message</span></span>

<span data-ttu-id="4f60d-105">Lädt System definierte Schaltflächen Bilder in die Bildliste eines Symbolleisten-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="4f60d-105">Loads system-defined button images into a toolbar control's image list.</span></span>

## <a name="parameters"></a><span data-ttu-id="4f60d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f60d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f60d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4f60d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f60d-108">Der Bezeichner einer System definierten Schaltflächen Bildliste.</span><span class="sxs-lookup"><span data-stu-id="4f60d-108">Identifier of a system-defined button image list.</span></span> <span data-ttu-id="4f60d-109">Dieser Parameter kann auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4f60d-109">This parameter can be set to one of the following values.</span></span>



| <span data-ttu-id="4f60d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="4f60d-110">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="4f60d-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4f60d-111">Meaning</span></span>                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <span data-ttu-id="4f60d-112"><dt>**hohe IDB- \_ \_ \_ Farbe**</dt></span><span class="sxs-lookup"><span data-stu-id="4f60d-112"><dt>**IDB\_HIST\_LARGE\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="4f60d-113">Windows Explorer-Bitmaps in großem Umfang.</span><span class="sxs-lookup"><span data-stu-id="4f60d-113">Windows Explorer bitmaps in large size.</span></span><br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <span data-ttu-id="4f60d-114"><dt>**IDB \_ Hist \_ Small \_ Color**</dt></span><span class="sxs-lookup"><span data-stu-id="4f60d-114"><dt>**IDB\_HIST\_SMALL\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="4f60d-115">Windows Explorer-Bitmaps in kleiner Größe.</span><span class="sxs-lookup"><span data-stu-id="4f60d-115">Windows Explorer bitmaps in small size.</span></span><br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <span data-ttu-id="4f60d-116"><dt>**\_ \_ hohe Farbe für IDB Std \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4f60d-116"><dt>**IDB\_STD\_LARGE\_COLOR**</dt></span></span> </dl>    | <span data-ttu-id="4f60d-117">Standard Bitmaps in großem Umfang.</span><span class="sxs-lookup"><span data-stu-id="4f60d-117">Standard bitmaps in large size.</span></span><br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <span data-ttu-id="4f60d-118"><dt>**IDB \_ Std \_ Small- \_ Farbe**</dt></span><span class="sxs-lookup"><span data-stu-id="4f60d-118"><dt>**IDB\_STD\_SMALL\_COLOR**</dt></span></span> </dl>    | <span data-ttu-id="4f60d-119">Standard Bitmaps in kleiner Größe.</span><span class="sxs-lookup"><span data-stu-id="4f60d-119">Standard bitmaps in small size.</span></span><br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <span data-ttu-id="4f60d-120"><dt>**IDB- \_ Sicht \_ große \_ Farbe**</dt></span><span class="sxs-lookup"><span data-stu-id="4f60d-120"><dt>**IDB\_VIEW\_LARGE\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="4f60d-121">Anzeigen von Bitmaps in großem Umfang.</span><span class="sxs-lookup"><span data-stu-id="4f60d-121">View bitmaps in large size.</span></span><br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <span data-ttu-id="4f60d-122"><dt>**IDB- \_ Sicht \_ kleine \_ Farbe**</dt></span><span class="sxs-lookup"><span data-stu-id="4f60d-122"><dt>**IDB\_VIEW\_SMALL\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="4f60d-123">Bitmaps in kleiner Größe anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4f60d-123">View bitmaps in small size.</span></span><br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <span data-ttu-id="4f60d-124"><dt>**IDB- \_ Hist \_ Normal**</dt></span><span class="sxs-lookup"><span data-stu-id="4f60d-124"><dt>**IDB\_HIST\_NORMAL**</dt></span></span> </dl>                 | <span data-ttu-id="4f60d-125">Windows-Explorer-Fahrten Schaltflächen und Favoriten Bitmaps im normalen Zustand.</span><span class="sxs-lookup"><span data-stu-id="4f60d-125">Windows Explorer travel buttons and favorites bitmaps in normal state.</span></span><br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <span data-ttu-id="4f60d-126"><dt>**IDB- \_ Hist- \_ Hot**</dt></span><span class="sxs-lookup"><span data-stu-id="4f60d-126"><dt>**IDB\_HIST\_HOT**</dt></span></span> </dl>                          | <span data-ttu-id="4f60d-127">Windows-Explorer-Reise Schaltflächen und Favoriten Bitmaps im aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="4f60d-127">Windows Explorer travel buttons and favorites bitmaps in hot state.</span></span><br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <span data-ttu-id="4f60d-128"><dt>**IDB- \_ Hist \_ deaktiviert**</dt></span><span class="sxs-lookup"><span data-stu-id="4f60d-128"><dt>**IDB\_HIST\_DISABLED**</dt></span></span> </dl>           | <span data-ttu-id="4f60d-129">Windows-Explorer-Reise Schaltflächen und Favoriten Bitmaps in deaktiviertem Zustand.</span><span class="sxs-lookup"><span data-stu-id="4f60d-129">Windows Explorer travel buttons and favorites bitmaps in disabled state.</span></span><br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <span data-ttu-id="4f60d-130"><dt>**IDB \_ Hist \_ gedrückt**</dt></span><span class="sxs-lookup"><span data-stu-id="4f60d-130"><dt>**IDB\_HIST\_PRESSED**</dt></span></span> </dl>              | <span data-ttu-id="4f60d-131">Windows-Explorer-Fahrten Schaltflächen und Favoriten Bitmaps im gedrückten Zustand.</span><span class="sxs-lookup"><span data-stu-id="4f60d-131">Windows Explorer travel buttons and favorites bitmaps in pressed state.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="4f60d-132">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f60d-132">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f60d-133">Instanzhandle.</span><span class="sxs-lookup"><span data-stu-id="4f60d-133">Instance handle.</span></span> <span data-ttu-id="4f60d-134">Dieser Parameter muss auf hInst kommctrl festgelegt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="4f60d-134">This parameter must be set to HINST\_COMMCTRL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f60d-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f60d-135">Return value</span></span>

<span data-ttu-id="4f60d-136">Die Anzahl der Bilder in der Bildliste.</span><span class="sxs-lookup"><span data-stu-id="4f60d-136">The count of images in the image list.</span></span> <span data-ttu-id="4f60d-137">Gibt 0 (null) zurück, wenn die Symbolleiste keine Bildliste aufweist oder wenn die vorhandene Bildliste leer ist.</span><span class="sxs-lookup"><span data-stu-id="4f60d-137">Returns zero if the toolbar has no image list or if the existing image list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f60d-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f60d-138">Remarks</span></span>

<span data-ttu-id="4f60d-139">Sie müssen die richtigen Bild Indexwerte verwenden, wenn Sie die [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Strukturen vor dem Senden der [**TB- \_ AddButtons**](tb-addbuttons.md) -Nachricht vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="4f60d-139">You must use the proper image index values when you prepare [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structures prior to sending the [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span> <span data-ttu-id="4f60d-140">Eine Liste der Bild Indexwerte für diese vordefinierten Bitmaps finden Sie unter [Indexwerte der Symbolleisten-Standard Schaltfläche](toolbar-standard-button-image-index-values.md).</span><span class="sxs-lookup"><span data-stu-id="4f60d-140">For a list of image index values for these preset bitmaps, see [Toolbar Standard Button Image Index Values](toolbar-standard-button-image-index-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4f60d-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f60d-141">Examples</span></span>

<span data-ttu-id="4f60d-142">Im folgenden Beispielcode werden die System Standard-Small Color-Bilder geladen.</span><span class="sxs-lookup"><span data-stu-id="4f60d-142">The following sample code loads the system standard small color images.</span></span>


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a><span data-ttu-id="4f60d-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f60d-143">Requirements</span></span>



| <span data-ttu-id="4f60d-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f60d-144">Requirement</span></span> | <span data-ttu-id="4f60d-145">Wert</span><span class="sxs-lookup"><span data-stu-id="4f60d-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f60d-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f60d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="4f60d-147">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f60d-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4f60d-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f60d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="4f60d-149">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f60d-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4f60d-150">Header</span><span class="sxs-lookup"><span data-stu-id="4f60d-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f60d-151"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f60d-151"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f60d-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f60d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f60d-153">**TB \_ AddBitmap**</span><span class="sxs-lookup"><span data-stu-id="4f60d-153">**TB\_ADDBITMAP**</span></span>](tb-addbitmap.md)
</dt> </dl>

 

 





