---
title: LVN_ITEMACTIVATE Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Listenansicht-Steuerelement gesendet, wenn der Benutzer ein Element aktiviert. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- Windows-Steuerelemente für LVN_ITEMACTIVATE Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_ITEMACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9f139559b03fd82ac655381972803a288f00db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106665"
---
# <a name="lvn_itemactivate-notification-code"></a><span data-ttu-id="8f55b-105">LVN \_ itemaktivierungs-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="8f55b-105">LVN\_ITEMACTIVATE notification code</span></span>

<span data-ttu-id="8f55b-106">Wird von einem Listenansicht-Steuerelement gesendet, wenn der Benutzer ein Element aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8f55b-106">Sent by a list-view control when the user activates an item.</span></span> <span data-ttu-id="8f55b-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="8f55b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMACTIVATE

#if (_WIN32_IE >= 0x0400)
    lpnmia = (LPNMITEMACTIVATE)lParam;
#else
    lpnm = (LPNMHDR)lParam;
#endif
```



## <a name="parameters"></a><span data-ttu-id="8f55b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f55b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f55b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f55b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f55b-110">[Version 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="8f55b-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="8f55b-111">Zeiger auf eine [**nmitemaktivierungs**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="8f55b-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains information about this notification code.</span></span>

<span data-ttu-id="8f55b-112">[Version 4,70](common-control-versions.md) und früher.</span><span class="sxs-lookup"><span data-stu-id="8f55b-112">[Version 4.70](common-control-versions.md) and earlier.</span></span> <span data-ttu-id="8f55b-113">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="8f55b-113">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f55b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f55b-114">Return value</span></span>

<span data-ttu-id="8f55b-115">Die Anwendung, die diesen Benachrichtigungs Code empfängt, muss NULL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8f55b-115">The application receiving this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f55b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f55b-116">Remarks</span></span>

<span data-ttu-id="8f55b-117">Zum Abrufen der zu aktivierenden Elemente sollte die empfangende Anwendung die [**LVM- \_ getselectedcount**](lvm-getselectedcount.md) -Nachricht verwenden, um die Anzahl der ausgewählten Elemente abzurufen, und dann die [**LVM- \_ GetNextItem**](lvm-getnextitem.md) -Nachricht mit dem **\_ ausgewählten "lvni** " senden, bis alle Elemente abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="8f55b-117">To obtain the items being activated, the receiving application should use the [**LVM\_GETSELECTEDCOUNT**](lvm-getselectedcount.md) message to retrieve the number of items that are selected and then send the [**LVM\_GETNEXTITEM**](lvm-getnextitem.md) message with **LVNI\_SELECTED** until all of the items have been retrieved.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f55b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f55b-118">Requirements</span></span>



| <span data-ttu-id="8f55b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f55b-119">Requirement</span></span> | <span data-ttu-id="8f55b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8f55b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f55b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f55b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8f55b-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f55b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8f55b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f55b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8f55b-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f55b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f55b-125">Header</span><span class="sxs-lookup"><span data-stu-id="8f55b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f55b-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f55b-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





