---
title: LVN_SETDISPINFO Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass die Informationen, die für ein Element verwaltet werden, aktualisiert werden müssen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 1ea51d50-4a57-4662-972e-89e916fa9b16
keywords:
- Windows-Steuerelemente für LVN_SETDISPINFO Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_SETDISPINFO
- LVN_SETDISPINFOA
- LVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659623d892f0f5a556f4890703d4e0dd725536b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956820"
---
# <a name="lvn_setdispinfo-notification-code"></a><span data-ttu-id="2b8fd-105">LVN \_ setdispinfo-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="2b8fd-105">LVN\_SETDISPINFO notification code</span></span>

<span data-ttu-id="2b8fd-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass die Informationen, die für ein Element verwaltet werden, aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2b8fd-106">Notifies a list-view control's parent window that it must update the information it maintains for an item.</span></span> <span data-ttu-id="2b8fd-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="2b8fd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_SETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a><span data-ttu-id="2b8fd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b8fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b8fd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b8fd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b8fd-110">Ein Zeiger auf eine [**nmlvdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) -Struktur, die Informationen für das geänderte Element angibt.</span><span class="sxs-lookup"><span data-stu-id="2b8fd-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure that specifies information for the changed item.</span></span> <span data-ttu-id="2b8fd-111">Das **Element Element** dieser Struktur ist eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur, die Informationen über das geänderte Element enthält.</span><span class="sxs-lookup"><span data-stu-id="2b8fd-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that contains information about the item that was changed.</span></span> <span data-ttu-id="2b8fd-112">Der **pszText** -Member des **Elements** enthält einen gültigen Wert, unabhängig davon, ob das lvif- \_ textflag im **Mask** -Member dieser Struktur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2b8fd-112">The **pszText** member of **item** contains a valid value, regardless of whether the LVIF\_TEXT flag is set in the **mask** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b8fd-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b8fd-113">Return value</span></span>

<span data-ttu-id="2b8fd-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="2b8fd-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b8fd-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b8fd-115">Remarks</span></span>

<span data-ttu-id="2b8fd-116">Der Benachrichtigungs Empfänger wandelt *LPARAM* ein, um die [**nmlvdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) -Struktur abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2b8fd-116">The notification receiver casts *lParam* to retrieve the [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="2b8fd-117">Der *wParam* -Parameter enthält den Nachrichten Code.</span><span class="sxs-lookup"><span data-stu-id="2b8fd-117">The *wParam* parameter contains the message code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b8fd-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b8fd-118">Requirements</span></span>



| <span data-ttu-id="2b8fd-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b8fd-119">Requirement</span></span> | <span data-ttu-id="2b8fd-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2b8fd-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b8fd-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b8fd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2b8fd-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b8fd-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2b8fd-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b8fd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2b8fd-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b8fd-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b8fd-125">Header</span><span class="sxs-lookup"><span data-stu-id="2b8fd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b8fd-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b8fd-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="2b8fd-127">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="2b8fd-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2b8fd-128">**LVN \_ Setdispinfow** (Unicode) und **LVN \_ setdispinfoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2b8fd-128">**LVN\_SETDISPINFOW** (Unicode) and **LVN\_SETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="2b8fd-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b8fd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b8fd-130">LVN \_ getdispinfo</span><span class="sxs-lookup"><span data-stu-id="2b8fd-130">LVN\_GETDISPINFO</span></span>](lvn-getdispinfo.md)
</dt> </dl>

 

 





