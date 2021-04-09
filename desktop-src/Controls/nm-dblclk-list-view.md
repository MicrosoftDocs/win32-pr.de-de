---
title: NM_DBLCLK (Listenansicht) Benachrichtigungs Code (kommstrg. h)
description: Wird von einem Listenansicht-Steuerelement gesendet, wenn der Benutzer auf ein Element mit der linken Maustaste doppelklickt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 28455109-177e-4932-88c5-500a3a91c13a
keywords:
- NM_DBLCLK (Listenansicht) Windows-Steuerelemente für Benachrichtigungs Code
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: add6af24b4272631be7c2be387a7ffda899469b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858648"
---
# <a name="nm_dblclk-list-view-notification-code"></a><span data-ttu-id="ba991-105">NM- \_ dblclk (Listenansicht)-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="ba991-105">NM\_DBLCLK (list view) notification code</span></span>

<span data-ttu-id="ba991-106">Wird von einem Listenansicht-Steuerelement gesendet, wenn der Benutzer auf ein Element mit der linken Maustaste doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="ba991-106">Sent by a list-view control when the user double-clicks an item with the left mouse button.</span></span> <span data-ttu-id="ba991-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="ba991-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ba991-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba991-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba991-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba991-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba991-110">[Version 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="ba991-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="ba991-111">Zeiger auf eine [**nmitemaktivierungs**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="ba991-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains additional information about this notification.</span></span> <span data-ttu-id="ba991-112">Die Member **iItem**, **iSubItem** und **ptaction** dieser Struktur enthalten Informationen über das Element.</span><span class="sxs-lookup"><span data-stu-id="ba991-112">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba991-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba991-113">Return value</span></span>

<span data-ttu-id="ba991-114">Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba991-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba991-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba991-115">Remarks</span></span>

<span data-ttu-id="ba991-116">Das **iItem** -Member von *LPARAM* ist nur gültig, wenn auf das Symbol oder die erste Spalten Bezeichnung geklickt wurde.</span><span class="sxs-lookup"><span data-stu-id="ba991-116">The **iItem** member of *lParam* is only valid if the icon or first-column label has been clicked.</span></span> <span data-ttu-id="ba991-117">Wenn Sie bestimmen möchten, welches Element ausgewählt wird, wenn ein Klick an einer anderen Stelle in einer Zeile erfolgt, senden Sie eine [**LVM \_ subitemhittest**](lvm-subitemhittest.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ba991-117">To determine which item is selected when a click takes place elsewhere in a row, send an [**LVM\_SUBITEMHITTEST**](lvm-subitemhittest.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba991-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba991-118">Requirements</span></span>



| <span data-ttu-id="ba991-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba991-119">Requirement</span></span> | <span data-ttu-id="ba991-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ba991-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba991-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba991-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ba991-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba991-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba991-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba991-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ba991-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba991-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba991-125">Header</span><span class="sxs-lookup"><span data-stu-id="ba991-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba991-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba991-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





