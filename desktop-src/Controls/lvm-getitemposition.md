---
title: LVM_GETITEMPOSITION Meldung (kommstrg. h)
description: Ruft die Position eines Listen Ansichts Elements ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ getitemposition-Makros senden.
ms.assetid: e5841089-c34e-498e-b94c-45c845bfc747
keywords:
- Windows-Steuerelemente für LVM_GETITEMPOSITION Meldung
topic_type:
- apiref
api_name:
- LVM_GETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40b5899634e2f357068caa6ef96339be82f600b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859158"
---
# <a name="lvm_getitemposition-message"></a><span data-ttu-id="10fff-105">LVM- \_ getitemposition-Nachricht</span><span class="sxs-lookup"><span data-stu-id="10fff-105">LVM\_GETITEMPOSITION message</span></span>

<span data-ttu-id="10fff-106">Ruft die Position eines Listen Ansichts Elements ab.</span><span class="sxs-lookup"><span data-stu-id="10fff-106">Retrieves the position of a list-view item.</span></span> <span data-ttu-id="10fff-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ getitemposition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="10fff-107">You can send this message explicitly or by using the [**ListView\_GetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="10fff-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="10fff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10fff-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10fff-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10fff-110">Der Index des Listen Ansichts Elements.</span><span class="sxs-lookup"><span data-stu-id="10fff-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="10fff-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10fff-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10fff-112">Zeiger auf eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur, die die Position der oberen linken Ecke des Elements in Ansichts Koordinaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="10fff-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the position of the item's upper-left corner, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10fff-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10fff-113">Return value</span></span>

<span data-ttu-id="10fff-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="10fff-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="10fff-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10fff-115">Requirements</span></span>



| <span data-ttu-id="10fff-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10fff-116">Requirement</span></span> | <span data-ttu-id="10fff-117">Wert</span><span class="sxs-lookup"><span data-stu-id="10fff-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10fff-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10fff-118">Minimum supported client</span></span><br/> | <span data-ttu-id="10fff-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10fff-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10fff-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10fff-120">Minimum supported server</span></span><br/> | <span data-ttu-id="10fff-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10fff-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10fff-122">Header</span><span class="sxs-lookup"><span data-stu-id="10fff-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="10fff-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="10fff-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

