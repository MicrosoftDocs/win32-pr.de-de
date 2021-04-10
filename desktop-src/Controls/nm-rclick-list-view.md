---
title: NM_RCLICK (Listenansicht) Benachrichtigungs Code (kommstrg. h)
description: Wird von einem Listenansicht-Steuerelement gesendet, wenn der Benutzer mit der rechten Maustaste auf ein Element klickt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: dc7f97b3-4aec-4a8f-a87c-62cef5ba4c40
keywords:
- NM_RCLICK (Listenansicht) Windows-Steuerelemente für Benachrichtigungs Code
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f01c21f1b1e869a909dd41dcfce693bf084f2fa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103916"
---
# <a name="nm_rclick-list-view-notification-code"></a><span data-ttu-id="b622f-105">NM \_ rclick-Benachrichtigungs Code (Listenansicht)</span><span class="sxs-lookup"><span data-stu-id="b622f-105">NM\_RCLICK (list view) notification code</span></span>

<span data-ttu-id="b622f-106">Wird von einem Listenansicht-Steuerelement gesendet, wenn der Benutzer mit der rechten Maustaste auf ein Element klickt.</span><span class="sxs-lookup"><span data-stu-id="b622f-106">Sent by a list-view control when the user clicks an item with the right mouse button.</span></span> <span data-ttu-id="b622f-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="b622f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b622f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b622f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b622f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b622f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b622f-110">[Version 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="b622f-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="b622f-111">Zeiger auf eine [**nmitemaktivierungs**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="b622f-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains additional information about this notification.</span></span> <span data-ttu-id="b622f-112">Die Member **iItem**, **iSubItem** und **ptaction** dieser Struktur enthalten Informationen über das Element.</span><span class="sxs-lookup"><span data-stu-id="b622f-112">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b622f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b622f-113">Return value</span></span>

<span data-ttu-id="b622f-114">Gibt einen Wert ungleich 0 (null) zurück, um die Standard Verarbeitung nicht zuzulassen, oder NULL, um die Standard Verarbeitung zuzulassen</span><span class="sxs-lookup"><span data-stu-id="b622f-114">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="remarks"></a><span data-ttu-id="b622f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b622f-115">Remarks</span></span>

<span data-ttu-id="b622f-116">Das **iItem** -Member von *LPARAM* ist nur gültig, wenn auf das Symbol oder die erste Spalten Bezeichnung geklickt wurde.</span><span class="sxs-lookup"><span data-stu-id="b622f-116">The **iItem** member of *lParam* is only valid if the icon or first-column label has been clicked.</span></span> <span data-ttu-id="b622f-117">Wenn Sie bestimmen möchten, welches Element ausgewählt wird, wenn ein Klick an einer anderen Stelle in einer Zeile erfolgt, senden Sie eine [**LVM \_ subitemhittest**](lvm-subitemhittest.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b622f-117">To determine which item is selected when a click takes place elsewhere in a row, send an [**LVM\_SUBITEMHITTEST**](lvm-subitemhittest.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b622f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b622f-118">Requirements</span></span>



| <span data-ttu-id="b622f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b622f-119">Requirement</span></span> | <span data-ttu-id="b622f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b622f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b622f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b622f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b622f-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b622f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b622f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b622f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b622f-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b622f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b622f-125">Header</span><span class="sxs-lookup"><span data-stu-id="b622f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b622f-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b622f-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





