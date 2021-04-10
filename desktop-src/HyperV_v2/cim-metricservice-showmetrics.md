---
description: 'Meldet Folgendes: die Metriken, die für ein verwaltetes Element erfasst werden können, die verwalteten Elemente, für die eine Metrik, die durch eine Instanz von CIM \_ basemetricdefinition definiert ist, zur Erfassung verfügbar ist, und ob eine bestimmte Metrik aktuell für ein verwaltetes Element erfasst wird.'
ms.assetid: 5af430d2-9ab3-4bee-ad51-d9045b51172a
title: Showmetrics-Methode der CIM_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1e0e062adaefd6c6d9bdabe6f168bd64e789acc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131748"
---
# <a name="showmetrics-method-of-the-cim_metricservice-class"></a><span data-ttu-id="0a709-103">Showmetrics-Methode der CIM \_ metricservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="0a709-103">ShowMetrics method of the CIM\_MetricService class</span></span>

<span data-ttu-id="0a709-104">Meldet Folgendes: die Metriken, die für ein verwaltetes Element erfasst werden können, die verwalteten Elemente, für die eine Metrik, die durch eine Instanz von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) definiert ist, zur Erfassung verfügbar ist, und ob eine bestimmte Metrik aktuell für ein verwaltetes Element erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="0a709-104">Reports the following: the metrics available to be collected for a managed element, the managed elements for which a metric defined by an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) is available to be collected, and whether or not a particular metric is currently being collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a709-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a709-105">Syntax</span></span>


```mof
uint32 ShowMetrics(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_ManagedElement       REF ManagedElements[],
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="0a709-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a709-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a709-107">*Betreff* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a709-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a709-108">Identifiziert eine Instanz von [**CIM \_ managedelta**](cim-managedelement.md) , für die die Methode Verweise auf Instanzen von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) zurückgibt, die Metriken definieren, die für das **CIM- \_ managedelta-Element** erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="0a709-108">Identifies an instance of [**CIM\_ManagedElement**](cim-managedelement.md) for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are being captured for the **CIM\_ManagedElement**.</span></span>

</dd> <dt>

<span data-ttu-id="0a709-109">*Definition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a709-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a709-110">Identifiziert eine Instanz von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="0a709-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="0a709-111">Die-Methode gibt Verweise auf Instanzen von [**CIM \_ managedelta**](cim-managedelement.md) aus, für die von der Instanz von **CIM \_ basemetricdefinition** definierte Metriken zur Erfassung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="0a709-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="0a709-112">*Managedelements* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0a709-112">*ManagedElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a709-113">Bei Erfolg enthält möglicherweise Verweise auf [**CIM \_ managedelta**](cim-managedelement.md) -Objekte, für die die vom *Definitions* Parameter identifizierte Metrik für die Sammlung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0a709-113">On success, may contain references to [**CIM\_ManagedElement**](cim-managedelement.md) objects for which the metric identified by the *Definition* parameter is available for collection.</span></span>

</dd> <dt>

<span data-ttu-id="0a709-114">*DefinitionList* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0a709-114">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a709-115">Bei Erfolg enthält möglicherweise Verweise auf Instanzen von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) -Objekten, die Metriken definieren, die für die Sammlung für das [**CIM- \_ managedelta**](cim-managedelement.md) verfügbar sind, das durch den *Subject* -Parameter identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="0a709-115">On success, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) objects that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0a709-116">*Metricnames* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0a709-116">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a709-117">Bei Erfolg muss jeder Array Index den Wert der **Name** -Eigenschaft für die Instanz von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) enthalten, auf die durch den entsprechenden Array Index des *DefinitionList* -Parameters verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0a709-117">On success, each array index shall contain the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0a709-118">*Metriccollectionaktivierte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0a709-118">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a709-119">Gibt an, ob eine Metrik für ein verwaltetes Element erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="0a709-119">Indicates whether a metric is being collected for a managed element.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="0a709-120">**Aktivieren** (2)</span><span class="sxs-lookup"><span data-stu-id="0a709-120">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="0a709-121">**Deaktivieren** (3)</span><span class="sxs-lookup"><span data-stu-id="0a709-121">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="0a709-122">**Reserviert** (4)</span><span class="sxs-lookup"><span data-stu-id="0a709-122">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0a709-123">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="0a709-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0a709-124">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="0a709-124">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="0a709-125"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0a709-125"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="0a709-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a709-126">Return value</span></span>

<span data-ttu-id="0a709-127">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0a709-127">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="0a709-128">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="0a709-128">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0a709-129">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="0a709-129">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0a709-130">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="0a709-130">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0a709-131">**Reservierte Methode** (..)</span><span class="sxs-lookup"><span data-stu-id="0a709-131">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0a709-132">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="0a709-132">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0a709-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a709-133">Requirements</span></span>



| <span data-ttu-id="0a709-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a709-134">Requirement</span></span> | <span data-ttu-id="0a709-135">Wert</span><span class="sxs-lookup"><span data-stu-id="0a709-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a709-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a709-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0a709-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0a709-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0a709-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a709-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0a709-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0a709-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0a709-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="0a709-140">Namespace</span></span><br/>                | <span data-ttu-id="0a709-141">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0a709-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0a709-142">MOF</span><span class="sxs-lookup"><span data-stu-id="0a709-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a709-143"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0a709-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a709-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0a709-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a709-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0a709-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0a709-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a709-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a709-147">**CIM- \_ metricservice**</span><span class="sxs-lookup"><span data-stu-id="0a709-147">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




