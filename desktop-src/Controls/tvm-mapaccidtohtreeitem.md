---
title: TVM_MAPACCIDTOHTREEITEM Meldung (kommstrg. h)
description: Ordnet einem HTREEITEM eine Barrierefreiheits-ID zu.
ms.assetid: f4feb7cb-2138-4930-b8ee-b9e2d4b19001
keywords:
- Windows-Steuerelemente für TVM_MAPACCIDTOHTREEITEM Meldung
topic_type:
- apiref
api_name:
- TVM_MAPACCIDTOHTREEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b827b18387723fe4792321f7932e1abb3673466e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040346"
---
# <a name="tvm_mapaccidtohtreeitem-message"></a><span data-ttu-id="396ca-104">TVM \_ mapacciddehtreeitem-Meldung</span><span class="sxs-lookup"><span data-stu-id="396ca-104">TVM\_MAPACCIDTOHTREEITEM message</span></span>

<span data-ttu-id="396ca-105">Ordnet einem **HTREEITEM** eine Barrierefreiheits-ID zu.</span><span class="sxs-lookup"><span data-stu-id="396ca-105">Maps an accessibility ID to an **HTREEITEM**.</span></span>

## <a name="parameters"></a><span data-ttu-id="396ca-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="396ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="396ca-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="396ca-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="396ca-108">**Uint** , das die Barrierefreiheits-ID enthält, die einem **HTREEITEM** zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="396ca-108">**UINT** that contains the accessibility ID to map to an **HTREEITEM**.</span></span> </dd> <dt>

<span data-ttu-id="396ca-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="396ca-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="396ca-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="396ca-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="396ca-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="396ca-111">Return value</span></span>

<span data-ttu-id="396ca-112">Gibt das **HTREEITEM** -Element zurück, dem die angegebene Barrierefreiheits-ID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="396ca-112">Returns the **HTREEITEM** that the specified accessibility ID is mapped to.</span></span>

## <a name="remarks"></a><span data-ttu-id="396ca-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="396ca-113">Remarks</span></span>

<span data-ttu-id="396ca-114">Wenn Sie ein Element zu einem Strukturansicht-Steuerelement hinzufügen, gibt ein **HTREEITEM** -Objekt zurück, das das Element eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="396ca-114">When you add an item to a tree-view control an **HTREEITEM** returns, which uniquely identifies the item.</span></span>

> [!Note]  
> <span data-ttu-id="396ca-115">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="396ca-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="396ca-116">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="396ca-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="396ca-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="396ca-117">Requirements</span></span>



| <span data-ttu-id="396ca-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="396ca-118">Requirement</span></span> | <span data-ttu-id="396ca-119">Wert</span><span class="sxs-lookup"><span data-stu-id="396ca-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="396ca-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="396ca-120">Minimum supported client</span></span><br/> | <span data-ttu-id="396ca-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="396ca-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="396ca-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="396ca-122">Minimum supported server</span></span><br/> | <span data-ttu-id="396ca-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="396ca-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="396ca-124">Header</span><span class="sxs-lookup"><span data-stu-id="396ca-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="396ca-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="396ca-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="396ca-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="396ca-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="396ca-127">**TreeView \_ mapaccidto HTREEITEM**</span><span class="sxs-lookup"><span data-stu-id="396ca-127">**TreeView\_MapAccIDToHTREEITEM**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
</dt> </dl>

 

 





