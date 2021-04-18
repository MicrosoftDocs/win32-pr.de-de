---
description: Beim Schreiben eines Hochleistungs Anbieters, der Klassen von Win32 \_ perfrawdata ableitet, müssen Sie bestimmte Konventionen befolgen, damit WMI Daten für die Eigenschaftswerte bereitstellen kann.
ms.assetid: 04abb2f9-800f-497a-ac8f-8ef210746273
ms.tgt_platform: multiple
title: Unterstützen der Win32_PerfRawData-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 835815c9171097bfe088d22e4154ac668d790c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347067"
---
# <a name="supporting-the-win32_perfrawdata-class"></a><span data-ttu-id="9e699-103">Unterstützen der Win32 \_ perfrawdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="9e699-103">Supporting the Win32\_PerfRawData Class</span></span>

<span data-ttu-id="9e699-104">Beim Schreiben eines Hochleistungs Anbieters, der Klassen von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)ableitet, müssen Sie bestimmte Konventionen befolgen, damit WMI Daten für die Eigenschaftswerte bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="9e699-104">When writing a high-performance provider that derives classes from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), you must follow specific conventions so that WMI can supply data to the property values.</span></span>

> [!Note]  
> <span data-ttu-id="9e699-105">Das Schreiben eines hochleistungsfähigen WMI-Anbieters zum Erstellen von Leistungsindikatoren wird in keiner Version des Windows-Betriebssystems empfohlen.</span><span class="sxs-lookup"><span data-stu-id="9e699-105">Writing a WMI high-performance provider to create performance counters is not recommended on any version of the Windows operating system.</span></span> <span data-ttu-id="9e699-106">Weitere Informationen finden Sie unter [Erstellen eines Instanzanbieters in einen High-Performance Anbieter](making-an-instance-provider-into-a-high-performance-provider.md)und [Leistungs Bibliotheken und WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="9e699-106">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

 

<span data-ttu-id="9e699-107">Im folgenden Verfahren wird beschrieben, wie die [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klasse mit Ihrem Hochleistungs Anbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="9e699-107">The following procedure describes how to support the [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class with your high-performance provider.</span></span>

<span data-ttu-id="9e699-108">**So unterstützen Sie die Win32 \_ perfrawdata-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9e699-108">**To support the Win32\_PerfRawData class**</span></span>

1.  <span data-ttu-id="9e699-109">Erstellen Sie die-Klasse im root \\ CIMv2-Namespace.</span><span class="sxs-lookup"><span data-stu-id="9e699-109">Create your class in the Root\\CIMv2 namespace.</span></span>

    <span data-ttu-id="9e699-110">Die Klasse muss von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) abgeleitet werden, und der **HiPerf-Qualifizierer** muss auf " **true**" festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="9e699-110">The class must be derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and have the **Hiperf** qualifier set to **TRUE**.</span></span> <span data-ttu-id="9e699-111">Sie können auch WDM-Leistungsdaten Klassen (Treiber) zum Stamm- \\ WMI-Namespace hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9e699-111">You can also add WDM (driver) performance data classes to the root\\wmi namespace.</span></span> <span data-ttu-id="9e699-112">Weitere Informationen zum Erstellen einer eigenen Klasse für WMI finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="9e699-112">For more information about creating your own class for WMI, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

2.  <span data-ttu-id="9e699-113">Geben Sie den Anbieter \_ \_ im **Anbieter Qualifizierer** als "NT5 genericperfprovider v1" an.</span><span class="sxs-lookup"><span data-stu-id="9e699-113">Specify the provider as "NT5\_GenericPerfProvider\_V1" in the **Provider** qualifier.</span></span>
3.  <span data-ttu-id="9e699-114">Geben Sie die folgenden Qualifizierer auf Klassenebene an:</span><span class="sxs-lookup"><span data-stu-id="9e699-114">Specify the following class-level qualifiers:</span></span>

    -   <span data-ttu-id="9e699-115">**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="9e699-115">**HiPerf**</span></span>
    -   <span data-ttu-id="9e699-116">**Gebietsschema**</span><span class="sxs-lookup"><span data-stu-id="9e699-116">**Locale**</span></span>
    -   <span data-ttu-id="9e699-117">**PerfDetail**</span><span class="sxs-lookup"><span data-stu-id="9e699-117">**PerfDetail**</span></span>
    -   <span data-ttu-id="9e699-118">**Anbieter**</span><span class="sxs-lookup"><span data-stu-id="9e699-118">**Provider**</span></span>

    <span data-ttu-id="9e699-119">Weitere Informationen finden Sie unter [**Klassen Qualifizierer für Leistungs Leistungs Leistungs-Klassen**](class-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="9e699-119">For more information, see [**Class Qualifiers for Performance Counter Classes**](class-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="9e699-120">Definieren Sie den **genericperfctr** -Qualifizierer nicht, da dieser für den ADAP-Prozess reserviert ist, der Leistungs Bibliotheksdaten in WMI-Klassen überträgt.</span><span class="sxs-lookup"><span data-stu-id="9e699-120">Do not define the **GenericPerfCtr** qualifier because that is reserved for the ADAP process that transfers performance library data into WMI classes.</span></span>

4.  <span data-ttu-id="9e699-121">Füllen Sie die entsprechenden Zeitstempel-und Frequency-Eigenschaften auf, die zum Berechnen von Counter-Type-Formeln verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e699-121">Populate the appropriate timestamp and frequency properties used to compute counter-type formulas.</span></span>

    <span data-ttu-id="9e699-122">Diese Eigenschaften werden von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) geerbt. Wenn Sie einen Hochleistungs Anbieter schreiben, müssen Sie diese Eigenschaften ausfüllen, damit die Klasse im System Monitor angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9e699-122">These properties are inherited from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and, if you are writing a high-performance provider, you must fill these out for the class to be displayed in System Monitor.</span></span>

5.  <span data-ttu-id="9e699-123">Fügen Sie eine Schlüsseleigenschaft namens **Name** in die Klasse ein (diese Eigenschaft ist für Singleton-Klassen nicht erforderlich).</span><span class="sxs-lookup"><span data-stu-id="9e699-123">Include a key property called **Name** in your class (this property is not required for singleton classes).</span></span>

    <span data-ttu-id="9e699-124">Sie dürfen keine andere Schlüsseleigenschaft als **Name** in ihrer Klasse verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e699-124">You must not use any key property other than **Name** on your class.</span></span>

6.  <span data-ttu-id="9e699-125">Erstellen Sie Eigenschaften Daten, die als **DWORD** (**UInt32**) oder **QWORD** (**UInt64**) typisiert sind.</span><span class="sxs-lookup"><span data-stu-id="9e699-125">Create properties data-typed as either **DWORD** (**uint32**) or **QWORD** (**uint64**).</span></span> <span data-ttu-id="9e699-126">Diese Eigenschaften werden bei der Übertragung in die Leistungs Bibliotheken zu Leistungsindikatoren.</span><span class="sxs-lookup"><span data-stu-id="9e699-126">These properties become performance counters when transferred to the performance libraries.</span></span>
7.  <span data-ttu-id="9e699-127">Geben Sie die folgenden Qualifizierer auf Eigenschaften Ebene für alle Eigenschaften in der Klasse an:</span><span class="sxs-lookup"><span data-stu-id="9e699-127">Specify the following property level qualifiers for all properties in your class:</span></span>

    -   <span data-ttu-id="9e699-128">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="9e699-128">**DisplayName**</span></span>
    -   <span data-ttu-id="9e699-129">**Counter Type**</span><span class="sxs-lookup"><span data-stu-id="9e699-129">**CounterType**</span></span>
    -   <span data-ttu-id="9e699-130">**DEFAULTSCALE**</span><span class="sxs-lookup"><span data-stu-id="9e699-130">**DefaultScale**</span></span>
    -   <span data-ttu-id="9e699-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9e699-131">**Description**</span></span>
    -   <span data-ttu-id="9e699-132">**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="9e699-132">**PerfDefault**</span></span>
    -   <span data-ttu-id="9e699-133">**PerfDetail**</span><span class="sxs-lookup"><span data-stu-id="9e699-133">**PerfDetail**</span></span>

    <span data-ttu-id="9e699-134">Weitere Informationen finden Sie unter [**Eigenschaften Qualifizierer für Leistungs Objektklassen**](property-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="9e699-134">For more information, see [**Property Qualifiers for Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="9e699-135">Außerdem enthält die Header Datei WINPERF. h Werte, die Sie für **PerfDetail** und **CounterType** angeben können.</span><span class="sxs-lookup"><span data-stu-id="9e699-135">In addition, the Winperf.h header file contains values that you can specify for **PerfDetail** and **CounterType**.</span></span>

    <span data-ttu-id="9e699-136">WMI verwendet die Qualifizierer " **Display Name**", " **locale**" und " **Description** " für die Lokalisierung.</span><span class="sxs-lookup"><span data-stu-id="9e699-136">WMI uses the **DisplayName**, **Locale**, and **Description** qualifiers for localization.</span></span> <span data-ttu-id="9e699-137">Sie müssen dem Namespace MS 409 (Englisch) geänderte Qualifizierer hinzufügen \_ , damit der System Monitor Ihre Klassen Daten ordnungsgemäß anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="9e699-137">You must add amended qualifiers to the MS\_409 (English) namespace so that System Monitor can properly display your class data.</span></span> <span data-ttu-id="9e699-138">Dies bedeutet, dass Sie die Eigenschafts Definition durch Hinzufügen eines **Beschreibungs** Qualifizierers mit erklärendem Text ändern und den Wert **Display Name** ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="9e699-138">This means that you amend the property definition by adding a **Description** qualifier with explanatory text and fill in the **DisplayName** value.</span></span> <span data-ttu-id="9e699-139">Außerdem müssen Sie allen anderen Gebiets Schema Namespaces, die Ihre Klasse unterstützt, geänderte Qualifizierer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9e699-139">You must also add amended qualifiers to any other locale namespace that your class supports.</span></span> <span data-ttu-id="9e699-140">Wenn ein Benutzerdaten von einem Gebiets Schema anfordert, für das Sie keine geänderten Qualifizierer bereitstellen, verwendet WMI standardmäßig die im MS \_ 409-Namespace angegebenen Definitionen.</span><span class="sxs-lookup"><span data-stu-id="9e699-140">If a user requests data from a locale for which you do not provide amended qualifiers, WMI defaults to the definitions specified in the MS\_409 namespace.</span></span>

8.  <span data-ttu-id="9e699-141">Erstellen Sie eine Basis Eigenschaft für jede Eigenschaft, die einen zähtertyp hat, der einen Basiswert erwartet.</span><span class="sxs-lookup"><span data-stu-id="9e699-141">Create a base property for any property that has a counter type expecting a base value.</span></span>

    <span data-ttu-id="9e699-142">Diese Eigenschaft folgt unmittelbar der-Eigenschaft und hat den Namen \* PropertyName \***\_ Base**.</span><span class="sxs-lookup"><span data-stu-id="9e699-142">This property immediately follows the property and is named \*propertyname\***\_Base**.</span></span> <span data-ttu-id="9e699-143">Die durchschnittliche Eigenschaft **avgdiskbytesperread** in der [**Win32 \_ perfrawdata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) -Klasse benötigt z. b. eine Basis Eigenschaft namens **avgdiskbytesperread \_ Base** , um die Anzahl der Stichproben zu zählen.</span><span class="sxs-lookup"><span data-stu-id="9e699-143">For example, the average property **AvgDiskBytesPerRead** in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class requires a base property named **AvgDiskBytesPerRead\_Base** to count the number of samples.</span></span> <span data-ttu-id="9e699-144">Wenn Sie bestimmen möchten, ob der zu verwendende zähtertyp eine Basis Eigenschaft erfordert, suchen Sie in den [WMI-Leistungs Leistungsdaten Typen](wmi-performance-counter-types.md)nach dem zähtertyp nach Name oder Dezimalwert.</span><span class="sxs-lookup"><span data-stu-id="9e699-144">To determine if the counter type you want to use requires a base property, locate the counter type by name or decimal value in [WMI Performance Counter Types](wmi-performance-counter-types.md).</span></span>

9.  <span data-ttu-id="9e699-145">Stellen Sie sicher, dass Ihr Anbieter die [Leistungsanforderungen](supporting-the-win32-perfformatteddata-class.md)erfüllt.</span><span class="sxs-lookup"><span data-stu-id="9e699-145">Make sure your provider meets the [performance requirements](supporting-the-win32-perfformatteddata-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e699-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9e699-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e699-147">Erstellen eines Instanzanbieters in einen High-Performance-Anbieter</span><span class="sxs-lookup"><span data-stu-id="9e699-147">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
