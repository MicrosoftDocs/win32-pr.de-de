---
title: LVM_SUBITEMHITTEST Meldung (kommstrg. h)
description: Bestimmt, welches Listen Ansichts Element oder Unterelement an einer bestimmten Position liegt. Sie können diese Nachricht explizit oder mithilfe des ListView \_ subitemhittest-Makros senden.
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- Windows-Steuerelemente für LVM_SUBITEMHITTEST Meldung
topic_type:
- apiref
api_name:
- LVM_SUBITEMHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c811a3ed85b9eb157920f700b34d5d9c99597e67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475366"
---
# <a name="lvm_subitemhittest-message"></a><span data-ttu-id="d6e15-105">LVM \_ subitemhittest-Meldung</span><span class="sxs-lookup"><span data-stu-id="d6e15-105">LVM\_SUBITEMHITTEST message</span></span>

<span data-ttu-id="d6e15-106">Bestimmt, welches Listen Ansichts Element oder Unterelement an einer bestimmten Position liegt.</span><span class="sxs-lookup"><span data-stu-id="d6e15-106">Determines which list-view item or subitem is at a given position.</span></span> <span data-ttu-id="d6e15-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ subitemhittest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="d6e15-107">You can send this message explicitly or by using the [**ListView\_SubItemHitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d6e15-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6e15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6e15-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d6e15-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d6e15-110">Muss den Wert 0 (null) haben.</span><span class="sxs-lookup"><span data-stu-id="d6e15-110">Must be 0.</span></span> <span data-ttu-id="d6e15-111">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="d6e15-111">**Windows Vista.**</span></span> <span data-ttu-id="d6e15-112">Sollte-1 sein, wenn das **igroup** -Mitglied von *LPARAM* abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6e15-112">Should be -1 if the **iGroup** member of *lParam* is to be retrieved.</span></span></dd> <dt>

<span data-ttu-id="d6e15-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6e15-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6e15-114">Zeiger auf eine [**lvhittestinfo**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d6e15-114">Pointer to an [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure.</span></span> <span data-ttu-id="d6e15-115">Die [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur innerhalb von " **lvhittestinfo** " sollte auf die Client Koordinaten festgelegt werden, damit Sie als Treffer getestet werden.</span><span class="sxs-lookup"><span data-stu-id="d6e15-115">The [**POINT**](/previous-versions//dd162805(v=vs.85)) structure within **LVHITTESTINFO** should be set to the client coordinates to be hit-tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6e15-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6e15-116">Return value</span></span>

<span data-ttu-id="d6e15-117">Gibt ggf. den Index des getesteten Elements oder des unter Elements zurück, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="d6e15-117">Returns the index of the item or subitem tested, if any, or -1 otherwise.</span></span> <span data-ttu-id="d6e15-118">Wenn ein Element oder Unterelement an den angegebenen Koordinaten steht, werden die Felder der Struktur " [**lvhittestinfo**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) " mit den entsprechenden Treffer Informationen aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="d6e15-118">If an item or subitem is at the given coordinates, the fields of the [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure will be filled with the applicable hit information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6e15-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6e15-119">Requirements</span></span>



| <span data-ttu-id="d6e15-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6e15-120">Requirement</span></span> | <span data-ttu-id="d6e15-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d6e15-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6e15-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6e15-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d6e15-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6e15-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d6e15-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6e15-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d6e15-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6e15-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d6e15-126">Header</span><span class="sxs-lookup"><span data-stu-id="d6e15-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6e15-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6e15-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

