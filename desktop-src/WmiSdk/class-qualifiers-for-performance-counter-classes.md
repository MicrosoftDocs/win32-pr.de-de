---
description: Geben Sie Informationen zum Leistungs Objekt an, dem die WMI-Leistungs Objektklasse zugeordnet ist.
ms.assetid: 7b8b7f00-95d8-4c1e-8638-157d0f4c7c32
ms.tgt_platform: multiple
title: Klassen Qualifizierer für Leistungs Leistungsdaten Klassen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4910af88ce7f96fda1b5f9b7ecd7a33479fc130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364086"
---
# <a name="class-qualifiers-for-performance-counter-classes"></a>Klassen Qualifizierer für Leistungs Leistungsdaten Klassen

Klassen Qualifizierer geben Informationen über das Leistungs Objekt an, dem die WMI- [Leistungs Objektklasse](/windows/desktop/CIMWin32Prov/performance-counter-classes) zugeordnet ist. Weitere Informationen finden Sie unter über [Wachen von Leistungsdaten](monitoring-performance-data.md).

-   [Qualifizierer für Rohdaten und formatierte performanceclasses](#qualifiers-for-raw-and-formatted-performanceclasses)
-   [Qualifizierer für rohleistungs Klassen](#)
-   [Qualifizierer für formatierte Leistungsklassen](#)
-   [Zugehörige Themen](#related-topics)


Leistungs Zählers – bestimmte Qualifizierer werden automatisch durch den Anbieter "WbemPerfClass" an [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klassen und-Eigenschaften in root CIMv2 angefügt \\ .

Diese Informationen gelten für alle Instanzen der-Klasse. Einige Qualifizierer mit **booleschen** Werten, die immer **false** sind, sind möglicherweise nicht für bestimmte Klassen vorhanden.

## <a name="qualifiers-for-raw-and-formatted-performanceclasses"></a>Qualifizierer für Rohdaten und formatierte performanceclasses

Die folgenden Qualifizierer gelten für alle Klassen, die von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) und [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleitet werden.

<dl> <dt>

<span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Über**
</dt> <dd>

**boolean**

Gibt an, ob die Klasse gekochte Daten enthält.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Display Name**
</dt> <dd>

**string**

Der Name des Leistungsobjekts. Weitere Informationen finden Sie unter [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**Detail Level**
</dt> <dd>

**sint32**

Stellt keine Detaildaten bereit. Enthält immer den Wert 100.

</dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Schem**
</dt> <dd>

**boolean**

Ist immer auf " **true** " festgelegt, da Instanzen immer dynamisch sind.

</dd> <dt>

<span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**Genericperfctr**
</dt> <dd>

**boolean**

Gibt an, ob die Klasse aus einer Legacy-Leistungs Bibliothek stammt. Immer auf " **true**" festgelegt.

</dd> <dt>

<span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**Helpindex**
</dt> <dd>

**sint32**

Indizes sind nicht mehr gültig. Dieser Qualifizierer ist immer NULL.

</dd> <dt>

<span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf** 
</dt> <dd>

**boolean**

Gibt an, dass die Klasse eine Hochleistungs Klasse ist. Immer auf " **true**" festgelegt.

</dd> <dt>

<span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Konfigurations**
</dt> <dd>

**sint32**

Gebietsschemabezeichner Der Wert ist immer 1033 (US-Englisch).

</dd> <dt>

<span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**Perfindex**
</dt> <dd>

**int32**

Indizes sind nicht mehr gültig. Dieser Qualifizierer ist immer NULL.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Ab**
</dt> <dd>

**string**

Der Name des Instanzanbieters. Der Wert ist "WbemPerfV2".

</dd> <dt>

<span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**
</dt> <dd>

**string**

Der Name des Treibers im Schlüssel des **lokalen HKEY-Computers \_ \_ \\ CurrentControlSet \\ Services** , unter dem sich der Leistungs Schlüssel befinden kann. Dieser Name ist auch der Name des Dienstanbieter, der den Leistungswert bereitstellt.

</dd> <dt>

<span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**
</dt> <dd>

**boolean**

**True** gibt an, dass nur eine einzelne Instanz der Klasse vorhanden ist.

</dd> </dl>

## <a name="qualifiers-for-raw-performance-classes"></a>Qualifizierer für rohleistungs Klassen

Die folgenden Qualifizierer gelten für alle Klassen, die von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)abgeleitet werden.

<dl> <dt>

<span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Aufwendigen**
</dt> <dd>

**boolean**

Gibt an, ob das Abrufen von Instanzen dieser Klasse ein kostspieliger Vorgang ist. Wird immer auf **true** festgelegt, wenn Klassen mit \_ dem "teuren" an das Ende des Klassen namens angehängt werden.

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**Detail Level**
</dt> <dd>

**uint32**

Stellt keine Detaildaten bereit. Enthält immer den Wert 100.

</dd> <dt>

<span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**
</dt> <dd>

**boolean**

Der Wert ist immer **false**.

</dd> </dl>

## <a name="qualifiers-for-formatted-performance-classes"></a>Qualifizierer für formatierte Leistungsklassen

Die folgenden Qualifizierer gelten für alle Klassen, die von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleitet werden.

<dl> <dt>

<span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**Autokoch**
</dt> <dd>

**int32**

Gibt an, dass die Werte in den Klassen Instanzen automatisch aus der entsprechenden Rohdaten Klasse berechnet werden. Der Wert ist immer 1.

</dd> <dt>

<span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**Autocook \_ rawclass**
</dt> <dd>

**string**

Der Name der RAW-Klasse, die für die Berechnung der formatierten Klasse verwendet werden soll. Dieser Qualifizierer ist erforderlich.

</dd> </dl>

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

 

 
