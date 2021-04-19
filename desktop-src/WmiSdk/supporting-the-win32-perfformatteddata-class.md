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
# <a name="supporting-the-win32_perfformatteddata-class"></a>Unterstützen der Win32 \_ perfformatteddata-Klasse

Beim Schreiben eines Hochleistungs Anbieters, der Klassen von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)ableitet, müssen Sie bestimmte Konventionen befolgen, damit die Eigenschaftswerte von WMI berechnet werden können.

> [!Note]  
> Das Schreiben eines hochleistungsfähigen WMI-Anbieters zum Erstellen von Leistungsindikatoren wird in keiner Version des Windows-Betriebssystems empfohlen. Weitere Informationen finden Sie unter [Erstellen eines Instanzanbieters in einen High-Performance Anbieter](making-an-instance-provider-into-a-high-performance-provider.md)und [Leistungs Bibliotheken und WMI](performance-libraries-and-wmi.md).

 

Im folgenden Verfahren wird beschrieben, wie die Win32 \_ perfformatteddata-Klasse unterstützt wird.

**So unterstützen Sie die Win32 \_ perfformatteddata-Klasse**

1.  Erstellen Sie die Klasse im selben Namespace wie die entsprechende RAW-Klasse. Die Klasse muss von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) abgeleitet werden, und der **HiPerf-Qualifizierer** muss auf " **true**" festgelegt sein. Weitere Informationen zum Erstellen einer eigenen Klasse für WMI finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md).
2.  Geben Sie \_ im [**Anbieter Qualifizierer**](class-qualifiers-for-performance-counter-classes.md) "hiperfkocher v1" an.
3.  Geben Sie zusätzlich zu den für die RAW-Klassen verwendeten Qualifizierern die folgenden Qualifizierer auf Klassenebene an:

    -   [**Autokoch**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Autocook \_ rawclass**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Über**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Aufwendigen**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Schem**](dynamic-qualifier.md)
    -   [**HiPerf**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Gebietsschema**](class-qualifiers-for-performance-counter-classes.md)
    -   [**PerfDefault**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Anbieter**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Singleton**](standard-wmi-qualifiers.md)

    > [!Note]  
    > Legen Sie keinen Wert für **genericperfctr**, **perfindex** oder **helpindex** fest, da diese durch den ADAP-Prozess festgelegt werden. Weitere Informationen finden Sie unter [**Klassen Qualifizierer für Leistungs Leistungs Leistungs-Klassen**](class-qualifiers-for-performance-counter-classes.md).

     

4.  Fügen Sie eine Schlüsseleigenschaft namens **Name** in die Klasse ein (diese Eigenschaft ist für Singleton-Klassen nicht erforderlich).

    Der Wert der **Name** -Eigenschaft muss mit der entsprechenden RAW-Klasse identisch sein. Sie dürfen keine andere Schlüsseleigenschaft als **Name** in ihrer Klasse verwenden.

5.  Erstellen Sie Eigenschaften Daten, die entweder als **DWORD** (**UInt32**) oder **QWORD** (**UInt64**) typisiert sind.

    Die Eigenschaften müssen entweder einer Eigenschaft in der RAW-Klasse oder einer Eigenschaft in der Klasse entsprechen, die Sie erstellen.

6.  Geben Sie die folgenden Qualifizierer auf Eigenschaften Ebene für alle Eigenschaften in der Klasse an, zusätzlich zu den **perfindex** -und **PerfDetail** -Qualifizierern, die für die RAW-Klasseneigenschaften

    -   [**Sock**](property-qualifiers-for-performance-counter-classes.md)
    -   [**Cookingtype**](property-qualifiers-for-performance-counter-classes.md)
    -   [**Leistungsindikator**](property-qualifiers-for-performance-counter-classes.md)
    -   [**Perftimestamp**](property-qualifiers-for-performance-counter-classes.md)
    -   [**Perftimefreq**](property-qualifiers-for-performance-counter-classes.md)
    -   [**SampleWindow**](property-qualifiers-for-performance-counter-classes.md)

    Weitere Informationen finden Sie unter [**Eigenschaften Qualifizierer für Leistungs Objektklassen**](property-qualifiers-for-performance-counter-classes.md). Außerdem enthält die Header Datei WINPERF. h Werte, die Sie für **PerfDetail** und **CounterType** angeben können.

7.  Stellen Sie sicher, dass Ihr Anbieter die [Leistungsanforderungen](#performance-requirements)erfüllt.

## <a name="performance-requirements"></a>Leistungsanforderungen

Wenn Sie einen Hochleistungs Anbieter schreiben, muss seine Leistung die folgenden Anforderungen erfüllen:

-   Das Öffnen der DLL-Datei mit hoher Leistung kann höchstens 100 Millisekunden dauern. Insgesamt kann das Öffnen der einzelnen Hochleistungs Anbieter und Leistungs Bibliotheken 5 Sekunden nicht überschreiten.
-   Die Datenaktualisierung kann höchstens 10 Millisekunden pro Erfassung dauern. Bei einem allgemeinen Aktualisierungs-und Sammel Vorgang können alle Hochleistungs Anbieter zusammen mehr als 800 Millisekunden beanspruchen.
-   Die CPU-Gesamtauslastung für alle Hochleistungs Anbieter kann den CPU-Overhead von 6-7% interaktiv oder 5% für die Protokollierung überschreiten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Instanzanbieters in einen High-Performance-Anbieter](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
