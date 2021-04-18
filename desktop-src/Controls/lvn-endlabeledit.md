---
title: LVN_ENDLABELEDIT Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements über das Ende der Bezeichnungs Bearbeitung für ein Element. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 03129fef-abf1-4374-b4b8-503c46ef7115
keywords:
- Windows-Steuerelemente für LVN_ENDLABELEDIT Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_ENDLABELEDIT
- LVN_ENDLABELEDITA
- LVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a33ab69a04202aeb3817d3eeadf01fb6f1fcaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341044"
---
# <a name="lvn_endlabeledit-notification-code"></a><span data-ttu-id="a4578-105">LVN \_ endlabeledit-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="a4578-105">LVN\_ENDLABELEDIT notification code</span></span>

<span data-ttu-id="a4578-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements über das Ende der Bezeichnungs Bearbeitung für ein Element.</span><span class="sxs-lookup"><span data-stu-id="a4578-106">Notifies a list-view control's parent window about the end of label editing for an item.</span></span> <span data-ttu-id="a4578-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="a4578-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ENDLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a4578-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4578-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4578-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a4578-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4578-110">Zeiger auf eine [**nmlvdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a4578-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="a4578-111">Das **Element Element** dieser Struktur ist eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur, deren **iItem** -Member das Element identifiziert, das bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="a4578-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure whose **iItem** member identifies the item being edited.</span></span> <span data-ttu-id="a4578-112">Der **pszText** -Member des **Elements** enthält einen gültigen Wert, wenn der LVN \_ endlabeledit-Benachrichtigungs Code gesendet wird, unabhängig davon, ob das lvif- \_ textflag im **Mask** -Member der **lvitem** -Struktur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a4578-112">The **pszText** member of **item** contains a valid value when the LVN\_ENDLABELEDIT notification code is sent, regardless of whether the LVIF\_TEXT flag is set in the **mask** member of the **LVITEM** structure.</span></span> <span data-ttu-id="a4578-113">Wenn der Benutzer die Bearbeitung abbricht, ist der **pszText** -Member der **lvitem** -Struktur **null**. Andernfalls ist **pszText** die Adresse des bearbeiteten Texts.</span><span class="sxs-lookup"><span data-stu-id="a4578-113">If the user cancels editing, the **pszText** member of the **LVITEM** structure is **NULL**; otherwise, **pszText** is the address of the edited text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4578-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4578-114">Return value</span></span>

<span data-ttu-id="a4578-115">Wenn der **pszText** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur nicht **null** ist, wird **true** zurückgegeben, um die Bezeichnung des Elements auf den bearbeiteten Text festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a4578-115">If the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure is non-**NULL**, return **TRUE** to set the item's label to the edited text.</span></span> <span data-ttu-id="a4578-116">Gibt **false** zurück, um den bearbeiteten Text abzulehnen und zur ursprünglichen Bezeichnung zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="a4578-116">Return **FALSE** to reject the edited text and revert to the original label.</span></span>

<span data-ttu-id="a4578-117">Wenn der **pszText** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur **null** ist, wird der Rückgabewert ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a4578-117">If the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure is **NULL**, the return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4578-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4578-118">Remarks</span></span>

<span data-ttu-id="a4578-119">Der Rückgabewert der Dialogfeld Prozedur ist, ob die Nachricht behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="a4578-119">The return value of the dialog procedure is whether the message was handled.</span></span> <span data-ttu-id="a4578-120">Der zweite Rückgabewert muss festgelegt werden, indem [**setwindowlongptr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) mit **DWLP_MSGRESULT** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a4578-120">The second return value must be set by calling [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) with **DWLP_MSGRESULT**.</span></span>

<span data-ttu-id="a4578-121">Wenn der Benutzer mit dem Bearbeiten einer Element Bezeichnung beginnt, empfängt das übergeordnete Fenster des Listenansicht-Steuer Elements einen [LVN \_ beginlabeledit](lvn-beginlabeledit.md) -Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="a4578-121">When the user begins editing an item label, the parent window of the list-view control receives an [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) notification code.</span></span> <span data-ttu-id="a4578-122">Wenn der Benutzer die Bearbeitung abbricht oder abschließt, empfängt das übergeordnete Fenster einen LVN \_ endlabeledit-Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="a4578-122">When the user cancels or completes the editing, the parent window receives an LVN\_ENDLABELEDIT notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4578-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4578-123">Requirements</span></span>



| <span data-ttu-id="a4578-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4578-124">Requirement</span></span> | <span data-ttu-id="a4578-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a4578-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4578-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4578-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a4578-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4578-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a4578-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4578-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a4578-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4578-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a4578-130">Header</span><span class="sxs-lookup"><span data-stu-id="a4578-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4578-131"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4578-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a4578-132">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="a4578-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a4578-133">**LVN \_ Endlabeleditw** (Unicode) und **LVN \_ endlabeledita** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a4578-133">**LVN\_ENDLABELEDITW** (Unicode) and **LVN\_ENDLABELEDITA** (ANSI)</span></span><br/>         |



 

 





