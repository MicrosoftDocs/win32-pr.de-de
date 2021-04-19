---
description: Bietet die Möglichkeit, eine gefilterte Liste von CIM \_ basemetricvalue-Instanzen zurückzugeben.
ms.assetid: c207a0ef-11f1-42c4-af77-3dcf3fbff8a7
title: Getmetricvalues-Methode der CIM_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3c84ae9f5128edecfd3dd4cb591f811fdbd86010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350258"
---
# <a name="getmetricvalues-method-of-the-cim_metricservice-class"></a><span data-ttu-id="1ca4c-103">Getmetricvalues-Methode der CIM \_ metricservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="1ca4c-103">GetMetricValues method of the CIM\_MetricService class</span></span>

<span data-ttu-id="1ca4c-104">Bietet die Möglichkeit, eine gefilterte Liste von [**CIM \_ basemetricvalue**](cim-basemetricvalue.md) -Instanzen zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="1ca4c-104">Provides the ability to return a filtered list of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ca4c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ca4c-105">Syntax</span></span>


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a><span data-ttu-id="1ca4c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ca4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ca4c-107">*Definition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ca4c-107">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ca4c-108">Gibt eine [**CIM- \_ basemetricdefinition**](cim-basemetricdefinition.md) an, für die Metriken zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1ca4c-108">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="1ca4c-109">*Bereich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ca4c-109">*Range* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ca4c-110">Gibt an, wie die Instanzen ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="1ca4c-110">Identifies how the instances are selected.</span></span> <span data-ttu-id="1ca4c-111">Der Algorithmus zum Anordnen von Wert Instanzen ist metrikdefinitionsspezifisch.</span><span class="sxs-lookup"><span data-stu-id="1ca4c-111">The algorithm for ordering value instances is metric-definition specific.</span></span>

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="1ca4c-112">**Minimal** (2)</span><span class="sxs-lookup"><span data-stu-id="1ca4c-112">**Minimum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="1ca4c-113">**Maximum** (3)</span><span class="sxs-lookup"><span data-stu-id="1ca4c-113">**Maximum** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1ca4c-114">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="1ca4c-114">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="1ca4c-115">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="1ca4c-115">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="1ca4c-116">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ca4c-116">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ca4c-117">Gibt die maximale Anzahl von-Instanzen an, die von der-Methode zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1ca4c-117">Identifies the maximum number of instances to be returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="1ca4c-118">*Werte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1ca4c-118">*Values* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ca4c-119">Nach erfolgreichem Abschluss der-Methode enthält Verweise auf Instanzen von [**CIM \_ basemetricvalue**](cim-basemetricvalue.md), die entsprechend den Werten der Eingabeparameter gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="1ca4c-119">Upon successful completion of the method, contains references to instances of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md), filtered according to the values of the input parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ca4c-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ca4c-120">Return value</span></span>

<span data-ttu-id="1ca4c-121">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1ca4c-121">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="1ca4c-122">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="1ca4c-122">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ca4c-123">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="1ca4c-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1ca4c-124">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="1ca4c-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1ca4c-125">**Reservierte Methode** (..)</span><span class="sxs-lookup"><span data-stu-id="1ca4c-125">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1ca4c-126">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="1ca4c-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1ca4c-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ca4c-127">Requirements</span></span>



| <span data-ttu-id="1ca4c-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ca4c-128">Requirement</span></span> | <span data-ttu-id="1ca4c-129">Wert</span><span class="sxs-lookup"><span data-stu-id="1ca4c-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ca4c-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ca4c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1ca4c-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1ca4c-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1ca4c-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ca4c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1ca4c-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1ca4c-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1ca4c-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ca4c-134">Namespace</span></span><br/>                | <span data-ttu-id="1ca4c-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1ca4c-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1ca4c-136">MOF</span><span class="sxs-lookup"><span data-stu-id="1ca4c-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ca4c-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1ca4c-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ca4c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1ca4c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ca4c-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1ca4c-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1ca4c-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ca4c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ca4c-141">**CIM- \_ metricservice**</span><span class="sxs-lookup"><span data-stu-id="1ca4c-141">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




