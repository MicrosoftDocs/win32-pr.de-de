---
title: TVN_ENDLABELEDIT Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements über das Ende der Bezeichnungs Bearbeitung für ein Element. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 82eb9fcd-de10-4efb-8501-78c5af5e089e
keywords:
- Windows-Steuerelemente für TVN_ENDLABELEDIT Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_ENDLABELEDIT
- TVN_ENDLABELEDITA
- TVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c30d494ad90b3d55f85b1ad154aed0f814a1eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103899"
---
# <a name="tvn_endlabeledit-notification-code"></a><span data-ttu-id="731dc-105">TVN \_ endlabeledit-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="731dc-105">TVN\_ENDLABELEDIT notification code</span></span>

<span data-ttu-id="731dc-106">Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements über das Ende der Bezeichnungs Bearbeitung für ein Element.</span><span class="sxs-lookup"><span data-stu-id="731dc-106">Notifies a tree-view control's parent window about the end of label editing for an item.</span></span> <span data-ttu-id="731dc-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="731dc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ENDLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="731dc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="731dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="731dc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="731dc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="731dc-110">Zeiger auf eine [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="731dc-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="731dc-111">Das **Element Element** dieser Struktur ist eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, deren **Hitem**-, **LPARAM**-und **pszText** -Member gültige Informationen über das Element enthalten, das bearbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="731dc-111">The **item** member of this structure is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **hItem**, **lParam**, and **pszText** members contain valid information about the item that was edited.</span></span> <span data-ttu-id="731dc-112">Wenn die Bezeichnungs Bearbeitung abgebrochen wurde, ist der **pszText** -Member der **tvitem** -Struktur **null**. Andernfalls ist **pszText** die Adresse des bearbeiteten Texts.</span><span class="sxs-lookup"><span data-stu-id="731dc-112">If label editing was canceled, the **pszText** member of the **TVITEM** structure is **NULL**; otherwise, **pszText** is the address of the edited text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="731dc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="731dc-113">Return value</span></span>

<span data-ttu-id="731dc-114">Wenn das **pszText** -Element nicht **null** ist, wird **true** zurückgegeben, um die Bezeichnung des Elements auf den bearbeiteten Text festzulegen.</span><span class="sxs-lookup"><span data-stu-id="731dc-114">If the **pszText** member is non-**NULL**, return **TRUE** to set the item's label to the edited text.</span></span> <span data-ttu-id="731dc-115">Gibt **false** zurück, um den bearbeiteten Text abzulehnen und zur ursprünglichen Bezeichnung zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="731dc-115">Return **FALSE** to reject the edited text and revert to the original label.</span></span>

## <a name="remarks"></a><span data-ttu-id="731dc-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="731dc-116">Remarks</span></span>

<span data-ttu-id="731dc-117">Wenn der **pszText** -Member **null** ist, wird der Rückgabewert ignoriert.</span><span class="sxs-lookup"><span data-stu-id="731dc-117">If the **pszText** member is **NULL**, the return value is ignored.</span></span>

<span data-ttu-id="731dc-118">Wenn Sie den LPSTR \_ -textcallback-Wert für dieses Element angegeben haben und das **pszText** -Element nicht **null** ist, \_ sollte der TVN endlabeledit-Handler den Text aus **pszText** in den lokalen Speicher kopieren.</span><span class="sxs-lookup"><span data-stu-id="731dc-118">If you specified the LPSTR\_TEXTCALLBACK value for this item and the **pszText** member is non-**NULL**, your TVN\_ENDLABELEDIT handler should copy the text from **pszText** to your local storage.</span></span>

## <a name="requirements"></a><span data-ttu-id="731dc-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="731dc-119">Requirements</span></span>



| <span data-ttu-id="731dc-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="731dc-120">Requirement</span></span> | <span data-ttu-id="731dc-121">Wert</span><span class="sxs-lookup"><span data-stu-id="731dc-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="731dc-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="731dc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="731dc-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="731dc-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="731dc-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="731dc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="731dc-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="731dc-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="731dc-126">Header</span><span class="sxs-lookup"><span data-stu-id="731dc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="731dc-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="731dc-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="731dc-128">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="731dc-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="731dc-129">**TVN \_ Endlabeleditw** (Unicode) und **TVN \_ endlabeledita** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="731dc-129">**TVN\_ENDLABELEDITW** (Unicode) and **TVN\_ENDLABELEDITA** (ANSI)</span></span><br/>         |



 

 





