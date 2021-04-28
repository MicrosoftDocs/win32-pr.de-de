---
description: 'ControlMetrics-Methode der CIM_MetricService Klasse: Aktiviert und deaktiviert die Sammlung von Metriken.'
ms.assetid: afb90863-e70a-46e5-b1b7-d959dcacc306
title: ControlMetrics-Methode der CIM_MetricService Klasse
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
ms.openlocfilehash: 19e732e50f8c367463e7f528a520a736117999b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090868"
---
# <a name="controlmetrics-method-of-the-cim_metricservice-class"></a><span data-ttu-id="ea705-103">ControlMetrics-Methode der CIM \_ MetricService-Klasse</span><span class="sxs-lookup"><span data-stu-id="ea705-103">ControlMetrics method of the CIM\_MetricService class</span></span>

<span data-ttu-id="ea705-104">Aktiviert und deaktiviert die Sammlung von Metriken. **ControlMetrics** wird verwendet, um die Sammlung der einzelnen Typen von Metriken für ein [**CIM \_ ManagedElement,**](cim-managedelement.md)die Auflistung eines bestimmten Metriktyps für alle verwalteten Elemente oder die Auflistung einer bestimmten Metrik für ein bestimmtes verwaltetes Element zu steuern.</span><span class="sxs-lookup"><span data-stu-id="ea705-104">Enables and disables the collection of metrics.**ControlMetrics** is used to control the collection of each type of metric for a [**CIM\_ManagedElement**](cim-managedelement.md), the collection of a given type of metric for all managed elements, or the collection of a specific metric for a specific managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea705-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea705-105">Syntax</span></span>


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="ea705-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea705-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea705-107">*Betreff* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ea705-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea705-108">Ein [**CIM \_ ManagedElement,**](cim-managedelement.md) das verwaltete Elemente identifiziert, für die Metriken gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="ea705-108">A [**CIM\_ManagedElement**](cim-managedelement.md) that identifies managed element(s) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="ea705-109">*Definition* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ea705-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea705-110">Identifiziert eine [**CIM \_ BaseMetricDefinition,**](cim-basemetricdefinition.md) für die Metriken gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="ea705-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="ea705-111">*MetricCollectionEnabled* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ea705-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea705-112">Gibt den gewünschten Vorgang an, der für die Metriken durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea705-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="ea705-113">**Aktivieren** (2)</span><span class="sxs-lookup"><span data-stu-id="ea705-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="ea705-114">**Deaktivieren** (3)</span><span class="sxs-lookup"><span data-stu-id="ea705-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="ea705-115">**Zurücksetzen** (4)</span><span class="sxs-lookup"><span data-stu-id="ea705-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ea705-116">**DMTF Reserved** (..)</span><span class="sxs-lookup"><span data-stu-id="ea705-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ea705-117">**Reservierter Anbieter** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="ea705-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="ea705-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ea705-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="ea705-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea705-119">Return value</span></span>

<span data-ttu-id="ea705-120">Gibt bei Erfolg eine 0 zurück. andernfalls gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="ea705-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="ea705-121">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="ea705-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ea705-122">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="ea705-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ea705-123">**Fehler** (2)</span><span class="sxs-lookup"><span data-stu-id="ea705-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ea705-124">**Reservierte Methode** (..)</span><span class="sxs-lookup"><span data-stu-id="ea705-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ea705-125">**Herstellerspezifisch** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="ea705-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ea705-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea705-126">Requirements</span></span>



| <span data-ttu-id="ea705-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea705-127">Requirement</span></span> | <span data-ttu-id="ea705-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ea705-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea705-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea705-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ea705-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ea705-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ea705-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea705-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ea705-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ea705-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ea705-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea705-133">Namespace</span></span><br/>                | <span data-ttu-id="ea705-134">\\Root-Virtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ea705-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ea705-135">MOF</span><span class="sxs-lookup"><span data-stu-id="ea705-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea705-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea705-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea705-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ea705-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea705-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ea705-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ea705-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ea705-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea705-140">**CIM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="ea705-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




