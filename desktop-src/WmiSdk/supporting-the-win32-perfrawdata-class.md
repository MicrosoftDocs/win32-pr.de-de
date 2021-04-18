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
# <a name="supporting-the-win32_perfrawdata-class"></a>Unterstützen der Win32 \_ perfrawdata-Klasse

Beim Schreiben eines Hochleistungs Anbieters, der Klassen von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)ableitet, müssen Sie bestimmte Konventionen befolgen, damit WMI Daten für die Eigenschaftswerte bereitstellen kann.

> [!Note]  
> Das Schreiben eines hochleistungsfähigen WMI-Anbieters zum Erstellen von Leistungsindikatoren wird in keiner Version des Windows-Betriebssystems empfohlen. Weitere Informationen finden Sie unter [Erstellen eines Instanzanbieters in einen High-Performance Anbieter](making-an-instance-provider-into-a-high-performance-provider.md)und [Leistungs Bibliotheken und WMI](performance-libraries-and-wmi.md).

 

Im folgenden Verfahren wird beschrieben, wie die [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klasse mit Ihrem Hochleistungs Anbieter unterstützt wird.

**So unterstützen Sie die Win32 \_ perfrawdata-Klasse**

1.  Erstellen Sie die-Klasse im root \\ CIMv2-Namespace.

    Die Klasse muss von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) abgeleitet werden, und der **HiPerf-Qualifizierer** muss auf " **true**" festgelegt sein. Sie können auch WDM-Leistungsdaten Klassen (Treiber) zum Stamm- \\ WMI-Namespace hinzufügen. Weitere Informationen zum Erstellen einer eigenen Klasse für WMI finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md).

2.  Geben Sie den Anbieter \_ \_ im **Anbieter Qualifizierer** als "NT5 genericperfprovider v1" an.
3.  Geben Sie die folgenden Qualifizierer auf Klassenebene an:

    -   **HiPerf**
    -   **Gebietsschema**
    -   **PerfDetail**
    -   **Anbieter**

    Weitere Informationen finden Sie unter [**Klassen Qualifizierer für Leistungs Leistungs Leistungs-Klassen**](class-qualifiers-for-performance-counter-classes.md). Definieren Sie den **genericperfctr** -Qualifizierer nicht, da dieser für den ADAP-Prozess reserviert ist, der Leistungs Bibliotheksdaten in WMI-Klassen überträgt.

4.  Füllen Sie die entsprechenden Zeitstempel-und Frequency-Eigenschaften auf, die zum Berechnen von Counter-Type-Formeln verwendet werden.

    Diese Eigenschaften werden von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) geerbt. Wenn Sie einen Hochleistungs Anbieter schreiben, müssen Sie diese Eigenschaften ausfüllen, damit die Klasse im System Monitor angezeigt wird.

5.  Fügen Sie eine Schlüsseleigenschaft namens **Name** in die Klasse ein (diese Eigenschaft ist für Singleton-Klassen nicht erforderlich).

    Sie dürfen keine andere Schlüsseleigenschaft als **Name** in ihrer Klasse verwenden.

6.  Erstellen Sie Eigenschaften Daten, die als **DWORD** (**UInt32**) oder **QWORD** (**UInt64**) typisiert sind. Diese Eigenschaften werden bei der Übertragung in die Leistungs Bibliotheken zu Leistungsindikatoren.
7.  Geben Sie die folgenden Qualifizierer auf Eigenschaften Ebene für alle Eigenschaften in der Klasse an:

    -   **DisplayName**
    -   **Counter Type**
    -   **DEFAULTSCALE**
    -   **Beschreibung**
    -   **PerfDefault**
    -   **PerfDetail**

    Weitere Informationen finden Sie unter [**Eigenschaften Qualifizierer für Leistungs Objektklassen**](property-qualifiers-for-performance-counter-classes.md). Außerdem enthält die Header Datei WINPERF. h Werte, die Sie für **PerfDetail** und **CounterType** angeben können.

    WMI verwendet die Qualifizierer " **Display Name**", " **locale**" und " **Description** " für die Lokalisierung. Sie müssen dem Namespace MS 409 (Englisch) geänderte Qualifizierer hinzufügen \_ , damit der System Monitor Ihre Klassen Daten ordnungsgemäß anzeigen kann. Dies bedeutet, dass Sie die Eigenschafts Definition durch Hinzufügen eines **Beschreibungs** Qualifizierers mit erklärendem Text ändern und den Wert **Display Name** ausfüllen. Außerdem müssen Sie allen anderen Gebiets Schema Namespaces, die Ihre Klasse unterstützt, geänderte Qualifizierer hinzufügen. Wenn ein Benutzerdaten von einem Gebiets Schema anfordert, für das Sie keine geänderten Qualifizierer bereitstellen, verwendet WMI standardmäßig die im MS \_ 409-Namespace angegebenen Definitionen.

8.  Erstellen Sie eine Basis Eigenschaft für jede Eigenschaft, die einen zähtertyp hat, der einen Basiswert erwartet.

    Diese Eigenschaft folgt unmittelbar der-Eigenschaft und hat den Namen * PropertyName ***\_ Base**. Die durchschnittliche Eigenschaft **avgdiskbytesperread** in der [**Win32 \_ perfrawdata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) -Klasse benötigt z. b. eine Basis Eigenschaft namens **avgdiskbytesperread \_ Base** , um die Anzahl der Stichproben zu zählen. Wenn Sie bestimmen möchten, ob der zu verwendende zähtertyp eine Basis Eigenschaft erfordert, suchen Sie in den [WMI-Leistungs Leistungsdaten Typen](wmi-performance-counter-types.md)nach dem zähtertyp nach Name oder Dezimalwert.

9.  Stellen Sie sicher, dass Ihr Anbieter die [Leistungsanforderungen](supporting-the-win32-perfformatteddata-class.md)erfüllt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Instanzanbieters in einen High-Performance-Anbieter](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
