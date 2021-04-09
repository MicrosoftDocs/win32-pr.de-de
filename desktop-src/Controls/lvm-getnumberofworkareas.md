---
title: LVM_GETNUMBEROFWORKAREAS Meldung (kommstrg. h)
description: Ruft die Anzahl der Arbeitsbereiche in einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit senden oder das ListView \_ getnumofworkareas-Makro verwenden.
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- Windows-Steuerelemente für LVM_GETNUMBEROFWORKAREAS Meldung
topic_type:
- apiref
api_name:
- LVM_GETNUMBEROFWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73c62b7184ba60b979356a98a93d2579c8f74a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956987"
---
# <a name="lvm_getnumberofworkareas-message"></a><span data-ttu-id="72be7-105">LVM \_ getnumofworkareas-Meldung</span><span class="sxs-lookup"><span data-stu-id="72be7-105">LVM\_GETNUMBEROFWORKAREAS message</span></span>

<span data-ttu-id="72be7-106">Ruft die Anzahl der Arbeitsbereiche in einem Listenansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="72be7-106">Retrieves the number of working areas in a list-view control.</span></span> <span data-ttu-id="72be7-107">Sie können diese Nachricht explizit senden oder das [**ListView \_ getnumofworkareas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="72be7-107">You can send this message explicitly or use the [**ListView\_GetNumberOfWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="72be7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="72be7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72be7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72be7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="72be7-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="72be7-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="72be7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72be7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72be7-112">Ein Zeiger auf einen uint-Wert, der die Anzahl der Arbeitsbereiche im Listenansicht-Steuerelement empfängt.</span><span class="sxs-lookup"><span data-stu-id="72be7-112">Pointer to a UINT value that receives the number of working areas in the list-view control.</span></span> <span data-ttu-id="72be7-113">Wenn NULL in diese Variable eingefügt wird, sind derzeit keine Arbeitsbereiche festgelegt.</span><span class="sxs-lookup"><span data-stu-id="72be7-113">If zero is placed in this variable, then no working areas are currently set.</span></span> <span data-ttu-id="72be7-114">Dieser Wert darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="72be7-114">This value cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72be7-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72be7-115">Return value</span></span>

<span data-ttu-id="72be7-116">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="72be7-116">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="72be7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72be7-117">Requirements</span></span>



| <span data-ttu-id="72be7-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72be7-118">Requirement</span></span> | <span data-ttu-id="72be7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="72be7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72be7-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72be7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="72be7-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72be7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="72be7-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72be7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="72be7-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72be7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72be7-124">Header</span><span class="sxs-lookup"><span data-stu-id="72be7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="72be7-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="72be7-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72be7-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72be7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72be7-127">Verwenden von List-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="72be7-127">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 





