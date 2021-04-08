---
description: Beim Arbeiten mit Leistungsdaten verwenden Sie die folgenden Strukturen.
ms.assetid: 97118b64-3a2f-49c0-92e7-324df08bdb12
title: Strukturen der Leistungsindikatoren
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 0629aa1763f08dfce9e2cc646bd1b5744d6591cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959749"
---
# <a name="performance-counters-structures"></a>Strukturen der Leistungsindikatoren

Beim Arbeiten mit Leistungsdaten verwenden Sie die folgenden Strukturen.

Informationen zu den Funktionen, die für die Arbeit mit Leistungsindikatoren verfügbar sind, finden Sie unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md).

## <a name="performance-data-helper-pdh-structures"></a>PDH-Strukturen (Performance Data Helper)

Consumer, die die [PDH-Funktionen (Performance Data Helper)](using-the-pdh-functions-to-consume-counter-data.md) verwenden, verwenden die folgenden Strukturen:

- [**PDH \_ Durchsuchen der \_ DLG- \_ Konfiguration**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a)
- [**PDH \_ Durchsuchen der \_ DLG- \_ Konfiguration \_ H**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_ha)
- [**PDH- \_ gegen \_ Info**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_info_a)
- [**PDH- \_ counter- \_ \_ Element Pfad Elemente**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)
- [**PDH- \_ Daten \_ Element Pfad- \_ \_ Elemente**](/windows/desktop/api/Pdh/ns-pdh-pdh_data_item_path_elements_a)
- [**PDH-Kenn Wort \_ \_ CounterValue**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue)
- [**PDH- \_ Element " \_ CounterValue" \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue_item_a)
- [**PDH- \_ Rohdaten \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)
- [**PDH- \_ rohleistungs-Leistungs \_ \_ Element**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter_item_a)
- [**PDH \_ - \_ rohprotokoll \_ Daten Satz**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_log_record)
- [**PDH- \_ Statistik**](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics)
- [**PDH- \_ Zeit \_ Informationen**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info)

## <a name="perflib-v2-consumer-structures"></a>Perflib v2-consumerstrukturen

Consumer, die die [Perflib v2](using-the-perflib-functions-to-consume-counter-data.md) -consumerfunktionen verwenden, verwenden die folgenden Strukturen:

- [**Leistungsdaten für Leistungs \_ \_ Daten**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_data)
- [**Leistungs \_ Zählers- \_ Header**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_header)
- [**Leistungs \_ \_ Bezeichner**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identifier)
- [**Zuordnungs \_ Informationen des Leistungs Zählers \_ \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_reg_info)
- [**Informationen zur Leistungsindikator-reg-über \_ legung \_ \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_reg_info)
- [**Perf- \_ Daten \_ Header**](/windows/desktop/api/Perflib/ns-perflib-perf_data_header)
- [**Perf \_ - \_ instanzheader**](/windows/desktop/api/Perflib/ns-perflib-perf_instance_header)
- [**Leistungsindikatoren für mehrere Leistungsindikatoren \_ \_**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_counters)
- [**\_mehrere Instanzen von perf \_**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_instances)
- [**Perf- \_ Zeichen folgen \_ Puffer \_ Header**](/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header)
- [**Leistungs \_ zeichenfolgencounter- \_ \_ Header**](/windows/win32/api/perflib/ns-perflib-perf_string_counter_header)

## <a name="perflib-v2-provider-structures"></a>Perflib v2-Anbieter Strukturen

[V2-Leistungsdaten Anbieter](providing-counter-data-using-version-2-0.md) verwenden die folgenden Strukturen:

- [**Identität des Leistungs \_ Zählers \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [**Leistungsdaten \_ gegen \_ Info**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [**Leistungsindikator \_ \_ Informationen**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [**Perf- \_ CounterSet- \_ Instanz**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)
- [**Perf- \_ Anbieter \_ Kontext**](/windows/win32/api/perflib/ns-perflib-perf_provider_context)

## <a name="performance-dll-structures"></a>Leistungs-DLL-Strukturen

[Leistungs Erweiterungen-DLL-Anbieter](providing-counter-data-using-a-performance-dll.md) und-Consumer [, die die Registrierungsfunktionen zum Verarbeiten von Leistungsdaten verwenden,](using-the-registry-functions-to-consume-counter-data.md) verwenden die folgenden Strukturen:

- [**Leistungs- \_ counter- \_ Block**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block)
- [**Leistungs-Leistungswert \_ \_ Definition**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)
- [**Perf- \_ Daten \_ Block**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block)
- [**Perf \_ - \_ Instanzdefinition**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition)
- [**Perf \_ - \_ Objekttyp**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type)
