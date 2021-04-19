---
description: Aktiviert und deaktiviert die Auflistung von Metriken.
ms.assetid: 1a53c7a7-c0fc-49d7-ad1b-d185d776ede5
title: Controlmetricsbyclass-Methode der CIM_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 46e961b298c212a7635599818fb1f7079805372d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362264"
---
# <a name="controlmetricsbyclass-method-of-the-cim_metricservice-class"></a><span data-ttu-id="24f01-103">Controlmetricsbyclass-Methode der CIM \_ metricservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="24f01-103">ControlMetricsByClass method of the CIM\_MetricService class</span></span>

<span data-ttu-id="24f01-104">Aktiviert und deaktiviert die Auflistung von Metriken. **Controlmetricsbyclass** wird verwendet, um die Sammlung der einzelnen metrikmetriken für alle Instanzen einer Klasse oder die Auflistung einer bestimmten Metrik für alle Instanzen einer Klasse zu steuern.</span><span class="sxs-lookup"><span data-stu-id="24f01-104">Enables and disables the collection of metrics.**ControlMetricsByClass** is used to control the collection of each type of metric for all instances of a class or the collection of a specific metric for all instances of a class.</span></span>

## <a name="syntax"></a><span data-ttu-id="24f01-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="24f01-105">Syntax</span></span>


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="24f01-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="24f01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24f01-107">*Betreff* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24f01-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f01-108">Identifiziert die [**CIM \_ managedelta ement**](cim-managedelement.md) -Klasse, für die Metriken gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="24f01-108">Identifies the [**CIM\_ManagedElement**](cim-managedelement.md) class for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="24f01-109">*Definition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24f01-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f01-110">Gibt eine [**CIM- \_ basemetricdefinition**](cim-basemetricdefinition.md) an, für die Metriken gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="24f01-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="24f01-111">*Metriccollectionaktivierte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24f01-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f01-112">Gibt den für die Metriken auszuführenden gewünschten Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="24f01-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="24f01-113">**Aktivieren** (2)</span><span class="sxs-lookup"><span data-stu-id="24f01-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="24f01-114">**Deaktivieren** (3)</span><span class="sxs-lookup"><span data-stu-id="24f01-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="24f01-115">**Zurücksetzen** (4)</span><span class="sxs-lookup"><span data-stu-id="24f01-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="24f01-116">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="24f01-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="24f01-117">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="24f01-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="24f01-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="24f01-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="24f01-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24f01-119">Return value</span></span>

<span data-ttu-id="24f01-120">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="24f01-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="24f01-121">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="24f01-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="24f01-122">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="24f01-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="24f01-123">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="24f01-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="24f01-124">**Reservierte Methode** (..)</span><span class="sxs-lookup"><span data-stu-id="24f01-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="24f01-125">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="24f01-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="24f01-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24f01-126">Requirements</span></span>



| <span data-ttu-id="24f01-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24f01-127">Requirement</span></span> | <span data-ttu-id="24f01-128">Wert</span><span class="sxs-lookup"><span data-stu-id="24f01-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24f01-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24f01-129">Minimum supported client</span></span><br/> | <span data-ttu-id="24f01-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="24f01-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="24f01-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24f01-131">Minimum supported server</span></span><br/> | <span data-ttu-id="24f01-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="24f01-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="24f01-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="24f01-133">Namespace</span></span><br/>                | <span data-ttu-id="24f01-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="24f01-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="24f01-135">MOF</span><span class="sxs-lookup"><span data-stu-id="24f01-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24f01-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="24f01-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="24f01-137">DLL</span><span class="sxs-lookup"><span data-stu-id="24f01-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24f01-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="24f01-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="24f01-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24f01-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24f01-140">**CIM- \_ metricservice**</span><span class="sxs-lookup"><span data-stu-id="24f01-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




