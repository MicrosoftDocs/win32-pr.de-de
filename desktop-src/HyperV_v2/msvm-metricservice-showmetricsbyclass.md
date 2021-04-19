---
description: Zeigt Metriken nach Klasse an.
ms.assetid: a08c0749-b60b-4b8a-996f-b3bbaf1fb2d3
title: Showmetricsbyclass-Methode der Msvm_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 93f132b24c6c20826b1551e979c128b1aa38c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349201"
---
# <a name="showmetricsbyclass-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="48b16-103">Showmetricsbyclass-Methode der MSVM \_ metricservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="48b16-103">ShowMetricsByClass method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="48b16-104">Zeigt Metriken nach Klasse an.</span><span class="sxs-lookup"><span data-stu-id="48b16-104">Shows metrics by class.</span></span>

## <a name="syntax"></a><span data-ttu-id="48b16-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="48b16-105">Syntax</span></span>


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="48b16-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="48b16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48b16-107">*Betreff* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48b16-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48b16-108">Identifiziert eine CIM-Klasse, für die die-Methode Verweise auf Instanzen von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) zurückgibt, die Metriken definieren, die für alle Instanzen der Klasse aufgezeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="48b16-108">Identifies a CIM class for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are available to be captured for all instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="48b16-109">*Definition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48b16-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48b16-110">Identifiziert eine Instanz von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="48b16-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="48b16-111">Die-Methode gibt Verweise auf Instanzen von [**CIM \_ managedelta**](cim-managedelement.md) aus, für die von der Instanz von **CIM \_ basemetricdefinition** definierte Metriken zur Erfassung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="48b16-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="48b16-112">*DefinitionList* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="48b16-112">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48b16-113">Nach erfolgreichem Abschluss der-Methode enthält möglicherweise Verweise auf Instanzen von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) , die Metriken definieren, die für die Sammlung für das [**CIM- \_ managedelta**](cim-managedelement.md) verfügbar sind, das durch den *Subject* -Parameter identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="48b16-113">Upon successful completion of the method, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="48b16-114">*Metricnames* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="48b16-114">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48b16-115">Nach erfolgreichem Abschluss der-Methode enthält jeder Array Index den Wert der **Name** -Eigenschaft für die Instanz von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) , auf die durch den entsprechenden Array Index des *DefinitionList* -Parameters verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="48b16-115">Upon successful completion of the method, each array index contains the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="48b16-116">*Metriccollectionaktivierte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="48b16-116">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48b16-117">Gibt an, ob eine Metrik für alle Instanzen einer Klasse verwalteter Elemente erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="48b16-117">Indicates whether a metric is being collected for all instances of a class of managed elements.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="48b16-118">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="48b16-118">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="48b16-119">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="48b16-119">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="48b16-120">**Reserviert** (4)</span><span class="sxs-lookup"><span data-stu-id="48b16-120">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="48b16-121">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="48b16-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="48b16-122">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="48b16-122">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="48b16-123"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="48b16-123"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="48b16-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48b16-124">Return value</span></span>

<span data-ttu-id="48b16-125">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="48b16-125">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="48b16-126">**Erfolg** ()</span><span class="sxs-lookup"><span data-stu-id="48b16-126">**Success** ()</span></span>
</dt> <dt>

<span data-ttu-id="48b16-127">**Nicht unterstützt** ()</span><span class="sxs-lookup"><span data-stu-id="48b16-127">**Not Supported** ()</span></span>
</dt> <dt>

<span data-ttu-id="48b16-128">Fehler **()**</span><span class="sxs-lookup"><span data-stu-id="48b16-128">**Failed** ()</span></span>
</dt> <dt>

<span data-ttu-id="48b16-129">**Reservierte Methode** ()</span><span class="sxs-lookup"><span data-stu-id="48b16-129">**Method Reserved** ()</span></span>
</dt> <dt>

<span data-ttu-id="48b16-130">**Hersteller spezifisch** ()</span><span class="sxs-lookup"><span data-stu-id="48b16-130">**Vendor Specific** ()</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="48b16-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48b16-131">Requirements</span></span>



| <span data-ttu-id="48b16-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48b16-132">Requirement</span></span> | <span data-ttu-id="48b16-133">Wert</span><span class="sxs-lookup"><span data-stu-id="48b16-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48b16-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48b16-134">Minimum supported client</span></span><br/> | <span data-ttu-id="48b16-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="48b16-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="48b16-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48b16-136">Minimum supported server</span></span><br/> | <span data-ttu-id="48b16-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="48b16-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="48b16-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="48b16-138">Namespace</span></span><br/>                | <span data-ttu-id="48b16-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="48b16-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="48b16-140">MOF</span><span class="sxs-lookup"><span data-stu-id="48b16-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48b16-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="48b16-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="48b16-142">DLL</span><span class="sxs-lookup"><span data-stu-id="48b16-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48b16-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="48b16-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="48b16-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48b16-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48b16-145">**MSVM \_ metricservice**</span><span class="sxs-lookup"><span data-stu-id="48b16-145">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




