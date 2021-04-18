---
description: Ruft Metrikwerte ab.
ms.assetid: 71c614ef-a005-45aa-9999-a19dc9f9c0df
title: Getmetricvalues-Methode der Msvm_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe3e32b21ec0baa497fcef781e1b48fae37fbf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350918"
---
# <a name="getmetricvalues-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="41cff-103">Getmetricvalues-Methode der MSVM \_ metricservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="41cff-103">GetMetricValues method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="41cff-104">Ruft Metrikwerte ab.</span><span class="sxs-lookup"><span data-stu-id="41cff-104">Gets metric values.</span></span>

## <a name="syntax"></a><span data-ttu-id="41cff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="41cff-105">Syntax</span></span>


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a><span data-ttu-id="41cff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="41cff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41cff-107">*Definition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41cff-107">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41cff-108">Gibt eine [**CIM- \_ basemetricdefinition**](cim-basemetricdefinition.md) an, für die Metriken zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="41cff-108">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="41cff-109">*Bereich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41cff-109">*Range* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41cff-110">Gibt an, wie die Instanzen ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="41cff-110">Identifies how the instances are selected.</span></span> <span data-ttu-id="41cff-111">Der Algorithmus zum Anordnen von Wert Instanzen ist metrikdefinitionsspezifisch.</span><span class="sxs-lookup"><span data-stu-id="41cff-111">The algorithm for ordering value instances is metric definition specific.</span></span>

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="41cff-112">**Minimal** (2)</span><span class="sxs-lookup"><span data-stu-id="41cff-112">**Minimum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="41cff-113">**Maximum** (3)</span><span class="sxs-lookup"><span data-stu-id="41cff-113">**Maximum** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="41cff-114">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="41cff-114">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="41cff-115">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="41cff-115">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="41cff-116">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41cff-116">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41cff-117">Gibt die maximale Anzahl von-Instanzen an, die von der-Methode zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="41cff-117">Identifies the maximum number of instances to be returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="41cff-118">*Werte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="41cff-118">*Values* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41cff-119">Nach erfolgreichem Abschluss der-Methode enthält Verweise auf Instanzen von [**CIM \_ basemetricvalue**](cim-basemetricvalue.md), die entsprechend den Werten der Eingabeparameter gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="41cff-119">Upon successful completion of the method, contains references to instances of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md), filtered according to the values of the input parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41cff-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41cff-120">Return value</span></span>

<span data-ttu-id="41cff-121">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="41cff-121">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="41cff-122">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="41cff-122">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="41cff-123">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="41cff-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="41cff-124">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="41cff-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="41cff-125">**Reservierte Methode** (..)</span><span class="sxs-lookup"><span data-stu-id="41cff-125">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="41cff-126">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="41cff-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="41cff-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41cff-127">Requirements</span></span>



| <span data-ttu-id="41cff-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41cff-128">Requirement</span></span> | <span data-ttu-id="41cff-129">Wert</span><span class="sxs-lookup"><span data-stu-id="41cff-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41cff-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41cff-130">Minimum supported client</span></span><br/> | <span data-ttu-id="41cff-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="41cff-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="41cff-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41cff-132">Minimum supported server</span></span><br/> | <span data-ttu-id="41cff-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="41cff-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="41cff-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="41cff-134">Namespace</span></span><br/>                | <span data-ttu-id="41cff-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="41cff-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="41cff-136">MOF</span><span class="sxs-lookup"><span data-stu-id="41cff-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41cff-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="41cff-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="41cff-138">DLL</span><span class="sxs-lookup"><span data-stu-id="41cff-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41cff-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="41cff-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="41cff-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41cff-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41cff-141">**MSVM \_ metricservice**</span><span class="sxs-lookup"><span data-stu-id="41cff-141">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




