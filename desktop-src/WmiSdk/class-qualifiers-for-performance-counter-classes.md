---
description: Geben Sie Informationen zum Leistungs Objekt an, dem die WMI-Leistungs Objektklasse zugeordnet ist.
ms.assetid: 7b8b7f00-95d8-4c1e-8638-157d0f4c7c32
ms.tgt_platform: multiple
title: Klassen Qualifizierer für Leistungs Leistungsdaten Klassen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4910af88ce7f96fda1b5f9b7ecd7a33479fc130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364086"
---
# <a name="class-qualifiers-for-performance-counter-classes"></a><span data-ttu-id="29fb7-103">Klassen Qualifizierer für Leistungs Leistungsdaten Klassen</span><span class="sxs-lookup"><span data-stu-id="29fb7-103">Class Qualifiers for Performance Counter Classes</span></span>

<span data-ttu-id="29fb7-104">Klassen Qualifizierer geben Informationen über das Leistungs Objekt an, dem die WMI- [Leistungs Objektklasse](/windows/desktop/CIMWin32Prov/performance-counter-classes) zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="29fb7-104">Class qualifiers specify information about the performance object to which the WMI [performance counter class](/windows/desktop/CIMWin32Prov/performance-counter-classes) is mapped.</span></span> <span data-ttu-id="29fb7-105">Weitere Informationen finden Sie unter über [Wachen von Leistungsdaten](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="29fb7-105">For more information, see [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

-   [<span data-ttu-id="29fb7-106">Qualifizierer für Rohdaten und formatierte performanceclasses</span><span class="sxs-lookup"><span data-stu-id="29fb7-106">Qualifiers for Raw and Formatted PerformanceClasses</span></span>](#qualifiers-for-raw-and-formatted-performanceclasses)
-   [<span data-ttu-id="29fb7-107">Qualifizierer für rohleistungs Klassen</span><span class="sxs-lookup"><span data-stu-id="29fb7-107">Qualifiers for Raw Performance Classes</span></span>](#)
-   [<span data-ttu-id="29fb7-108">Qualifizierer für formatierte Leistungsklassen</span><span class="sxs-lookup"><span data-stu-id="29fb7-108">Qualifiers for Formatted Performance Classes</span></span>](#)
-   [<span data-ttu-id="29fb7-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="29fb7-109">Related topics</span></span>](#related-topics)


<span data-ttu-id="29fb7-110">Leistungs Zählers – bestimmte Qualifizierer werden automatisch durch den Anbieter "WbemPerfClass" an [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klassen und-Eigenschaften in root CIMv2 angefügt \\ .</span><span class="sxs-lookup"><span data-stu-id="29fb7-110">Performance counter–specific qualifiers are automatically attached by the "WbemPerfClass" provider to [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes and properties in Root\\CIMv2.</span></span>

<span data-ttu-id="29fb7-111">Diese Informationen gelten für alle Instanzen der-Klasse.</span><span class="sxs-lookup"><span data-stu-id="29fb7-111">This information applies to all instances of the class.</span></span> <span data-ttu-id="29fb7-112">Einige Qualifizierer mit **booleschen** Werten, die immer **false** sind, sind möglicherweise nicht für bestimmte Klassen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="29fb7-112">Some qualifiers with **Boolean** values that are always **False** may not be present on specific classes.</span></span>

## <a name="qualifiers-for-raw-and-formatted-performanceclasses"></a><span data-ttu-id="29fb7-113">Qualifizierer für Rohdaten und formatierte performanceclasses</span><span class="sxs-lookup"><span data-stu-id="29fb7-113">Qualifiers for Raw and Formatted PerformanceClasses</span></span>

<span data-ttu-id="29fb7-114">Die folgenden Qualifizierer gelten für alle Klassen, die von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) und [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="29fb7-114">The following qualifiers apply to all classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="29fb7-115"><span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Über**</span><span class="sxs-lookup"><span data-stu-id="29fb7-115"><span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Cooked**</span></span>
</dt> <dd>

<span data-ttu-id="29fb7-116">**boolean**</span><span class="sxs-lookup"><span data-stu-id="29fb7-116">**boolean**</span></span>

<span data-ttu-id="29fb7-117">Gibt an, ob die Klasse gekochte Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="29fb7-117">Indicates whether the class contains cooked data.</span></span>

</dd> <dt>

<span data-ttu-id="29fb7-118"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Display Name**</span><span class="sxs-lookup"><span data-stu-id="29fb7-118"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="29fb7-119">**string**</span><span class="sxs-lookup"><span data-stu-id="29fb7-119">**string**</span></span>

<span data-ttu-id="29fb7-120">Der Name des Leistungsobjekts.</span><span class="sxs-lookup"><span data-stu-id="29fb7-120">Performance object name.</span></span> <span data-ttu-id="29fb7-121">Weitere Informationen finden Sie unter [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="29fb7-121">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

</dd> <dt>

<span data-ttu-id="29fb7-122"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**Detail Level**</span><span class="sxs-lookup"><span data-stu-id="29fb7-122"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span></span>
</dt> <dd>

<span data-ttu-id="29fb7-123">**sint32**</span><span class="sxs-lookup"><span data-stu-id="29fb7-123">**sint32**</span></span>

<span data-ttu-id="29fb7-124">Stellt keine Detaildaten bereit.</span><span class="sxs-lookup"><span data-stu-id="29fb7-124">Does not provide detail data.</span></span> <span data-ttu-id="29fb7-125">Enthält immer den Wert 100.</span><span class="sxs-lookup"><span data-stu-id="29fb7-125">Always contains value of 100.</span></span>

</dd> <dt>

<span data-ttu-id="29fb7-126"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Schem**</span><span class="sxs-lookup"><span data-stu-id="29fb7-126"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Dynamic**</span></span>
</dt> <dd>

<span data-ttu-id="29fb7-127">**boolean**</span><span class="sxs-lookup"><span data-stu-id="29fb7-127">**boolean**</span></span>

<span data-ttu-id="29fb7-128">Ist immer auf " **true** " festgelegt, da Instanzen immer dynamisch sind.</span><span class="sxs-lookup"><span data-stu-id="29fb7-128">Always set to **True** because instances are always dynamic.</span></span>

</dd> <dt>

<span data-ttu-id="29fb7-129"><span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**Genericperfctr**</span><span class="sxs-lookup"><span data-stu-id="29fb7-129"><span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**</span></span>
</dt> <dd>

<span data-ttu-id="29fb7-130">**boolean**</span><span class="sxs-lookup"><span data-stu-id="29fb7-130">**boolean**</span></span>

<span data-ttu-id="29fb7-131">Gibt an, ob die Klasse aus einer Legacy-Leistungs Bibliothek stammt.</span><span class="sxs-lookup"><span data-stu-id="29fb7-131">Indicates whether the class comes from a legacy performance library.</span></span> <span data-ttu-id="29fb7-132">Immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="29fb7-132">Always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="29fb7-133"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**Helpindex**</span><span class="sxs-lookup"><span data-stu-id="29fb7-133"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span></span>
</dt> <dd>

<span data-ttu-id="29fb7-134">**sint32**</span><span class="sxs-lookup"><span data-stu-id="29fb7-134">**sint32**</span></span>

<span data-ttu-id="29fb7-135">Indizes sind nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="29fb7-135">Indexes are no longer valid.</span></span> <span data-ttu-id="29fb7-136">Dieser Qualifizierer ist immer NULL.</span><span class="sxs-lookup"><span data-stu-id="29fb7-136">This qualifier is always zero.</span></span>

</dd> <dt>

<span data-ttu-id="29fb7-137"><span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="29fb7-137"><span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf**</span></span> 
</dt> <dd>

<span data-ttu-id="29fb7-138">**boolean**</span><span class="sxs-lookup"><span data-stu-id="29fb7-138">**boolean**</span></span>

<span data-ttu-id="29fb7-139">Gibt an, dass die Klasse eine Hochleistungs Klasse ist.</span><span class="sxs-lookup"><span data-stu-id="29fb7-139">Indicates that the class is a high-performance class.</span></span> <span data-ttu-id="29fb7-140">Immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="29fb7-140">Always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="29fb7-141"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Konfigurations**</span><span class="sxs-lookup"><span data-stu-id="29fb7-141"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**</span></span>
</dt> <dd>

<span data-ttu-id="29fb7-142">**sint32**</span><span class="sxs-lookup"><span data-stu-id="29fb7-142">**sint32**</span></span>

<span data-ttu-id="29fb7-143">Gebietsschemabezeichner</span><span class="sxs-lookup"><span data-stu-id="29fb7-143">Locale identifier.</span></span> <span data-ttu-id="29fb7-144">Der Wert ist immer 1033 (US-Englisch).</span><span class="sxs-lookup"><span data-stu-id="29fb7-144">Value is always 1033 (U.S. English).</span></span>

</dd> <dt>

<span data-ttu-id="29fb7-145"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**Perfindex**</span><span class="sxs-lookup"><span data-stu-id="29fb7-145"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span></span>
</dt> <dd>

<span data-ttu-id="29fb7-146">**int32**</span><span class="sxs-lookup"><span data-stu-id="29fb7-146">**int32**</span></span>

<span data-ttu-id="29fb7-147">Indizes sind nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="29fb7-147">Indexes are no longer valid.</span></span> <span data-ttu-id="29fb7-148">Dieser Qualifizierer ist immer NULL.</span><span class="sxs-lookup"><span data-stu-id="29fb7-148">This qualifier is always zero.</span></span>

</dd> <dt>

<span data-ttu-id="29fb7-149"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Ab**</span><span class="sxs-lookup"><span data-stu-id="29fb7-149"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="29fb7-150">**string**</span><span class="sxs-lookup"><span data-stu-id="29fb7-150">**string**</span></span>

<span data-ttu-id="29fb7-151">Der Name des Instanzanbieters.</span><span class="sxs-lookup"><span data-stu-id="29fb7-151">Name of the instance provider.</span></span> <span data-ttu-id="29fb7-152">Der Wert ist "WbemPerfV2".</span><span class="sxs-lookup"><span data-stu-id="29fb7-152">Value is "WbemPerfV2".</span></span>

</dd> <dt>

<span data-ttu-id="29fb7-153"><span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**</span><span class="sxs-lookup"><span data-stu-id="29fb7-153"><span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**</span></span>
</dt> <dd>

<span data-ttu-id="29fb7-154">**string**</span><span class="sxs-lookup"><span data-stu-id="29fb7-154">**string**</span></span>

<span data-ttu-id="29fb7-155">Der Name des Treibers im Schlüssel des **lokalen HKEY-Computers \_ \_ \\ CurrentControlSet \\ Services** , unter dem sich der Leistungs Schlüssel befinden kann.</span><span class="sxs-lookup"><span data-stu-id="29fb7-155">Name of the driver in the **HKEY\_LOCAL\_MACHINE\\CurrentControlSet\\Services** key, under which the performance key can be located.</span></span> <span data-ttu-id="29fb7-156">Dieser Name ist auch der Name des Dienstanbieter, der den Leistungswert bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="29fb7-156">This name is also the name of the service that provides the performance counter.</span></span>

</dd> <dt>

<span data-ttu-id="29fb7-157"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span><span class="sxs-lookup"><span data-stu-id="29fb7-157"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span></span>
</dt> <dd>

<span data-ttu-id="29fb7-158">**boolean**</span><span class="sxs-lookup"><span data-stu-id="29fb7-158">**boolean**</span></span>

<span data-ttu-id="29fb7-159">**True** gibt an, dass nur eine einzelne Instanz der Klasse vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="29fb7-159">If **True**, indicates that only a single instance of the class exists.</span></span>

</dd> </dl>

## <a name="qualifiers-for-raw-performance-classes"></a><span data-ttu-id="29fb7-160">Qualifizierer für rohleistungs Klassen</span><span class="sxs-lookup"><span data-stu-id="29fb7-160">Qualifiers for Raw Performance Classes</span></span>

<span data-ttu-id="29fb7-161">Die folgenden Qualifizierer gelten für alle Klassen, die von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="29fb7-161">The following qualifiers apply to all classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span>

<dl> <dt>

<span data-ttu-id="29fb7-162"><span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Aufwendigen**</span><span class="sxs-lookup"><span data-stu-id="29fb7-162"><span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Costly**</span></span>
</dt> <dd>

<span data-ttu-id="29fb7-163">**boolean**</span><span class="sxs-lookup"><span data-stu-id="29fb7-163">**boolean**</span></span>

<span data-ttu-id="29fb7-164">Gibt an, ob das Abrufen von Instanzen dieser Klasse ein kostspieliger Vorgang ist.</span><span class="sxs-lookup"><span data-stu-id="29fb7-164">Indicates whether obtaining instances of this class is a costly operation.</span></span> <span data-ttu-id="29fb7-165">Wird immer auf **true** festgelegt, wenn Klassen mit \_ dem "teuren" an das Ende des Klassen namens angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="29fb7-165">Always set to **True** for classes with "\_Costly" appended to the end of the class name.</span></span>

</dd> <dt>

<span data-ttu-id="29fb7-166"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**Detail Level**</span><span class="sxs-lookup"><span data-stu-id="29fb7-166"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span></span>
</dt> <dd>

<span data-ttu-id="29fb7-167">**uint32**</span><span class="sxs-lookup"><span data-stu-id="29fb7-167">**uint32**</span></span>

<span data-ttu-id="29fb7-168">Stellt keine Detaildaten bereit.</span><span class="sxs-lookup"><span data-stu-id="29fb7-168">Does not provide detail data.</span></span> <span data-ttu-id="29fb7-169">Enthält immer den Wert 100.</span><span class="sxs-lookup"><span data-stu-id="29fb7-169">Always contains value of 100.</span></span>

</dd> <dt>

<span data-ttu-id="29fb7-170"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="29fb7-170"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span></span>
</dt> <dd>

<span data-ttu-id="29fb7-171">**boolean**</span><span class="sxs-lookup"><span data-stu-id="29fb7-171">**boolean**</span></span>

<span data-ttu-id="29fb7-172">Der Wert ist immer **false**.</span><span class="sxs-lookup"><span data-stu-id="29fb7-172">Value is always **False**.</span></span>

</dd> </dl>

## <a name="qualifiers-for-formatted-performance-classes"></a><span data-ttu-id="29fb7-173">Qualifizierer für formatierte Leistungsklassen</span><span class="sxs-lookup"><span data-stu-id="29fb7-173">Qualifiers for Formatted Performance Classes</span></span>

<span data-ttu-id="29fb7-174">Die folgenden Qualifizierer gelten für alle Klassen, die von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="29fb7-174">The following qualifiers apply to all classes that are derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="29fb7-175"><span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**Autokoch**</span><span class="sxs-lookup"><span data-stu-id="29fb7-175"><span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**AutoCook**</span></span>
</dt> <dd>

<span data-ttu-id="29fb7-176">**int32**</span><span class="sxs-lookup"><span data-stu-id="29fb7-176">**int32**</span></span>

<span data-ttu-id="29fb7-177">Gibt an, dass die Werte in den Klassen Instanzen automatisch aus der entsprechenden Rohdaten Klasse berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="29fb7-177">Indicates that the values in class instances are automatically calculated from the corresponding raw data class.</span></span> <span data-ttu-id="29fb7-178">Der Wert ist immer 1.</span><span class="sxs-lookup"><span data-stu-id="29fb7-178">Value is always 1.</span></span>

</dd> <dt>

<span data-ttu-id="29fb7-179"><span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**Autocook \_ rawclass**</span><span class="sxs-lookup"><span data-stu-id="29fb7-179"><span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**AutoCook\_RawClass**</span></span>
</dt> <dd>

<span data-ttu-id="29fb7-180">**string**</span><span class="sxs-lookup"><span data-stu-id="29fb7-180">**string**</span></span>

<span data-ttu-id="29fb7-181">Der Name der RAW-Klasse, die für die Berechnung der formatierten Klasse verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="29fb7-181">Name of the raw class to use for calculation for the formatted class.</span></span> <span data-ttu-id="29fb7-182">Dieser Qualifizierer ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="29fb7-182">This qualifier is required.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="29fb7-183">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="29fb7-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29fb7-184">Überwachen von Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="29fb7-184">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="29fb7-185">Für WMI-Leistungsklassen spezifische Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="29fb7-185">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="29fb7-186">Leistungs Leistungsdaten-Klassen</span><span class="sxs-lookup"><span data-stu-id="29fb7-186">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="29fb7-187">Zugreifen auf vorinstallierte WMI-Leistungsklassen</span><span class="sxs-lookup"><span data-stu-id="29fb7-187">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="29fb7-188">WMI-Tasks: Leistungsüberwachung</span><span class="sxs-lookup"><span data-stu-id="29fb7-188">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
