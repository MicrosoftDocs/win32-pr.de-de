---
title: LVN_ITEMCHANGING Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass sich ein Element ändert. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ed6b5fc2-7e8c-4392-aa39-498b18922a98
keywords:
- Windows-Steuerelemente für LVN_ITEMCHANGING Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6183cd218792a34276db75dce5953189a8118674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957260"
---
# <a name="lvn_itemchanging-notification-code"></a><span data-ttu-id="258d1-105">LVN \_ ItemChanging-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="258d1-105">LVN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="258d1-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass sich ein Element ändert.</span><span class="sxs-lookup"><span data-stu-id="258d1-106">Notifies a list-view control's parent window that an item is changing.</span></span> <span data-ttu-id="258d1-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="258d1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMCHANGING

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="258d1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="258d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="258d1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="258d1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="258d1-110">Ein Zeiger auf eine [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur, die das Element identifiziert und angibt, welche seiner Attribute geändert werden.</span><span class="sxs-lookup"><span data-stu-id="258d1-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that identifies the item and specifies which of its attributes are changing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="258d1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="258d1-111">Return value</span></span>

<span data-ttu-id="258d1-112">Gibt **true** zurück, um die Änderung zu verhindern, oder **false** , um die Änderung zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="258d1-112">Returns **TRUE** to prevent the change, or **FALSE** to allow the change.</span></span>

## <a name="remarks"></a><span data-ttu-id="258d1-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="258d1-113">Remarks</span></span>

<span data-ttu-id="258d1-114">Wenn das Listenansicht-Steuerelement den [**LVS \_**](list-view-window-styles.md) -Besitzer Daten Stil hat, \_ werden keine LVN-ItemChanging-Benachrichtigungs Codes gesendet.</span><span class="sxs-lookup"><span data-stu-id="258d1-114">If the list-view control has the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, LVN\_ITEMCHANGING notification codes are not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="258d1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="258d1-115">Requirements</span></span>



| <span data-ttu-id="258d1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="258d1-116">Requirement</span></span> | <span data-ttu-id="258d1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="258d1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="258d1-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="258d1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="258d1-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="258d1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="258d1-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="258d1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="258d1-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="258d1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="258d1-122">Header</span><span class="sxs-lookup"><span data-stu-id="258d1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="258d1-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="258d1-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





