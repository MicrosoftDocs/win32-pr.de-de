---
title: TVN_ASYNCDRAW Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Strukturansicht-Steuerelement an das übergeordnete Steuerelement gesendet, wenn beim Zeichnen eines Symbols oder Overlay ein Fehler aufgetreten ist. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 209bfffb-e57d-435d-98a1-8b117c4969b1
keywords:
- Windows-Steuerelemente für TVN_ASYNCDRAW Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_ASYNCDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a8b04db2e4efbd78d6176214ecd9088f1bc30c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344102"
---
# <a name="tvn_asyncdraw-notification-code"></a><span data-ttu-id="bfc97-105">TVN \_ asyncdraw-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="bfc97-105">TVN\_ASYNCDRAW notification code</span></span>

<span data-ttu-id="bfc97-106">Wird von einem Strukturansicht-Steuerelement an das übergeordnete Steuerelement gesendet, wenn beim Zeichnen eines Symbols oder Overlay ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="bfc97-106">Sent by a tree-view control to its parent when the drawing of a icon or overlay has failed.</span></span> <span data-ttu-id="bfc97-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="bfc97-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ASYNCDRAW
        
    pnmTVAsynchDraw =  (NMTVASYNCDRAW *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="bfc97-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfc97-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfc97-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bfc97-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfc97-110">Zeiger auf eine [**nmtvasyncdraw**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="bfc97-110">Pointer to an [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) structure.</span></span> <span data-ttu-id="bfc97-111">Die **nmtvasyncdraw** -Struktur enthält den Grund, warum das Zeichnen nicht ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="bfc97-111">The **NMTVASYNCDRAW** structure contains the reason the draw failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfc97-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bfc97-112">Return value</span></span>

<span data-ttu-id="bfc97-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="bfc97-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfc97-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfc97-114">Remarks</span></span>

<span data-ttu-id="bfc97-115">Das Strukturansicht-Steuerelement muss über den erweiterten Stil " [**TVs \_ Ex \_ drawimageasync**](tree-view-control-window-extended-styles.md) " verfügen.</span><span class="sxs-lookup"><span data-stu-id="bfc97-115">The tree-view control must have the [**TVS\_EX\_DRAWIMAGEASYNC**](tree-view-control-window-extended-styles.md) extended style.</span></span> <span data-ttu-id="bfc97-116">Beachten Sie, dass dies dem LVN-LVN-Flag von List-View \_ und dem zugehörigen Stil entspricht.</span><span class="sxs-lookup"><span data-stu-id="bfc97-116">Note that this is equivalent to list-view's LVN\_ASYNCDRAWN flag and its corresponding style.</span></span>

<span data-ttu-id="bfc97-117">Dieses Steuerelement wird nicht asynchron gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bfc97-117">This control does not draw asynchronously.</span></span> <span data-ttu-id="bfc97-118">Asynchronous wird in dem Kontext verwendet, in dem das Strukturansicht-Steuerelement ein Bild nicht synchron extrahiert, wenn es nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="bfc97-118">Asynchronous is used in the context that the tree-view control does not synchronously extract an image if it is not available.</span></span> <span data-ttu-id="bfc97-119">(Beispielsweise ist das Bild möglicherweise nicht verfügbar, wenn das Strukturansicht-Steuerelement eine Liste mit geringer Dichte verwendet, da das Bild möglicherweise entladen wird.) Wenn ein Bild nicht verfügbar ist, fragt das Steuerelement stattdessen das übergeordnete Element ab, welche Aktion ausgeführt werden soll, indem das übergeordnete Element eine TVN \_ asyncdraw-Benachrichtigung mit einer [**nmtvasyncdraw**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) -Struktur gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="bfc97-119">(For instance, the image may not be available if the tree-view control uses a sparse image list, since the image may be unloaded.) Instead, when an image is not available, the control synchronously asks the parent what action to take by sending the parent an TVN\_ASYNCDRAW notification with a [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) structure.</span></span> <span data-ttu-id="bfc97-120">Der **HR** -Member dieser Struktur beschreibt den Grund, warum das Zeichnen des Steuer Elements fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="bfc97-120">The **hr** member of this structure describes the reason the control's draw failed.</span></span> <span data-ttu-id="bfc97-121">Ein **HR** -Ergebnis von E \_ Pending bedeutet, dass das Image überhaupt nicht vorhanden ist (das Abbild muss extrahiert werden).</span><span class="sxs-lookup"><span data-stu-id="bfc97-121">An **hr** result of E\_PENDING means the image is not present at all (the image needs to be extracted).</span></span> <span data-ttu-id="bfc97-122">Erfolg gibt an, dass das Bild vorhanden ist, aber nicht die erforderliche Bildqualität.</span><span class="sxs-lookup"><span data-stu-id="bfc97-122">Success indicates that the image is present but not at the required image quality.</span></span>

<span data-ttu-id="bfc97-123">Das übergeordnete Element legt den **dwretflags** -Member der Struktur fest, um dem Steuerelement mitzuteilen, wie der Vorgang fortgesetzt wird</span><span class="sxs-lookup"><span data-stu-id="bfc97-123">The parent sets the **dwRetFlags** member of the structure to inform the control how to proceed.</span></span> <span data-ttu-id="bfc97-124">Beispielsweise kann das übergeordnete Element ein anderes Bild im **iretimageindex** -Member zurückgeben, damit das Steuerelement gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="bfc97-124">For instance, the parent may return another image, in the **iRetImageIndex** member, for the control to draw.</span></span> <span data-ttu-id="bfc97-125">In diesem Fall legt das übergeordnete Element den **dwretflags** -Member auf adrf \_ DrawImage fest.</span><span class="sxs-lookup"><span data-stu-id="bfc97-125">In this case, the parent sets the **dwRetFlags** member to ADRF\_DRAWIMAGE.</span></span> <span data-ttu-id="bfc97-126">Wenn das Steuerelement feststellt, dass das zurückgegebene Bild nicht extrahiert wurde, kann eine andere TVN- \_ asyncdraw-Benachrichtigung vom Steuerelement gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="bfc97-126">If the control finds the returned image has not been extracted, yet another TVN\_ASYNCDRAW notification may be sent by the control.</span></span>

<span data-ttu-id="bfc97-127">Wenn ein Bild nicht verfügbar ist, besteht die Idee hinter asynchronen darin, dass das übergeordnete Element die Extraktion im Hintergrund durchführen soll, damit der UI-Thread, d. h. der Thread, in dem sich das Steuerelement befindet, durch Extrahieren nicht blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="bfc97-127">If an image is not available, the idea behind asynchronous is to allow the parent do the extraction in the background so that extraction does not block the UI thread, that is, the thread the control is on.</span></span> <span data-ttu-id="bfc97-128">Das übergeordnete Element gibt möglicherweise adrf \_ drawnothing an das Steuerelement zurück und startet dann einen Hintergrund Thread, um das Symbol zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="bfc97-128">The parent may return ADRF\_DRAWNOTHING to the control, then launch a background thread to extract the icon.</span></span> <span data-ttu-id="bfc97-129">Nach dem extrahieren kann das übergeordnete Element das Symbol im TreeView-Steuerelement mit dem Makro [**TreeView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem)festlegen.</span><span class="sxs-lookup"><span data-stu-id="bfc97-129">Once extracted, the parent may set the icon in the treeview control with macro [**TreeView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem).</span></span> <span data-ttu-id="bfc97-130">Dies bewirkt, dass die Strukturansicht das Element für ungültig erklärt und es schließlich mit dem extrahierten Bild in der Bildliste neu zeichnet.</span><span class="sxs-lookup"><span data-stu-id="bfc97-130">This causes tree-view to invalidate the item and eventually repaint it with the extracted image in the image list.</span></span>

<span data-ttu-id="bfc97-131">Im folgenden Codebeispiel, das als Teil eines größeren Programms verwendet werden soll, wird veranschaulicht, wie ein übergeordnetes Element in dieser Benachrichtigung zwei mögliche Rückgabecodes von einem-Steuerelement verarbeiten kann und wie Sie entscheiden, welche Aktion das Steuerelement ausführen sollte.</span><span class="sxs-lookup"><span data-stu-id="bfc97-131">The following code example, to be used as part of a larger program, shows how a parent may process two possible return codes in this notification by a control, and decide what action the control should take.</span></span> <span data-ttu-id="bfc97-132">Das Festlegen von **dwretflags** wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bfc97-132">Setting **dwRetFlags** is not shown.</span></span>


```
case TVN_ASYNCDRAW:

   NMTVASYNCDRAW *pnm =  (NMTVASYNCDRAW *)lParam
   short dwDrawSuccessFlags = ShortFromResult(pnm->hr);

   if (dwDrawSuccessFlags & ILDRF_IMAGELOWQUALITY)
   {
        // Need to re-extract the icon
   }

   if (dwDrawSuccessFlags & ILDRF_OVERLAYLOWQUALITY)
   {
        // Need to re-extract the overlay
   }
```



## <a name="requirements"></a><span data-ttu-id="bfc97-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfc97-133">Requirements</span></span>



| <span data-ttu-id="bfc97-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfc97-134">Requirement</span></span> | <span data-ttu-id="bfc97-135">Wert</span><span class="sxs-lookup"><span data-stu-id="bfc97-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bfc97-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfc97-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bfc97-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfc97-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bfc97-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfc97-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bfc97-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfc97-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bfc97-140">Header</span><span class="sxs-lookup"><span data-stu-id="bfc97-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfc97-141"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfc97-141"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





