---
title: LVM_GETITEMSPACING Meldung (kommstrg. h)
description: Bestimmt den Abstand zwischen Elementen in einem Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des ListView \_ getitemspacing-Makros senden.
ms.assetid: 4e43fb43-468c-4b8a-9e3b-1694e90ffef8
keywords:
- Windows-Steuerelemente für LVM_GETITEMSPACING Meldung
topic_type:
- apiref
api_name:
- LVM_GETITEMSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea08a7fc1004ffb46d710da6d1c2a8b0fb18e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956990"
---
# <a name="lvm_getitemspacing-message"></a><span data-ttu-id="26eca-105">LVM- \_ getitemspacing-Nachricht</span><span class="sxs-lookup"><span data-stu-id="26eca-105">LVM\_GETITEMSPACING message</span></span>

<span data-ttu-id="26eca-106">Bestimmt den Abstand zwischen Elementen in einem Listenansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="26eca-106">Determines the spacing between items in a list-view control.</span></span> <span data-ttu-id="26eca-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ getitemspacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="26eca-107">You can send this message explicitly or by using the [**ListView\_GetItemSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="26eca-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="26eca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26eca-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="26eca-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26eca-110">Die Ansicht, für die die Element Abstände abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="26eca-110">View for which to retrieve the item spacing.</span></span> <span data-ttu-id="26eca-111">Dieser Parameter ist für die kleine Symbol Ansicht **true** , oder für die Symbol Ansicht ist der Wert **false** .</span><span class="sxs-lookup"><span data-stu-id="26eca-111">This parameter is **TRUE** for small icon view, or **FALSE** for icon view.</span></span>

</dd> <dt>

<span data-ttu-id="26eca-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26eca-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="26eca-113">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="26eca-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26eca-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26eca-114">Return value</span></span>

<span data-ttu-id="26eca-115">Gibt den Abstand zwischen Elementen zurück.</span><span class="sxs-lookup"><span data-stu-id="26eca-115">Returns the amount of spacing between items.</span></span> <span data-ttu-id="26eca-116">Der horizontale Abstand ist im [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthalten, und der vertikale Abstand ist im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))enthalten.</span><span class="sxs-lookup"><span data-stu-id="26eca-116">The horizontal spacing is contained in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the vertical spacing is contained in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="26eca-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26eca-117">Requirements</span></span>



| <span data-ttu-id="26eca-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26eca-118">Requirement</span></span> | <span data-ttu-id="26eca-119">Wert</span><span class="sxs-lookup"><span data-stu-id="26eca-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26eca-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26eca-120">Minimum supported client</span></span><br/> | <span data-ttu-id="26eca-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26eca-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26eca-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26eca-122">Minimum supported server</span></span><br/> | <span data-ttu-id="26eca-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26eca-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26eca-124">Header</span><span class="sxs-lookup"><span data-stu-id="26eca-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="26eca-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="26eca-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

