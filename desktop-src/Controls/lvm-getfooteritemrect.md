---
title: LVM_GETFOOTERITEMRECT Meldung (kommstrg. h)
description: Ruft die Koordinaten einer Fußzeile für ein angegebenes Element in einem Listenansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getfooteritemrect-Makros.
ms.assetid: 4a6055d3-1cc1-4c3d-a5f6-006617ff3bce
keywords:
- Windows-Steuerelemente für LVM_GETFOOTERITEMRECT Meldung
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142cb92806fa1d58faa0414c10c41bd2815d5b6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213702"
---
# <a name="lvm_getfooteritemrect-message"></a><span data-ttu-id="68728-105">LVM \_ getfooteritemrect-Meldung</span><span class="sxs-lookup"><span data-stu-id="68728-105">LVM\_GETFOOTERITEMRECT message</span></span>

<span data-ttu-id="68728-106">Ruft die Koordinaten einer Fußzeile für ein angegebenes Element in einem Listenansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="68728-106">Gets the coordinates of a footer for a specified item in a list-view control.</span></span> <span data-ttu-id="68728-107">Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getfooteritemrect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) -Makros.</span><span class="sxs-lookup"><span data-stu-id="68728-107">Send this message explicitly or by using the [**ListView\_GetFooterItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="68728-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="68728-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68728-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68728-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68728-110">Der Index des Elements im Listenansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="68728-110">The index of the item in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="68728-111">*LPARAM* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="68728-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="68728-112">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Koordinaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="68728-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="68728-113">Die aufrufenden Anwendung ist für die Zuordnung dieser Struktur verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="68728-113">The calling application is responsible for allocating this structure.</span></span> <span data-ttu-id="68728-114">Die empfangenen Koordinaten werden als Client Koordinaten ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="68728-114">The coordinates received are expressed as client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68728-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68728-115">Return value</span></span>

<span data-ttu-id="68728-116">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="68728-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="68728-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68728-117">Requirements</span></span>



| <span data-ttu-id="68728-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68728-118">Requirement</span></span> | <span data-ttu-id="68728-119">Wert</span><span class="sxs-lookup"><span data-stu-id="68728-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68728-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68728-120">Minimum supported client</span></span><br/> | <span data-ttu-id="68728-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68728-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="68728-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68728-122">Minimum supported server</span></span><br/> | <span data-ttu-id="68728-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68728-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68728-124">Header</span><span class="sxs-lookup"><span data-stu-id="68728-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="68728-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="68728-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

