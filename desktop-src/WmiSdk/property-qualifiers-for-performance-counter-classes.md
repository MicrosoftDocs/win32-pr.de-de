---
description: Eigenschafts Qualifizierer geben Informationen über den Leistungs Bezeichner an, dem die Eigenschaft zugeordnet wird.
ms.assetid: f1761f71-af4e-4b89-aba7-b7f294c30ffc
ms.tgt_platform: multiple
title: Eigenschafts Qualifizierer für Leistungs Objektklassen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4e060d072c34d248f9faf634aec7710f5638721b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218172"
---
# <a name="property-qualifiers-for-performance-counter-classes"></a>Eigenschafts Qualifizierer für Leistungs Objektklassen

Eigenschafts Qualifizierer geben Informationen über den Leistungs Bezeichner an, dem die Eigenschaft zugeordnet wird.

-   [Eigenschaften Qualifizierer für formatierte und formatierte Leistungsklassen](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Eigenschafts Qualifizierer für rohleistungs Klassen](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Eigenschafts Qualifizierer für formatierte Leistungsklassen](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Interpretieren von Eigenschaften Qualifizierern](#how-to-interpret-property-qualifiers)
-   [Zugehörige Themen](#related-topics)

Der Leistungsdaten Träger ist Teil eines Leistungs [**Objekts, das \_**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) durch einen Leistungs Leistungs Leistungs- [Leistungs Leistungs Leistungs](/windows/desktop/CIMWin32Prov/performance-counter-classes) -Leistungs Leistungs Leistungs-Leistungs Leistungs-Leistungs Leistungs Leistungs-Leistungs Leistungs-Leistungs Leistungs-Leistungs Leistungs-Leistungs Leistungs-Leistungs Leistungs-Leistungs Leistungs-Objekt – \\

Diese Informationen gelten für alle Instanzen der Performance-Klasse. Einige Qualifizierer mit **booleschen** Werten, die immer false sind, sind möglicherweise nicht für bestimmte Klassen vorhanden.

## <a name="property-qualifiers-for-raw-and-formatted-performance-classes"></a>Eigenschaften Qualifizierer für formatierte und formatierte Leistungsklassen

In der folgenden Liste sind die Qualifizierer aufgeführt, die für Eigenschaften in Klassen gelten, die entweder von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) oder [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleitet werden.

<dl> <dt>

<span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**Counter Type**](countertype-qualifier.md)
</dt> <dd>

**sint32**

Ganzzahliger Wert in der Enumeration des Zählers, wie in Winperf. h oder Perflib. h definiert. Der [**Counter Type**](countertype-qualifier.md)-Qualifizierer gibt die Formel oder den Algorithmus zum Berechnen des Werts an, der im System Monitor für den Indikator angezeigt wird, den die Eigenschaft darstellt.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Display Name**
</dt> <dd>

**string**

Der Name des Leistungs Zählers, wie durch das Leistungsdaten-Hilfsprogramm (PDH) angegeben.

</dd> <dt>

<span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**Helpindex**
</dt> <dd>

**sint32**

Nicht verwendet. Enthält immer 0.

</dd> <dt>

<span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**Perfindex**
</dt> <dd>

**sint32**

Nicht verwendet. Enthält immer 0.

</dd> </dl>

## <a name="property-qualifiers-for-raw-performance-classes"></a>Eigenschafts Qualifizierer für rohleistungs Klassen

In der folgenden Liste sind die Qualifizierer aufgeführt, die für alle Eigenschaften von Klassen gelten, die von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)abgeleitet werden.

<dl> <dt>

<span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**
</dt> <dd>

**boolean**

Gibt an, ob diese Eigenschaft der in Listenfeldern zu verwendende Standardwert ist. Dieser Qualifizierer ist für die Leistungsindikatoren der Version 6,0 standardmäßig auf **false** eingestellt, da Sie keine Daten dafür bereitstellen. Weitere Informationen finden Sie unter [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

</dd> <dt>

<span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DEFAULTSCALE**
</dt> <dd>

**sint32**

Die Potenz von 10, die für die Anzeige des Zählers verwendet werden soll. Bei 0 (null) beträgt der geschätzte Höchstwert 10 ^ 0 oder 1.

</dd> <dt>

<span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)
</dt> <dd>

**sint32**

Zielgruppe des Wissens. Nicht verwendet. Der Wert ist immer 100.

</dd> </dl>

## <a name="property-qualifiers-for-formatted-performance-classes"></a>Eigenschafts Qualifizierer für formatierte Leistungsklassen

In der folgenden Liste sind die Qualifizierer aufgelistet, die für alle Eigenschaften von Klassen gelten, die von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleitet werden.

<dl> <dt>

<span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**Cookingtype**
</dt> <dd>

**string**

Der Formel-Typ, mit dem das Ergebnis erzeugt wird. Jeder zähtertyp verwendet die anderen Eigenschaften Qualifizierer, um das als Wert der aktuellen Eigenschaft angezeigte Ergebnis zu berechnen. Die Qualifizierer " **Counter**", " **perftimestamp**" und " **perftimefreq** " sind Eigenschaften in einer RAW-Klasse zugeordnet, die die Daten bereitstellen

Weitere Informationen finden Sie unter [Counter Type-Qualifizierer](countertype-qualifier.md).

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Indikator**
</dt> <dd>

**string**

Der Name einer erforderlichen Eigenschaft in der entsprechenden RAW-Klasse, die als Leistungswert in der Koch Formel verwendet werden soll. Der Wert muss der Eigenschaftsname der Datenquellen Eigenschaft in der entsprechenden RAW-Klasse sein.

</dd> <dt>

<span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**Perftimestamp**
</dt> <dd>

**string**

Der Name einer Eigenschaft in einer RAW-Klasse, die als Häufigkeit in der Koch Formel verwendet werden soll. Der entsprechende Standardwert auf Klassenebene wird verwendet, wenn dieser Qualifizierer für die Eigenschaft nicht vorhanden ist. Die Häufigkeit stellt die Ticks pro Sekunde des Zeitstempels dar.

</dd> <dt>

<span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**Perftimefreq**
</dt> <dd>

**string**

Der Name einer Eigenschaft in einer RAW-Klasse, die in der Koch Formel als Zeitstempel verwendet werden soll. Der geeignete Standardwert auf Klassenebene wird verwendet, wenn dieser Qualifizierer für die Eigenschaft nicht vorhanden ist. Ein automatisch generierter Zeitstempel kann einen Fehler in einer Berechnung verursachen, da der Zeitstempel ein Näherungswert ist und keinen mehr Aufwand verursacht, der durch das Marshalling und die tatsächliche Datenerfassung verursacht wird.

</dd> </dl>

## <a name="how-to-interpret-property-qualifiers"></a>Interpretieren von Eigenschaften Qualifizierern

Eigenschaften in den [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) -Klassen enthalten die berechneten Daten, die von der [formatierten Leistungs Datenanbieter](formatted-performance-data-provider.md)bereitgestellt werden. Der Eigenschafts Wert ist das abschließende berechnete Ergebnis. Die Qualifizierer stellen eine Anleitung bereit.

Der **Counter** -und der **Basis** Qualifizierer zeigen auf die Datenquellen, und **cookingtype** gibt die Formel an, mit der das Ergebnis erzeugt wird. Der Zeitstempel und die Stichproben Häufigkeit stammen auch aus der entsprechenden RAW-Klasse und sind in **perftimestamp** und **perftimefreq** benannt.

Beispielsweise enthält eine der formatierten Klassen, die von WMI, [**Win32 \_ perfformatteddata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), bereitgestellt wird, eine Eigenschaft mit dem Namen **avgdiskbytesperread**. Der Name der Eigenschaft in der formatierten Klasse muss mit der Eigenschaft in der RAW-Klasse identisch sein. Die **avgdiskbytesperread** -Eigenschaft verfügt über die folgenden Qualifizierer.

In der folgenden Liste sind die verfügbaren Eigenschafts Qualifizierer für Eigenschaften aller von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleiteten Klassen aufgeführt.



| Qualifizierer         | Wert                     |
|-------------------|---------------------------|
| **Cookingtype**   | Durchschn. \_ Durchschnittswert \_       |
| **Leistungsindikator**       | Avgdiskbytesperread       |
| **Perftimestamp** | Zeitstempel ( \_ PerfTime)       |
| **Perftimefreq**  | \_PerfTime-Häufigkeit       |
| **Perfindex**     | 408                       |
| **Helpindex**     | 409                       |
| **Sock**          | Avgdiskbytesperread- \_ Basis |



 

Die **avgdiskbytesperread** -Eigenschaft meldet die durchschnittliche Anzahl von Bytes, die während Lesevorgängen vom Datenträger übertragen werden. Die Formel für die durchschnittliche Leistungsdauer \_ \_ ist:

(Sample2-sample1)/(Base sample2-Base sample1)

Der Lesevorgang wird mit der durch **perftimefreq** angegebenen Häufigkeit mit dem **perftimestamp** -Wert, der das aktuelle Beispiel anzeigt, abgefragt. Die Rohdaten des Leistungsindikators in Bytes werden von der **avgdiskbytesperread** -Eigenschaft in der [**Win32 \_ perfrawdata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) -Klasse entnommen. Die Basis Anzahl der Vorgangs Daten wird von der **avgdiskbytesperread- \_ Basis** Eigenschaft in derselben Klasse entnommen.

Weitere Informationen finden Sie unter Abrufen [statistischer Leistungsdaten](obtaining-statistical-performance-data.md) und über [Wachen von Leistungsdaten](monitoring-performance-data.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überwachen von Leistungsdaten](monitoring-performance-data.md)
</dt> <dt>

[Für WMI-Leistungsklassen spezifische Qualifizierer](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[Leistungs Leistungsdaten-Klassen](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Zugreifen auf vorinstallierte WMI-Leistungsklassen](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[WMI-Tasks: Leistungsüberwachung](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
