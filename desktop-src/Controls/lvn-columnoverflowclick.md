---
title: LVN_COLUMNOVERFLOWCLICK Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Listenansicht-Steuerelement gesendet, wenn auf seine Überlauf Schaltfläche geklickt wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 3d3bb7be-b598-450a-b829-a5aa5b1a0c5d
keywords:
- Windows-Steuerelemente für LVN_COLUMNOVERFLOWCLICK Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_COLUMNOVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7938d28be337f7255a9b84422fa090da5a494cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479447"
---
# <a name="lvn_columnoverflowclick-notification-code"></a><span data-ttu-id="29288-105">LVN \_ COLUMNOVERFLOWCLICK Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="29288-105">LVN\_COLUMNOVERFLOWCLICK notification code</span></span>

<span data-ttu-id="29288-106">Wird von einem Listenansicht-Steuerelement gesendet, wenn auf seine Überlauf Schaltfläche geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="29288-106">Sent by a list-view control when its overflow button is clicked.</span></span> <span data-ttu-id="29288-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="29288-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_COLUMNOVERFLOWCLICK
     
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="29288-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="29288-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29288-109">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29288-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29288-110">Zeiger auf eine [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur, die den Benachrichtigungs Code beschreibt.</span><span class="sxs-lookup"><span data-stu-id="29288-110">Pointer to a [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that describes the notification code.</span></span> <span data-ttu-id="29288-111">Der Aufrufer ist dafür verantwortlich, diese Struktur zuzuordnen, einschließlich der enthaltenen [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="29288-111">The caller is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span> <span data-ttu-id="29288-112">Legen Sie die Member der **NMHDR** -Struktur fest.</span><span class="sxs-lookup"><span data-stu-id="29288-112">Set the members of the **NMHDR** structure.</span></span> <span data-ttu-id="29288-113">Der **Codemember** muss auf LVN COLUMNOVERFLOWCLICK festgelegt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="29288-113">The **code** member must be set to LVN\_COLUMNOVERFLOWCLICK.</span></span>

<span data-ttu-id="29288-114">Legen Sie den **iItem** -Member der [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur auf-1 fest.</span><span class="sxs-lookup"><span data-stu-id="29288-114">Set the **iItem** member of the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure to -1.</span></span> <span data-ttu-id="29288-115">Legen Sie den **iSubItem** -Member auf den Index des unter Elements fest.</span><span class="sxs-lookup"><span data-stu-id="29288-115">Set the **iSubItem** member to the index of the subitem.</span></span> <span data-ttu-id="29288-116">Legen Sie die Member **unewstate**, **uoldstate** und **LPARAM** auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="29288-116">Set the **uNewState**, **uOldState**, and **lParam** members to zero.</span></span> <span data-ttu-id="29288-117">Die übrigen Member der **NMLISTVIEW** -Struktur werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="29288-117">The remaining members of the **NMLISTVIEW** structure are not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29288-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29288-118">Return value</span></span>

<span data-ttu-id="29288-119">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="29288-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29288-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29288-120">Remarks</span></span>

<span data-ttu-id="29288-121">Der Benachrichtigungs Empfänger wandelt *LPARAM* ein, um die [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur abzurufen.</span><span class="sxs-lookup"><span data-stu-id="29288-121">The notification receiver casts *lParam* to retrieve the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="29288-122">Der *wParam* -Parameter enthält die ID des Steuer Elements, das den Benachrichtigungs Code sendet.</span><span class="sxs-lookup"><span data-stu-id="29288-122">The *wParam* parameter contains the ID of the control that sends the notification code.</span></span>

<span data-ttu-id="29288-123">Wenn ein Header Steuerelement ein untergeordnetes Element von ListView ist, sollte das Header Steuerelement diesen Benachrichtigungs Code an das ListView-Steuerelement senden, wenn das Header-Steuerelement den Hdn-Benachrichtigungs Code für den [ \_ Überlauf](hdn-overflowclick.md) Befehl empfängt.</span><span class="sxs-lookup"><span data-stu-id="29288-123">If a header control is a child of the listview, the header control should send this notification code to the listview control when the header control receives the [HDN\_OVERFLOWCLICK](hdn-overflowclick.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="29288-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29288-124">Requirements</span></span>



| <span data-ttu-id="29288-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29288-125">Requirement</span></span> | <span data-ttu-id="29288-126">Wert</span><span class="sxs-lookup"><span data-stu-id="29288-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29288-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29288-127">Minimum supported client</span></span><br/> | <span data-ttu-id="29288-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29288-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="29288-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29288-129">Minimum supported server</span></span><br/> | <span data-ttu-id="29288-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29288-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="29288-131">Header</span><span class="sxs-lookup"><span data-stu-id="29288-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="29288-132"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="29288-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





