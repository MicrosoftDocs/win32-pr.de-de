---
title: TVM_GETITEMHEIGHT Meldung (kommstrg. h)
description: Ruft die aktuelle Höhe der einzelnen Struktur Ansichts Elemente ab. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetItemHeight-Makros senden.
ms.assetid: 017476a3-1929-4a31-97a7-0f66175d47ea
keywords:
- Windows-Steuerelemente für TVM_GETITEMHEIGHT Meldung
topic_type:
- apiref
api_name:
- TVM_GETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789347b7a50f9bb42a7aebb6fecddf24c42c559c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859325"
---
# <a name="tvm_getitemheight-message"></a><span data-ttu-id="924bf-105">TVM \_ GetItemHeight-Meldung</span><span class="sxs-lookup"><span data-stu-id="924bf-105">TVM\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="924bf-106">Ruft die aktuelle Höhe der einzelnen Struktur Ansichts Elemente ab.</span><span class="sxs-lookup"><span data-stu-id="924bf-106">Retrieves the current height of the each tree-view item.</span></span> <span data-ttu-id="924bf-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="924bf-107">You can send this message explicitly or by using the [**TreeView\_GetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="924bf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="924bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="924bf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="924bf-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="924bf-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="924bf-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="924bf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="924bf-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="924bf-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="924bf-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="924bf-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="924bf-113">Return value</span></span>

<span data-ttu-id="924bf-114">Gibt die Höhe der einzelnen Elemente in Pixel zurück.</span><span class="sxs-lookup"><span data-stu-id="924bf-114">Returns the height of each item, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="924bf-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="924bf-115">Requirements</span></span>



| <span data-ttu-id="924bf-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="924bf-116">Requirement</span></span> | <span data-ttu-id="924bf-117">Wert</span><span class="sxs-lookup"><span data-stu-id="924bf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="924bf-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="924bf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="924bf-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="924bf-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="924bf-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="924bf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="924bf-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="924bf-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="924bf-122">Header</span><span class="sxs-lookup"><span data-stu-id="924bf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="924bf-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="924bf-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="924bf-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="924bf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="924bf-125">**TVM- \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="924bf-125">**TVM\_SETITEMHEIGHT**</span></span>](tvm-setitemheight.md)
</dt> </dl>

 

 





