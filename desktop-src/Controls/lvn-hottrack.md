---
title: LVN_HOTTRACK Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Listenansicht-Steuerelement gesendet, wenn der Benutzer die Maus über ein Element bewegt. Dieser Benachrichtigungs Code wird nur von Listenansicht-Steuerelementen gesendet, die über den erweiterten LVS \_ Ex \_ trackselect-Listen Ansichts Stil verfügen. Sie wird in Form einer WM- \_ Benachrichtigungs Meldung gesendet.
ms.assetid: 6bbfe6b8-9b67-49e4-9481-65abe98608bb
keywords:
- Windows-Steuerelemente für LVN_HOTTRACK Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_HOTTRACK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c677b69fa21cdbe3680442304f6745cfb3a907de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859345"
---
# <a name="lvn_hottrack-notification-code"></a><span data-ttu-id="a1e46-106">LVN \_ HotTrack-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="a1e46-106">LVN\_HOTTRACK notification code</span></span>

<span data-ttu-id="a1e46-107">Wird von einem Listenansicht-Steuerelement gesendet, wenn der Benutzer die Maus über ein Element bewegt.</span><span class="sxs-lookup"><span data-stu-id="a1e46-107">Sent by a list-view control when the user moves the mouse over an item.</span></span> <span data-ttu-id="a1e46-108">Dieser Benachrichtigungs Code wird nur von Listenansicht-Steuerelementen gesendet, die über den erweiterten [**LVS \_ Ex \_ trackselect**](extended-list-view-styles.md) -Listen Ansichts Stil verfügen.</span><span class="sxs-lookup"><span data-stu-id="a1e46-108">This notification code is only sent by list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) extended list-view style.</span></span> <span data-ttu-id="a1e46-109">Sie wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="a1e46-109">It is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_HOTTRACK

    lpnmlv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a1e46-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1e46-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1e46-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1e46-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e46-112">Zeiger auf eine [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="a1e46-112">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that contains information about this notification code.</span></span> <span data-ttu-id="a1e46-113">Die Member **iItem**, **iSubItem** und **ptaction** dieser Struktur enthalten Informationen über das Element.</span><span class="sxs-lookup"><span data-stu-id="a1e46-113">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span> <span data-ttu-id="a1e46-114">Die empfangende Anwendung kann den **iItem** -Member ändern, um das Element anzugeben, das ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="a1e46-114">The receiving application can modify the **iItem** member to specify the item that will be selected.</span></span> <span data-ttu-id="a1e46-115">Wenn **iItem** auf-1 festgelegt ist, wird kein Element ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="a1e46-115">If **iItem** is set to -1, no item will be selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1e46-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1e46-116">Return value</span></span>

<span data-ttu-id="a1e46-117">0 (null) zurückgeben, damit die Listenansicht den normalen Track-Prozess ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="a1e46-117">Return zero to allow the list view to perform its normal track select processing.</span></span> <span data-ttu-id="a1e46-118">Wenn die Anwendung einen Wert ungleich 0 (null) zurückgibt, wird das Element nicht ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="a1e46-118">If the application returns nonzero, the item will not be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1e46-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1e46-119">Requirements</span></span>



| <span data-ttu-id="a1e46-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1e46-120">Requirement</span></span> | <span data-ttu-id="a1e46-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a1e46-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1e46-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1e46-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a1e46-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1e46-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a1e46-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1e46-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a1e46-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1e46-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a1e46-126">Header</span><span class="sxs-lookup"><span data-stu-id="a1e46-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1e46-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1e46-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





