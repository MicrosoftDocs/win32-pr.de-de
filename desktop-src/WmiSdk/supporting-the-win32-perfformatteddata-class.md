---
description: Beim Schreiben eines Hochleistungsanbieters, der Klassen von Win32 \_ PerfFormattedData ablege, müssen Sie bestimmte Konventionen befolgen, damit WMI die Eigenschaftswerte berechnen kann.
ms.assetid: 57912f6f-45ca-491c-8a6c-77e2a6937ccc
ms.tgt_platform: multiple
title: Unterstützen der Win32_PerfFormattedData-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bbed50bde7ef16f6362d28151744cf22d66e5d0f56df253ad48ab469b397d0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050128"
---
# <a name="supporting-the-win32_perfformatteddata-class"></a>Unterstützen der Win32 \_ PerfFormattedData-Klasse

Beim Schreiben eines Hochleistungsanbieters, der Klassen von [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)ablege, müssen Sie bestimmte Konventionen befolgen, damit WMI die Eigenschaftswerte berechnen kann.

> [!Note]  
> Das Schreiben eines WMI-Hochleistungsanbieters zum Erstellen von Leistungsindikatoren wird für keine Version des Windows Betriebssystems empfohlen. Weitere Informationen finden Sie unter [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and Performance [Libraries und WMI](performance-libraries-and-wmi.md).

 

Im folgenden Verfahren wird beschrieben, wie die Win32 \_ PerfFormattedData-Klasse unterstützt wird.

**So unterstützen Sie die Win32 \_ PerfFormattedData-Klasse**

1.  Erstellen Sie Ihre Klasse im selben Namespace wie die entsprechende rohe Klasse. Die Klasse muss von [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) abgeleitet sein und den **HiPerf-Qualifizierer** auf **TRUE** festlegen. Weitere Informationen zum Erstellen einer eigenen Klasse für WMI finden Sie unter [Entwerfen von MOF-Klassen (Managed Object Format).](designing-managed-object-format--mof--classes.md)
2.  Geben Sie "HiPerfCooker \_ v1" im [**Anbieterqualifizierer**](class-qualifiers-for-performance-counter-classes.md) an.
3.  Geben Sie zusätzlich zu den Qualifizierern, die für die rohen Klassen verwendet werden, die folgenden Qualifizierer auf Klassenebene an:

    -   [**AutoCook**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Autocook \_ RawClass**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Gekocht**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Teuer**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Dynamisch**](dynamic-qualifier.md)
    -   [**HiPerf**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Gebietsschema**](class-qualifiers-for-performance-counter-classes.md)
    -   [**PerfDefault**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Anbieter**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Singleton**](standard-wmi-qualifiers.md)

    > [!Note]  
    > Legen Sie keinen Wert für **GenericPerfCtr,** **PerfIndex** oder **HelpIndex** fest, da diese vom ADAP-Prozess festgelegt werden. Weitere Informationen finden Sie unter [**Klassenqualifizierer für Leistungsindikatorklassen.**](class-qualifiers-for-performance-counter-classes.md)

     

4.  Schließen Sie eine Schlüsseleigenschaft namens **Name** in Ihre Klasse ein (diese Eigenschaft ist für Singletonklassen nicht erforderlich).

    Der Wert der **Name-Eigenschaft** muss mit der entsprechenden rohen Klasse identisch sein. Sie dürfen keine andere Schlüsseleigenschaft als **Name** für Ihre Klasse verwenden.

5.  Erstellen Sie Eigenschaftendaten, die entweder als **DWORD** (**uint32**) oder **QWORD** (**uint64**) typisiert sind.

    Die Eigenschaften müssen entweder einer Eigenschaft in der raw-Klasse oder einer Eigenschaft in der Klasse entsprechen, die Sie erstellen.

6.  Geben Sie zusätzlich zu den **Qualifizierern PerfIndex** und **PerfDetail,** die für die Rohklasseneigenschaften verwendet werden, die folgenden Eigenschaftsebenenqualifizierer für alle Eigenschaften in der Klasse an:

    -   [**Basis**](property-qualifiers-for-performance-counter-classes.md)
    -   [**Erodetyp**](property-qualifiers-for-performance-counter-classes.md)
    -   [**Leistungsindikator**](property-qualifiers-for-performance-counter-classes.md)
    -   [**PerfTimeStamp**](property-qualifiers-for-performance-counter-classes.md)
    -   [**PerfTimeFreq**](property-qualifiers-for-performance-counter-classes.md)
    -   [**SampleWindow**](property-qualifiers-for-performance-counter-classes.md)

    Weitere Informationen finden Sie unter [**Eigenschaftenqualifizierer für Leistungsindikatorklassen.**](property-qualifiers-for-performance-counter-classes.md) Darüber hinaus enthält die Headerdatei Winperf.h Werte, die Sie für **PerfDetail** und **CounterType** angeben können.

7.  Stellen Sie sicher, dass Ihr Anbieter die [Leistungsanforderungen](#performance-requirements)erfüllt.

## <a name="performance-requirements"></a>Leistungsanforderungen

Wenn Sie einen Hochleistungsanbieter schreiben, muss seine Leistung die folgenden Anforderungen erfüllen:

-   Das Öffnen der Hochleistungs-DLL-Datei kann nicht mehr als 100 Millisekunden dauern. Insgesamt darf das Öffnen jedes Anbieters und der Leistungsbibliothek für hohe Leistung 5 Sekunden nicht überschreiten.
-   Die Datenaktualisierung kann nicht mehr als 10 Millisekunden pro Sammlung dauern. Bei einem allgemeinen Aktualisierungs- und Erfassungsvorgang können alle Hochleistungsanbieter zusammen nicht mehr als 800 Millisekunden dauern.
-   Die CPU-Gesamtauslastung für alle Anbieter mit hoher Leistung darf 6 bis 7 % CPU-Mehraufwand interaktiv oder 5 % für die Protokollierung nicht überschreiten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Instanzanbieters zu einem High-Performance Anbieter](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
