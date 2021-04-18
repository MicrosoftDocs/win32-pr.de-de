---
description: Steuert Metriken nach Klasse.
ms.assetid: f848fdec-561b-4be0-b1e9-a59e15196d1d
title: Controlmetricsbyclass-Methode der Msvm_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4149da6327edf774afda20e64f34ae0958f7c3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351546"
---
# <a name="controlmetricsbyclass-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="ffd1e-103">Controlmetricsbyclass-Methode der MSVM \_ metricservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="ffd1e-103">ControlMetricsByClass method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="ffd1e-104">Steuert Metriken nach Klasse.</span><span class="sxs-lookup"><span data-stu-id="ffd1e-104">Controls metrics by class.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffd1e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffd1e-105">Syntax</span></span>


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="ffd1e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffd1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffd1e-107">*Betreff* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ffd1e-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd1e-108">Identifiziert die CIM-Klasse, für die Metriken gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="ffd1e-108">Identifies the CIM class for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="ffd1e-109">*Definition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ffd1e-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd1e-110">Gibt eine [**CIM- \_ basemetricdefinition**](cim-basemetricdefinition.md) an, für die Metriken gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="ffd1e-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="ffd1e-111">*Metriccollectionaktivierte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ffd1e-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd1e-112">Gibt den für die Metriken auszuführenden gewünschten Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="ffd1e-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="ffd1e-113">**Aktivieren** (2)</span><span class="sxs-lookup"><span data-stu-id="ffd1e-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="ffd1e-114">**Deaktivieren** (3)</span><span class="sxs-lookup"><span data-stu-id="ffd1e-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="ffd1e-115">**Zurücksetzen** (4)</span><span class="sxs-lookup"><span data-stu-id="ffd1e-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ffd1e-116">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="ffd1e-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ffd1e-117">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="ffd1e-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="ffd1e-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ffd1e-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="ffd1e-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ffd1e-119">Return value</span></span>

<span data-ttu-id="ffd1e-120">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="ffd1e-120">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ffd1e-121">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="ffd1e-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ffd1e-122">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="ffd1e-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ffd1e-123">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="ffd1e-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ffd1e-124">**Reservierte Methode** (..)</span><span class="sxs-lookup"><span data-stu-id="ffd1e-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ffd1e-125">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="ffd1e-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ffd1e-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffd1e-126">Requirements</span></span>



| <span data-ttu-id="ffd1e-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffd1e-127">Requirement</span></span> | <span data-ttu-id="ffd1e-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ffd1e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd1e-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ffd1e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ffd1e-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ffd1e-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ffd1e-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ffd1e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ffd1e-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ffd1e-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ffd1e-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="ffd1e-133">Namespace</span></span><br/>                | <span data-ttu-id="ffd1e-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ffd1e-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ffd1e-135">MOF</span><span class="sxs-lookup"><span data-stu-id="ffd1e-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffd1e-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ffd1e-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffd1e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ffd1e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffd1e-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ffd1e-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ffd1e-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffd1e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffd1e-140">**MSVM \_ metricservice**</span><span class="sxs-lookup"><span data-stu-id="ffd1e-140">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




