---
title: TVM_GETSCROLLTIME Meldung (kommstrg. h)
description: Ruft die maximale Scrollzeit für das Strukturansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des TreeView- \_ getscrolltime-Makros senden.
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- Windows-Steuerelemente für TVM_GETSCROLLTIME Meldung
topic_type:
- apiref
api_name:
- TVM_GETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f0bacc6c12dd7f54f20d882faf738c11848d59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103210"
---
# <a name="tvm_getscrolltime-message"></a><span data-ttu-id="4b0ff-105">TVM \_ getscrolltime-Meldung</span><span class="sxs-lookup"><span data-stu-id="4b0ff-105">TVM\_GETSCROLLTIME message</span></span>

<span data-ttu-id="4b0ff-106">Ruft die maximale Scrollzeit für das Strukturansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="4b0ff-106">Retrieves the maximum scroll time for the tree-view control.</span></span> <span data-ttu-id="4b0ff-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView- \_ getscrolltime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="4b0ff-107">You can send this message explicitly or by using the [**TreeView\_GetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4b0ff-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b0ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b0ff-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4b0ff-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4b0ff-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="4b0ff-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4b0ff-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4b0ff-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4b0ff-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="4b0ff-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b0ff-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4b0ff-113">Return value</span></span>

<span data-ttu-id="4b0ff-114">Gibt die maximale Scrollzeit in Millisekunden zurück.</span><span class="sxs-lookup"><span data-stu-id="4b0ff-114">Returns the maximum scroll time, in milliseconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b0ff-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b0ff-115">Remarks</span></span>

<span data-ttu-id="4b0ff-116">Die maximale Scrollzeit ist die längste Zeitspanne, die ein scrollvorgang ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="4b0ff-116">The maximum scroll time is the longest amount of time that a scroll operation can take.</span></span> <span data-ttu-id="4b0ff-117">Der Bildlauf wird so angepasst, dass der Bildlauf innerhalb der maximalen Scrollzeit stattfindet.</span><span class="sxs-lookup"><span data-stu-id="4b0ff-117">The scrolling will be adjusted so that the scroll will take place within the maximum scroll time.</span></span> <span data-ttu-id="4b0ff-118">Ein scrollvorgang kann weniger Zeit in Anspruch nehmen als das Maximum.</span><span class="sxs-lookup"><span data-stu-id="4b0ff-118">A scroll operation may take less time than the maximum.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b0ff-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b0ff-119">Requirements</span></span>



| <span data-ttu-id="4b0ff-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b0ff-120">Requirement</span></span> | <span data-ttu-id="4b0ff-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4b0ff-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b0ff-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b0ff-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4b0ff-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b0ff-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4b0ff-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b0ff-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4b0ff-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b0ff-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4b0ff-126">Header</span><span class="sxs-lookup"><span data-stu-id="4b0ff-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b0ff-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b0ff-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b0ff-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b0ff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b0ff-129">**TVM \_ setscrolltime**</span><span class="sxs-lookup"><span data-stu-id="4b0ff-129">**TVM\_SETSCROLLTIME**</span></span>](tvm-setscrolltime.md)
</dt> </dl>

 

 





