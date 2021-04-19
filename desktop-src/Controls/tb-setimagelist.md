---
title: TB_SETIMAGELIST Meldung (kommstrg. h)
description: Legt die Bildliste fest, die die Symbolleiste zum Anzeigen von Schaltflächen verwendet, die sich in Ihrem Standardzustand befinden.
ms.assetid: 432ffdfc-bb63-4405-90da-9392910fdbb6
keywords:
- Windows-Steuerelemente für TB_SETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- TB_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0b7ad631e8b56824ae65a2b262c5478611e75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346515"
---
# <a name="tb_setimagelist-message"></a><span data-ttu-id="21f9c-104">TB \_ SetImageList-Meldung</span><span class="sxs-lookup"><span data-stu-id="21f9c-104">TB\_SETIMAGELIST message</span></span>

<span data-ttu-id="21f9c-105">Legt die Bildliste fest, die die Symbolleiste zum Anzeigen von Schaltflächen verwendet, die sich in Ihrem Standardzustand befinden.</span><span class="sxs-lookup"><span data-stu-id="21f9c-105">Sets the image list that the toolbar uses to display buttons that are in their default state.</span></span>

## <a name="parameters"></a><span data-ttu-id="21f9c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="21f9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21f9c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="21f9c-107">*wParam*</span></span> 
</dt> <dd>

[<span data-ttu-id="21f9c-108">Version 5,80.</span><span class="sxs-lookup"><span data-stu-id="21f9c-108">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="21f9c-109">Der Index der Liste.</span><span class="sxs-lookup"><span data-stu-id="21f9c-109">The index of the list.</span></span> <span data-ttu-id="21f9c-110">Wenn Sie nur eine Bildliste oder eine frühere Version der allgemeinen Steuerelemente verwenden, legen Sie *wParam* auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="21f9c-110">If you use only one image list, or an earlier version of the common controls, set *wParam* to zero.</span></span> <span data-ttu-id="21f9c-111">Weitere Informationen zur Verwendung mehrerer Bildlisten finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="21f9c-111">See Remarks for details on using multiple image lists.</span></span>

</dd> <dt>

<span data-ttu-id="21f9c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="21f9c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21f9c-113">Handle für die festzulegende Bildliste.</span><span class="sxs-lookup"><span data-stu-id="21f9c-113">Handle to the image list to set.</span></span> <span data-ttu-id="21f9c-114">Wenn dieser Parameter **null** ist, werden keine Bilder in den Schaltflächen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="21f9c-114">If this parameter is **NULL**, no images are displayed in the buttons.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21f9c-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21f9c-115">Return value</span></span>

<span data-ttu-id="21f9c-116">Gibt das Handle für die Bildliste zurück, die zuvor zum Anzeigen von Schaltflächen in Ihrem Standardzustand verwendet wurde, oder **null** , wenn zuvor keine Bildliste festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="21f9c-116">Returns the handle to the image list previously used to display buttons in their default state, or **NULL** if no image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="21f9c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21f9c-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="21f9c-118">Die Anwendung ist dafür verantwortlich, die Bildliste freizugeben, nachdem die Symbolleiste zerstört wurde.</span><span class="sxs-lookup"><span data-stu-id="21f9c-118">Your application is responsible for freeing the image list after the toolbar is destroyed.</span></span>

 

<span data-ttu-id="21f9c-119">Die **TB- \_ SetImageList** -Nachricht kann nicht mit [**TB \_ AddBitmap**](tb-addbitmap.md)kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="21f9c-119">The **TB\_SETIMAGELIST** message cannot be combined with [**TB\_ADDBITMAP**](tb-addbitmap.md).</span></span> <span data-ttu-id="21f9c-120">Sie kann auch nicht mit Symbolleisten verwendet werden, die mit " [**kreatetoolbarex**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex)" erstellt wurden, wodurch " **TB \_ AddBitmap** " intern aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="21f9c-120">It also cannot be used with toolbars created with [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), which calls **TB\_ADDBITMAP** internally.</span></span> <span data-ttu-id="21f9c-121">Wenn Sie eine Symbolleiste mit " **kreatetoolbarex** " erstellen oder zum Hinzufügen von Bildern " **TB \_ AddBitmap** " verwenden, wird die Bildliste von der Symbolleiste intern verwaltet.</span><span class="sxs-lookup"><span data-stu-id="21f9c-121">When you create a toolbar with **CreateToolbarEx** or use **TB\_ADDBITMAP** to add images, the toolbar manages the image list internally.</span></span> <span data-ttu-id="21f9c-122">Der Versuch, ihn mit **TB \_ SetImageList** zu ändern, hat unvorhersehbare Konsequenzen.</span><span class="sxs-lookup"><span data-stu-id="21f9c-122">Attempting to modify it with **TB\_SETIMAGELIST** has unpredictable consequences.</span></span>

<span data-ttu-id="21f9c-123">Bei [Version 5,80](common-control-versions.md) oder höher der allgemeinen Steuerelemente müssen Schaltflächen Bilder nicht aus derselben Bildliste stammen.</span><span class="sxs-lookup"><span data-stu-id="21f9c-123">With [version 5.80](common-control-versions.md) or later of the common controls, button images need not come from the same image list.</span></span> <span data-ttu-id="21f9c-124">So verwenden Sie mehrere Bildlisten für Ihre Symbolleisten-Schaltflächen Bilder:</span><span class="sxs-lookup"><span data-stu-id="21f9c-124">To use multiple image lists for your toolbar button images:</span></span>

1.  <span data-ttu-id="21f9c-125">Aktivieren Sie mehrere Bildlisten, indem Sie das Symbolleisten-Steuerelement eine [**ccm- \_ setVersion**](ccm-setversion.md) -Nachricht mit *wParam* (Versionsnummer) an 5 senden.</span><span class="sxs-lookup"><span data-stu-id="21f9c-125">Enable multiple image lists by sending the toolbar control a [**CCM\_SETVERSION**](ccm-setversion.md) message with *wParam* (the version number) set to 5.</span></span>
2.  <span data-ttu-id="21f9c-126">Senden Sie für jede Bildliste, die Sie verwenden möchten, das Symbolleisten-Steuerelement eine **TB- \_ SetImageList** -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="21f9c-126">For each image list you want to use, send the toolbar control a **TB\_SETIMAGELIST** message.</span></span> <span data-ttu-id="21f9c-127">Legen Sie *wParam* auf einen von der Anwendung definierten *wParam* -Wert fest, der verwendet wird, um die Liste zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="21f9c-127">Set *wParam* to an application-defined *wParam* value that will be used to identify the list.</span></span> <span data-ttu-id="21f9c-128">Legen Sie *LPARAM* auf das HIMAGELIST-Handle der Liste fest.</span><span class="sxs-lookup"><span data-stu-id="21f9c-128">Set *lParam* to the list's HIMAGELIST handle.</span></span>
3.  <span data-ttu-id="21f9c-129">Legen Sie für jede Schaltfläche den **ibitmap** -Member der [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur der Schaltfläche auf makelong (*iIndex*, *iimageid*) fest.</span><span class="sxs-lookup"><span data-stu-id="21f9c-129">For each button, set the **iBitmap** member of the button's [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure to MAKELONG(*iIndex*, *iImageID*).</span></span> <span data-ttu-id="21f9c-130">Der *iimageid* -Wert ist die ID der entsprechenden Bildliste, die in Schritt 2 definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="21f9c-130">The *iImageID* value is the ID of the appropriate image list that was defined in step two.</span></span> <span data-ttu-id="21f9c-131">Der *iIndex* -Wert ist der Index des jeweiligen Bilds in dieser Liste.</span><span class="sxs-lookup"><span data-stu-id="21f9c-131">The *iIndex* value is the index of the particular image within that list.</span></span>
4.  <span data-ttu-id="21f9c-132">Fügen Sie die Schaltflächen hinzu, indem Sie das Symbolleisten-Steuerelement an eine [**TB- \_ AddButtons**](tb-addbuttons.md)</span><span class="sxs-lookup"><span data-stu-id="21f9c-132">Add the buttons by sending the toolbar control a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>

<span data-ttu-id="21f9c-133">Im folgenden Code Fragment wird veranschaulicht, wie einer Symbolleiste mit Bildern aus drei verschiedenen Bildlisten fünf Schaltflächen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="21f9c-133">The following code fragment illustrates how to add five buttons to a toolbar, with images from three different image lists.</span></span> <span data-ttu-id="21f9c-134">Die Unterstützung für mehrere Bildlisten wird mit einer [**ccm- \_ setVersion**](ccm-setversion.md) -Nachricht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="21f9c-134">Support for multiple image lists is enabled with a [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span> <span data-ttu-id="21f9c-135">Anschließend werden die Bildlisten und die zugewiesenen IDs 0-2 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="21f9c-135">The image lists are then set and assigned IDs of 0-2.</span></span> <span data-ttu-id="21f9c-136">Den Schaltflächen werden Bilder aus den Bildlisten wie folgt zugewiesen:</span><span class="sxs-lookup"><span data-stu-id="21f9c-136">The buttons are assigned images from the image lists as follows:</span></span>

-   <span data-ttu-id="21f9c-137">Die Schaltfläche 0 ist aus der Bildliste NULL (ahim \[ 0 \] ) mit dem Index 1.</span><span class="sxs-lookup"><span data-stu-id="21f9c-137">Button 0 is from image list zero (ahim\[0\]) with index of 1.</span></span>
-   <span data-ttu-id="21f9c-138">Schaltfläche 1 ist von der Bildliste 1 (ahim \[ 1 \] ) mit dem Index 1.</span><span class="sxs-lookup"><span data-stu-id="21f9c-138">Button 1 is from image list one (ahim\[1\]) with an index of 1.</span></span>
-   <span data-ttu-id="21f9c-139">Schaltfläche 2 basiert auf der Bildliste 2 (ahim \[ 2 \] ) mit einem Index von 1.</span><span class="sxs-lookup"><span data-stu-id="21f9c-139">Button 2 is from image list two (ahim\[2\]) with an index of 1.</span></span>
-   <span data-ttu-id="21f9c-140">Schaltfläche 3 ist von Image List Zero (ahim \[ 0 \] ) mit einem Index von 2.</span><span class="sxs-lookup"><span data-stu-id="21f9c-140">Button 3 is from image list zero (ahim\[0\]) with an index of 2.</span></span>
-   <span data-ttu-id="21f9c-141">Schaltfläche 4 basiert auf der Bildliste 1 (ahim \[ 1 \] ) mit einem Index von 3.</span><span class="sxs-lookup"><span data-stu-id="21f9c-141">Button 4 is from image list one (ahim\[1\]) with an index of 3.</span></span>

<span data-ttu-id="21f9c-142">Zum Schluss werden dem Symbolleisten-Steuerelement mit einer [**TB- \_ AddButtons**](tb-addbuttons.md) -Meldung die Schaltflächen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="21f9c-142">Finally, the buttons are added to the toolbar control with a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>


```
//Enable multiple image lists
    SendMessage(hwndTB, CCM_SETVERSION, (WPARAM) 5, 0); 

    //Set the image lists and assign them IDs of 0-2
    SendMessage(hwndTB, TB_SETIMAGELIST, 0, (LPARAM)ahiml[0]);
    SendMessage(hwndTB, TB_SETIMAGELIST, 1, (LPARAM)ahiml[1]);
    SendMessage(hwndTB, TB_SETIMAGELIST, 2, (LPARAM)ahiml[2]);

    // Create the five buttons
    TBBUTTON rgtb[5];
    
    //... initialize the TBBUTTON structures as usual ...
    
    //Assign images to each button
    rgtb[0].iBitmap = MAKELONG(1, 0);
    rgtb[1].iBitmap = MAKELONG(1, 1);
    rgtb[2].iBitmap = MAKELONG(1, 2);
    rgtb[3].iBitmap = MAKELONG(2, 0);
    rgtb[4].iBitmap = MAKELONG(3, 1);

    // Add the five buttons to the toolbar control
    SendMessage(hwndTB, TB_ADDBUTTONS, 5, (LPARAM)(&rgtb);
```



## <a name="requirements"></a><span data-ttu-id="21f9c-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21f9c-143">Requirements</span></span>



| <span data-ttu-id="21f9c-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21f9c-144">Requirement</span></span> | <span data-ttu-id="21f9c-145">Wert</span><span class="sxs-lookup"><span data-stu-id="21f9c-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21f9c-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21f9c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="21f9c-147">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21f9c-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="21f9c-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21f9c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="21f9c-149">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21f9c-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="21f9c-150">Header</span><span class="sxs-lookup"><span data-stu-id="21f9c-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="21f9c-151"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="21f9c-151"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21f9c-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21f9c-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="21f9c-153">[**Makelong**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="21f9c-153">[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span></span>
</dt> </dl>

 

