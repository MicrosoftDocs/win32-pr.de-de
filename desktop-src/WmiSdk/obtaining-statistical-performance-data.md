---
description: In WMI können Sie statistische Leistungsdaten basierend auf Daten in formatierten Leistungsklassen definieren, die von Win32 \_ perfformatteddata abgeleitet werden. Die verfügbaren Statistiken sind Mittelwert, minimal, maximal, Bereich und Varianz, wie in den statistischen Leistungstypen definiert.
ms.assetid: 5552d5fc-df8c-4353-8593-c106ee19dc84
ms.tgt_platform: multiple
title: Abrufen statistischer Leistungsdaten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 65892608e642b675440d81127ef9afa0badd1d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128076"
---
# <a name="obtaining-statistical-performance-data"></a><span data-ttu-id="28bf1-104">Abrufen statistischer Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="28bf1-104">Obtaining Statistical Performance Data</span></span>

<span data-ttu-id="28bf1-105">In WMI können Sie statistische Leistungsdaten basierend auf Daten in formatierten Leistungsklassen definieren, die von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="28bf1-105">In WMI, you can define statistical performance data based on data in formatted performance classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="28bf1-106">Die verfügbaren Statistiken sind Mittelwert, minimal, maximal, Bereich und Varianz, wie in den [statistischen Leistungstypen](statistical-counter-types.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="28bf1-106">The available statistics are average, minimum, maximum, range, and variance, as defined in [Statistical Counter Types](statistical-counter-types.md).</span></span>

<span data-ttu-id="28bf1-107">Die folgende Liste enthält die speziellen statistischen gegen Typen:</span><span class="sxs-lookup"><span data-stu-id="28bf1-107">The following list includes the special statistical counter types:</span></span>

-   [<span data-ttu-id="28bf1-108">\_kochmittel Wert</span><span class="sxs-lookup"><span data-stu-id="28bf1-108">COOKER\_AVERAGE</span></span>](cooker-average.md)
-   [<span data-ttu-id="28bf1-109">Koch \_ Min.</span><span class="sxs-lookup"><span data-stu-id="28bf1-109">COOKER\_MIN</span></span>](cooker-min.md)
-   [<span data-ttu-id="28bf1-110">Maximaler kochwert \_</span><span class="sxs-lookup"><span data-stu-id="28bf1-110">COOKER\_MAX</span></span>](cooker-max.md)
-   [<span data-ttu-id="28bf1-111">Koch \_ Bereich</span><span class="sxs-lookup"><span data-stu-id="28bf1-111">COOKER\_RANGE</span></span>](cooker-range.md)
-   [<span data-ttu-id="28bf1-112">Koch \_ Varianz</span><span class="sxs-lookup"><span data-stu-id="28bf1-112">COOKER\_VARIANCE</span></span>](cooker-variance.md)

<span data-ttu-id="28bf1-113">In den folgenden Beispielen wird gezeigt, wie Sie:</span><span class="sxs-lookup"><span data-stu-id="28bf1-113">The following examples show how to:</span></span>

-   <span data-ttu-id="28bf1-114">Erstellen Sie eine MOF-Datei, die eine Klasse berechneter Daten definiert.</span><span class="sxs-lookup"><span data-stu-id="28bf1-114">Create a MOF file that defines a class of calculated data.</span></span>
-   <span data-ttu-id="28bf1-115">Schreiben Sie ein Skript, das eine Instanz der-Klasse erstellt, und aktualisiert die Daten in der Instanz in regelmäßigen Abständen mit den neu berechneten statistischen Werten.</span><span class="sxs-lookup"><span data-stu-id="28bf1-115">Write a script that creates an instance of the class, and periodically refreshes the data in the instance with the recalculated statistical values.</span></span>

## <a name="mof-file"></a><span data-ttu-id="28bf1-116">MOF-Datei</span><span class="sxs-lookup"><span data-stu-id="28bf1-116">MOF File</span></span>

<span data-ttu-id="28bf1-117">Im folgenden MOF-Codebeispiel wird eine neue berechnete Datenklasse mit dem Namen **Win32 \_ perfformatteddata \_ availablemb** erstellt.</span><span class="sxs-lookup"><span data-stu-id="28bf1-117">The following MOF code example creates a new calculated data class named **Win32\_PerfFormattedData\_AvailableMBytes**.</span></span> <span data-ttu-id="28bf1-118">Diese Klasse enthält Daten aus der **availablemb** -Eigenschaft der RAW-Klasse [**Win32 \_ perfrawdata \_ perfos \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).</span><span class="sxs-lookup"><span data-stu-id="28bf1-118">This class contains data from the **AvailableMBytes** property of the raw class [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).</span></span> <span data-ttu-id="28bf1-119">Die **Win32 \_ perfformatteddata \_ AvailableBytes** -Klasse definiert die Eigenschaften **Average**, **Min**, **Max**, **Range** und **Varianz**.</span><span class="sxs-lookup"><span data-stu-id="28bf1-119">The **Win32\_PerfFormattedData\_AvailableBytes** class defines the properties **Average**, **Min**, **Max**, **Range**, and **Variance**.</span></span>

<span data-ttu-id="28bf1-120">Die MOF-Datei verwendet die [**Eigenschafts Qualifizierer für formatierte Leistungs Objektklassen**](property-qualifiers-for-performance-counter-classes.md) , um die Eigenschaften Datenquelle und die Berechnungsformel zu definieren.</span><span class="sxs-lookup"><span data-stu-id="28bf1-120">The MOF file uses the [**Property Qualifiers for Formatted Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md) to define the property data source and the calculation formula.</span></span>

-   <span data-ttu-id="28bf1-121">Die **Average** -Eigenschaft ruft Rohdaten aus dem [**Win32 \_ perfrawdata- \_ perfos- \_ Speicher**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)ab.**Availablemb** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="28bf1-121">The **Average** property obtains raw data from the [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).**AvailableMBytes** property.</span></span>
-   <span data-ttu-id="28bf1-122">Der Counter- **Qualifizierer** für die **Average** -Eigenschaft gibt die Rohdaten Quelle an.</span><span class="sxs-lookup"><span data-stu-id="28bf1-122">The Counter **qualifier** for the **Average** property specifies the raw data source.</span></span>
-   <span data-ttu-id="28bf1-123">Der **cookingtype** -Qualifizierer gibt den Formel [Koch \_ Min](cooker-min.md) zum Berechnen der Daten an.</span><span class="sxs-lookup"><span data-stu-id="28bf1-123">The **CookingType** qualifier specifies the formula [COOKER\_MIN](cooker-min.md) for calculating the data.</span></span>
-   <span data-ttu-id="28bf1-124">Der **samplewindow** -Qualifizierer gibt an, wie viele Stichproben vor der Berechnung durchgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="28bf1-124">The **SampleWindow** qualifier specifies how many samples to take before performing the calculation.</span></span>


```mof
// Store the new Win32_PerfFormattedData_MemoryStatistics
//     class in the Root\Cimv2 namespace
#pragma autorecover
#pragma namespace("\\\\.\\Root\\CimV2")

qualifier vendor:ToInstance;
qualifier guid:ToInstance;
qualifier displayname:ToInstance;
qualifier perfindex:ToInstance;
qualifier helpindex:ToInstance;
qualifier perfdetail:ToInstance;
qualifier countertype:ToInstance;
qualifier perfdefault:ToInstance;
qualifier defaultscale:ToInstance;

qualifier dynamic:ToInstance;
qualifier hiperf:ToInstance;
qualifier AutoCook:ToInstance;
qualifier AutoCook_RawClass:ToInstance;
qualifier CookingType:ToInstance;
qualifier Counter:ToInstance;


// Define the Win32_PerFormattedData_MemoryStatistics
//     class, derived from Win32_PerfFormattedData
[
  dynamic,
  // Name of formatted data provider: "WMIPerfInst" for Vista 
  //   and later
  provider("HiPerfCooker_v1"), 
  // Text that will identify new counter in Perfmon
  displayname("My Calculated Counter"),                            
  // A high performance class     
  Hiperf,
  // Contains calculated data 
  Cooked, 
  // Value must be 1 
  AutoCook(1), 
  // Raw performance class to get data for calculations
  AutoCook_RawClass("Win32_PerfRawData_PerfOS_Memory"),
  // Value must be 1        
  AutoCook_RawDefault(1),
  // Name of raw class property to use for timestamp in formulas 
  PerfSysTimeStamp("Timestamp_PerfTime"), 
  // Name of raw class property to use for frequency in formulas
  PerfSysTimeFreq("Frequency_PerfTime"), 
  // Name of raw class property to use for timestamp in formulas
  Perf100NSTimeStamp("Timestamp_Sys100NS"),
  // Name of raw class property to use for frequency in formulas
  Perf100NSTimeFreq("Frequency_Sys100NS"),
  // Name of raw class property to use for timestamp in formulas
  PerfObjTimeStamp("Timestamp_Object"),
  // Name of raw class property to use for frequency in formulas 
  PerfObjTimeFreq("Frequency_Object"),
  // Only one instance of class allowed in namespace
  singleton                                                   
]

class Win32_PerfFormattedData_MemoryStatistics
          : Win32_PerfFormattedData
{

// Define the properties for the class. 
// All the properties perform different
//     statistical operations on the same
//     property, AvailableMBytes, in the raw class

// Define the Average property,
//     which uses the "COOKER_AVERAGE" counter type and 
//     gets its data from the AvailableMBytes 
//     property in the raw class

    [
     CookingType("COOKER_AVERAGE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Average = 0;

// Define the Min property, which uses
//     the "COOKER_MIN" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_MIN"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Min = 0;

// Define the Max property, which uses
//     the "COOKER_MAX" counter type and 
//     gets its data from the
//     AvailableMBytes property in the raw class

    [
     CookingType("COOKER_MAX"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Max = 0;

// Define the Range property, which uses
//     the "COOKER_RANGE" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_RANGE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Range = 0;

// Define the Variance property, which uses
//     the "COOKER_VARIANCE" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_VARIANCE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Variance = 0;
};
```



## <a name="script"></a><span data-ttu-id="28bf1-125">Skript</span><span class="sxs-lookup"><span data-stu-id="28bf1-125">Script</span></span>

<span data-ttu-id="28bf1-126">Im folgenden Skriptcode Beispiel werden Statistiken zum verfügbaren Arbeitsspeicher (in Megabyte) mithilfe des zuvor erstellten MOF abgerufen.</span><span class="sxs-lookup"><span data-stu-id="28bf1-126">The following script code example obtains statistics about available memory, in megabytes, using the MOF created previously.</span></span> <span data-ttu-id="28bf1-127">Das Skript verwendet das Skript Objekt " [**Swap**](swbemrefresher.md) -Aktualisierungs Fehler", um ein Aktualisierungs Programm zu erstellen, das eine Instanz der Statistik Klasse enthält, die von der MOF-Datei erstellt wird. Hierbei handelt es sich um **Win32 \_ perfformatteddata \_ memorystatistics**.</span><span class="sxs-lookup"><span data-stu-id="28bf1-127">The script uses the [**SWbemRefresher**](swbemrefresher.md) scripting object to create a refresher that contains one instance of the statistics class that the MOF file creates, which is **Win32\_PerfFormattedData\_MemoryStatistics**.</span></span> <span data-ttu-id="28bf1-128">Weitere Informationen zur Verwendung von Skripts finden Sie unter Aktualisieren von [WMI-Daten in Skripts](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="28bf1-128">For more information about using scripts, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span> <span data-ttu-id="28bf1-129">Wenn Sie in C++ arbeiten, finden Sie weitere Informationen unter [zugreifen auf Leistungsdaten in C++](accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="28bf1-129">If working in C++, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span>

> [!Note]  
> <span data-ttu-id="28bf1-130">" [**Taubemfreshableitem. Object**](swbemrefreshableitem-object.md) " muss aufgerufen werden, nachdem das Element aus dem Aufruf von " [**Swap. Add**](swbemrefresher-add.md) " abgerufen wurde. andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="28bf1-130">[**SWbemRefreshableItem.Object**](swbemrefreshableitem-object.md) must be called after obtaining the item from the call to [**SWbemRefresher.Add**](swbemrefresher-add.md) or the script will fail.</span></span> <span data-ttu-id="28bf1-131">" [**Swap. Refresh**](swbemrefresher-refresh.md) " muss vor dem Eingeben der Schleife aufgerufen werden, um Baselinewerte zu erhalten, oder die statistischen Eigenschaften sind beim ersten Durchlauf NULL (0).</span><span class="sxs-lookup"><span data-stu-id="28bf1-131">[**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) must be called before entering the loop to obtain baseline values, or the statistical properties is zero (0) on the first pass.</span></span>

 


```VB
' Connect to the Root\Cimv2 namespace
strComputer = "."
Set objService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")

' Create a refresher
Set Refresher = CreateObject("WbemScripting.SWbemRefresher")
If Err <> 0 Then
WScript.Echo Err
WScript.Quit
End If

' Add the single instance of the statistics
'    class to the refresher
Set obMemoryStatistics = Refresher.Add(objService, _
    "Win32_PerfFormattedData_MemoryStatistics=@").Object

' Refresh once to obtain base values for cooking calculations
Refresher.Refresh

Const REFRESH_INTERVAL = 10

' Refresh every REFRESH_INTERVAL seconds 
For I=1 to 3
  WScript.Sleep REFRESH_INTERVAL * 1000
  Refresher.Refresh

  WScript.Echo "System memory statistics" _
      & "(Available Megabytes) " _
      & "for the past 100 seconds - pass " & i 
  WScript.Echo "Average = " _
     & obMemoryStatistics.Average & VBNewLine & "Max = " _
     & obMemoryStatistics.Max & VBNewLine & "Min = " _
     & obMemoryStatistics.Min & VBNewLine & "Range = " _ 
     & obMemoryStatistics.Range & VBNewLine & "Variance = " _
     & obMemoryStatistics.Variance 
Next
```



## <a name="running-the-script"></a><span data-ttu-id="28bf1-132">Ausführen des Skripts</span><span class="sxs-lookup"><span data-stu-id="28bf1-132">Running the Script</span></span>

<span data-ttu-id="28bf1-133">Im folgenden Verfahren wird beschrieben, wie das Beispiel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28bf1-133">The following procedure describes how to run the example.</span></span>

<span data-ttu-id="28bf1-134">**So führen Sie das Beispielskript aus**</span><span class="sxs-lookup"><span data-stu-id="28bf1-134">**To run the example script**</span></span>

1.  <span data-ttu-id="28bf1-135">Kopieren Sie sowohl den MOF-Code als auch das Skript in Dateien auf Ihrem Computer.</span><span class="sxs-lookup"><span data-stu-id="28bf1-135">Copy both the MOF code and script to files on your computer.</span></span>
2.  <span data-ttu-id="28bf1-136">Nennen Sie die MOF-Dateierweiterung ". mof" und die Skriptdatei ". VSB".</span><span class="sxs-lookup"><span data-stu-id="28bf1-136">Give the MOF file a .mof extension and the script file a .vbs description.</span></span>
3.  <span data-ttu-id="28bf1-137">Wechseln Sie in der Befehlszeile in das Verzeichnis, in dem die Dateien gespeichert sind, und führen Sie in der MOF-Datei den Befehl " [**mufcomp**](mofcomp.md) " aus.</span><span class="sxs-lookup"><span data-stu-id="28bf1-137">On the command line, change to the directory where the files are stored, and run [**Mofcomp**](mofcomp.md) on the MOF file.</span></span> <span data-ttu-id="28bf1-138">Wenn Sie z. b. die Datei *calculateddata. MOF* benennen, ist der Befehl " **MUF Comp** *calculateddata. mof".*</span><span class="sxs-lookup"><span data-stu-id="28bf1-138">For example, if you name the file *CalculatedData.mof*, then the command is **Mofcomp** *CalculatedData.mof*</span></span>
4.  <span data-ttu-id="28bf1-139">Führen Sie das Skript aus.</span><span class="sxs-lookup"><span data-stu-id="28bf1-139">Run the script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28bf1-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="28bf1-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28bf1-141">Überwachen von Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="28bf1-141">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="28bf1-142">Zugreifen auf vorinstallierte WMI-Leistungsklassen</span><span class="sxs-lookup"><span data-stu-id="28bf1-142">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="28bf1-143">**Eigenschafts Qualifizierer für formatierte Leistungs Objektklassen**</span><span class="sxs-lookup"><span data-stu-id="28bf1-143">**Property Qualifiers for Formatted Performance Counter Classes**</span></span>](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="28bf1-144">Statistische Counter-Typen</span><span class="sxs-lookup"><span data-stu-id="28bf1-144">Statistical Counter Types</span></span>](statistical-counter-types.md)
</dt> </dl>

 

 
