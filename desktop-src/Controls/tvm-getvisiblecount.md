---
title: TVM_GETVISIBLECOUNT Meldung (kommstrg. h)
description: Ruft die Anzahl der Elemente ab, die im Client Fenster eines Strukturansicht-Steuer Elements vollständig sichtbar sein können. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetVisibleCount-Makros senden.
ms.assetid: c3519543-3fb2-4ecf-ac01-905d0946cb1b
keywords:
- Windows-Steuerelemente für TVM_GETVISIBLECOUNT Meldung
topic_type:
- apiref
api_name:
- TVM_GETVISIBLECOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1927d21741b109c5f00aa964b058dc0c34732529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949589"
---
# <a name="tvm_getvisiblecount-message"></a><span data-ttu-id="bfec2-105">TVM \_ GetVisibleCount-Meldung</span><span class="sxs-lookup"><span data-stu-id="bfec2-105">TVM\_GETVISIBLECOUNT message</span></span>

<span data-ttu-id="bfec2-106">Ruft die Anzahl der Elemente ab, die im Client Fenster eines Strukturansicht-Steuer Elements vollständig sichtbar sein können.</span><span class="sxs-lookup"><span data-stu-id="bfec2-106">Obtains the number of items that can be fully visible in the client window of a tree-view control.</span></span> <span data-ttu-id="bfec2-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetVisibleCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="bfec2-107">You can send this message explicitly or by using the [**TreeView\_GetVisibleCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bfec2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfec2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfec2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bfec2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bfec2-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="bfec2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bfec2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bfec2-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bfec2-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="bfec2-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfec2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bfec2-113">Return value</span></span>

<span data-ttu-id="bfec2-114">Gibt die Anzahl der Elemente zurück, die im Client Fenster des Strukturansicht-Steuer Elements vollständig sichtbar sein können.</span><span class="sxs-lookup"><span data-stu-id="bfec2-114">Returns the number of items that can be fully visible in the client window of the tree-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfec2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfec2-115">Remarks</span></span>

<span data-ttu-id="bfec2-116">Die Anzahl der Elemente, die vollständig sichtbar sein können, ist möglicherweise größer als die Anzahl der Elemente im Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="bfec2-116">The number of items that can be fully visible may be greater than the number of items in the control.</span></span> <span data-ttu-id="bfec2-117">Das-Steuerelement berechnet diesen Wert durch Aufteilen der Höhe des Client Fensters durch die Höhe eines Elements.</span><span class="sxs-lookup"><span data-stu-id="bfec2-117">The control calculates this value by dividing the height of the client window by the height of an item.</span></span>

<span data-ttu-id="bfec2-118">Beachten Sie, dass der Rückgabewert die Anzahl der Elemente ist, die *vollständig* sichtbar sein können.</span><span class="sxs-lookup"><span data-stu-id="bfec2-118">Note that the return value is the number of items that can be *fully* visible.</span></span> <span data-ttu-id="bfec2-119">Wenn Sie alle 20 Elemente und einen Teil von einem weiteren Element sehen können, ist der Rückgabewert 20.</span><span class="sxs-lookup"><span data-stu-id="bfec2-119">If you can see all of 20 items and part of one more item, the return value is 20.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfec2-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfec2-120">Requirements</span></span>



| <span data-ttu-id="bfec2-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfec2-121">Requirement</span></span> | <span data-ttu-id="bfec2-122">Wert</span><span class="sxs-lookup"><span data-stu-id="bfec2-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bfec2-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfec2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bfec2-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfec2-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bfec2-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfec2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bfec2-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfec2-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bfec2-127">Header</span><span class="sxs-lookup"><span data-stu-id="bfec2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfec2-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfec2-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





