---
description: Ermöglicht die Angabe des Zeitpunkts, an dem die Metrik Erfassung gestartet werden soll, und die Angabe der gewünschten Stichproben Intervallzeit für die regelmäßige Datensammlung.
ms.assetid: 3dd6dc16-a618-49ff-bbaf-cfa25c249cf1
title: Controlsampletimes-Methode der CIM_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e32d184199ff7ddc63be5d1fcfcd4ea376dad89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358498"
---
# <a name="controlsampletimes-method-of-the-cim_metricservice-class"></a><span data-ttu-id="9307f-103">Controlsampletimes-Methode der CIM \_ metricservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="9307f-103">ControlSampleTimes method of the CIM\_MetricService class</span></span>

<span data-ttu-id="9307f-104">Ermöglicht die Angabe des Zeitpunkts, an dem die Metrik Erfassung gestartet werden soll, und die Angabe der gewünschten Stichproben Intervallzeit für die regelmäßige Datensammlung.</span><span class="sxs-lookup"><span data-stu-id="9307f-104">Allows specification of the point in time metric gathering is to be started and to specify the preferred sample interval time for periodic data gathering.</span></span>

<span data-ttu-id="9307f-105">Wenn die Stichprobenentnahme für zusätzliche Metriken gestartet wird, können die von dieser Methode angegebenen Einstellungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9307f-105">Whenever sampling for additional metrics is started, the settings specified by this method may be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="9307f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9307f-106">Syntax</span></span>


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a><span data-ttu-id="9307f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9307f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9307f-108">*Startsampletime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9307f-108">*StartSampleTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9307f-109">Der Zeitpunkt, zu dem die Stichprobenentnahme für die Metriken gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9307f-109">Point in time when sampling for the metrics is to be started.</span></span>

<span data-ttu-id="9307f-110">Der Wert 99990101000000.000000 + 000 gibt an, dass die Stichprobenentnahme bei der nächsten Synchronisierung mit der vollen Stunde gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9307f-110">A value of 99990101000000.000000+000 shall indicate that sampling should start at the next time it is synchronized to the full hour.</span></span> <span data-ttu-id="9307f-111">Die Stichprobenentnahme wird mit der vollen Stunde synchronisiert, wenn in Sekunden seit Mitternacht Modulo-Stichproben Intervall (in Sekunden) gleich 0 ist.</span><span class="sxs-lookup"><span data-stu-id="9307f-111">Sampling is synchronized to the full hour if seconds since midnight modulo sample interval in seconds is equal to 0.</span></span>

</dd> <dt>

<span data-ttu-id="9307f-112">*Preferredsampleingeterval* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9307f-112">*PreferredSampleInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9307f-113">Die bevorzugte Stichproben Intervallzeit.</span><span class="sxs-lookup"><span data-stu-id="9307f-113">Preferred sample interval time.</span></span> <span data-ttu-id="9307f-114">Um korrelierbare Metriken zu erhalten, empfiehlt es sich, das Stichproben Intervall so zu wählen, dass 3600 Modulo Sample Interval Time in Sekunden gleich 0 ist.</span><span class="sxs-lookup"><span data-stu-id="9307f-114">In order to get correlatable metrics, it is recommended that the sample interval be chosen in a way that 3600 modulo sample interval time in seconds is equal to 0.</span></span>

<span data-ttu-id="9307f-115">Es liegt in der Verantwortung der CIM Metric Service-Implementierung, zu entscheiden, ob die angeforderte Stichproben Intervallzeit berücksichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="9307f-115">It is the responsibility of the CIM metric service implementation to decide whether the requested sample interval time is honored.</span></span>

<span data-ttu-id="9307f-116">Der CIM-Client kann überprüfen, ob die metrikanbieter die angeforderte Stichproben Intervallzeit überprüfen, indem Sie verwandte basemetricdefinition-Instanzen abrufen und den Inhalt von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md)überprüfen.**Sampleingeterval** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9307f-116">The CIM client can check whether or not the metric providers are honoring the requested sample interval time by retrieving related BaseMetricDefinition instances and checking the contents of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**SampleInterval** property.</span></span>

</dd> <dt>

<span data-ttu-id="9307f-117">*Restarterfassung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9307f-117">*RestartGathering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9307f-118">" **True** ", um anzufordern, dass das Sammeln aller Metriken, die dem metrikdienst zugeordnet sind, mit diesem Methoden Aufrufvorgang neu gestartet</span><span class="sxs-lookup"><span data-stu-id="9307f-118">**TRUE** to request that gathering of all metrics associated to the metric service is re-started with this method call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9307f-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9307f-119">Return value</span></span>

<span data-ttu-id="9307f-120">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9307f-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="9307f-121">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="9307f-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9307f-122">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="9307f-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9307f-123">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="9307f-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9307f-124">**Reservierte Methode** (..)</span><span class="sxs-lookup"><span data-stu-id="9307f-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9307f-125">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="9307f-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9307f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9307f-126">Requirements</span></span>



| <span data-ttu-id="9307f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9307f-127">Requirement</span></span> | <span data-ttu-id="9307f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="9307f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9307f-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9307f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9307f-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9307f-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="9307f-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9307f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9307f-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9307f-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="9307f-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="9307f-133">Namespace</span></span><br/>                | <span data-ttu-id="9307f-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9307f-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9307f-135">MOF</span><span class="sxs-lookup"><span data-stu-id="9307f-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9307f-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9307f-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9307f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9307f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9307f-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9307f-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9307f-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9307f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9307f-140">**CIM- \_ metricservice**</span><span class="sxs-lookup"><span data-stu-id="9307f-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




