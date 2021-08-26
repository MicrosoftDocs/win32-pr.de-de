---
description: Eigenschaftenqualifizierer geben Informationen zum Leistungsindikator an, dem die Eigenschaft zusteuert.
ms.assetid: f1761f71-af4e-4b89-aba7-b7f294c30ffc
ms.tgt_platform: multiple
title: Eigenschaftenqualifizierer für Leistungsindikatorklassen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 105bd010704364dc3865b2e704b3daeaafdb29a772d4f3b3fe036b88da2d43cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996180"
---
# <a name="property-qualifiers-for-performance-counter-classes"></a>Eigenschaftenqualifizierer für Leistungsindikatorklassen

Eigenschaftenqualifizierer geben Informationen zum Leistungsindikator an, dem die Eigenschaft zusteuert.

-   [Eigenschaftenqualifizierer für Unformatierte und formatierte Leistungsklassen](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Eigenschaftenqualifizierer für Rohleistungsklassen](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Eigenschaftenqualifizierer für formatierte Leistungsklassen](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Interpretieren von Eigenschaftsqualifizierern](#how-to-interpret-property-qualifiers)
-   [Zugehörige Themen](#related-topics)

Der Leistungsindikator ist Teil eines Leistungsobjekts, das durch eine WMI-Leistungsindikatorklasse dargestellt wird. Leistungsindikatorspezifische Qualifizierer werden automatisch vom WbemPerfClass-Anbieter an [**Win32 \_ PerfRawData-Klassen**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) und -Eigenschaften in Root [](/windows/desktop/CIMWin32Prov/performance-counter-classes) \\ CIMv2 angefügt.

Diese Informationen gelten für alle Instanzen der Leistungsklasse. Einige Qualifizierer **mit booleschen Werten,** die immer FALSE sind, sind für bestimmte Klassen möglicherweise nicht vorhanden.

## <a name="property-qualifiers-for-raw-and-formatted-performance-classes"></a>Eigenschaftenqualifizierer für Unformatierte und formatierte Leistungsklassen

In der folgenden Liste sind Qualifizierer aufgeführt, die für Eigenschaften in Klassen gelten, die entweder von [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) oder [**Win32 \_ PerfFormattedData abgeleitet sind.**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)

<dl> <dt>

<span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**Countertype**](countertype-qualifier.md)
</dt> <dd>

**sint32**

Ganzzahliger Wert in der Enumeration des Indikatortyps, wie in Winperf.h oder Perflib.h definiert. Der [**CounterType-Qualifizierer**](countertype-qualifier.md)gibt die Formel oder den Algorithmus an, mit der bzw. dem der im Systemmonitor angezeigte Wert für den Zähler berechnet wird, den die Eigenschaft darstellt.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Displayname**
</dt> <dd>

**string**

Der Name des Leistungsindikators, wie von Performance Data Helper (PDH) angegeben.

</dd> <dt>

<span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**
</dt> <dd>

**sint32**

Wird nicht verwendet. Enthält immer 0.

</dd> <dt>

<span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**
</dt> <dd>

**sint32**

Wird nicht verwendet. Enthält immer 0.

</dd> </dl>

## <a name="property-qualifiers-for-raw-performance-classes"></a>Eigenschaftenqualifizierer für Rohleistungsklassen

In der folgenden Liste sind Qualifizierer aufgeführt, die für alle Eigenschaften von Klassen gelten, die von [**Win32 \_ PerfRawData abgeleitet sind.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)

<dl> <dt>

<span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**
</dt> <dd>

**boolean**

Gibt an, ob diese Eigenschaft der Standardindikator ist, der in Listenfeldern verwendet werden soll. Dieser Qualifizierer ist für Die Leistungsindikatoren Version 6.0 standardmäßig auf **False** festgelegt, da er keine Daten dafür liefert. Weitere Informationen finden Sie unter [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

</dd> <dt>

<span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DefaultScale**
</dt> <dd>

**sint32**

Die Leistung von 10, die für die Anzeige des Leistungsindikators verwendet werden soll. Für 0 (null) beträgt der geschätzte Höchstwert 10^0 oder 1.

</dd> <dt>

<span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)
</dt> <dd>

**sint32**

Kenntnisstand der Zielgruppe. Wird nicht verwendet. Der Wert ist immer 100.

</dd> </dl>

## <a name="property-qualifiers-for-formatted-performance-classes"></a>Eigenschaftenqualifizierer für formatierte Leistungsklassen

In der folgenden Liste sind Qualifizierer aufgeführt, die für alle Eigenschaften von Klassen gelten, die von [**Win32 \_ PerfFormattedData abgeleitet sind.**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)

<dl> <dt>

<span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**Durchdungstyp**
</dt> <dd>

**string**

Formeltyp, der zum Erzeugen des Ergebnisses verwendet wird. Jeder Indikatortyp verwendet die anderen Eigenschaftenqualifizierer, um das als Wert der aktuellen Eigenschaft angezeigte Ergebnis zu berechnen. Die Qualifizierer **Counter,** **PerfTimeStamp** und **PerfTimeFreq** werden Eigenschaften in einer rohen Klasse, die die Daten liefert, zuordnen.

Weitere Informationen finden Sie unter [CounterType-Qualifizierer](countertype-qualifier.md).

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Zähler**
</dt> <dd>

**string**

Der Name einer erforderlichen Eigenschaft in der entsprechenden rohen Klasse, die als Indikatorwert in der Formel für die Formel verwendet werden soll. Der Wert muss der Eigenschaftenname der Datenquelleneigenschaft in der entsprechenden rohen Klasse sein.

</dd> <dt>

<span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**
</dt> <dd>

**string**

Der Name einer Eigenschaft in einer rohen Klasse, die als Häufigkeit in der Formel für die Formel für Die Formel verwendet werden soll. Der entsprechende Standardwert auf Klassenebene wird verwendet, wenn dieser Qualifizierer für die Eigenschaft nicht vorhanden ist. Die Häufigkeit stellt die Ticks pro Sekunde des Zeitstempels dar.

</dd> <dt>

<span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**
</dt> <dd>

**string**

Name einer Eigenschaft in einer rohen Klasse, die als Zeitstempel in der Formel für die Formel der Formel verwendet werden soll. Der entsprechende Standardwert auf Klassenebene wird verwendet, wenn dieser Qualifizierer für die Eigenschaft nicht vorhanden ist. Ein automatisch generierter Zeitstempel führt möglicherweise zu einem Fehler in einer Berechnung, da der Zeitstempel eine Näherung ist und den Mehraufwand durch Marshalling und die tatsächliche Datensammlung nicht berücksichtigt.

</dd> </dl>

## <a name="how-to-interpret-property-qualifiers"></a>Interpretieren von Eigenschaftsqualifizierern

Eigenschaften in den [**Win32 \_ PerfFormattedData-Klassen**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) enthalten die berechneten Daten, die von [der Formatted Performance Datenanbieter.](formatted-performance-data-provider.md) Der Eigenschaftswert ist das berechnete Endergebnis. Die Qualifizierer geben ein Rezept an.

Die  **Qualifizierer Counter** und Base zeigen auf die Datenquellen, **und Der Zählertyp** gibt die Formel an, die zum Erzeugen des Ergebnisses verwendet wird. Der Zeitstempel und die Stichprobenhäufigkeit stammen ebenfalls aus der entsprechenden rohen Klasse und werden in **PerfTimeStamp** und **PerfTimeFreq benannt.**

Beispielsweise enthält eine der von WMI bereitgestellten formatierten Klassen [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md)eine Eigenschaft namens **AvgDiskBytesPerRead.** Der Name der Eigenschaft in der formatierten Klasse muss mit der Eigenschaft in der rohen Klasse identisch sein. Die **AvgDiskBytesPerRead-Eigenschaft** verfügt über die folgenden Qualifizierer.

In der folgenden Liste sind die verfügbaren Eigenschaftenqualifizierer für Eigenschaften aller Klassen aufgeführt, die von [**Win32 \_ PerfFormattedData abgeleitet wurden.**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)



| Qualifizierer         | Wert                     |
|-------------------|---------------------------|
| **Durchdungstyp**   | PERF \_ AVERAGE \_ BULK       |
| **Leistungsindikator**       | AvgDiskBytesPerRead       |
| **PerfTimeStamp** | Timestamp \_ PerfTime       |
| **PerfTimeFreq**  | Frequency \_ PerfTime       |
| **PerfIndex**     | 408                       |
| **HelpIndex**     | 409                       |
| **Basis**          | AvgDiskBytesPerRead-Basis \_ |



 

Die **AvgDiskBytesPerRead-Eigenschaft** meldet die durchschnittliche Anzahl von Bytes, die während Lesevorgängen vom Datenträger übertragen werden. Die Formel für PERF \_ AVERAGE \_ BULK ist:

(Sample2 – Sample1) / (Basisbeispiel2 – Basisbeispiel1)

Die Stichprobenentnahme für den Lesevorgang wird mit der von **PerfTimeFreq** angegebenen Häufigkeit durchgeführt, und der **PerfTimeStamp-Wert** gibt das neueste Beispiel an. Die rohen Indikatordaten in Bytes werden aus der **AvgDiskBytesPerRead-Eigenschaft** in der [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk-Klasse**](./retrieving-raw-and-formatted-performance-data.md) übernommen. Die Basisanzahl der Betriebsdaten wird aus der **AvgDiskBytesPerRead \_ Base-Eigenschaft** in derselben Klasse übernommen.

Weitere Informationen finden Sie unter [Abrufen statistischer Leistungsdaten und](obtaining-statistical-performance-data.md) [Überwachen von Leistungsdaten.](monitoring-performance-data.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überwachen von Leistungsdaten](monitoring-performance-data.md)
</dt> <dt>

[Spezifische Qualifizierer für WMI-Leistungsklassen](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[Leistungsindikatorklassen](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Zugreifen auf vorinstallierte WMI-Leistungsklassen](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[WMI-Aufgaben: Leistungsüberwachung](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
