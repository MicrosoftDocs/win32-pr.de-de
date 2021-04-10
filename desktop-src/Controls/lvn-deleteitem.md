---
title: LVN_DELETEITEM Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass ein Element gerade gelöscht wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 6e3d1955-ee35-488b-8b96-3d6ebbe5ceb5
keywords:
- Windows-Steuerelemente für LVN_DELETEITEM Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 009d39e78aa93d5c5230e9c1b06b84d2854a0d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106671"
---
# <a name="lvn_deleteitem-notification-code"></a><span data-ttu-id="f867f-105">LVN \_ DeleteItem-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="f867f-105">LVN\_DELETEITEM notification code</span></span>

<span data-ttu-id="f867f-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass ein Element gerade gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="f867f-106">Notifies a list-view control's parent window that an item is about to be deleted.</span></span> <span data-ttu-id="f867f-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="f867f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_DELETEITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f867f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f867f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f867f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f867f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f867f-110">Zeiger auf eine [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f867f-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="f867f-111">Das Element **iItem** identifiziert das Element, das gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="f867f-111">The **iItem** member identifies the item being deleted.</span></span> <span data-ttu-id="f867f-112">Wenn das Steuerelement nicht über den **LVS \_** -Besitzer Daten Stil verfügt, handelt es sich bei dem *LPARAM* um die Anwendungs definierten Daten, die dem Element zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f867f-112">If the control does not have the **LVS\_OWNERDATA** style, then the *lParam* is the application-defined data associated with the item.</span></span> <span data-ttu-id="f867f-113">Alle anderen Elemente dieser Struktur sind 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f867f-113">All other members of this structure are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f867f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f867f-114">Return value</span></span>

<span data-ttu-id="f867f-115">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="f867f-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f867f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f867f-116">Remarks</span></span>

<span data-ttu-id="f867f-117">Elemente in der Listenansicht beim Verarbeiten dieses Benachrichtigungs Codes nicht hinzufügen, löschen oder neu anordnen.</span><span class="sxs-lookup"><span data-stu-id="f867f-117">Do not add, delete, or rearrange items in the list view while processing this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f867f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f867f-118">Requirements</span></span>



| <span data-ttu-id="f867f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f867f-119">Requirement</span></span> | <span data-ttu-id="f867f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f867f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f867f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f867f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f867f-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f867f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f867f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f867f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f867f-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f867f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f867f-125">Header</span><span class="sxs-lookup"><span data-stu-id="f867f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f867f-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f867f-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





