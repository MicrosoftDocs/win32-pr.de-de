---
title: TVM_MAPHTREEITEMTOACCID Meldung (kommstrg. h)
description: Ordnet ein HTREEITEM einer Barrierefreiheits-ID zu.
ms.assetid: 87ef0785-88c1-49f4-8a05-872577e16fe4
keywords:
- Windows-Steuerelemente für TVM_MAPHTREEITEMTOACCID Meldung
topic_type:
- apiref
api_name:
- TVM_MAPHTREEITEMTOACCID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6267c2040583917283fc444db74ddacbdabd69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103719"
---
# <a name="tvm_maphtreeitemtoaccid-message"></a><span data-ttu-id="6cce5-104">TVM- \_ Meldung "maphtreeitemdeaccid"</span><span class="sxs-lookup"><span data-stu-id="6cce5-104">TVM\_MAPHTREEITEMTOACCID message</span></span>

<span data-ttu-id="6cce5-105">Ordnet ein **HTREEITEM** einer Barrierefreiheits-ID zu.</span><span class="sxs-lookup"><span data-stu-id="6cce5-105">Maps an **HTREEITEM** to an accessibility ID.</span></span>

## <a name="parameters"></a><span data-ttu-id="6cce5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cce5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cce5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6cce5-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6cce5-108">**HTREEITEM** , das einer Barrierefreiheits-ID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6cce5-108">**HTREEITEM** that is mapped to an accessibility ID.</span></span></dd> <dt>

<span data-ttu-id="6cce5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6cce5-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6cce5-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="6cce5-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cce5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6cce5-111">Return value</span></span>

<span data-ttu-id="6cce5-112">Gibt eine Barrierefreiheits-ID zurück.</span><span class="sxs-lookup"><span data-stu-id="6cce5-112">Returns an accessibility ID.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cce5-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6cce5-113">Remarks</span></span>

<span data-ttu-id="6cce5-114">Wenn Sie ein Element zu einem Strukturansicht-Steuerelement hinzufügen, wird ein **HTREEITEM** -Handle zurückgegeben, das das Element eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6cce5-114">When you add an item to a tree-view control an **HTREEITEM** handle is returned that uniquely identifies the item.</span></span>

> [!Note]  
> <span data-ttu-id="6cce5-115">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="6cce5-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6cce5-116">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6cce5-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6cce5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6cce5-117">Requirements</span></span>



| <span data-ttu-id="6cce5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6cce5-118">Requirement</span></span> | <span data-ttu-id="6cce5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6cce5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cce5-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6cce5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6cce5-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6cce5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6cce5-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6cce5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6cce5-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6cce5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6cce5-124">Header</span><span class="sxs-lookup"><span data-stu-id="6cce5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cce5-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cce5-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cce5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6cce5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cce5-127">**TreeView \_ maphtreeitemteaccid**</span><span class="sxs-lookup"><span data-stu-id="6cce5-127">**TreeView\_MapHTREEITEMtoAccID**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
</dt> </dl>

 

 





