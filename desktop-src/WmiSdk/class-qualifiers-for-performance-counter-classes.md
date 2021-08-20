---
description: Geben Sie Informationen zum Leistungsobjekt an, dem die WMI-Leistungsindikatorklasse zugeordnet ist.
ms.assetid: 7b8b7f00-95d8-4c1e-8638-157d0f4c7c32
ms.tgt_platform: multiple
title: Klassenqualifizierer für Leistungsindikatorklassen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b8168dcc0523c629202ac4d5c4a0ea51ecc8bd68d5ac4498fb38059b940fd83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820095"
---
# <a name="class-qualifiers-for-performance-counter-classes"></a>Klassenqualifizierer für Leistungsindikatorklassen

Klassenqualifizierer geben Informationen über das Leistungsobjekt an, dem die [WMI-Leistungsindikatorklasse](/windows/desktop/CIMWin32Prov/performance-counter-classes) zugeordnet ist. Weitere Informationen finden Sie unter [Überwachen von Leistungsdaten.](monitoring-performance-data.md)

-   [Qualifizierer für "Raw" und "Formatted PerformanceClasses"](#qualifiers-for-raw-and-formatted-performanceclasses)
-   [Qualifizierer für Rohleistungsklassen](#)
-   [Qualifizierer für formatierte Leistungsklassen](#)
-   [Zugehörige Themen](#related-topics)


Leistungsindikatorspezifische Qualifizierer werden automatisch vom Anbieter "WbemPerfClass" an [**Win32 \_ PerfRawData-Klassen**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) und -Eigenschaften in Root \\ CIMv2 angefügt.

Diese Informationen gelten für alle Instanzen der -Klasse. Einige Qualifizierer **mit booleschen Werten,** die immer **FALSE** sind, sind für bestimmte Klassen möglicherweise nicht vorhanden.

## <a name="qualifiers-for-raw-and-formatted-performanceclasses"></a>Qualifizierer für "Raw" und "Formatted PerformanceClasses"

Die folgenden Qualifizierer gelten für alle Klassen, die von [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) und [**Win32 \_ PerfFormattedData abgeleitet werden.**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)

<dl> <dt>

<span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Gekocht**
</dt> <dd>

**boolean**

Gibt an, ob die Klasse kapselte Daten enthält.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Displayname**
</dt> <dd>

**string**

Leistungsobjektname. Weitere Informationen finden Sie unter [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**
</dt> <dd>

**sint32**

Stellt keine Detaildaten zur Verfügung. Enthält immer den Wert 100.

</dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Dynamische**
</dt> <dd>

**boolean**

Immer auf **True festgelegt,** da Instanzen immer dynamisch sind.

</dd> <dt>

<span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**
</dt> <dd>

**boolean**

Gibt an, ob die Klasse aus einer Legacyleistungsbibliothek stammt. Legen Sie immer auf **True fest.**

</dd> <dt>

<span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**
</dt> <dd>

**sint32**

Indizes sind nicht mehr gültig. Dieser Qualifizierer ist immer 0 (null).

</dd> <dt>

<span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf** 
</dt> <dd>

**boolean**

Gibt an, dass die -Klasse eine Hochleistungsklasse ist. Legen Sie immer auf **True fest.**

</dd> <dt>

<span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**
</dt> <dd>

**sint32**

Gebietsschemabezeichner Der Wert ist immer 1033 (ENGLISCH, USA).

</dd> <dt>

<span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**
</dt> <dd>

**int32**

Indizes sind nicht mehr gültig. Dieser Qualifizierer ist immer 0 (null).

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Anbieter**
</dt> <dd>

**string**

Name des Instanzanbieters. Der Wert ist "WbemPerfV2".

</dd> <dt>

<span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**Registrykey**
</dt> <dd>

**string**

Name des Treibers im **Schlüssel HKEY \_ LOCAL MACHINE \_ \\ CurrentControlSet \\ Services,** unter dem sich der Leistungsschlüssel befinden kann. Dieser Name ist auch der Name des Diensts, der den Leistungsindikator bietet.

</dd> <dt>

<span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**
</dt> <dd>

**boolean**

True **gibt** an, dass nur eine einzelne Instanz der -Klasse vorhanden ist.

</dd> </dl>

## <a name="qualifiers-for-raw-performance-classes"></a>Qualifizierer für Rohleistungsklassen

Die folgenden Qualifizierer gelten für alle Klassen, die von [**Win32 \_ PerfRawData abgeleitet werden.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)

<dl> <dt>

<span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Teuer**
</dt> <dd>

**boolean**

Gibt an, ob das Abrufen von Instanzen dieser Klasse ein kostspieliger Vorgang ist. Legen Sie für **Klassen,** deren "Costly" an das Ende des Klassennamens angefügt ist, immer \_ auf True fest.

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**
</dt> <dd>

**uint32**

Stellt keine Detaildaten zur Verfügung. Enthält immer den Wert 100.

</dd> <dt>

<span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**
</dt> <dd>

**boolean**

Der Wert ist immer **False.**

</dd> </dl>

## <a name="qualifiers-for-formatted-performance-classes"></a>Qualifizierer für formatierte Leistungsklassen

Die folgenden Qualifizierer gelten für alle Klassen, die von [**Win32 \_ PerfFormattedData abgeleitet werden.**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)

<dl> <dt>

<span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**AutoCook**
</dt> <dd>

**int32**

Gibt an, dass die Werte in Klasseninstanzen automatisch aus der entsprechenden Rohdatenklasse berechnet werden. Der Wert ist immer 1.

</dd> <dt>

<span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**AutoCook \_ RawClass**
</dt> <dd>

**string**

Name der rohen Klasse, die für die Berechnung der formatierten Klasse verwendet werden soll. Dieser Qualifizierer ist erforderlich.

</dd> </dl>

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

 

 
