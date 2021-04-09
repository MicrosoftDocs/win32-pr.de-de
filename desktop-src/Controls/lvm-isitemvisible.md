---
title: LVM_ISITEMVISIBLE Meldung (kommstrg. h)
description: Gibt an, ob ein Element im Listenansicht-Steuerelement sichtbar ist. Senden Sie diese Nachricht explizit oder mithilfe des ListView-Objekts \_ isitemvisible.
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- Windows-Steuerelemente für LVM_ISITEMVISIBLE Meldung
topic_type:
- apiref
api_name:
- LVM_ISITEMVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a95116d2d6da6e3554e63a8149c9b91d6c97f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859148"
---
# <a name="lvm_isitemvisible-message"></a><span data-ttu-id="e8d3a-105">LVM- \_ isitemvisible-Meldung</span><span class="sxs-lookup"><span data-stu-id="e8d3a-105">LVM\_ISITEMVISIBLE message</span></span>

<span data-ttu-id="e8d3a-106">Gibt an, ob ein Element im Listenansicht-Steuerelement sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="e8d3a-106">Indicates if an item in the list-view control is visible.</span></span> <span data-ttu-id="e8d3a-107">Senden Sie diese Nachricht explizit oder mithilfe des [**ListView-Objekts \_ isitemvisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) .</span><span class="sxs-lookup"><span data-stu-id="e8d3a-107">Send this message explicitly or by using the [**ListView\_IsItemVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8d3a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8d3a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8d3a-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8d3a-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8d3a-110">Ein Index des Elements im Listenansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="e8d3a-110">An index of the item in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="e8d3a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8d3a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e8d3a-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e8d3a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8d3a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8d3a-113">Return value</span></span>

<span data-ttu-id="e8d3a-114">Gibt **true** zurück, wenn es sichtbar ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="e8d3a-114">Returns **TRUE** if visible, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8d3a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8d3a-115">Requirements</span></span>



| <span data-ttu-id="e8d3a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8d3a-116">Requirement</span></span> | <span data-ttu-id="e8d3a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e8d3a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8d3a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8d3a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e8d3a-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8d3a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8d3a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8d3a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e8d3a-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8d3a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8d3a-122">Header</span><span class="sxs-lookup"><span data-stu-id="e8d3a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8d3a-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8d3a-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





