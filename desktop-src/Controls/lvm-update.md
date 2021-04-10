---
title: LVM_UPDATE Meldung (kommstrg. h)
description: Aktualisiert ein Listen Ansichts Element. Wenn das Listenansicht-Steuerelement den LVS \_ AutoArrange-Stil hat, bewirkt dieses Makro, dass das Listenansicht-Steuerelement angeordnet ist. Sie können diese Nachricht explizit oder mithilfe des ListView- \_ Update Makros senden.
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- Windows-Steuerelemente für LVM_UPDATE Meldung
topic_type:
- apiref
api_name:
- LVM_UPDATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cf2a4316e3ae3fc4dbab5e1afe780b03829b30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858680"
---
# <a name="lvm_update-message"></a><span data-ttu-id="f62e0-106">LVM- \_ Aktualisierungs Meldung</span><span class="sxs-lookup"><span data-stu-id="f62e0-106">LVM\_UPDATE message</span></span>

<span data-ttu-id="f62e0-107">Aktualisiert ein Listen Ansichts Element.</span><span class="sxs-lookup"><span data-stu-id="f62e0-107">Updates a list-view item.</span></span> <span data-ttu-id="f62e0-108">Wenn das Listenansicht-Steuerelement den [**LVS \_ AutoArrange**](list-view-window-styles.md) -Stil hat, bewirkt dieses Makro, dass das Listenansicht-Steuerelement angeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f62e0-108">If the list-view control has the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style, this macro causes the list-view control to be arranged.</span></span> <span data-ttu-id="f62e0-109">Sie können diese Nachricht explizit oder mithilfe des [**ListView- \_ Update**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) Makros senden.</span><span class="sxs-lookup"><span data-stu-id="f62e0-109">You can send this message explicitly or by using the [**ListView\_Update**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f62e0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f62e0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f62e0-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f62e0-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f62e0-112">Der Index des zu aktualisierenden Elements.</span><span class="sxs-lookup"><span data-stu-id="f62e0-112">Index of the item to update.</span></span>

</dd> <dt>

<span data-ttu-id="f62e0-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f62e0-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f62e0-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f62e0-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f62e0-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f62e0-115">Return value</span></span>

<span data-ttu-id="f62e0-116">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="f62e0-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f62e0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f62e0-117">Requirements</span></span>



| <span data-ttu-id="f62e0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f62e0-118">Requirement</span></span> | <span data-ttu-id="f62e0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f62e0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f62e0-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f62e0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f62e0-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f62e0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f62e0-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f62e0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f62e0-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f62e0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f62e0-124">Header</span><span class="sxs-lookup"><span data-stu-id="f62e0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f62e0-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f62e0-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





