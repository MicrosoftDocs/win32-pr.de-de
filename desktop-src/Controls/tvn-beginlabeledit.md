---
title: TVN_BEGINLABELEDIT Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements über den Anfang der Bezeichnungs Bearbeitung für ein Element. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44
keywords:
- Windows-Steuerelemente für TVN_BEGINLABELEDIT Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_BEGINLABELEDIT
- TVN_BEGINLABELEDITA
- TVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34eccdeda553d0792a2862e3ca81a0889539d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338736"
---
# <a name="tvn_beginlabeledit-notification-code"></a><span data-ttu-id="cf7bb-105">TVN \_ beginlabeledit-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="cf7bb-105">TVN\_BEGINLABELEDIT notification code</span></span>

<span data-ttu-id="cf7bb-106">Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements über den Anfang der Bezeichnungs Bearbeitung für ein Element.</span><span class="sxs-lookup"><span data-stu-id="cf7bb-106">Notifies a tree-view control's parent window about the start of label editing for an item.</span></span> <span data-ttu-id="cf7bb-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="cf7bb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="cf7bb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf7bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf7bb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf7bb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf7bb-110">Zeiger auf eine [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="cf7bb-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="cf7bb-111">Das **Element Element** ist eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, die gültige Informationen über das Element enthält, das in den Elementen **Hitem**, **State**, **LPARAM** und **pszText** bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="cf7bb-111">The **item** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the item being edited in the **hItem**, **state**, **lParam**, and **pszText** members.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf7bb-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf7bb-112">Return value</span></span>

<span data-ttu-id="cf7bb-113">Gibt **true** zurück, um die Bezeichnungs Bearbeitung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="cf7bb-113">Returns **TRUE** to cancel label editing.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf7bb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf7bb-114">Remarks</span></span>

<span data-ttu-id="cf7bb-115">Wenn die Bezeichnungs Bearbeitung beginnt, wird ein Bearbeitungs Steuerelement erstellt, aber nicht positioniert oder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cf7bb-115">When label editing begins, an edit control is created but not positioned or displayed.</span></span> <span data-ttu-id="cf7bb-116">Bevor es angezeigt wird, sendet das Strukturansicht-Steuerelement seinen übergeordneten Fenster einen TVN \_ beginlabeledit-Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="cf7bb-116">Before it is displayed, the tree-view control sends its parent window a TVN\_BEGINLABELEDIT notification code.</span></span>

<span data-ttu-id="cf7bb-117">Zum Anpassen der Bezeichnungs Bearbeitung implementieren Sie einen Handler für TVN \_ beginlabeledit und senden eine [**TVM \_ geteditcontrol**](tvm-geteditcontrol.md) -Nachricht an das Strukturansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="cf7bb-117">To customize label editing, implement a handler for TVN\_BEGINLABELEDIT and have it send a [**TVM\_GETEDITCONTROL**](tvm-geteditcontrol.md) message to the tree-view control.</span></span> <span data-ttu-id="cf7bb-118">Wenn eine Bezeichnung bearbeitet wird, ist der Rückgabewert ein Handle für das Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="cf7bb-118">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="cf7bb-119">Verwenden Sie dieses Handle, um das Bearbeitungs Steuerelement anzupassen, indem Sie die üblichen EM \_ xxx-Meldungen senden.</span><span class="sxs-lookup"><span data-stu-id="cf7bb-119">Use this handle to customize the edit control by sending the usual EM\_XXX messages.</span></span>

<span data-ttu-id="cf7bb-120">Wenn der Benutzer die Bearbeitung abbricht oder abschließt, empfängt das übergeordnete Fenster einen [TVN- \_ endlabeledit](tvn-endlabeledit.md) -Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="cf7bb-120">When the user cancels or completes the editing, the parent window receives a [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf7bb-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf7bb-121">Requirements</span></span>



| <span data-ttu-id="cf7bb-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf7bb-122">Requirement</span></span> | <span data-ttu-id="cf7bb-123">Wert</span><span class="sxs-lookup"><span data-stu-id="cf7bb-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf7bb-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf7bb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cf7bb-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf7bb-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf7bb-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf7bb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cf7bb-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf7bb-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf7bb-128">Header</span><span class="sxs-lookup"><span data-stu-id="cf7bb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf7bb-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf7bb-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="cf7bb-130">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="cf7bb-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cf7bb-131">**TVN \_ Beginlabeleditw** (Unicode) und **TVN \_ beginlabeledita** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cf7bb-131">**TVN\_BEGINLABELEDITW** (Unicode) and **TVN\_BEGINLABELEDITA** (ANSI)</span></span><br/>     |



 

 





