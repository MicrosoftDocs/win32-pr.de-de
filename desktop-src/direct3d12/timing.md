---
title: Zeitliche Steuerung (Direct3D 12-Grafiken)
description: In diesem Abschnitt wird das Abfragen von Zeitstempeln und das Kalibrieren der GPU-und CPU-Zeitstempelzähler behandelt.
ms.assetid: CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 979c51b3c88be184cb23afaa2008e90eaec1f9c5
ms.sourcegitcommit: a1f58e231315e95bbf9178994f8c52303fc0d4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2020
ms.locfileid: "104548753"
---
# <a name="timing-direct3d-12-graphics"></a>Zeitliche Steuerung (Direct3D 12-Grafiken)

In diesem Abschnitt wird das Abfragen von Zeitstempeln und das Kalibrieren der GPU-und CPU-Zeitstempelzähler behandelt.

## <a name="timestamp-frequency"></a>Zeitstempel Häufigkeit

Die Anwendung kann die GPU-Zeitstempel Häufigkeit pro Befehls Warteschlange Abfragen (Weitere Informationen finden Sie in der [**ID3D12CommandQueue:: gettimestampfrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) -Methode).

Die zurückgegebene Häufigkeit wird in Hz (Ticks/Sek.) gemessen. Wenn die angegebene Befehls Warteschlange keine Zeitstempel unterstützt (siehe die Tabelle im Abschnitt " [Abfragen](queries.md) "), schlägt diese API fehl (und gibt **E_FAIL** zurück). [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) und [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) unterstützen stets Zeitstempel. [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) optional Zeitstempel unterstützt, wenn der [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: copyqueuetimestampqueriessupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) -Member " **true**" ist.

## <a name="timestamp-calibration"></a>Zeitstempel-Kalibrierung

D3D12 ermöglicht Anwendungen das korrelieren von Ergebnissen, die von Zeitstempel-Abfragen abgerufen wurden, mit Ergebnissen, die durch `QueryPerformanceCounter` den Aufruf Dies wird durch den Aufrufen von [**ID3D12CommandQueue:: getclockkalibrierung**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)ermöglicht.

[**Getclockkalibrierung**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) erfasst den GPU-Zeitstempel-Counter für eine bestimmte Befehls Warteschlange und erfasst den CPU-Wert über `QueryPerformanceCounter` nahezu zur gleichen Zeit. Auch diese API schlägt fehl (bei Rückgabe von E \_ Fail), wenn die angegebene Befehls Warteschlange keine Zeitstempel unterstützt (siehe Tabelle im Thema [Abfragen](queries.md) ).

Beachten Sie, dass GPU-und CPU-Zeitstempel-Indikatoren nicht notwendigerweise direkt mit der Taktfrequenz dieser Prozessoren in Zusammenhang stehen, sondern von Zeitstempel Ticks arbeiten.

## <a name="timestamp-queries"></a>Timestamp-Abfragen

Sie können Zeitstempel als Teil einer Befehlsliste (anstelle eines CPU-seitigen Aufrufes Aufrufes in einer Befehls Warteschlange) über Zeitstempel-Abfragen abrufen. (Weitere Informationen zu Abfragen im Allgemeinen finden Sie unter [Abfragen](queries.md) .) 

Alle Zeitstempel-Abfragen verwenden den Type- [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) für die eigentliche Abfrage. Aufgrund von Hardwarebeschränkungen verwenden [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) und [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) jedoch einen anderen [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) als den, der von [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) verwendet wird.

Direct-und Compute-Warteschlangen verwenden [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).

Kopier Warteschlangen verwenden [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).

Abfragen zum Kopieren von Warteschlangen werden nur unterstützt, wenn der [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: copyqueuetimestampqueriessupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) -Member " **true**" ist.

Timestamp-Abfragen, die über [**ID3D12GraphicsCommandList:: resolvequerydata**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)aufgelöst werden, sind ein **UINT64** , das Ticks darstellt, wie von [**ID3D12CommandQueue:: getclockkalibrierung**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)zurückgegeben, und daher muss Sie durch die Warteschlangen Häufigkeit geteilt werden, um die Länge in Sekunden zu erhalten.

> [!IMPORTANT]
> Verwenden Sie aus Gründen der Genauigkeit beim Berechnen der Sekunden-oder millisekundenintervalle von Zeitstempeln Gleit Komma Arithmetik. Verwenden Sie z. B. `queriedTicks / (double)Frequency` statt `queriedTicks / Frequency`.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Zähler und Abfragen](counters-and-queries.md)
</dt> <dt>

[**ID3D12Device:: setstablepowerstate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
</dt> <dt>

[**ID3D12Object:: SetName**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname)
</dt> <dt>

[**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)
</dt> <dt>

[Leistungsmessung](performance-measurement.md)
</dt> </dl>
