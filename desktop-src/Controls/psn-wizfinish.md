---
title: PSN_WIZFINISH Benachrichtigungs Code (prsht. h)
description: Benachrichtigt eine Seite, dass der Benutzer in einem Assistenten auf die Schaltfläche Fertigstellen geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 8ef0a8a7-2d25-4969-9b8f-e42dcc1c8fb5
keywords:
- Windows-Steuerelemente für PSN_WIZFINISH Benachrichtigungs
topic_type:
- apiref
api_name:
- PSN_WIZFINISH
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0654384b0944d90731288922c32326e42019cdc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477892"
---
# <a name="psn_wizfinish-notification-code"></a><span data-ttu-id="1eb62-105">\_Benachrichtigungs Code für PSN-witzfinish</span><span class="sxs-lookup"><span data-stu-id="1eb62-105">PSN\_WIZFINISH notification code</span></span>

<span data-ttu-id="1eb62-106">Benachrichtigt eine Seite, dass der Benutzer in einem Assistenten auf die Schaltfläche **Fertig** stellen geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="1eb62-106">Notifies a page that the user has clicked the **Finish** button in a wizard.</span></span> <span data-ttu-id="1eb62-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="1eb62-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_WIZFINISH 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1eb62-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1eb62-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eb62-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1eb62-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1eb62-110">Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="1eb62-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="1eb62-111">Diese Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member dieser **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt.</span><span class="sxs-lookup"><span data-stu-id="1eb62-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="1eb62-112">Der **LPARAM** -Member der **pshnotify** -Struktur enthält keine Informationen.</span><span class="sxs-lookup"><span data-stu-id="1eb62-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eb62-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1eb62-113">Return value</span></span>

-   <span data-ttu-id="1eb62-114">Gibt **true** zurück, um zu verhindern, dass der Assistent abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="1eb62-114">Returns **TRUE** to prevent the wizard from finishing.</span></span>
-   [<span data-ttu-id="1eb62-115">Version 5,80.</span><span class="sxs-lookup"><span data-stu-id="1eb62-115">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="1eb62-116">und höher.</span><span class="sxs-lookup"><span data-stu-id="1eb62-116">and later.</span></span> <span data-ttu-id="1eb62-117">Gibt ein Fenster Handle zurück, um zu verhindern, dass der Assistent abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="1eb62-117">Returns a window handle to prevent the wizard from finishing.</span></span> <span data-ttu-id="1eb62-118">Der Fokus wird auf das Fenster festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1eb62-118">The wizard will set the focus to that window.</span></span> <span data-ttu-id="1eb62-119">Das Fenster muss im Besitz der Assistenten Seite sein.</span><span class="sxs-lookup"><span data-stu-id="1eb62-119">The window must be owned by the wizard page.</span></span>
-   <span data-ttu-id="1eb62-120">Gibt **false** zurück, damit der Assistent abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="1eb62-120">Returns **FALSE** to allow the wizard to finish.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eb62-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1eb62-121">Remarks</span></span>

<span data-ttu-id="1eb62-122">Um den Rückgabewert festzulegen, muss die Dialogfeld Prozedur für die Seite die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion mit dem DWL \_ msgresult-Wert verwenden, und die Dialogfeld Prozedur muss **true** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1eb62-122">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

[<span data-ttu-id="1eb62-123">Version 5,80.</span><span class="sxs-lookup"><span data-stu-id="1eb62-123">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="1eb62-124">Wenn die Anwendung **true** zurückgibt, um zu verhindern, dass ein Assistent beendet wird, hat Sie keine Kontrolle darüber, welches Fenster auf der Seite den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="1eb62-124">If your application returns **TRUE** to prevent a wizard from finishing, it has no control over which window on the page receives focus.</span></span> <span data-ttu-id="1eb62-125">Anwendungen, die den Abschluss eines Assistenten beenden müssen, sollten dies normalerweise tun, indem Sie das Fenster Handle auf der Assistenten Seite zurückgeben, das den Fokus erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="1eb62-125">Applications that need to stop a wizard from finishing should normally do so by returning the handle of the window on the wizard page that is to receive focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eb62-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1eb62-126">Requirements</span></span>



| <span data-ttu-id="1eb62-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1eb62-127">Requirement</span></span> | <span data-ttu-id="1eb62-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1eb62-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb62-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1eb62-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1eb62-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1eb62-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1eb62-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1eb62-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1eb62-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1eb62-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1eb62-133">Header</span><span class="sxs-lookup"><span data-stu-id="1eb62-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1eb62-134"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="1eb62-134"><dt>Prsht.h</dt></span></span> </dl> |



 

