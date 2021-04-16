---
title: LVN_INSERTITEM Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass ein neues Element eingefügt wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 8d368fb2-e4fc-4dc4-a89e-872ba1278b75
keywords:
- Windows-Steuerelemente für LVN_INSERTITEM Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba70ba806dea2725385badee4b5c57e927a9d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479439"
---
# <a name="lvn_insertitem-notification-code"></a><span data-ttu-id="ab6a8-105">LVN \_ InsertItem-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="ab6a8-105">LVN\_INSERTITEM notification code</span></span>

<span data-ttu-id="ab6a8-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass ein neues Element eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-106">Notifies a list-view control's parent window that a new item was inserted.</span></span> <span data-ttu-id="ab6a8-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_INSERTITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ab6a8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab6a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab6a8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ab6a8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab6a8-110">Zeiger auf eine [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="ab6a8-111">Der **iItem** -Member identifiziert das neue Element, und die anderen Elemente sind 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ab6a8-111">The **iItem** member identifies the new item, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab6a8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab6a8-112">Return value</span></span>

<span data-ttu-id="ab6a8-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="ab6a8-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab6a8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab6a8-114">Requirements</span></span>



| <span data-ttu-id="ab6a8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab6a8-115">Requirement</span></span> | <span data-ttu-id="ab6a8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ab6a8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ab6a8-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab6a8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ab6a8-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab6a8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ab6a8-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab6a8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ab6a8-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab6a8-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ab6a8-121">Header</span><span class="sxs-lookup"><span data-stu-id="ab6a8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab6a8-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab6a8-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





