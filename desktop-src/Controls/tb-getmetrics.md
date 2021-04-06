---
title: TB_GETMETRICS Meldung (kommstrg. h)
description: Ruft die Metriken eines Symbolleisten-Steuer Elements ab.
ms.assetid: 19c735cf-09f8-443e-8a73-dd64af0193a1
keywords:
- Windows-Steuerelemente für TB_GETMETRICS Meldung
topic_type:
- apiref
api_name:
- TB_GETMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1ee299f56b367eef649a05657d713e22206a7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859102"
---
# <a name="tb_getmetrics-message"></a><span data-ttu-id="cb28d-104">TB \_ getmetrics-Nachricht</span><span class="sxs-lookup"><span data-stu-id="cb28d-104">TB\_GETMETRICS message</span></span>

<span data-ttu-id="cb28d-105">Ruft die Metriken eines Symbolleisten-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="cb28d-105">Retrieves the metrics of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb28d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb28d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb28d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb28d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cb28d-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="cb28d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cb28d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb28d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb28d-110">Zeiger auf eine [**tbmetrics**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) -Struktur, die die Toolbar-Metriken empfängt.</span><span class="sxs-lookup"><span data-stu-id="cb28d-110">Pointer to a [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) structure that receives the toolbar metrics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb28d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb28d-111">Return value</span></span>

<span data-ttu-id="cb28d-112">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb28d-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb28d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb28d-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cb28d-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="cb28d-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="cb28d-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cb28d-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cb28d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb28d-116">Requirements</span></span>



| <span data-ttu-id="cb28d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb28d-117">Requirement</span></span> | <span data-ttu-id="cb28d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cb28d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb28d-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb28d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cb28d-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb28d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb28d-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb28d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cb28d-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb28d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb28d-123">Header</span><span class="sxs-lookup"><span data-stu-id="cb28d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb28d-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb28d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





