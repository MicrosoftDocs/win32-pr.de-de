---
description: Zeigt die angegebenen Metriken an.
ms.assetid: 3716b5e6-b360-4719-a0f3-60b8d39deb31
title: Showmetrics-Methode der Msvm_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9823ea61864b0d87245ebe8b171195a2fd3c411a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868507"
---
# <a name="showmetrics-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="e14ab-103">Showmetrics-Methode der MSVM \_ metricservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="e14ab-103">ShowMetrics method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="e14ab-104">Zeigt die angegebenen Metriken an.</span><span class="sxs-lookup"><span data-stu-id="e14ab-104">Shows the specified metrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="e14ab-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e14ab-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="e14ab-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e14ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e14ab-107">*Betreff* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e14ab-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e14ab-108">Der Subject-Parameter identifiziert eine Instanz von [**CIM \_ managedelta**](cim-managedelement.md) , für die die Methode Verweise auf Instanzen von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) zurückgibt, die Metriken definieren, die für das **CIM- \_ managedelta-Element** erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="e14ab-108">The Subject parameter identifies an instance of [**CIM\_ManagedElement**](cim-managedelement.md) for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are being captured for the **CIM\_ManagedElement**.</span></span>

</dd> <dt>

<span data-ttu-id="e14ab-109">*Definition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e14ab-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e14ab-110">Der Definitions Parameter identifiziert eine Instanz von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="e14ab-110">The Definition parameter identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="e14ab-111">Die-Methode gibt Verweise auf Instanzen von [**CIM \_ managedelta**](cim-managedelement.md) aus, für die von der Instanz von **CIM \_ basemetricdefinition** definierte Metriken zur Erfassung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e14ab-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="e14ab-112">*Managedelements* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e14ab-112">*ManagedElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e14ab-113">Nach erfolgreichem Abschluss der-Methode kann der *managedelements* - \[ \] Parameter Verweise auf [**CIM \_ managedelate**](cim-managedelement.md) enthalten, für die die durch den *Definitions* Parameter identifizierte Metrik für die Sammlung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e14ab-113">Upon successful completion of the method, the *ManagedElements*\[\] parameter may contain references to [**CIM\_ManagedElement**](cim-managedelement.md) for which the metric identified by *Definition* parameter is available for collection.</span></span>

</dd> <dt>

<span data-ttu-id="e14ab-114">*DefinitionList* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e14ab-114">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e14ab-115">Nach erfolgreichem Abschluss der-Methode enthält der *DefinitionList* -Parameter möglicherweise Verweise auf Instanzen von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) , die Metriken definieren, die für die Sammlung für das [**CIM- \_ managedelta**](cim-managedelement.md) verfügbar sind, das durch den *Subject* -Parameter identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e14ab-115">Upon successful completion of the method, the *DefinitionList* parameter may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e14ab-116">*Metricnames* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e14ab-116">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e14ab-117">Nach erfolgreichem Abschluss der Methode muss jeder Array Index des *metricnames* -Parameters den Wert der Name-Eigenschaft für die Instanz von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) enthalten, auf die durch den entsprechenden Array Index des *DefinitionList* -Parameters verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e14ab-117">Upon successful completion of the method, each array index of the *MetricNames* parameter shall contain the value of the Name property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e14ab-118">*Metriccollectionaktivierte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e14ab-118">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e14ab-119">Der *metriccollectionaktivierte* Parameter gibt an, ob eine Metrik für ein verwaltetes Element erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="e14ab-119">The *MetricCollectionEnabled* parameter indicates whether a metric is being collected for a managed element.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="e14ab-120">**Aktivieren** (2)</span><span class="sxs-lookup"><span data-stu-id="e14ab-120">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="e14ab-121">**Deaktivieren** (3)</span><span class="sxs-lookup"><span data-stu-id="e14ab-121">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="e14ab-122">**Reserviert** (4)</span><span class="sxs-lookup"><span data-stu-id="e14ab-122">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e14ab-123">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="e14ab-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e14ab-124">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="e14ab-124">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="e14ab-125"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e14ab-125"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="e14ab-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e14ab-126">Return value</span></span>

<span data-ttu-id="e14ab-127">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="e14ab-127">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e14ab-128">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="e14ab-128">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e14ab-129">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="e14ab-129">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e14ab-130">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="e14ab-130">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e14ab-131">**Reservierte Methode** (..)</span><span class="sxs-lookup"><span data-stu-id="e14ab-131">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e14ab-132">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="e14ab-132">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e14ab-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e14ab-133">Requirements</span></span>



| <span data-ttu-id="e14ab-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e14ab-134">Requirement</span></span> | <span data-ttu-id="e14ab-135">Wert</span><span class="sxs-lookup"><span data-stu-id="e14ab-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e14ab-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e14ab-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e14ab-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e14ab-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="e14ab-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e14ab-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e14ab-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e14ab-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="e14ab-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="e14ab-140">Namespace</span></span><br/>                | <span data-ttu-id="e14ab-141">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e14ab-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e14ab-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e14ab-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e14ab-143"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e14ab-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e14ab-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e14ab-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e14ab-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e14ab-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e14ab-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e14ab-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e14ab-147">**MSVM \_ metricservice**</span><span class="sxs-lookup"><span data-stu-id="e14ab-147">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




