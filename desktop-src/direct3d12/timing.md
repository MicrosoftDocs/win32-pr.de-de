---
title: Zeitsteuerung (Direct3D 12-Grafiken)
description: In diesem Abschnitt wird das Abfragen von Zeitstempeln und das Kalibrieren der GPU- und CPU-Zeitstempelzähler behandelt.
ms.assetid: CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84676d36523fe23d33946e164d245e1619eb41d0af11a898acc52194348e439
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045368"
---
# <a name="timing-direct3d-12-graphics"></a>Zeitsteuerung (Direct3D 12-Grafiken)

In diesem Abschnitt wird das Abfragen von Zeitstempeln und das Kalibrieren der GPU- und CPU-Zeitstempelzähler behandelt.

## <a name="timestamp-frequency"></a>Zeitstempelhäufigkeit

Ihre Anwendung kann die GPU-Zeitstempelhäufigkeit pro Befehlswarteschlange abfragen (siehe [**ID3D12CommandQueue::GetTimestampFrequency-Methode).**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency)

Die zurückgegebene Häufigkeit wird in Hz (Ticks/s) gemessen. Wenn die angegebene [Befehlswarteschlange](queries.md) keine Zeitstempel unterstützt (siehe Tabelle im Abschnitt Abfragen), schlägt diese API fehl (und gibt E_FAIL) **zurück.** [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) und [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) unterstützen immer Zeitstempel. [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) unterstützt optional Zeitstempel, wenn das [**D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported-Member**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) **TRUE ist.**

## <a name="timestamp-calibration"></a>Zeitstempel-Kalibrierung

D3D12 ermöglicht Anwendungen das Korrelieren von Ergebnissen aus Zeitstempelabfragen mit Ergebnissen, die beim Aufrufen von erhalten `QueryPerformanceCounter` wurden. Dies wird durch den Aufruf [**ID3D12CommandQueue::GetClockCalibration aktiviert.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)

[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) samples the GPU timestamp counter for a given command queue and samples the CPU counter via `QueryPerformanceCounter` at fast the same time. Auch hier schlägt diese API fehl (gibt E FAIL zurück), wenn die angegebene Befehlswarteschlange keine Zeitstempel unterstützt (siehe Tabelle \_ im [Thema Abfragen).](queries.md)

Beachten Sie, dass GPU- und CPU-Zeitstempelindikatoren nicht unbedingt direkt mit der Taktgeschwindigkeit dieser Prozessoren verknüpft sind, sondern stattdessen über Zeitstempel-Ticks funktionieren.

## <a name="timestamp-queries"></a>Zeitstempelabfragen

Sie können Zeitstempel als Teil einer Befehlsliste (anstelle eines CPU-seitenden Aufrufs in einer Befehlswarteschlange) über Zeitstempelabfragen abrufen. (Weitere [Informationen zu](queries.md) Abfragen im Allgemeinen finden Sie unter Abfragen.) 

Alle Zeitstempelabfragen verwenden den [**Typ**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) D3D12_QUERY_TYPE_TIMESTAMP für die eigentliche Abfrage. Aufgrund von Hardwareeinschränkungen verwenden [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) [**und**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) D3D12_COMMAND_LIST_TYPE_COMPUTE jedoch [](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) eine andere D3D12_QUERY_HEAP_TYPE als die, die [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) verwendet.

Direkte Warteschlangen und Computewarteschlangen verwenden [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).

Kopierwarteschlangen verwenden [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).

Kopierwarteschlangenabfragen werden nur unterstützt, wenn das [**D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported-Mitglied**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) **TRUE ist.**

Zeitstempelabfragen sind nach der Auflösung über [**ID3D12GraphicsCommandList::ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)ein **UINT64,** der Ticks darstellt, wie es von [**ID3D12CommandQueue::GetClockCalibration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)zurückgegeben wird. Daher muss es durch die Warteschlangenhäufigkeit dividiert werden, um die Länge in Sekunden zu erhalten.

> [!IMPORTANT]
> Verwenden Sie zur Richtigkeit die Gleitkommaarithmetik, wenn Sie Zeitstempelintervalle im Sekunden- oder Millisekundenbereich berechnen. Verwenden Sie z. B. `queriedTicks / (double)Frequency` statt `queriedTicks / Frequency`.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Leistungsindikatoren und Abfragen](counters-and-queries.md)
</dt> <dt>

[**ID3D12Device::SetStablePowerState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
</dt> <dt>

[**ID3D12Object::SetName**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname)
</dt> <dt>

[**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)
</dt> <dt>

[Leistungsmessung](performance-measurement.md)
</dt> </dl>
