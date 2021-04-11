---
description: Aktiviert und deaktiviert die Auflistung von Metriken.
ms.assetid: afb90863-e70a-46e5-b1b7-d959dcacc306
title: Controlmetrics-Methode der CIM_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 60a7d0b34227594cf7146a988aa7e0d232f2d6cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216249"
---
# <a name="controlmetrics-method-of-the-cim_metricservice-class"></a><span data-ttu-id="dd35b-103">Controlmetrics-Methode der CIM \_ metricservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="dd35b-103">ControlMetrics method of the CIM\_MetricService class</span></span>

<span data-ttu-id="dd35b-104">Aktiviert und deaktiviert die Auflistung von Metriken. **Controlmetrics** wird verwendet, um die Sammlung der einzelnen metrikmetriken für ein [**CIM- \_ managedelement**](cim-managedelement.md), die Sammlung eines bestimmten metriktyps für alle verwalteten Elemente oder die Auflistung einer bestimmten Metrik für ein bestimmtes verwaltetes Element zu steuern.</span><span class="sxs-lookup"><span data-stu-id="dd35b-104">Enables and disables the collection of metrics.**ControlMetrics** is used to control the collection of each type of metric for a [**CIM\_ManagedElement**](cim-managedelement.md), the collection of a given type of metric for all managed elements, or the collection of a specific metric for a specific managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd35b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd35b-105">Syntax</span></span>


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="dd35b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd35b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd35b-107">*Betreff* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd35b-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd35b-108">Ein [**CIM- \_ managedelement**](cim-managedelement.md) , das verwaltete (n) Elemente identifiziert, für die Metriken gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="dd35b-108">A [**CIM\_ManagedElement**](cim-managedelement.md) that identifies managed element(s) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="dd35b-109">*Definition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd35b-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd35b-110">Gibt eine [**CIM- \_ basemetricdefinition**](cim-basemetricdefinition.md) an, für die Metriken gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="dd35b-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="dd35b-111">*Metriccollectionaktivierte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd35b-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd35b-112">Gibt den für die Metriken auszuführenden gewünschten Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="dd35b-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="dd35b-113">**Aktivieren** (2)</span><span class="sxs-lookup"><span data-stu-id="dd35b-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="dd35b-114">**Deaktivieren** (3)</span><span class="sxs-lookup"><span data-stu-id="dd35b-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="dd35b-115">**Zurücksetzen** (4)</span><span class="sxs-lookup"><span data-stu-id="dd35b-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="dd35b-116">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="dd35b-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="dd35b-117">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="dd35b-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="dd35b-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dd35b-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="dd35b-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd35b-119">Return value</span></span>

<span data-ttu-id="dd35b-120">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dd35b-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="dd35b-121">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="dd35b-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dd35b-122">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="dd35b-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dd35b-123">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="dd35b-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dd35b-124">**Reservierte Methode** (..)</span><span class="sxs-lookup"><span data-stu-id="dd35b-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dd35b-125">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="dd35b-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dd35b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd35b-126">Requirements</span></span>



| <span data-ttu-id="dd35b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd35b-127">Requirement</span></span> | <span data-ttu-id="dd35b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="dd35b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd35b-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd35b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dd35b-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dd35b-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="dd35b-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd35b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dd35b-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dd35b-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="dd35b-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd35b-133">Namespace</span></span><br/>                | <span data-ttu-id="dd35b-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="dd35b-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dd35b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="dd35b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd35b-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dd35b-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd35b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="dd35b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd35b-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd35b-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dd35b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd35b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd35b-140">**CIM- \_ metricservice**</span><span class="sxs-lookup"><span data-stu-id="dd35b-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




