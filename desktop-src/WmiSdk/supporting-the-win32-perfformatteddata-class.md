---
description: Beim Schreiben eines Hochleistungs Anbieters, der Klassen von Win32 \_ perfformatteddata ableitet, müssen Sie bestimmte Konventionen befolgen, damit die Eigenschaftswerte von WMI berechnet werden können.
ms.assetid: 57912f6f-45ca-491c-8a6c-77e2a6937ccc
ms.tgt_platform: multiple
title: Unterstützen der Win32_PerfFormattedData-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54911105f5c485d3a80ddb93b96f0af2637c9506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355364"
---
# <a name="supporting-the-win32_perfformatteddata-class"></a><span data-ttu-id="759e1-103">Unterstützen der Win32 \_ perfformatteddata-Klasse</span><span class="sxs-lookup"><span data-stu-id="759e1-103">Supporting the Win32\_PerfFormattedData Class</span></span>

<span data-ttu-id="759e1-104">Beim Schreiben eines Hochleistungs Anbieters, der Klassen von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)ableitet, müssen Sie bestimmte Konventionen befolgen, damit die Eigenschaftswerte von WMI berechnet werden können.</span><span class="sxs-lookup"><span data-stu-id="759e1-104">When writing a high-performance provider that derives classes from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), you must follow specific conventions so that WMI can calculate the property values.</span></span>

> [!Note]  
> <span data-ttu-id="759e1-105">Das Schreiben eines hochleistungsfähigen WMI-Anbieters zum Erstellen von Leistungsindikatoren wird in keiner Version des Windows-Betriebssystems empfohlen.</span><span class="sxs-lookup"><span data-stu-id="759e1-105">Writing a WMI high-performance provider to create performance counters is not recommended on any version of the Windows operating system.</span></span> <span data-ttu-id="759e1-106">Weitere Informationen finden Sie unter [Erstellen eines Instanzanbieters in einen High-Performance Anbieter](making-an-instance-provider-into-a-high-performance-provider.md)und [Leistungs Bibliotheken und WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="759e1-106">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

 

<span data-ttu-id="759e1-107">Im folgenden Verfahren wird beschrieben, wie die Win32 \_ perfformatteddata-Klasse unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="759e1-107">The following procedure describes how to support the Win32\_PerfFormattedData class.</span></span>

<span data-ttu-id="759e1-108">**So unterstützen Sie die Win32 \_ perfformatteddata-Klasse**</span><span class="sxs-lookup"><span data-stu-id="759e1-108">**To support the Win32\_PerfFormattedData class**</span></span>

1.  <span data-ttu-id="759e1-109">Erstellen Sie die Klasse im selben Namespace wie die entsprechende RAW-Klasse.</span><span class="sxs-lookup"><span data-stu-id="759e1-109">Create your class in the same namespace as the corresponding raw class.</span></span> <span data-ttu-id="759e1-110">Die Klasse muss von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) abgeleitet werden, und der **HiPerf-Qualifizierer** muss auf " **true**" festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="759e1-110">The class must be derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) and have the **HiPerf** qualifier set to **TRUE**.</span></span> <span data-ttu-id="759e1-111">Weitere Informationen zum Erstellen einer eigenen Klasse für WMI finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="759e1-111">For more information about creating your own class for WMI, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="759e1-112">Geben Sie \_ im [**Anbieter Qualifizierer**](class-qualifiers-for-performance-counter-classes.md) "hiperfkocher v1" an.</span><span class="sxs-lookup"><span data-stu-id="759e1-112">Specify "HiPerfCooker\_v1" in the [**Provider**](class-qualifiers-for-performance-counter-classes.md) qualifier.</span></span>
3.  <span data-ttu-id="759e1-113">Geben Sie zusätzlich zu den für die RAW-Klassen verwendeten Qualifizierern die folgenden Qualifizierer auf Klassenebene an:</span><span class="sxs-lookup"><span data-stu-id="759e1-113">Specify the following class-level qualifiers in addition to the qualifiers used for the raw classes:</span></span>

    -   [<span data-ttu-id="759e1-114">**Autokoch**</span><span class="sxs-lookup"><span data-stu-id="759e1-114">**AutoCook**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="759e1-115">**Autocook \_ rawclass**</span><span class="sxs-lookup"><span data-stu-id="759e1-115">**Autocook\_RawClass**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="759e1-116">**Über**</span><span class="sxs-lookup"><span data-stu-id="759e1-116">**Cooked**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="759e1-117">**Aufwendigen**</span><span class="sxs-lookup"><span data-stu-id="759e1-117">**Costly**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="759e1-118">**Schem**</span><span class="sxs-lookup"><span data-stu-id="759e1-118">**Dynamic**</span></span>](dynamic-qualifier.md)
    -   [<span data-ttu-id="759e1-119">**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="759e1-119">**HiPerf**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="759e1-120">**Gebietsschema**</span><span class="sxs-lookup"><span data-stu-id="759e1-120">**Locale**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="759e1-121">**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="759e1-121">**PerfDefault**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="759e1-122">**Anbieter**</span><span class="sxs-lookup"><span data-stu-id="759e1-122">**Provider**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="759e1-123">**Singleton**</span><span class="sxs-lookup"><span data-stu-id="759e1-123">**Singleton**</span></span>](standard-wmi-qualifiers.md)

    > [!Note]  
    > <span data-ttu-id="759e1-124">Legen Sie keinen Wert für **genericperfctr**, **perfindex** oder **helpindex** fest, da diese durch den ADAP-Prozess festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="759e1-124">Do not set any value for **GenericPerfCtr**, **PerfIndex**, or **HelpIndex** because these will be set by the ADAP process.</span></span> <span data-ttu-id="759e1-125">Weitere Informationen finden Sie unter [**Klassen Qualifizierer für Leistungs Leistungs Leistungs-Klassen**](class-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="759e1-125">For more information, see [**Class Qualifiers for Performance Counter Classes**](class-qualifiers-for-performance-counter-classes.md).</span></span>

     

4.  <span data-ttu-id="759e1-126">Fügen Sie eine Schlüsseleigenschaft namens **Name** in die Klasse ein (diese Eigenschaft ist für Singleton-Klassen nicht erforderlich).</span><span class="sxs-lookup"><span data-stu-id="759e1-126">Include a key property called **Name** in your class (this property is not required for singleton classes).</span></span>

    <span data-ttu-id="759e1-127">Der Wert der **Name** -Eigenschaft muss mit der entsprechenden RAW-Klasse identisch sein.</span><span class="sxs-lookup"><span data-stu-id="759e1-127">The value of the **Name** property must be the same as the corresponding raw class.</span></span> <span data-ttu-id="759e1-128">Sie dürfen keine andere Schlüsseleigenschaft als **Name** in ihrer Klasse verwenden.</span><span class="sxs-lookup"><span data-stu-id="759e1-128">You must not use any key property other than **Name** on your class.</span></span>

5.  <span data-ttu-id="759e1-129">Erstellen Sie Eigenschaften Daten, die entweder als **DWORD** (**UInt32**) oder **QWORD** (**UInt64**) typisiert sind.</span><span class="sxs-lookup"><span data-stu-id="759e1-129">Create properties data typed as either **DWORD** (**uint32**) or **QWORD** (**uint64**).</span></span>

    <span data-ttu-id="759e1-130">Die Eigenschaften müssen entweder einer Eigenschaft in der RAW-Klasse oder einer Eigenschaft in der Klasse entsprechen, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="759e1-130">The properties must correspond either to a property in the raw class or a property in the class you are creating.</span></span>

6.  <span data-ttu-id="759e1-131">Geben Sie die folgenden Qualifizierer auf Eigenschaften Ebene für alle Eigenschaften in der Klasse an, zusätzlich zu den **perfindex** -und **PerfDetail** -Qualifizierern, die für die RAW-Klasseneigenschaften</span><span class="sxs-lookup"><span data-stu-id="759e1-131">Specify the following property level qualifiers for all properties in your class in addition to the **PerfIndex** and **PerfDetail** qualifiers used for the raw class properties:</span></span>

    -   [<span data-ttu-id="759e1-132">**Sock**</span><span class="sxs-lookup"><span data-stu-id="759e1-132">**Base**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="759e1-133">**Cookingtype**</span><span class="sxs-lookup"><span data-stu-id="759e1-133">**CookingType**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="759e1-134">**Leistungsindikator**</span><span class="sxs-lookup"><span data-stu-id="759e1-134">**Counter**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="759e1-135">**Perftimestamp**</span><span class="sxs-lookup"><span data-stu-id="759e1-135">**PerfTimeStamp**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="759e1-136">**Perftimefreq**</span><span class="sxs-lookup"><span data-stu-id="759e1-136">**PerfTimeFreq**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="759e1-137">**SampleWindow**</span><span class="sxs-lookup"><span data-stu-id="759e1-137">**SampleWindow**</span></span>](property-qualifiers-for-performance-counter-classes.md)

    <span data-ttu-id="759e1-138">Weitere Informationen finden Sie unter [**Eigenschaften Qualifizierer für Leistungs Objektklassen**](property-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="759e1-138">For more information, see [**Property Qualifiers for Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="759e1-139">Außerdem enthält die Header Datei WINPERF. h Werte, die Sie für **PerfDetail** und **CounterType** angeben können.</span><span class="sxs-lookup"><span data-stu-id="759e1-139">In addition, the Winperf.h header file contains values that you can specify for **PerfDetail** and **CounterType**.</span></span>

7.  <span data-ttu-id="759e1-140">Stellen Sie sicher, dass Ihr Anbieter die [Leistungsanforderungen](#performance-requirements)erfüllt.</span><span class="sxs-lookup"><span data-stu-id="759e1-140">Make sure your provider meets the [performance requirements](#performance-requirements).</span></span>

## <a name="performance-requirements"></a><span data-ttu-id="759e1-141">Leistungsanforderungen</span><span class="sxs-lookup"><span data-stu-id="759e1-141">Performance Requirements</span></span>

<span data-ttu-id="759e1-142">Wenn Sie einen Hochleistungs Anbieter schreiben, muss seine Leistung die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="759e1-142">When you write a high-performance provider, its performance must meet the following requirements:</span></span>

-   <span data-ttu-id="759e1-143">Das Öffnen der DLL-Datei mit hoher Leistung kann höchstens 100 Millisekunden dauern.</span><span class="sxs-lookup"><span data-stu-id="759e1-143">Opening the high-performance DLL file can take no more than 100 milliseconds.</span></span> <span data-ttu-id="759e1-144">Insgesamt kann das Öffnen der einzelnen Hochleistungs Anbieter und Leistungs Bibliotheken 5 Sekunden nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="759e1-144">Overall, opening each the high-performance provider and performance library cannot exceed 5 seconds.</span></span>
-   <span data-ttu-id="759e1-145">Die Datenaktualisierung kann höchstens 10 Millisekunden pro Erfassung dauern.</span><span class="sxs-lookup"><span data-stu-id="759e1-145">Data refresh can take no more than 10 milliseconds per collect.</span></span> <span data-ttu-id="759e1-146">Bei einem allgemeinen Aktualisierungs-und Sammel Vorgang können alle Hochleistungs Anbieter zusammen mehr als 800 Millisekunden beanspruchen.</span><span class="sxs-lookup"><span data-stu-id="759e1-146">On an overall refresh and collect operation, all the high-performance providers together cannot take more than 800 milliseconds.</span></span>
-   <span data-ttu-id="759e1-147">Die CPU-Gesamtauslastung für alle Hochleistungs Anbieter kann den CPU-Overhead von 6-7% interaktiv oder 5% für die Protokollierung überschreiten.</span><span class="sxs-lookup"><span data-stu-id="759e1-147">The overall CPU load for all high-performance providers cannot exceed 6-7% CPU overhead interactively or 5% for logging.</span></span>

## <a name="related-topics"></a><span data-ttu-id="759e1-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="759e1-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="759e1-149">Erstellen eines Instanzanbieters in einen High-Performance-Anbieter</span><span class="sxs-lookup"><span data-stu-id="759e1-149">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
