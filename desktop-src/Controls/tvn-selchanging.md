---
title: TVN_SELCHANGING Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Baumansicht-Steuer Elements, dass sich die Auswahl von einem Element in ein anderes ändert. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 53f24ee0-433c-4680-9075-5e2b21117ed9
keywords:
- Windows-Steuerelemente für TVN_SELCHANGING Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_SELCHANGING
- TVN_SELCHANGINGA
- TVN_SELCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14de700bc058b8c6454a2f7e08fb9986697438fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040496"
---
# <a name="tvn_selchanging-notification-code"></a><span data-ttu-id="ea574-105">TVN \_ selchanging-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="ea574-105">TVN\_SELCHANGING notification code</span></span>

<span data-ttu-id="ea574-106">Benachrichtigt das übergeordnete Fenster eines Baumansicht-Steuer Elements, dass sich die Auswahl von einem Element in ein anderes ändert.</span><span class="sxs-lookup"><span data-stu-id="ea574-106">Notifies a tree-view control's parent window that the selection is about to change from one item to another.</span></span> <span data-ttu-id="ea574-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="ea574-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SELCHANGING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="ea574-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea574-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea574-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea574-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea574-110">Zeiger auf eine [**nmtreeview**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ea574-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="ea574-111">Die Member **itemold** und **itemnew** enthalten gültige Informationen über das aktuell ausgewählte Element und das neu ausgewählte Element.</span><span class="sxs-lookup"><span data-stu-id="ea574-111">The **itemOld** and **itemNew** members contain valid information about the currently selected item and the newly selected item.</span></span> <span data-ttu-id="ea574-112">Der **Aktionsmember** gibt an, ob eine Maus-oder Tastatur Aktion eine Änderung der Auswahl bewirkt.</span><span class="sxs-lookup"><span data-stu-id="ea574-112">The **action** member indicates whether a mouse or keyboard action is causing the selection to change.</span></span> <span data-ttu-id="ea574-113">Eine Liste der möglichen Werte finden Sie in der Beschreibung des von der [TVN \_ selchanged](tvn-selchanged.md) -Benachrichtigungs Codes.</span><span class="sxs-lookup"><span data-stu-id="ea574-113">For a list of possible values, see the description of the [TVN\_SELCHANGED](tvn-selchanged.md) notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea574-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea574-114">Return value</span></span>

<span data-ttu-id="ea574-115">Gibt **true** zurück, um zu verhindern, dass sich die Auswahl ändert.</span><span class="sxs-lookup"><span data-stu-id="ea574-115">Returns **TRUE** to prevent the selection from changing.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea574-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea574-116">Remarks</span></span>

<span data-ttu-id="ea574-117">Bei der Reaktion auf diesen Benachrichtigungs Code sollten Anwendungen die Elemente, die die Auswahl erhalten oder verlieren, nicht löschen.</span><span class="sxs-lookup"><span data-stu-id="ea574-117">When responding to this notification code, applications should not delete the items that are gaining or losing the selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea574-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea574-118">Requirements</span></span>



| <span data-ttu-id="ea574-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea574-119">Requirement</span></span> | <span data-ttu-id="ea574-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ea574-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea574-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea574-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ea574-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea574-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea574-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea574-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ea574-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea574-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea574-125">Header</span><span class="sxs-lookup"><span data-stu-id="ea574-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea574-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea574-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ea574-127">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="ea574-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ea574-128">**TVN \_ Selchangingw** (Unicode) und **TVN \_ selchanginga** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ea574-128">**TVN\_SELCHANGINGW** (Unicode) and **TVN\_SELCHANGINGA** (ANSI)</span></span><br/>           |



 

 





