---
title: LVM_FINDITEM Meldung (kommstrg. h)
description: Sucht nach einem Listen Ansichts Element mit den angegebenen Merkmalen. Sie können diese Nachricht explizit oder mithilfe des ListView \_ FindItem-Makros senden.
ms.assetid: 3b18c8ad-97e6-4f4d-bf89-afb95f925ed1
keywords:
- Windows-Steuerelemente für LVM_FINDITEM Meldung
topic_type:
- apiref
api_name:
- LVM_FINDITEM
- LVM_FINDITEMA
- LVM_FINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f7dfc19e263a6ab7ad29b5e514fa4e52c1a9ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475186"
---
# <a name="lvm_finditem-message"></a><span data-ttu-id="8603b-105">LVM- \_ FindItem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="8603b-105">LVM\_FINDITEM message</span></span>

<span data-ttu-id="8603b-106">Sucht nach einem Listen Ansichts Element mit den angegebenen Merkmalen.</span><span class="sxs-lookup"><span data-stu-id="8603b-106">Searches for a list-view item with the specified characteristics.</span></span> <span data-ttu-id="8603b-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ FindItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="8603b-107">You can send this message explicitly or by using the [**ListView\_FindItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8603b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8603b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8603b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8603b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8603b-110">Der Index des Elements, mit dem mit der Suche begonnen werden soll, oder-1, um von Anfang an zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="8603b-110">The index of the item to begin the search with or -1 to start from the beginning.</span></span> <span data-ttu-id="8603b-111">Das angegebene Element ist selbst von der Suche ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8603b-111">The specified item is itself excluded from the search.</span></span>

</dd> <dt>

<span data-ttu-id="8603b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8603b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8603b-113">Ein Zeiger auf eine [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) -Struktur, die Informationen darüber enthält, nach welchen Informationen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="8603b-113">A pointer to an [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure that contains information about what to search for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8603b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8603b-114">Return value</span></span>

<span data-ttu-id="8603b-115">Gibt den Index des Elements zurück, wenn erfolgreich, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="8603b-115">Returns the index of the item if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8603b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8603b-116">Requirements</span></span>



| <span data-ttu-id="8603b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8603b-117">Requirement</span></span> | <span data-ttu-id="8603b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8603b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8603b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8603b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8603b-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8603b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8603b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8603b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8603b-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8603b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8603b-123">Header</span><span class="sxs-lookup"><span data-stu-id="8603b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8603b-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8603b-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8603b-125">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="8603b-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8603b-126">**LVM \_ Finditemw** (Unicode) und **LVM \_ finditema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8603b-126">**LVM\_FINDITEMW** (Unicode) and **LVM\_FINDITEMA** (ANSI)</span></span><br/>                 |



 

 





