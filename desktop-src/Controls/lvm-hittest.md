---
title: LVM_HITTEST Meldung (kommstrg. h)
description: Bestimmt, welches Listen Ansichts Element, sofern vorhanden, an einer angegebenen Position liegt. Sie können diese Nachricht explizit oder mithilfe des ListView \_ HitTest-Makros senden.
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- Windows-Steuerelemente für LVM_HITTEST Meldung
topic_type:
- apiref
api_name:
- LVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb770c8f5a47f1dcbbf23a11443afa581aea2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956983"
---
# <a name="lvm_hittest-message"></a><span data-ttu-id="7f153-105">LVM- \_ HitTest-Meldung</span><span class="sxs-lookup"><span data-stu-id="7f153-105">LVM\_HITTEST message</span></span>

<span data-ttu-id="7f153-106">Bestimmt, welches Listen Ansichts Element, sofern vorhanden, an einer angegebenen Position liegt.</span><span class="sxs-lookup"><span data-stu-id="7f153-106">Determines which list-view item, if any, is at a specified position.</span></span> <span data-ttu-id="7f153-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="7f153-107">You can send this message explicitly or by using the [**ListView\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7f153-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f153-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f153-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7f153-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7f153-110">Muss den Wert 0 (null) haben.</span><span class="sxs-lookup"><span data-stu-id="7f153-110">Must be 0.</span></span> <span data-ttu-id="7f153-111">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="7f153-111">**Windows Vista.**</span></span> <span data-ttu-id="7f153-112">Sollte-1 sein, wenn die Elemente **igroup** und **iSubItem** der *LPARAM* -Struktur abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7f153-112">Should be -1 if the **iGroup** and **iSubItem** members of the *lParam* structure are to be retrieved.</span></span></dd> <dt>

<span data-ttu-id="7f153-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f153-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f153-114">Ein Zeiger auf eine " [**lvhittestinfo**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) "-Struktur, die die Position zum Treffer Test enthält und Informationen zu den Ergebnissen des Treffer Tests empfängt.</span><span class="sxs-lookup"><span data-stu-id="7f153-114">Pointer to an [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure that contains the position to hit test and receives information about the results of the hit test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f153-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f153-115">Return value</span></span>

<span data-ttu-id="7f153-116">Gibt den Index des Elements an der angegebenen Position zurück, falls vorhanden, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="7f153-116">Returns the index of the item at the specified position, if any, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f153-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f153-117">Requirements</span></span>



| <span data-ttu-id="7f153-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f153-118">Requirement</span></span> | <span data-ttu-id="7f153-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7f153-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f153-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f153-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7f153-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f153-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7f153-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f153-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7f153-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f153-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7f153-124">Header</span><span class="sxs-lookup"><span data-stu-id="7f153-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f153-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f153-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





