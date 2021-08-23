---
description: Beim Arbeiten mit Leistungsdaten verwenden Sie die folgenden Strukturen.
ms.assetid: 97118b64-3a2f-49c0-92e7-324df08bdb12
title: Strukturen der Leistungsindikatoren
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 00e9a505a9fe74592f571f3db108af2247a6d44889bc3ddbc2e4dae0844600b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674750"
---
# <a name="performance-counters-structures"></a>Strukturen der Leistungsindikatoren

Beim Arbeiten mit Leistungsdaten verwenden Sie die folgenden Strukturen.

Informationen zu den Funktionen, die für die Arbeit mit Leistungsindikatoren verfügbar sind, finden Sie unter Funktionen für [Leistungsindikatoren.](performance-counters-functions.md)

## <a name="performance-data-helper-pdh-structures"></a>PdH-Strukturen (Performance Data Helper)

Consumer, die die [PdH-Funktionen (Performance Data Helper)](using-the-pdh-functions-to-consume-counter-data.md) verwenden, verwenden die folgenden Strukturen:

- [**PDH \_ BROWSE \_ DLG \_ CONFIG**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a)
- [**PDH \_ BROWSE \_ DLG \_ CONFIG \_ H**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_ha)
- [**\_PDH-INDIKATORINFORMATIONEN \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_info_a)
- [**\_ \_ PDH-INDIKATORPFADELEMENTE \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)
- [**\_ \_ PDH-DATENELEMENTPFADELEMENTE \_ \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_data_item_path_elements_a)
- [**PDH \_ FMT \_ COUNTERVALUE**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue)
- [**PDH \_ FMT \_ COUNTERVALUE \_ ITEM**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue_item_a)
- [**PDH \_ RAW \_ COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)
- [**PDH \_ RAW \_ COUNTER \_ ITEM**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter_item_a)
- [**\_UNFORMATIERTEN \_ PDH-PROTOKOLLDATENSATZ \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_log_record)
- [**PDH \_ STATISTICS**](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics)
- [**PDH \_ TIME \_ INFO**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info)

## <a name="perflib-v2-consumer-structures"></a>PerfLib V2-Consumerstrukturen

Consumer, die die [PerfLib V2-Consumerfunktionen](using-the-perflib-functions-to-consume-counter-data.md) verwenden, verwenden die folgenden Strukturen:

- [**\_PERF-INDIKATORDATEN \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_data)
- [**\_ \_ PERF-INDIKATORHEADER**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_header)
- [**\_ \_ PERF-INDIKATORBEZEICHNER**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identifier)
- [**PERF \_ COUNTER \_ REG \_ INFO**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_reg_info)
- [**PERF \_ COUNTERSET \_ REG \_ INFO**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_reg_info)
- [**\_ \_ PERF-DATENHEADER**](/windows/desktop/api/Perflib/ns-perflib-perf_data_header)
- [**\_ \_ PERF-INSTANZHEADER**](/windows/desktop/api/Perflib/ns-perflib-perf_instance_header)
- [**PERF \_ MULTI \_ COUNTERS**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_counters)
- [**PERF \_ MULTI \_ INSTANCES**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_instances)
- [**\_ \_ PERF-ZEICHENFOLGENPUFFERHEADER \_**](/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header)
- [**\_ \_ PERF-ZEICHENFOLGENZÄHLERHEADER \_**](/windows/win32/api/perflib/ns-perflib-perf_string_counter_header)

## <a name="perflib-v2-provider-structures"></a>PerfLib V2-Anbieterstrukturen

[V2-Leistungsdatenanbieter](providing-counter-data-using-version-2-0.md) verwenden die folgenden Strukturen:

- [**\_PERF-INDIKATORIDENTITÄT \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [**\_PERF-INDIKATORINFORMATIONEN \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [**PERF \_ COUNTERSET \_ INFO**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [**PERF \_ \_ COUNTERSET-INSTANZ**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)
- [**\_PERF-ANBIETERKONTEXT \_**](/windows/win32/api/perflib/ns-perflib-perf_provider_context)

## <a name="performance-dll-structures"></a>Leistungs-DLL-Strukturen

[DLL-Anbieter](providing-counter-data-using-a-performance-dll.md) und Consumer der Leistungserweiterung, die die Registrierungsfunktionen zum Nutzen von [Indikatordaten verwenden,](using-the-registry-functions-to-consume-counter-data.md) verwenden die folgenden Strukturen:

- [**\_PERF-INDIKATORBLOCK \_**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block)
- [**\_PERF-INDIKATORDEFINITION \_**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)
- [**\_PERF-DATENBLOCK \_**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block)
- [**\_PERF-INSTANZDEFINITION \_**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition)
- [**\_PERF-OBJEKTTYP \_**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type)
