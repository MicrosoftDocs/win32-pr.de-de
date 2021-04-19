---
description: Wird verwendet, um die Sammlung von Metriken für ein verwaltetes Element oder Elemente zu steuern.
ms.assetid: 3DC043ED-A790-4322-BF80-55961E9946C2
title: Controlmetrics-Methode der Msvm_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b12fbf71b860571bb3bb5ee06cb58483e782f479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362575"
---
# <a name="controlmetrics-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="4fec9-103">Controlmetrics-Methode der MSVM \_ metricservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="4fec9-103">ControlMetrics method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="4fec9-104">Wird verwendet, um die Sammlung von Metriken für ein verwaltetes Element oder Elemente zu steuern.</span><span class="sxs-lookup"><span data-stu-id="4fec9-104">Used to control the collection of metrics for a managed element or elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fec9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fec9-105">Syntax</span></span>


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="4fec9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fec9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fec9-107">*Betreff* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fec9-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fec9-108">Eine [**CIM \_ managedelements**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Instanz, die die verwalteten Elemente identifiziert, für die Metriken erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="4fec9-108">A [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) instance that identifies the managed elements for which metrics will be collected.</span></span> <span data-ttu-id="4fec9-109">Wenn dieser Parameter **null** ist, werden die Metriken für alle verwalteten Elemente, die dem *Definitions* Parameter zugeordnet sind, gesammelt.</span><span class="sxs-lookup"><span data-stu-id="4fec9-109">If this parameter is **Null**, the metrics for all the managed elements associated with the *Definition* parameter will be collected.</span></span>

</dd> <dt>

<span data-ttu-id="4fec9-110">*Definition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fec9-110">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fec9-111">Eine [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md) -Instanz, die angibt, welche Metriken erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="4fec9-111">An [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance that specifies which metrics will be collected.</span></span> <span data-ttu-id="4fec9-112">Wenn dieser Parameter **null** ist, werden die Metriken für alle Definitionen, die dem verwalteten Element zugeordnet sind, das durch den *Subject* -Parameter identifiziert wird, erfasst.</span><span class="sxs-lookup"><span data-stu-id="4fec9-112">If this parameter is **Null**, the metrics for all the definitions associated with the managed element identified by the *Subject* parameter will be collected</span></span>

</dd> <dt>

<span data-ttu-id="4fec9-113">*Metriccollectionaktivierte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fec9-113">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fec9-114">Gibt den Vorgang an, der für die metriksammlung auszuführen ist.</span><span class="sxs-lookup"><span data-stu-id="4fec9-114">Specifies the operation to perform on the metrics collection.</span></span> <span data-ttu-id="4fec9-115">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="4fec9-115">This must be one of the following values.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="4fec9-116"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Aktivieren** (2)</span><span class="sxs-lookup"><span data-stu-id="4fec9-116"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Enable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4fec9-117">Aktivieren Sie die metriksammlung.</span><span class="sxs-lookup"><span data-stu-id="4fec9-117">Enable metrics collection.</span></span>

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="4fec9-118"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deaktivieren** (3)</span><span class="sxs-lookup"><span data-stu-id="4fec9-118"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4fec9-119">Deaktivieren Sie die metrikauflistung.</span><span class="sxs-lookup"><span data-stu-id="4fec9-119">Disable metrics collection.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="4fec9-120"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (4)</span><span class="sxs-lookup"><span data-stu-id="4fec9-120"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4fec9-121">Zurücksetzen von Metrikwerten.</span><span class="sxs-lookup"><span data-stu-id="4fec9-121">Reset metrics values.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4fec9-122"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="4fec9-122"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="4fec9-123"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="4fec9-123"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="4fec9-124"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4fec9-124"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="4fec9-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4fec9-125">Return value</span></span>

<span data-ttu-id="4fec9-126">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="4fec9-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4fec9-127">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="4fec9-127">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4fec9-128">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="4fec9-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4fec9-129">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="4fec9-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4fec9-130">**Reservierte Methode** (..)</span><span class="sxs-lookup"><span data-stu-id="4fec9-130">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4fec9-131">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="4fec9-131">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="4fec9-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4fec9-132">Remarks</span></span>

<span data-ttu-id="4fec9-133">Bei dieser Methode tritt in den folgenden Fällen ein Fehler auf:</span><span class="sxs-lookup"><span data-stu-id="4fec9-133">This method will fail in the following instances:</span></span>

-   <span data-ttu-id="4fec9-134">Die Parameter " *Subject* " und " *Definition* " sind beide **null**.</span><span class="sxs-lookup"><span data-stu-id="4fec9-134">The *Subject* and *Definition* parameters are both **Null**.</span></span>
-   <span data-ttu-id="4fec9-135">Die Parameter " *Subject* " und " *Definition* " sind nicht **null** , und es ist keine Instanz von [**MSVM \_ metricdefforme**](msvm-metricdefforme.md) vorhanden, die die beiden Instanzen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="4fec9-135">The *Subject* and *Definition* parameters are both non-**Null** and there is not an instance of [**Msvm\_MetricDefForME**](msvm-metricdefforme.md) that associates the two instances.</span></span>
-   <span data-ttu-id="4fec9-136">Der *Definitions* Parameter ist ein Verweis auf eine Instanz von [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md) , die nicht mit MSVM [**\_ metricservice**](msvm-metricservice.md) über [**MSVM \_ serviceaffectselements**](msvm-serviceaffectselement.md)verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="4fec9-136">The *Definition* parameter is a reference to an instance of [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) that is not associated with the [**Msvm\_MetricService**](msvm-metricservice.md) through [**Msvm\_ServiceAffectsElement**](msvm-serviceaffectselement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4fec9-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fec9-137">Requirements</span></span>



| <span data-ttu-id="4fec9-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fec9-138">Requirement</span></span> | <span data-ttu-id="4fec9-139">Wert</span><span class="sxs-lookup"><span data-stu-id="4fec9-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fec9-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fec9-140">Minimum supported client</span></span><br/> | <span data-ttu-id="4fec9-141">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fec9-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4fec9-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fec9-142">Minimum supported server</span></span><br/> | <span data-ttu-id="4fec9-143">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fec9-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4fec9-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="4fec9-144">Namespace</span></span><br/>                | <span data-ttu-id="4fec9-145">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4fec9-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4fec9-146">MOF</span><span class="sxs-lookup"><span data-stu-id="4fec9-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4fec9-147"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4fec9-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4fec9-148">DLL</span><span class="sxs-lookup"><span data-stu-id="4fec9-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fec9-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4fec9-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4fec9-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fec9-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fec9-151">**MSVM \_ metricservice**</span><span class="sxs-lookup"><span data-stu-id="4fec9-151">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

