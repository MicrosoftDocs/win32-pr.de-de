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
# <a name="obtaining-statistical-performance-data"></a>Abrufen statistischer Leistungsdaten

In WMI können Sie statistische Leistungsdaten basierend auf Daten in formatierten Leistungsklassen definieren, die von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleitet werden. Die verfügbaren Statistiken sind Mittelwert, minimal, maximal, Bereich und Varianz, wie in den [statistischen Leistungstypen](statistical-counter-types.md)definiert.

Die folgende Liste enthält die speziellen statistischen gegen Typen:

-   [\_kochmittel Wert](cooker-average.md)
-   [Koch \_ Min.](cooker-min.md)
-   [Maximaler kochwert \_](cooker-max.md)
-   [Koch \_ Bereich](cooker-range.md)
-   [Koch \_ Varianz](cooker-variance.md)

In den folgenden Beispielen wird gezeigt, wie Sie:

-   Erstellen Sie eine MOF-Datei, die eine Klasse berechneter Daten definiert.
-   Schreiben Sie ein Skript, das eine Instanz der-Klasse erstellt, und aktualisiert die Daten in der Instanz in regelmäßigen Abständen mit den neu berechneten statistischen Werten.

## <a name="mof-file"></a>MOF-Datei

Im folgenden MOF-Codebeispiel wird eine neue berechnete Datenklasse mit dem Namen **Win32 \_ perfformatteddata \_ availablemb** erstellt. Diese Klasse enthält Daten aus der **availablemb** -Eigenschaft der RAW-Klasse [**Win32 \_ perfrawdata \_ perfos \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data). Die **Win32 \_ perfformatteddata \_ AvailableBytes** -Klasse definiert die Eigenschaften **Average**, **Min**, **Max**, **Range** und **Varianz**.

Die MOF-Datei verwendet die [**Eigenschafts Qualifizierer für formatierte Leistungs Objektklassen**](property-qualifiers-for-performance-counter-classes.md) , um die Eigenschaften Datenquelle und die Berechnungsformel zu definieren.

-   Die **Average** -Eigenschaft ruft Rohdaten aus dem [**Win32 \_ perfrawdata- \_ perfos- \_ Speicher**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)ab.**Availablemb** -Eigenschaft.
-   Der Counter- **Qualifizierer** für die **Average** -Eigenschaft gibt die Rohdaten Quelle an.
-   Der **cookingtype** -Qualifizierer gibt den Formel [Koch \_ Min](cooker-min.md) zum Berechnen der Daten an.
-   Der **samplewindow** -Qualifizierer gibt an, wie viele Stichproben vor der Berechnung durchgeführt werden sollen.


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



## <a name="script"></a>Skript

Im folgenden Skriptcode Beispiel werden Statistiken zum verfügbaren Arbeitsspeicher (in Megabyte) mithilfe des zuvor erstellten MOF abgerufen. Das Skript verwendet das Skript Objekt " [**Swap**](swbemrefresher.md) -Aktualisierungs Fehler", um ein Aktualisierungs Programm zu erstellen, das eine Instanz der Statistik Klasse enthält, die von der MOF-Datei erstellt wird. Hierbei handelt es sich um **Win32 \_ perfformatteddata \_ memorystatistics**. Weitere Informationen zur Verwendung von Skripts finden Sie unter Aktualisieren von [WMI-Daten in Skripts](refreshing-wmi-data-in-scripts.md). Wenn Sie in C++ arbeiten, finden Sie weitere Informationen unter [zugreifen auf Leistungsdaten in C++](accessing-performance-data-in-c--.md).

> [!Note]  
> " [**Taubemfreshableitem. Object**](swbemrefreshableitem-object.md) " muss aufgerufen werden, nachdem das Element aus dem Aufruf von " [**Swap. Add**](swbemrefresher-add.md) " abgerufen wurde. andernfalls tritt ein Fehler auf. " [**Swap. Refresh**](swbemrefresher-refresh.md) " muss vor dem Eingeben der Schleife aufgerufen werden, um Baselinewerte zu erhalten, oder die statistischen Eigenschaften sind beim ersten Durchlauf NULL (0).

 


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



## <a name="running-the-script"></a>Ausführen des Skripts

Im folgenden Verfahren wird beschrieben, wie das Beispiel ausgeführt wird.

**So führen Sie das Beispielskript aus**

1.  Kopieren Sie sowohl den MOF-Code als auch das Skript in Dateien auf Ihrem Computer.
2.  Nennen Sie die MOF-Dateierweiterung ". mof" und die Skriptdatei ". VSB".
3.  Wechseln Sie in der Befehlszeile in das Verzeichnis, in dem die Dateien gespeichert sind, und führen Sie in der MOF-Datei den Befehl " [**mufcomp**](mofcomp.md) " aus. Wenn Sie z. b. die Datei *calculateddata. MOF* benennen, ist der Befehl " **MUF Comp** *calculateddata. mof".*
4.  Führen Sie das Skript aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überwachen von Leistungsdaten](monitoring-performance-data.md)
</dt> <dt>

[Zugreifen auf vorinstallierte WMI-Leistungsklassen](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[**Eigenschafts Qualifizierer für formatierte Leistungs Objektklassen**](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[Statistische Counter-Typen](statistical-counter-types.md)
</dt> </dl>

 

 
