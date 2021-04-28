---
description: 'ControlMetricsByClass-Methode der CIM_MetricService-Klasse: Aktiviert und deaktiviert die Sammlung von Metriken.'
ms.assetid: 1a53c7a7-c0fc-49d7-ad1b-d185d776ede5
title: ControlMetricsByClass-Methode der CIM_MetricService-Klasse
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
ms.openlocfilehash: fda8407d49ed3eec7ff86abc94ced6b63d2d77c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109708"
---
# <a name="controlmetricsbyclass-method-of-the-cim_metricservice-class"></a><span data-ttu-id="addef-103">ControlMetricsByClass-Methode der CIM \_ MetricService-Klasse</span><span class="sxs-lookup"><span data-stu-id="addef-103">ControlMetricsByClass method of the CIM\_MetricService class</span></span>

<span data-ttu-id="addef-104">Aktiviert und deaktiviert die Sammlung von Metriken. **ControlMetricsByClass** wird verwendet, um die Auflistung der einzelnen Metriktypen für alle Instanzen einer Klasse oder die Sammlung einer bestimmten Metrik für alle Instanzen einer Klasse zu steuern.</span><span class="sxs-lookup"><span data-stu-id="addef-104">Enables and disables the collection of metrics.**ControlMetricsByClass** is used to control the collection of each type of metric for all instances of a class or the collection of a specific metric for all instances of a class.</span></span>

## <a name="syntax"></a><span data-ttu-id="addef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="addef-105">Syntax</span></span>


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="addef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="addef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="addef-107">*Betreff* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="addef-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="addef-108">Identifiziert die [**CIM \_ ManagedElement-Klasse,**](cim-managedelement.md) für die Metriken gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="addef-108">Identifies the [**CIM\_ManagedElement**](cim-managedelement.md) class for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="addef-109">*Definition* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="addef-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="addef-110">Identifiziert eine [**CIM \_ BaseMetricDefinition,**](cim-basemetricdefinition.md) für die Metriken gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="addef-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="addef-111">*MetricCollectionEnabled* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="addef-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="addef-112">Gibt den gewünschten Vorgang an, der für die Metriken ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="addef-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="addef-113">**Aktivieren** (2)</span><span class="sxs-lookup"><span data-stu-id="addef-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="addef-114">**Deaktivieren** (3)</span><span class="sxs-lookup"><span data-stu-id="addef-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="addef-115">**Zurücksetzen** (4)</span><span class="sxs-lookup"><span data-stu-id="addef-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="addef-116">**DMTF Reserved** (..)</span><span class="sxs-lookup"><span data-stu-id="addef-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="addef-117">**Reservierter Anbieter** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="addef-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="addef-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="addef-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="addef-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="addef-119">Return value</span></span>

<span data-ttu-id="addef-120">Gibt bei Erfolg den Wert 0 zurück. andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="addef-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="addef-121">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="addef-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="addef-122">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="addef-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="addef-123">**Fehler** (2)</span><span class="sxs-lookup"><span data-stu-id="addef-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="addef-124">**Reservierte Methode** (..)</span><span class="sxs-lookup"><span data-stu-id="addef-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="addef-125">**Herstellerspezifisch** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="addef-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="addef-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="addef-126">Requirements</span></span>



| <span data-ttu-id="addef-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="addef-127">Requirement</span></span> | <span data-ttu-id="addef-128">Wert</span><span class="sxs-lookup"><span data-stu-id="addef-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="addef-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="addef-129">Minimum supported client</span></span><br/> | <span data-ttu-id="addef-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="addef-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="addef-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="addef-131">Minimum supported server</span></span><br/> | <span data-ttu-id="addef-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="addef-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="addef-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="addef-133">Namespace</span></span><br/>                | <span data-ttu-id="addef-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="addef-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="addef-135">MOF</span><span class="sxs-lookup"><span data-stu-id="addef-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="addef-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="addef-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="addef-137">DLL</span><span class="sxs-lookup"><span data-stu-id="addef-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="addef-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="addef-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="addef-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="addef-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="addef-140">**CIM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="addef-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




