---
description: Legt die Beispiel Zeiten für das Steuerelement fest.
ms.assetid: 17ffa106-8b6b-4077-895c-03400505c2a0
title: Controlsampletimes-Methode der Msvm_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1bb3797523153592610714406306035f59fc844c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215926"
---
# <a name="controlsampletimes-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="62211-103">Controlsampletimes-Methode der MSVM \_ metricservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="62211-103">ControlSampleTimes method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="62211-104">Legt die Beispiel Zeiten für das Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="62211-104">Sets the control sample times.</span></span>

## <a name="syntax"></a><span data-ttu-id="62211-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="62211-105">Syntax</span></span>


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a><span data-ttu-id="62211-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="62211-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62211-107">*Startsampletime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62211-107">*StartSampleTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62211-108">Der Zeitpunkt, zu dem die Stichprobenentnahme für die Metriken gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="62211-108">Point in time when sampling for the metrics is to be started.</span></span>

<span data-ttu-id="62211-109">Der Wert 99990101000000.000000 + 000 gibt an, dass die Stichprobenentnahme bei der nächsten Synchronisierung mit der vollen Stunde gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="62211-109">A value of 99990101000000.000000+000 shall indicate that sampling should start at the next time it is synchronized to the full hour.</span></span> <span data-ttu-id="62211-110">Die Stichprobenentnahme wird mit der vollen Stunde synchronisiert, wenn in Sekunden seit Mitternacht Modulo-Stichproben Intervall (in Sekunden) gleich 0 ist.</span><span class="sxs-lookup"><span data-stu-id="62211-110">Sampling is synchronized to the full hour if seconds since midnight modulo sample interval in seconds is equal to 0.</span></span>

</dd> <dt>

<span data-ttu-id="62211-111">*Preferredsampleingeterval* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62211-111">*PreferredSampleInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62211-112">Die bevorzugte Stichproben Intervallzeit.</span><span class="sxs-lookup"><span data-stu-id="62211-112">Preferred sample interval time.</span></span> <span data-ttu-id="62211-113">Um korrelierbare Metriken zu erhalten, empfiehlt es sich, das Stichproben Intervall so zu wählen, dass 3600 Modulo Sample Interval Time in Sekunden gleich 0 ist.</span><span class="sxs-lookup"><span data-stu-id="62211-113">In order to get correlatable metrics, it is recommended that the sample interval be chosen in a way that 3600 modulo sample interval time in seconds is equal to 0.</span></span>

<span data-ttu-id="62211-114">Es liegt in der Verantwortung der CIM Metric Service-Implementierung, zu entscheiden, ob die angeforderte Stichproben Intervallzeit berücksichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="62211-114">It is the responsibility of the CIM metric service implementation to decide whether the requested sample interval time is honored.</span></span>

<span data-ttu-id="62211-115">Der CIM-Client kann überprüfen, ob die metrikanbieter die angeforderte Stichproben Intervallzeit berücksichtigen, indem Sie verwandte basemetricdefinition-Instanzen abrufen und den Inhalt der CIM \_ basemetricdefinition. sampleinterval-Eigenschaft überprüfen.</span><span class="sxs-lookup"><span data-stu-id="62211-115">The CIM client can check whether or not the metric providers are honoring the requested sample interval time by retrieving related BaseMetricDefinition instances and checking the contents of the "CIM\_BaseMetricDefinition.SampleInterval" property.</span></span>

</dd> <dt>

<span data-ttu-id="62211-116">*Restarterfassung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62211-116">*RestartGathering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62211-117">Boolescher Wert, der bei Festlegung auf "true" Anforderungen, dass das Sammeln aller Metriken, die dem metrikdienst zugeordnet sind, mit diesem Methoden Aufrufsatz neu gestartet</span><span class="sxs-lookup"><span data-stu-id="62211-117">Boolean that when set to TRUE requests that gathering of all metrics associated to the metric service is re-started with this method call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62211-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62211-118">Return value</span></span>

<span data-ttu-id="62211-119">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="62211-119">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="62211-120">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="62211-120">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="62211-121">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="62211-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="62211-122">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="62211-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="62211-123">**Reservierte Methode** (..)</span><span class="sxs-lookup"><span data-stu-id="62211-123">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="62211-124">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="62211-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="62211-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62211-125">Requirements</span></span>



| <span data-ttu-id="62211-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62211-126">Requirement</span></span> | <span data-ttu-id="62211-127">Wert</span><span class="sxs-lookup"><span data-stu-id="62211-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62211-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62211-128">Minimum supported client</span></span><br/> | <span data-ttu-id="62211-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="62211-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="62211-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62211-130">Minimum supported server</span></span><br/> | <span data-ttu-id="62211-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="62211-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="62211-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="62211-132">Namespace</span></span><br/>                | <span data-ttu-id="62211-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="62211-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="62211-134">MOF</span><span class="sxs-lookup"><span data-stu-id="62211-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62211-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="62211-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="62211-136">DLL</span><span class="sxs-lookup"><span data-stu-id="62211-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62211-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="62211-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="62211-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62211-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62211-139">**MSVM \_ metricservice**</span><span class="sxs-lookup"><span data-stu-id="62211-139">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




