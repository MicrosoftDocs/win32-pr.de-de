---
title: TVM_GETITEMSTATE Meldung (kommstrg. h)
description: Ruft einige oder alle Zustands Attribute eines Struktur Ansichts Elements ab. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetItemState-Makros senden.
ms.assetid: 89aaaa82-2809-4e4e-a325-5666a57c5cbb
keywords:
- Windows-Steuerelemente für TVM_GETITEMSTATE Meldung
topic_type:
- apiref
api_name:
- TVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b851ff3845743c802a2a914a0f40d5d9eb65c6a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040788"
---
# <a name="tvm_getitemstate-message"></a><span data-ttu-id="c8b88-105">TVM- \_ GetItemState-Meldung</span><span class="sxs-lookup"><span data-stu-id="c8b88-105">TVM\_GETITEMSTATE message</span></span>

<span data-ttu-id="c8b88-106">Ruft einige oder alle Zustands Attribute eines Struktur Ansichts Elements ab.</span><span class="sxs-lookup"><span data-stu-id="c8b88-106">Retrieves some or all of a tree-view item's state attributes.</span></span> <span data-ttu-id="c8b88-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="c8b88-107">You can send this message explicitly or by using the [**TreeView\_GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8b88-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8b88-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8b88-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8b88-110">Handle für das Element.</span><span class="sxs-lookup"><span data-stu-id="c8b88-110">Handle to the item.</span></span>

</dd> <dt>

<span data-ttu-id="c8b88-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8b88-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8b88-112">Maske, die verwendet wird, um die abzufragende Zustände anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c8b88-112">Mask used to specify the states to query for.</span></span> <span data-ttu-id="c8b88-113">Dies entspricht dem **Status Ask** -Member von [**tvitemex**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span><span class="sxs-lookup"><span data-stu-id="c8b88-113">It is equivalent to the **stateMask** member of [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8b88-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8b88-114">Return value</span></span>

<span data-ttu-id="c8b88-115">Gibt einen **uint** -Wert zurück, bei dem die entsprechenden Zustands Bits auf **true** festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="c8b88-115">Returns a **UINT** value with the appropriate state bits set to **TRUE**.</span></span> <span data-ttu-id="c8b88-116">Nur die Bits, die von *LPARAM* angegeben werden und **true** sind, werden festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c8b88-116">Only those bits that are specified by *lParam* and that are **TRUE** will be set.</span></span> <span data-ttu-id="c8b88-117">Dieser Wert entspricht dem **State** -Member von [**tvitemex**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span><span class="sxs-lookup"><span data-stu-id="c8b88-117">This value is equivalent to the **state** member of [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8b88-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8b88-118">Requirements</span></span>



| <span data-ttu-id="c8b88-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8b88-119">Requirement</span></span> | <span data-ttu-id="c8b88-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c8b88-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b88-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8b88-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c8b88-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8b88-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8b88-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8b88-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c8b88-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8b88-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8b88-125">Header</span><span class="sxs-lookup"><span data-stu-id="c8b88-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8b88-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8b88-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





