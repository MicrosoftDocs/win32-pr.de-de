---
description: Beim Schreiben eines Hochleistungsanbieters, der Klassen von Win32 \_ PerfRawData abgeleitet, müssen Sie bestimmte Konventionen befolgen, damit WMI Daten für die Eigenschaftswerte bereitstellen kann.
ms.assetid: 04abb2f9-800f-497a-ac8f-8ef210746273
ms.tgt_platform: multiple
title: Unterstützen der Win32_PerfRawData-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70c9899c88849c70265b019c1d73021c61cae4758c41f462349537bd2e806ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050118"
---
# <a name="supporting-the-win32_perfrawdata-class"></a>Unterstützen der Win32 \_ PerfRawData-Klasse

Beim Schreiben eines Hochleistungsanbieters, der Klassen von [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)abgeleitet, müssen Sie bestimmte Konventionen befolgen, damit WMI Daten für die Eigenschaftswerte bereitstellen kann.

> [!Note]  
> Das Schreiben eines WMI-Hochleistungsanbieters zum Erstellen von Leistungsindikatoren wird für keine Version des Windows Betriebssystems empfohlen. Weitere Informationen finden Sie unter [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and Performance [Libraries und WMI](performance-libraries-and-wmi.md).

 

Im folgenden Verfahren wird beschrieben, wie Sie die [**Win32 \_ PerfRawData-Klasse**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) mit Ihrem Hochleistungsanbieter unterstützen.

**So unterstützen Sie die Win32 \_ PerfRawData-Klasse**

1.  Erstellen Sie Ihre Klasse im \\ Root CIMv2-Namespace.

    Die Klasse muss von [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) abgeleitet sein und den **Hiperf-Qualifizierer** auf **TRUE** festlegen. Sie können dem wmi-Stammnamespace auch Leistungsdatenklassen für WDM (Treiber) \\ hinzufügen. Weitere Informationen zum Erstellen einer eigenen Klasse für WMI finden Sie unter [Entwerfen von MOF-Klassen (Managed Object Format).](designing-managed-object-format--mof--classes.md)

2.  Geben Sie den Anbieter im Anbieterqualifizierer als "NT5 \_ GenericPerfProvider \_ V1" an. 
3.  Geben Sie die folgenden Qualifizierer auf Klassenebene an:

    -   **HiPerf**
    -   **Gebietsschema**
    -   **PerfDetail**
    -   **Anbieter**

    Weitere Informationen finden Sie unter [**Klassenqualifizierer für Leistungsindikatorklassen.**](class-qualifiers-for-performance-counter-classes.md) Definieren Sie den **GenericPerfCtr-Qualifizierer** nicht, da dieser für den ADAP-Prozess reserviert ist, der Leistungsbibliotheksdaten in WMI-Klassen überträgt.

4.  Füllen Sie die entsprechenden Zeitstempel- und Häufigkeitseigenschaften auf, die zum Berechnen von Gegentypformeln verwendet werden.

    Diese Eigenschaften werden von [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) geerbt. Wenn Sie einen Hochleistungsanbieter schreiben, müssen Sie diese angaben, damit die Klasse im Systemmonitor angezeigt wird.

5.  Schließen Sie eine Schlüsseleigenschaft namens **Name** in Ihre Klasse ein (diese Eigenschaft ist für Singletonklassen nicht erforderlich).

    Sie dürfen keine andere Schlüsseleigenschaft als **Name** für Ihre Klasse verwenden.

6.  Erstellen Sie Eigenschaften, die entweder als **DWORD** (**uint32**) oder **QWORD** (**uint64**) typisiert sind. Diese Eigenschaften werden zu Leistungsindikatoren, wenn sie an die Leistungsbibliotheken übertragen werden.
7.  Geben Sie die folgenden Eigenschaftsebenenqualifizierer für alle Eigenschaften in Ihrer Klasse an:

    -   **DisplayName**
    -   **Countertype**
    -   **DefaultScale**
    -   **Beschreibung**
    -   **PerfDefault**
    -   **PerfDetail**

    Weitere Informationen finden Sie unter [**Eigenschaftenqualifizierer für Leistungsindikatorklassen.**](property-qualifiers-for-performance-counter-classes.md) Darüber hinaus enthält die Headerdatei Winperf.h Werte, die Sie für **PerfDetail** und **CounterType** angeben können.

    WMI verwendet die Qualifizierer **DisplayName,** **Locale** und **Description** für die Lokalisierung. Sie müssen dem MS \_ 409-Namespace (Englisch) geänderte Qualifizierer hinzufügen, damit SystemMonitor Ihre Klassendaten ordnungsgemäß anzeigen kann. Dies bedeutet, dass Sie die  Eigenschaftendefinition ändern, indem Sie einen Description-Qualifizierer mit erläuterndem Text hinzufügen und den **DisplayName-Wert** ausfüllen. Außerdem müssen Sie jedem anderen Gebietsschemanamespace, den Ihre Klasse unterstützt, geänderte Qualifizierer hinzufügen. Wenn ein Benutzer Daten von einem Gebietsschema anfordert, für das Sie keine geänderten Qualifizierer angeben, verwendet WMI standardmäßig die Definitionen, die im MS \_ 409-Namespace angegeben sind.

8.  Erstellen Sie eine Basiseigenschaft für jede Eigenschaft, die über einen Indikatortyp verfügt, der einen Basiswert erwartet.

    Diese Eigenschaft folgt unmittelbar auf die -Eigenschaft und hat den Namen *Propertyname***\_ Basis.** Beispielsweise erfordert die durchschnittliche Eigenschaft **AvgDiskBytesPerRead** in der [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk-Klasse**](./retrieving-raw-and-formatted-performance-data.md) eine Basiseigenschaft mit dem Namen **AvgDiskBytesPerRead \_ Base,** um die Anzahl der Stichproben zu zählen. Um zu bestimmen, ob der indikatortyp, den Sie verwenden möchten, eine Basiseigenschaft erfordert, suchen Sie den Indikatortyp nach Name oder Dezimalwert in [WMI-Leistungsindikatortypen.](wmi-performance-counter-types.md)

9.  Stellen Sie sicher, dass Ihr Anbieter die [Leistungsanforderungen](supporting-the-win32-perfformatteddata-class.md)erfüllt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Instanzanbieters zu einem High-Performance Anbieter](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
