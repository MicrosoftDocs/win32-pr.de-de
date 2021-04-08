---
title: TB_SETMETRICS Meldung (kommstrg. h)
description: Legt die Metriken eines Symbolleisten-Steuer Elements fest.
ms.assetid: 60e35d65-6291-4a55-a4cf-19b5b1db8a65
keywords:
- Windows-Steuerelemente für TB_SETMETRICS Meldung
topic_type:
- apiref
api_name:
- TB_SETMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5320ecc85f0a44c4c80868ae5699b051e1ac1781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949594"
---
# <a name="tb_setmetrics-message"></a><span data-ttu-id="ae387-104">TB \_ setmetrics-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ae387-104">TB\_SETMETRICS message</span></span>

<span data-ttu-id="ae387-105">Legt die Metriken eines Symbolleisten-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="ae387-105">Sets the metrics of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae387-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae387-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae387-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae387-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ae387-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ae387-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ae387-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae387-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae387-110">[**Tbmetrics**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) -Struktur, die die festzulegenden Toolbar-Metriken enthält.</span><span class="sxs-lookup"><span data-stu-id="ae387-110">[**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) structure that contains the toolbar metrics to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae387-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae387-111">Return value</span></span>

<span data-ttu-id="ae387-112">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ae387-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae387-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae387-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ae387-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="ae387-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ae387-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ae387-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ae387-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae387-116">Requirements</span></span>



| <span data-ttu-id="ae387-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae387-117">Requirement</span></span> | <span data-ttu-id="ae387-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ae387-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae387-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae387-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ae387-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae387-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae387-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae387-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ae387-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae387-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae387-123">Header</span><span class="sxs-lookup"><span data-stu-id="ae387-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae387-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae387-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





