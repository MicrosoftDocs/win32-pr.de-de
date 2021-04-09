---
title: LVM_DELETEITEM Meldung (kommstrg. h)
description: Entfernt ein Element aus einem Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des ListView \_ DeleteItem-Makros senden.
ms.assetid: 0eddd4c1-7786-4a8c-a16d-9fd83cce98b3
keywords:
- Windows-Steuerelemente für LVM_DELETEITEM Meldung
topic_type:
- apiref
api_name:
- LVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19fce5afbbaa6702f296df12acf7dad4edac16fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102903"
---
# <a name="lvm_deleteitem-message"></a><span data-ttu-id="3690e-105">LVM \_ DeleteItem-Meldung</span><span class="sxs-lookup"><span data-stu-id="3690e-105">LVM\_DELETEITEM message</span></span>

<span data-ttu-id="3690e-106">Entfernt ein Element aus einem Listenansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="3690e-106">Removes an item from a list-view control.</span></span> <span data-ttu-id="3690e-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="3690e-107">You can send this message explicitly or by using the [**ListView\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3690e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3690e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3690e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3690e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3690e-110">Der Index des zu löschenden Listen Ansichts Elements.</span><span class="sxs-lookup"><span data-stu-id="3690e-110">The index of the list-view item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="3690e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3690e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3690e-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="3690e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3690e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3690e-113">Return value</span></span>

<span data-ttu-id="3690e-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="3690e-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3690e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3690e-115">Requirements</span></span>



| <span data-ttu-id="3690e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3690e-116">Requirement</span></span> | <span data-ttu-id="3690e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3690e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3690e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3690e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3690e-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3690e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3690e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3690e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3690e-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3690e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3690e-122">Header</span><span class="sxs-lookup"><span data-stu-id="3690e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3690e-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3690e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





