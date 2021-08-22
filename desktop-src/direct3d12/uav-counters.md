---
title: UAV-Leistungsindikatoren
description: Sie können UAV-Indikatoren (Unordered Access View) verwenden, um einen 32-Bit-Atomarzähler einer ungeordneten Zugriffsansicht (UAV) zuzuordnen.
ms.assetid: 0B77E238-E8CF-466B-9188-3DE96AF97F42
ms.localizationpriority: high
ms.topic: article
ms.date: 02/10/2020
ms.openlocfilehash: c33321b02f22378f4d039137b8ff65559a25a32ed219c2bf336528913777791d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460790"
---
# <a name="uav-counters"></a>UAV-Leistungsindikatoren
Sie können UAV-Indikatoren (Unordered Access View) verwenden, um einen 32-Bit-Atomarzähler einer ungeordneten Zugriffsansicht (UAV) zuzuordnen.

## <a name="differences-in-uav-counters-from-direct3d-11-to-direct3d-12"></a>Unterschiede bei UAV-Indikatoren von Direct3D 11 zu Direct3D 12
Direct3D 12-Apps und Direct3D 11-Apps verwenden beide die gleichen HLSL-Shaderfunktionen (High-Level Shader Language), um auf die UAV-Indikatoren zuzugreifen.

-   **IncrementCounter**
-   **DecrementCounter**
-   **Append** (Anfügen)
-   **Nutzen**

### <a name="direct3d-12"></a>Direct3D 12
In Direct3D 12 werden die 32-Bit-Werte von der Anwendung zugeordnet, sodass die 32-Bit-Werte von der CPU oder der GPU gelesen und geschrieben werden können, genau wie jede andere Direct3D 12-Ressource.

### <a name="direct3d-11"></a>Direct3D 11
Außerhalb der Shader müssen Sie mit Direct3D 11 API-Methoden aufrufen, um auf die Leistungsindikatoren zuzugreifen (z.B. [ID3D11DeviceContext::CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).

## <a name="using-uav-counters"></a>Verwenden von UAV-Indikatoren
Ihre App ist für die Zuordnung von 32-Bit-Speicher für UAV-Indikatoren verantwortlich. Dieser Speicher kann in einer anderen Ressource als der Ressource zugeordnet werden, die Daten enthält, auf die über die UAV zugegriffen werden kann.

Weitere Informationen finden Sie unter [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12 \_ BUFFER \_ UAV \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) und [**D3D12 \_ BUFFER \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).

Wenn *pCounterResource* im Aufruf von [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)angegeben wird, ist dem UAV ein Zähler zugeordnet. In diesem Fall:

-   *StructureByteStride* muss größer als 0 (null) sein.
-   Das Format muss DXGI FORMAT UNKNOWN sein. \_ \_
-   Das RAW-Flag darf nicht festgelegt werden.
-   Beide Ressourcen müssen Puffer sein.
-   *CounterOffsetInBytes* muss ein Vielfaches von 4 Bytes sein.
-   *CounterOffsetInBytes* muss innerhalb des Bereichs der Indikatorressource liegen.
-   *pDesc* darf nicht NULL sein
-   *pResource* darf nicht NULL sein

Beachten Sie außerdem die folgenden Anwendungsfälle:

-   Wenn *pCounterResource* nicht angegeben ist, muss *CounterOffsetInBytes* 0 sein.
-   Wenn das RAW-Flag festgelegt ist, muss das Format DXGI \_ FORMAT \_ R32 \_ TYPELESS und die UAV-Ressource ein Puffer sein.
-   Wenn *pCounterResource* nicht festgelegt ist, muss *CounterOffsetInBytes* 0 sein.
-   Wenn das RAW-Flag nicht festgelegt ist und *StructureByteStride* = 0 ist, muss das Format ein gültiges UAV-Format sein.

Direct3D 12 entfernt die Unterscheidung zwischen Anfüge- und Indikator-UAVs (obwohl die Unterscheidung in HLSL-Bytecode noch vorhanden ist).

Die Kernlaufzeit überprüft diese Einschränkungen innerhalb von [**CreateUnorderedAccessView.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)

Während draw/dispatch muss sich die Indikatorressource im Zustand [**D3D12 \_ RESOURCE \_ STATE \_ UNORDERED \_ ACCESS befinden.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) Außerdem ist es innerhalb eines einzelnen Draw/Dispatch-Aufrufs ungültig, dass eine Anwendung über zwei separate UAV-Indikatoren auf die gleiche 32-Bit-Speicherposition zugreift. Die Debugebene gibt Fehler aus, wenn eine dieser Fehler erkannt wird.

Es gibt keine Methoden "SetUnorderedAccessViewCounterValue" oder "CopyStructureCount", da Apps Daten einfach direkt in den Zählerwert kopieren können.

Die dynamische Indizierung von UAVs mit Leistungsindikatoren wird unterstützt.

Wenn ein Shader versucht, auf den Leistungsindikator eines UAV zuzugreifen, dem kein Zähler zugeordnet ist, gibt die Debugebene eine Warnung aus, und ein GPU-Seitenfehler führt dazu, dass das Gerät der Apps entfernt wird.

UAV-Leistungsindikatoren werden in allen Heaptypen unterstützt (Standard, Upload, Readback).

## <a name="related-topics"></a>Zugehörige Themen

* [Leistungsindikatoren und Abfragen](counters-and-queries.md)