---
description: Enthält Akku Informationen.
ms.assetid: 6a236f48-5a06-4537-a769-bd68e5c0eb27
title: BATTERY_INFORMATION-Struktur (poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 1e892a14263822ddd009b162c6343975e1689683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356162"
---
# <a name="battery_information-structure"></a><span data-ttu-id="c040e-103">Struktur der Akku \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="c040e-103">BATTERY\_INFORMATION structure</span></span>

<span data-ttu-id="c040e-104">Enthält Akku Informationen.</span><span class="sxs-lookup"><span data-stu-id="c040e-104">Contains battery information.</span></span> <span data-ttu-id="c040e-105">Diese Struktur wird von dem IOCTL-Steuerelement Code für die [**\_ Akku \_ Abfrage \_ Informationen**](ioctl-battery-query-information.md) zurückgegeben, wenn die Informationen auf der Ebene "Akku Information" angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="c040e-105">This structure is returned by the [**IOCTL\_BATTERY\_QUERY\_INFORMATION**](ioctl-battery-query-information.md) control code when the BatteryInformation information level is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="c040e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c040e-106">Syntax</span></span>


```C++
typedef struct _BATTERY_INFORMATION {
  ULONG Capabilities;
  UCHAR Technology;
  UCHAR Reserved[3];
  UCHAR Chemistry[4];
  ULONG DesignedCapacity;
  ULONG FullChargedCapacity;
  ULONG DefaultAlert1;
  ULONG DefaultAlert2;
  ULONG CriticalBias;
  ULONG CycleCount;
} BATTERY_INFORMATION, *PBATTERY_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="c040e-107">Member</span><span class="sxs-lookup"><span data-stu-id="c040e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c040e-108">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="c040e-108">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="c040e-109">Die Akku Funktionen.</span><span class="sxs-lookup"><span data-stu-id="c040e-109">The battery capabilities.</span></span> <span data-ttu-id="c040e-110">Dieser Member kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c040e-110">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="c040e-111">Wert</span><span class="sxs-lookup"><span data-stu-id="c040e-111">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="c040e-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c040e-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CAPACITY_RELATIVE"></span><span id="battery_capacity_relative"></span><dl> <span data-ttu-id="c040e-113"><dt>**Akku \_ Kapazitäts \_ Verhältnis**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="c040e-113"><dt>**BATTERY\_CAPACITY\_RELATIVE**</dt> <dt>0x40000000</dt></span></span> </dl>                    | <span data-ttu-id="c040e-114">Gibt an, dass die Akkukapazität und die Preisinformationen relativ und nicht in bestimmten Einheiten sind.</span><span class="sxs-lookup"><span data-stu-id="c040e-114">Indicates that the battery capacity and rate information are relative, and not in any specific units.</span></span> <span data-ttu-id="c040e-115">Wenn dieses Bit nicht festgelegt ist, sind die Berichterstattungs Einheiten Milliwatt-Stunden (MWh) für Kapazität und Milliwatt (MW) für die Rate.</span><span class="sxs-lookup"><span data-stu-id="c040e-115">If this bit is not set, the reporting units are milliwatt-hours (mWh) for capacity and milliwatts (mW) for rate.</span></span> <span data-ttu-id="c040e-116">Wenn dieses Bit festgelegt ist, können alle Verweise auf Einheiten in der anderen Akku Dokumentation ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c040e-116">If this bit is set, all references to units in the other battery documentation can be ignored.</span></span> <span data-ttu-id="c040e-117">Alle rateninformationen werden in Einheiten pro Stunde gemeldet.</span><span class="sxs-lookup"><span data-stu-id="c040e-117">All rate information is reported in units per hour.</span></span> <span data-ttu-id="c040e-118">Wenn z. b. die vollständig berechnete Kapazität als 100 gemeldet wird, bedeutet eine Rate von 200, dass der Akku seine gesamte Kapazität in einer halben Stunde verbrauchen wird.</span><span class="sxs-lookup"><span data-stu-id="c040e-118">For example, if the fully charged capacity is reported as 100, a rate of 200 indicates that the battery will use all of its capacity in half an hour.</span></span><br/> |
| <span id="BATTERY_IS_SHORT_TERM"></span><span id="battery_is_short_term"></span><dl> <span data-ttu-id="c040e-119"><dt>**Akku \_ Ist \_ kurzfristiger \_**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="c040e-119"><dt>**BATTERY\_IS\_SHORT\_TERM**</dt> <dt>0x20000000</dt></span></span> </dl>                               | <span data-ttu-id="c040e-120">Gibt an, dass der normale Vorgang für eine ausfallsichere Funktion gilt.</span><span class="sxs-lookup"><span data-stu-id="c040e-120">Indicates that the normal operation is for a fail-safe function.</span></span> <span data-ttu-id="c040e-121">Wenn dieses Bit nicht festgelegt ist, wird erwartet, dass der Akku während der normalen System Verwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c040e-121">If this bit is not set the battery is expected to be used during normal system usage.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BATTERY_SET_CHARGE_SUPPORTED"></span><span id="battery_set_charge_supported"></span><dl> <span data-ttu-id="c040e-122"><dt>**Akku \_ Set \_ - \_ Unterstützung**</dt> für <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="c040e-122"><dt>**BATTERY\_SET\_CHARGE\_SUPPORTED**</dt> <dt>0x00000001</dt></span></span> </dl>          | <span data-ttu-id="c040e-123">Gibt an, dass die Anforderungen zum Festlegen von Informationen vom Typ "Akkuladung" von diesem Akku Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c040e-123">Indicates that set information requests of the type BatteryCharge are supported by this battery device.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="BATTERY_SET_DISCHARGE_SUPPORTED"></span><span id="battery_set_discharge_supported"></span><dl> <span data-ttu-id="c040e-124"><dt>**Akku \_ Festlegen von " \_ entladen" \_ unterstützt**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="c040e-124"><dt>**BATTERY\_SET\_DISCHARGE\_SUPPORTED**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="c040e-125">Gibt an, dass Set Information-Anforderungen vom Typ "Akku Entladung" von diesem Akku Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c040e-125">Indicates that set information requests of the type BatteryDischarge are supported by this battery device.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="BATTERY_SYSTEM_BATTERY"></span><span id="battery_system_battery"></span><dl> <span data-ttu-id="c040e-126"><dt>**Akku \_ System \_ Batterie**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="c040e-126"><dt>**BATTERY\_SYSTEM\_BATTERY**</dt> <dt>0x80000000</dt></span></span> </dl>                             | <span data-ttu-id="c040e-127">Gibt an, dass der Akku eine allgemeine Stromversorgung zum Ausführen des Systems bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c040e-127">Indicates that the battery can provide general power to run the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="c040e-128">**Technologie**</span><span class="sxs-lookup"><span data-stu-id="c040e-128">**Technology**</span></span>
</dt> <dd>

<span data-ttu-id="c040e-129">Die Akku Technologie.</span><span class="sxs-lookup"><span data-stu-id="c040e-129">The battery technology.</span></span> <span data-ttu-id="c040e-130">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c040e-130">This member can be one of the following values.</span></span>



| <span data-ttu-id="c040e-131">Wert</span><span class="sxs-lookup"><span data-stu-id="c040e-131">Value</span></span>                                                                        | <span data-ttu-id="c040e-132">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c040e-132">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="c040e-133"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c040e-133"><dt>0</dt></span></span> </dl> | <span data-ttu-id="c040e-134">Nicht aufladbarer Akku, z. b. "Alkaline".</span><span class="sxs-lookup"><span data-stu-id="c040e-134">Nonrechargeable battery, for example, alkaline.</span></span><br/> |
| <dl> <span data-ttu-id="c040e-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c040e-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="c040e-136">Akku Akku, z. b. Lead Acid.</span><span class="sxs-lookup"><span data-stu-id="c040e-136">Rechargeable battery, for example, lead acid.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="c040e-137">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="c040e-137">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="c040e-138">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="c040e-138">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c040e-139">**Chemi**</span><span class="sxs-lookup"><span data-stu-id="c040e-139">**Chemistry**</span></span>
</dt> <dd>

<span data-ttu-id="c040e-140">Eine abgekürzte Zeichenfolge, die die Chemie des Akkus angibt.</span><span class="sxs-lookup"><span data-stu-id="c040e-140">An abbreviated character string that indicates the battery's chemistry.</span></span> <span data-ttu-id="c040e-141">Diese Zeichenfolge muss nicht notwendigerweise mit 0 (null) beendet werden.</span><span class="sxs-lookup"><span data-stu-id="c040e-141">This string is not necessarily zero-terminated.</span></span> <span data-ttu-id="c040e-142">Im folgenden finden Sie eine partielle Liste der Abkürzungen, die zurückgegeben werden können, und die zugeordneten chemisserien.</span><span class="sxs-lookup"><span data-stu-id="c040e-142">The following is a partial list of abbreviations that can be returned and the associated chemistries.</span></span>



| <span data-ttu-id="c040e-143">Unicode-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c040e-143">Unicode string</span></span>                                                                                                                                           | <span data-ttu-id="c040e-144">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c040e-144">Meaning</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="PbAc"></span><span id="pbac"></span><span id="PBAC"></span><dl> <span data-ttu-id="c040e-145"><dt>**Pbac**</dt></span><span class="sxs-lookup"><span data-stu-id="c040e-145"><dt>**PbAc**</dt></span></span> </dl> | <span data-ttu-id="c040e-146">Führende Acid</span><span class="sxs-lookup"><span data-stu-id="c040e-146">Lead Acid</span></span><br/>                       |
| <span id="LION"></span><span id="lion"></span><dl> <span data-ttu-id="c040e-147"><dt>**Herz**</dt></span><span class="sxs-lookup"><span data-stu-id="c040e-147"><dt>**LION**</dt></span></span> </dl>                        | <span data-ttu-id="c040e-148">Lithium-Ionen</span><span class="sxs-lookup"><span data-stu-id="c040e-148">Lithium Ion</span></span><br/>                     |
| <span id="Li-I"></span><span id="li-i"></span><span id="LI-I"></span><dl> <span data-ttu-id="c040e-149"><dt>**Li-I**</dt></span><span class="sxs-lookup"><span data-stu-id="c040e-149"><dt>**Li-I**</dt></span></span> </dl> | <span data-ttu-id="c040e-150">Lithium-Ionen</span><span class="sxs-lookup"><span data-stu-id="c040e-150">Lithium Ion</span></span><br/>                     |
| <span id="NiCd"></span><span id="nicd"></span><span id="NICD"></span><dl> <span data-ttu-id="c040e-151"><dt>**NiCd**</dt></span><span class="sxs-lookup"><span data-stu-id="c040e-151"><dt>**NiCd**</dt></span></span> </dl> | <span data-ttu-id="c040e-152">Nickel-Kadmium</span><span class="sxs-lookup"><span data-stu-id="c040e-152">Nickel Cadmium</span></span><br/>                  |
| <span id="NiMH"></span><span id="nimh"></span><span id="NIMH"></span><dl> <span data-ttu-id="c040e-153"><dt>**NiMH**</dt></span><span class="sxs-lookup"><span data-stu-id="c040e-153"><dt>**NiMH**</dt></span></span> </dl> | <span data-ttu-id="c040e-154">Nickel-Metal-Hydride</span><span class="sxs-lookup"><span data-stu-id="c040e-154">Nickel Metal Hydride</span></span><br/>            |
| <span id="NiZn"></span><span id="nizn"></span><span id="NIZN"></span><dl> <span data-ttu-id="c040e-155"><dt>**NiZn**</dt></span><span class="sxs-lookup"><span data-stu-id="c040e-155"><dt>**NiZn**</dt></span></span> </dl> | <span data-ttu-id="c040e-156">Nickel-Zink</span><span class="sxs-lookup"><span data-stu-id="c040e-156">Nickel Zinc</span></span><br/>                     |
| <span id="RAM"></span><span id="ram"></span><dl> <span data-ttu-id="c040e-157"><dt>**RAM**</dt></span><span class="sxs-lookup"><span data-stu-id="c040e-157"><dt>**RAM**</dt></span></span> </dl>                           | <span data-ttu-id="c040e-158">Aufladbare Alkaline-Manganese</span><span class="sxs-lookup"><span data-stu-id="c040e-158">Rechargeable Alkaline-Manganese</span></span><br/> |



 

<span data-ttu-id="c040e-159">Andere chemisserien werden möglicherweise in der Zukunft angezeigt, und Ihr Code sollte in der Lage sein, Sie zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c040e-159">Other chemistries may appear in the future and your code should be able to handle them.</span></span>

</dd> <dt>

<span data-ttu-id="c040e-160">**Designedcapacity**</span><span class="sxs-lookup"><span data-stu-id="c040e-160">**DesignedCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="c040e-161">Die theoretische Kapazität des Akkus, wenn neu, in MWh, es sei denn, die Akku \_ Kapazität \_ ist relativ eingestellt.</span><span class="sxs-lookup"><span data-stu-id="c040e-161">The theoretical capacity of the battery when new, in mWh unless BATTERY\_CAPACITY\_RELATIVE is set.</span></span> <span data-ttu-id="c040e-162">In diesem Fall sind die Einheiten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="c040e-162">In that case, the units are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="c040e-163">**Fullchargedcapacity**</span><span class="sxs-lookup"><span data-stu-id="c040e-163">**FullChargedCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="c040e-164">Die aktuell vollständig berechnete Kapazität des Akkus in MWh (oder relativ).</span><span class="sxs-lookup"><span data-stu-id="c040e-164">The battery's current fully charged capacity in mWh (or relative).</span></span> <span data-ttu-id="c040e-165">Vergleichen Sie diesen Wert mit **designedcapacity** , um den Akku Verschleiß einzuschätzen.</span><span class="sxs-lookup"><span data-stu-id="c040e-165">Compare this value to **DesignedCapacity** to estimate the battery's wear.</span></span>

</dd> <dt>

<span data-ttu-id="c040e-166">**DefaultAlert1**</span><span class="sxs-lookup"><span data-stu-id="c040e-166">**DefaultAlert1**</span></span>
</dt> <dd>

<span data-ttu-id="c040e-167">Die von dem Hersteller vorgeschlagene Kapazität in MWh, bei der eine geringe Akku Warnung auftritt.</span><span class="sxs-lookup"><span data-stu-id="c040e-167">The manufacturer's suggested capacity, in mWh, at which a low battery alert should occur.</span></span> <span data-ttu-id="c040e-168">Die Definitionen niedriger variieren von Hersteller zu Hersteller.</span><span class="sxs-lookup"><span data-stu-id="c040e-168">Definitions of low vary from manufacturer to manufacturer.</span></span> <span data-ttu-id="c040e-169">Im Allgemeinen tritt ein Warn Status vor einem niedrigen Status auf, aber Sie sollten nicht davon ausgehen, dass dies immer der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="c040e-169">In general, a warning state will occur before a low state, but you should not assume that it always will.</span></span> <span data-ttu-id="c040e-170">Um das Risiko eines Daten Verlusts zu verringern, wird dieser Wert normalerweise als Standardeinstellung für den Alarm "kritischer Akku" verwendet.</span><span class="sxs-lookup"><span data-stu-id="c040e-170">To reduce risk of data loss, this value is usually used as the default setting for the critical battery alarm.</span></span>

</dd> <dt>

<span data-ttu-id="c040e-171">**DefaultAlert2**</span><span class="sxs-lookup"><span data-stu-id="c040e-171">**DefaultAlert2**</span></span>
</dt> <dd>

<span data-ttu-id="c040e-172">Die von dem Hersteller vorgeschlagene Kapazität in MWh, bei der eine Warnung zu einem Akku ausgelöst werden sollte.</span><span class="sxs-lookup"><span data-stu-id="c040e-172">The manufacturer's suggested capacity, in mWh, at which a warning battery alert should occur.</span></span> <span data-ttu-id="c040e-173">Die Definitionen der Warnung variieren von Hersteller zu Hersteller.</span><span class="sxs-lookup"><span data-stu-id="c040e-173">Definitions of warning vary from manufacturer to manufacturer.</span></span> <span data-ttu-id="c040e-174">Im Allgemeinen tritt ein Warn Status vor einem niedrigen Status auf, aber Sie sollten nicht davon ausgehen, dass dies immer der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="c040e-174">In general, a warning state will occur before a low state, but you should not assume that it always will.</span></span> <span data-ttu-id="c040e-175">Um das Risiko eines Daten Verlusts zu verringern, wird dieser Wert normalerweise als Standardeinstellung für den Alarm mit niedrigem Akku verwendet.</span><span class="sxs-lookup"><span data-stu-id="c040e-175">To reduce risk of data loss, this value is usually used as the default setting for the low battery alarm.</span></span>

</dd> <dt>

<span data-ttu-id="c040e-176">**Criticalbias**</span><span class="sxs-lookup"><span data-stu-id="c040e-176">**CriticalBias**</span></span>
</dt> <dd>

<span data-ttu-id="c040e-177">Eine Abweichung von 0 (null) in MWh, die auf die Akku Berichterstattung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c040e-177">A bias from zero, in mWh, which is applied to battery reporting.</span></span> <span data-ttu-id="c040e-178">Einige Akkus reservieren eine geringe Belastung, die aus den Kapazitäts Werten des Akkus besteht, um "0" als kritischen Akku Pegel anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c040e-178">Some batteries reserve a small charge that is biased out of the battery's capacity values to show "0" as the critical battery level.</span></span> <span data-ttu-id="c040e-179">Kritischer Bias ist analog zum Festlegen eines Kraftstoff Messgerätes, um "Empty" anzuzeigen, wenn mehrere Benzin verbleiben.</span><span class="sxs-lookup"><span data-stu-id="c040e-179">Critical bias is analogous to setting a fuel gauge to show "empty" when there are several liters of fuel left.</span></span>

</dd> <dt>

<span data-ttu-id="c040e-180">**Cyclecount**</span><span class="sxs-lookup"><span data-stu-id="c040e-180">**CycleCount**</span></span>
</dt> <dd>

<span data-ttu-id="c040e-181">Die Anzahl der in der Akku Erfahrung/Entladezyklen.</span><span class="sxs-lookup"><span data-stu-id="c040e-181">The number of charge/discharge cycles the battery has experienced.</span></span> <span data-ttu-id="c040e-182">Dies bietet die Möglichkeit, den Akku Verschleiß zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="c040e-182">This provides a means to determine the battery's wear.</span></span> <span data-ttu-id="c040e-183">Wenn der Akku keinen Zyklen unterstützt, ist dieser Member 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c040e-183">If the battery does not support a cycle counter, this member is zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c040e-184">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c040e-184">Remarks</span></span>

<span data-ttu-id="c040e-185">Im Allgemeinen tritt ein Warn Status vor einem niedrigen Status auf, aber Sie sollten nicht davon ausgehen, dass dies der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="c040e-185">Generally, a warning state occurs before a low state, but you should not assume it will.</span></span> <span data-ttu-id="c040e-186">Es ist möglich, einen Akku abzufragen und zu ermitteln, dass weder eine Warnstufe aufgetreten ist, noch den Akku abzufragen und ihn so zu finden, dass beide Ebenen erreicht wurden.</span><span class="sxs-lookup"><span data-stu-id="c040e-186">It is possible to poll a battery and find that neither alert level has occurred, and poll the battery again and find it discharged to the extent that both levels have been achieved.</span></span> <span data-ttu-id="c040e-187">Dies weist möglicherweise darauf hin, dass Sie nicht oft genug Abfragen.</span><span class="sxs-lookup"><span data-stu-id="c040e-187">This may indicate that you are not polling often enough.</span></span> <span data-ttu-id="c040e-188">Es kann auch darauf hindeuten, dass der Akku nicht sehr lange eine Abrechnung durchläuft und schneller als erwartet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c040e-188">It may also indicate that the battery is unable to hold a charge for very long and is discharging more rapidly than you expected.</span></span> <span data-ttu-id="c040e-189">Ein solcher Akku ist möglicherweise am Ende der nützlichen Lebensdauer oder beschädigt.</span><span class="sxs-lookup"><span data-stu-id="c040e-189">Such a battery may be nearing the end of its useful life, or it may be damaged.</span></span>

## <a name="requirements"></a><span data-ttu-id="c040e-190">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c040e-190">Requirements</span></span>



| <span data-ttu-id="c040e-191">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c040e-191">Requirement</span></span> | <span data-ttu-id="c040e-192">Wert</span><span class="sxs-lookup"><span data-stu-id="c040e-192">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c040e-193">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c040e-193">Minimum supported client</span></span><br/> | <span data-ttu-id="c040e-194">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c040e-194">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="c040e-195">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c040e-195">Minimum supported server</span></span><br/> | <span data-ttu-id="c040e-196">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c040e-196">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="c040e-197">Header</span><span class="sxs-lookup"><span data-stu-id="c040e-197">Header</span></span><br/>                   | <dl> <span data-ttu-id="c040e-198"><dt>Poclass. h; </dt> <dt>Batclass. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="c040e-198"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c040e-199">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c040e-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c040e-200">**IOCTL- \_ Akku \_ Abfrage \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="c040e-200">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> </dl>

 

 




