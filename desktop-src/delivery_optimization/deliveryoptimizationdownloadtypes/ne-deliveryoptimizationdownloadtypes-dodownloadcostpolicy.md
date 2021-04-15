---
title: Dodownloadcostpolicy-Enumeration
description: Gibt die ID der Kosten Richtlinien Optionen an, die mit der **DODownloadProperty_CostPolicy** Eigenschaft verknüpft sind.
keywords:
- Dodownloadcostpolicy-Enumeration, dodownloadcostpolicy
topic_type:
- apiref
api_name:
- DODownloadCostPolicy
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: c70384f7c7da1633b910db36c42a335d1c463bae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391582"
---
# <a name="dodownloadcostpolicy-enumeration"></a><span data-ttu-id="1d6b0-104">Dodownloadcostpolicy-Enumeration</span><span class="sxs-lookup"><span data-stu-id="1d6b0-104">DODownloadCostPolicy enumeration</span></span>

<span data-ttu-id="1d6b0-105">Die **dodownloadcostpolicy** -Enumeration gibt die ID der Kosten Richtlinien Optionen an, die mit der **DODownloadProperty_CostPolicy** -Eigenschaft verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="1d6b0-105">The **DODownloadCostPolicy** enumeration specifies the ID of cost policies options associated with the **DODownloadProperty_CostPolicy** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d6b0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d6b0-106">Syntax</span></span>

```cpp
typedef enum _DODownloadCostPolicy
{
  DODownloadCostPolicy_Always = 0,
  DODownloadCostPolicy_Unrestricted,
  DODownloadCostPolicy_Standard,    
  DODownloadCostPolicy_NoRoaming,   
  DODownloadCostPolicy_NoSurcharge, 
  DODownloadCostPolicy_NoCellular
} DODownloadCostPolicy;
```

## <a name="constants"></a><span data-ttu-id="1d6b0-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="1d6b0-107">Constants</span></span>

| <span data-ttu-id="1d6b0-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d6b0-108">Requirement</span></span> | <span data-ttu-id="1d6b0-109">Wert</span><span class="sxs-lookup"><span data-stu-id="1d6b0-109">Value</span></span> |
|-|-|
| <span data-ttu-id="1d6b0-110">DODownloadCostPolicy_Always</span><span class="sxs-lookup"><span data-stu-id="1d6b0-110">DODownloadCostPolicy_Always</span></span> | <span data-ttu-id="1d6b0-111">Der Download wird unabhängig von den Kosten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d6b0-111">Download runs regardless of the cost.</span></span> |
| <span data-ttu-id="1d6b0-112">DODownloadCostPolicy_Unrestricted</span><span class="sxs-lookup"><span data-stu-id="1d6b0-112">DODownloadCostPolicy_Unrestricted</span></span> | <span data-ttu-id="1d6b0-113">Download Ausführungen, es sei denn, Sie erzwingen Kosten oder Datenverkehrs Limits</span><span class="sxs-lookup"><span data-stu-id="1d6b0-113">Download runs unless imposes costs or traffic limits.</span></span> |
| <span data-ttu-id="1d6b0-114">DODownloadCostPolicy_Standard</span><span class="sxs-lookup"><span data-stu-id="1d6b0-114">DODownloadCostPolicy_Standard</span></span> | <span data-ttu-id="1d6b0-115">Der Download wird ausgeführt, es sei denn, es gibt keine Zuschläge und keine beinahe-Erschöpfung</span><span class="sxs-lookup"><span data-stu-id="1d6b0-115">Download runs unless neither subject to a surcharge nor near exhaustion.</span></span> |
| <span data-ttu-id="1d6b0-116">DODownloadCostPolicy_NoRoaming</span><span class="sxs-lookup"><span data-stu-id="1d6b0-116">DODownloadCostPolicy_NoRoaming</span></span> | <span data-ttu-id="1d6b0-117">Download wird ausgeführt, es sei denn, die Konnektivität unterliegt roamingzuschläge</span><span class="sxs-lookup"><span data-stu-id="1d6b0-117">Download runs unless that connectivity is subject to roaming surcharges.</span></span> |
| <span data-ttu-id="1d6b0-118">DODownloadCostPolicy_NoSurcharge</span><span class="sxs-lookup"><span data-stu-id="1d6b0-118">DODownloadCostPolicy_NoSurcharge</span></span> | <span data-ttu-id="1d6b0-119">Download wird ausgeführt, es sei denn, es wird ein Zuschlag</span><span class="sxs-lookup"><span data-stu-id="1d6b0-119">Download runs unless subject to a surcharge.</span></span> |
| <span data-ttu-id="1d6b0-120">DODownloadCostPolicy_NoCellular</span><span class="sxs-lookup"><span data-stu-id="1d6b0-120">DODownloadCostPolicy_NoCellular</span></span> | <span data-ttu-id="1d6b0-121">Der Download wird ausgeführt, es sei denn, das Netzwerk ist</span><span class="sxs-lookup"><span data-stu-id="1d6b0-121">Download runs unless network is on cellular.</span></span> |

## <a name="requirements"></a><span data-ttu-id="1d6b0-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d6b0-122">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="1d6b0-123">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="1d6b0-123">**Minimum supported client**</span></span> | <span data-ttu-id="1d6b0-124">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="1d6b0-124">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="1d6b0-125">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="1d6b0-125">**Minimum supported server**</span></span> | <span data-ttu-id="1d6b0-126">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="1d6b0-126">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="1d6b0-127">**Header**</span><span class="sxs-lookup"><span data-stu-id="1d6b0-127">**Header**</span></span> | <span data-ttu-id="1d6b0-128">Deliveryoptimizationdownloadtypes. h</span><span class="sxs-lookup"><span data-stu-id="1d6b0-128">DeliveryOptimizationDownloadTypes.h</span></span> |
