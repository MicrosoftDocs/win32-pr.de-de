---
title: TB_SETPRESSEDIMAGELIST Meldung (kommstrg. h)
description: Legt die Bildliste fest, die von der Symbolleiste zum Anzeigen von Schaltflächen mit gedrücktem Zustand verwendet wird.
ms.assetid: d0e061ec-3a89-4c2d-b7f7-5f2061098428
keywords:
- Windows-Steuerelemente für TB_SETPRESSEDIMAGELIST Meldung
topic_type:
- apiref
api_name:
- TB_SETPRESSEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a3c6dafed6dbfdf2a654f4f95f1cef636ba762
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519303"
---
# <a name="tb_setpressedimagelist-message"></a><span data-ttu-id="f77b9-104">TB \_ setpressedimagelist-Meldung</span><span class="sxs-lookup"><span data-stu-id="f77b9-104">TB\_SETPRESSEDIMAGELIST message</span></span>

<span data-ttu-id="f77b9-105">Legt die Bildliste fest, die von der Symbolleiste zum Anzeigen von Schaltflächen mit gedrücktem Zustand verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f77b9-105">Sets the image list that the toolbar uses to display buttons that are in a pressed state.</span></span>

## <a name="parameters"></a><span data-ttu-id="f77b9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f77b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f77b9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f77b9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f77b9-108">Der Index der Bildliste.</span><span class="sxs-lookup"><span data-stu-id="f77b9-108">The index of the image list.</span></span> <span data-ttu-id="f77b9-109">Wenn Sie nur eine Bildliste verwenden, legen Sie diesen Parameter auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="f77b9-109">If you use only one image list, set this parameter to zero.</span></span> <span data-ttu-id="f77b9-110">Weitere Informationen zur Verwendung mehrerer Bildlisten finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="f77b9-110">See Remarks for details on using multiple image lists.</span></span>

</dd> <dt>

<span data-ttu-id="f77b9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f77b9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f77b9-112">Handle für die festzulegende Bildliste.</span><span class="sxs-lookup"><span data-stu-id="f77b9-112">Handle to the image list to set.</span></span> <span data-ttu-id="f77b9-113">Wenn dieser Parameter **null** ist, werden keine Bilder in den Schaltflächen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f77b9-113">If this parameter is **NULL**, no images are displayed in the buttons.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f77b9-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f77b9-114">Return value</span></span>

<span data-ttu-id="f77b9-115">Gibt das Handle für die Bildliste zurück, die zuvor zum Anzeigen von Schaltflächen im gedrückten Zustand verwendet wurde, oder **null** , wenn zuvor keine solche Bildliste festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="f77b9-115">Returns the handle to the image list previously used to display buttons in their pressed state, or **NULL** if no such image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="f77b9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f77b9-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f77b9-117">Die Anwendung ist dafür verantwortlich, die Bildliste freizugeben, nachdem die Symbolleiste zerstört wurde.</span><span class="sxs-lookup"><span data-stu-id="f77b9-117">Your application is responsible for freeing the image list after the toolbar is destroyed.</span></span>

 

<span data-ttu-id="f77b9-118">Die **TB- \_ setpressedimagelist** -Nachricht kann nicht mit [**TB \_ AddBitmap**](tb-addbitmap.md)kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="f77b9-118">The **TB\_SETPRESSEDIMAGELIST** message cannot be combined with [**TB\_ADDBITMAP**](tb-addbitmap.md).</span></span> <span data-ttu-id="f77b9-119">Sie kann auch nicht mit Symbolleisten verwendet werden, die mit " [**kreatetoolbarex**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex)" erstellt wurden, wodurch " **TB \_ AddBitmap** " intern aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f77b9-119">It also cannot be used with toolbars created with [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), which calls **TB\_ADDBITMAP** internally.</span></span> <span data-ttu-id="f77b9-120">Wenn Sie eine Symbolleiste mit " **kreatetoolbarex** " erstellen oder zum Hinzufügen von Bildern " **TB \_ AddBitmap** " verwenden, wird die Bildliste von der Symbolleiste intern verwaltet.</span><span class="sxs-lookup"><span data-stu-id="f77b9-120">When you create a toolbar with **CreateToolbarEx** or use **TB\_ADDBITMAP** to add images, the toolbar manages the image list internally.</span></span> <span data-ttu-id="f77b9-121">Der Versuch, ihn mit **TB \_ setpressedimagelist** zu ändern, hat unvorhersehbare Konsequenzen.</span><span class="sxs-lookup"><span data-stu-id="f77b9-121">Attempting to modify it with **TB\_SETPRESSEDIMAGELIST** has unpredictable consequences.</span></span>

<span data-ttu-id="f77b9-122">Schaltflächen Bilder müssen nicht aus derselben Bildliste stammen.</span><span class="sxs-lookup"><span data-stu-id="f77b9-122">Button images need not come from the same image list.</span></span> <span data-ttu-id="f77b9-123">So verwenden Sie mehrere Bildlisten für Ihre Symbolleisten-Schaltflächen Bilder:</span><span class="sxs-lookup"><span data-stu-id="f77b9-123">To use multiple image lists for your toolbar button images:</span></span>

1.  <span data-ttu-id="f77b9-124">Aktivieren Sie mehrere Bildlisten, indem Sie das Symbolleisten-Steuerelement eine [**ccm- \_ setVersion**](ccm-setversion.md) -Nachricht mit *wParam* (Versionsnummer) an 5 senden.</span><span class="sxs-lookup"><span data-stu-id="f77b9-124">Enable multiple image lists by sending the toolbar control a [**CCM\_SETVERSION**](ccm-setversion.md) message with *wParam* (the version number) set to 5.</span></span>
2.  <span data-ttu-id="f77b9-125">Für jede Bildliste, die Sie verwenden möchten, senden Sie das Symbolleisten-Steuerelement an eine **TB- \_ setpressedimagelist** -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="f77b9-125">For each image list you want to use, send the toolbar control a **TB\_SETPRESSEDIMAGELIST** message.</span></span> <span data-ttu-id="f77b9-126">Legen Sie *wParam* auf einen von der Anwendung definierten *wParam* -Wert fest, der verwendet wird, um die Liste zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f77b9-126">Set *wParam* to an application-defined *wParam* value that will be used to identify the list.</span></span> <span data-ttu-id="f77b9-127">Legen Sie *LPARAM* auf das HIMAGELIST-Handle der Liste fest.</span><span class="sxs-lookup"><span data-stu-id="f77b9-127">Set *lParam* to the list's HIMAGELIST handle.</span></span>
3.  <span data-ttu-id="f77b9-128">Legen Sie für jede Schaltfläche den **ibitmap** -Member der [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur der Schaltfläche auf makelong (*iIndex*, *iimageid*) fest.</span><span class="sxs-lookup"><span data-stu-id="f77b9-128">For each button, set the **iBitmap** member of the button's [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure to MAKELONG(*iIndex*, *iImageID*).</span></span> <span data-ttu-id="f77b9-129">Der *iimageid* -Wert ist die ID der entsprechenden Bildliste, die in Schritt 2 definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f77b9-129">The *iImageID* value is the ID of the appropriate image list that was defined in step two.</span></span> <span data-ttu-id="f77b9-130">Der *iIndex* -Wert ist der Index des jeweiligen Bilds in dieser Liste.</span><span class="sxs-lookup"><span data-stu-id="f77b9-130">The *iIndex* value is the index of the particular image within that list.</span></span>
4.  <span data-ttu-id="f77b9-131">Fügen Sie die Schaltflächen hinzu, indem Sie das Symbolleisten-Steuerelement an eine [**TB- \_ AddButtons**](tb-addbuttons.md)</span><span class="sxs-lookup"><span data-stu-id="f77b9-131">Add the buttons by sending the toolbar control a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>

<span data-ttu-id="f77b9-132">Im folgenden Code Fragment wird veranschaulicht, wie einer Symbolleiste mit Bildern aus drei verschiedenen Bildlisten fünf Schaltflächen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f77b9-132">The following code fragment illustrates how to add five buttons to a toolbar, with images from three different image lists.</span></span> <span data-ttu-id="f77b9-133">Die Unterstützung für mehrere Bildlisten wird mit einer [**ccm- \_ setVersion**](ccm-setversion.md) -Nachricht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f77b9-133">Support for multiple image lists is enabled with a [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span> <span data-ttu-id="f77b9-134">Anschließend werden die Bildlisten und die zugewiesenen IDs 0-2 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f77b9-134">The image lists are then set and assigned IDs of 0-2.</span></span> <span data-ttu-id="f77b9-135">Den Schaltflächen werden Bilder aus den Bildlisten wie folgt zugewiesen:</span><span class="sxs-lookup"><span data-stu-id="f77b9-135">The buttons are assigned images from the image lists as follows:</span></span>

-   <span data-ttu-id="f77b9-136">Die Schaltfläche 0 ist aus der Bildliste NULL (ahim \[ 0 \] ) mit dem Index 1.</span><span class="sxs-lookup"><span data-stu-id="f77b9-136">Button 0 is from image list zero (ahim\[0\]) with index of 1.</span></span>
-   <span data-ttu-id="f77b9-137">Schaltfläche 1 ist von der Bildliste 1 (ahim \[ 1 \] ) mit dem Index 1.</span><span class="sxs-lookup"><span data-stu-id="f77b9-137">Button 1 is from image list one (ahim\[1\]) with an index of 1.</span></span>
-   <span data-ttu-id="f77b9-138">Schaltfläche 2 basiert auf der Bildliste 2 (ahim \[ 2 \] ) mit einem Index von 1.</span><span class="sxs-lookup"><span data-stu-id="f77b9-138">Button 2 is from image list two (ahim\[2\]) with an index of 1.</span></span>
-   <span data-ttu-id="f77b9-139">Schaltfläche 3 ist von Image List Zero (ahim \[ 0 \] ) mit einem Index von 2.</span><span class="sxs-lookup"><span data-stu-id="f77b9-139">Button 3 is from image list zero (ahim\[0\]) with an index of 2.</span></span>
-   <span data-ttu-id="f77b9-140">Schaltfläche 4 basiert auf der Bildliste 1 (ahim \[ 1 \] ) mit einem Index von 3.</span><span class="sxs-lookup"><span data-stu-id="f77b9-140">Button 4 is from image list one (ahim\[1\]) with an index of 3.</span></span>

<span data-ttu-id="f77b9-141">Zum Schluss werden dem Symbolleisten-Steuerelement mit einer [**TB- \_ AddButtons**](tb-addbuttons.md) -Meldung die Schaltflächen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f77b9-141">Finally, the buttons are added to the toolbar control with a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>


```
// Enable multiple image lists
    SendMessage(hwndTB, CCM_SETVERSION, (WPARAM) 5, 0); 

    //Set the image lists and assign them IDs of 0-2
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 0, (LPARAM)ahiml[0]);
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 1, (LPARAM)ahiml[1]);
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 2, (LPARAM)ahiml[2]);

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



## <a name="requirements"></a><span data-ttu-id="f77b9-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f77b9-142">Requirements</span></span>



| <span data-ttu-id="f77b9-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f77b9-143">Requirement</span></span> | <span data-ttu-id="f77b9-144">Wert</span><span class="sxs-lookup"><span data-stu-id="f77b9-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f77b9-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f77b9-145">Minimum supported client</span></span><br/> | <span data-ttu-id="f77b9-146">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f77b9-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f77b9-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f77b9-147">Minimum supported server</span></span><br/> | <span data-ttu-id="f77b9-148">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f77b9-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f77b9-149">Header</span><span class="sxs-lookup"><span data-stu-id="f77b9-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="f77b9-150"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f77b9-150"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f77b9-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f77b9-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="f77b9-152">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f77b9-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f77b9-153">**TB \_ getpressedimagelist**</span><span class="sxs-lookup"><span data-stu-id="f77b9-153">**TB\_GETPRESSEDIMAGELIST**</span></span>](tb-getpressedimagelist.md)
</dt> <dt>

<span data-ttu-id="f77b9-154">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="f77b9-154">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="f77b9-155">[**Makelong**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f77b9-155">[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span></span>
</dt> </dl>

 

