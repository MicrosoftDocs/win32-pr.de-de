---
description: 'Gibt Folgendes an: die verfügbaren Metriken für alle Instanzen einer CIM-Klasse, die CIM-Klassen, für die eine von einer Instanz von CIM \_ basemetricdefinition definierte Metrik zur Erfassung verfügbar ist, und ob für ein verwaltetes Element zurzeit eine bestimmte Metrik erfasst wird.'
ms.assetid: 0115a5b5-2824-4c43-a8dc-757524c5d3dd
title: Showmetricsbyclass-Methode der CIM_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f843c835e6c92e39c4ac1f9628d0479b94a691bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865540"
---
# <a name="showmetricsbyclass-method-of-the-cim_metricservice-class"></a><span data-ttu-id="b6ea9-103">Showmetricsbyclass-Methode der CIM \_ metricservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="b6ea9-103">ShowMetricsByClass method of the CIM\_MetricService class</span></span>

<span data-ttu-id="b6ea9-104">Gibt Folgendes an: die verfügbaren Metriken für alle Instanzen einer CIM-Klasse, die CIM-Klassen, für die eine von einer Instanz von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) definierte Metrik zur Erfassung verfügbar ist, und ob für ein verwaltetes Element zurzeit eine bestimmte Metrik erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="b6ea9-104">Reports the following: the metrics available to be collected for all instances of a CIM class, The CIM classes for which a metric defined by an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) is available to be collected, and whether or not a particular metric is currently being collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6ea9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6ea9-105">Syntax</span></span>


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="b6ea9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6ea9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6ea9-107">*Betreff* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6ea9-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6ea9-108">Identifiziert eine CIM-Klasse, für die die-Methode Verweise auf Instanzen von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) zurückgibt, die Metriken definieren, die für alle Instanzen der Klasse aufgezeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="b6ea9-108">Identifies a CIM class for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are available to be captured for all instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="b6ea9-109">*Definition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6ea9-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6ea9-110">Identifiziert eine Instanz von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="b6ea9-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="b6ea9-111">Die-Methode gibt Verweise auf Instanzen von [**CIM \_ managedelta**](cim-managedelement.md) aus, für die von der Instanz von **CIM \_ basemetricdefinition** definierte Metriken zur Erfassung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b6ea9-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="b6ea9-112">*DefinitionList* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b6ea9-112">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6ea9-113">Bei Erfolg enthält möglicherweise Verweise auf Instanzen von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) -Objekten, die Metriken definieren, die für die Sammlung für das [**CIM- \_ managedelta**](cim-managedelement.md) verfügbar sind, das durch den *Subject* -Parameter identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="b6ea9-113">On success, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) objects that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b6ea9-114">*Metricnames* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b6ea9-114">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6ea9-115">Bei Erfolg muss jeder Array Index den Wert der **Name** -Eigenschaft für die Instanz von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) enthalten, auf die durch den entsprechenden Array Index des *DefinitionList* -Parameters verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b6ea9-115">On success, each array index shall contain the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b6ea9-116">*Metriccollectionaktivierte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b6ea9-116">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6ea9-117">Gibt an, ob eine Metrik für alle Instanzen einer Klasse verwalteter Elemente erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="b6ea9-117">Indicates whether a metric is being collected for all instances of a class of managed elements.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b6ea9-118">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="b6ea9-118">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b6ea9-119">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="b6ea9-119">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="b6ea9-120">**Reserviert** (4)</span><span class="sxs-lookup"><span data-stu-id="b6ea9-120">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b6ea9-121">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="b6ea9-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b6ea9-122">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="b6ea9-122">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="b6ea9-123"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b6ea9-123"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="b6ea9-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6ea9-124">Return value</span></span>

<span data-ttu-id="b6ea9-125">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b6ea9-125">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="b6ea9-126">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="b6ea9-126">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b6ea9-127">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="b6ea9-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b6ea9-128">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="b6ea9-128">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b6ea9-129">**Reservierte Methode** (..)</span><span class="sxs-lookup"><span data-stu-id="b6ea9-129">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b6ea9-130">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="b6ea9-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b6ea9-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6ea9-131">Requirements</span></span>



| <span data-ttu-id="b6ea9-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6ea9-132">Requirement</span></span> | <span data-ttu-id="b6ea9-133">Wert</span><span class="sxs-lookup"><span data-stu-id="b6ea9-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ea9-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6ea9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b6ea9-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b6ea9-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b6ea9-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6ea9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b6ea9-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b6ea9-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b6ea9-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="b6ea9-138">Namespace</span></span><br/>                | <span data-ttu-id="b6ea9-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b6ea9-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b6ea9-140">MOF</span><span class="sxs-lookup"><span data-stu-id="b6ea9-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6ea9-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b6ea9-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6ea9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b6ea9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6ea9-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b6ea9-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b6ea9-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6ea9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ea9-145">**CIM- \_ metricservice**</span><span class="sxs-lookup"><span data-stu-id="b6ea9-145">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




