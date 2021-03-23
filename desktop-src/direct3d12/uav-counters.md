---
title: UAV-Leistungsindikatoren
description: Sie können die UAV-Leistungsindikatoren (unsortierter Zugriffs Ansicht) verwenden, um einen atomaren 32-Bit-Zähler mit einer nicht geordneten Zugriffs Ansicht (UAV) zuzuordnen.
ms.assetid: 0B77E238-E8CF-466B-9188-3DE96AF97F42
ms.localizationpriority: high
ms.topic: article
ms.date: 02/10/2020
ms.openlocfilehash: 94bc1492e3b984d96c76788430d2e63c0672ca76
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104548673"
---
# <a name="uav-counters"></a>UAV-Leistungsindikatoren
Sie können die UAV-Leistungsindikatoren (unsortierter Zugriffs Ansicht) verwenden, um einen atomaren 32-Bit-Zähler mit einer nicht geordneten Zugriffs Ansicht (UAV) zuzuordnen.

## <a name="differences-in-uav-counters-from-direct3d-11-to-direct3d-12"></a>Unterschiede bei UAV-Indikatoren von Direct3D 11 bis Direct3D 12
Für den Zugriff auf die UAV-Indikatoren verwenden Direct3D 12 apps und Direct3D 11-apps die gleichen High-Level-Shader-Funktionen (HLSL).

-   **Incrementcounter**
-   **Dekrementcounter**
-   **Append**
-   **Nutzen**

### <a name="direct3d-12"></a>Direct3D 12
In Direct3D 12 werden die 32-Bit-Werte von der Anwendung zugeordnet, sodass die 32-Bit-Werte wie jede andere Direct3D 12-Ressource entweder von der CPU oder der GPU gelesen und geschrieben werden können.

### <a name="direct3d-11"></a>Direct3D 11
Außerhalb der Shader müssen Sie mit Direct3D 11 API-Methoden aufrufen, um auf die Indikatoren zuzugreifen (z. b. [Verknüpfung id3d11devicecontext aus:: copystructurecount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).

## <a name="using-uav-counters"></a>Verwenden von UAV-Leistungsindikatoren
Ihre APP ist dafür verantwortlich, 32 Bits Speicher für UAV-Indikatoren zuzuordnen. Dieser Speicher kann in einer anderen Ressource zugewiesen werden als der, der Daten enthält, auf die über die UAV zugegriffen werden kann.

Weitere Informationen finden Sie unter " [**kreateunorderedaccessview**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)", [**D3D12 \_ buffer \_ UAV \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) und [**D3D12 \_ buffer \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).

Wenn " *pcounterresource* " im Aufrufen von " [**anateunorderedaccessview**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)" angegeben wird, ist der UAV ein Indikator zugeordnet. In diesem Fall:

-   *Structurebytestride* muss größer als 0 (null) sein.
-   Das Format muss im DXGI- \_ Format unbekannt sein. \_
-   Das RAW-Flag darf nicht festgelegt werden.
-   Beide Ressourcen müssen Puffer sein.
-   *Counteroffset-Bytes* muss ein Vielfaches von 4 Bytes sein.
-   *Counteroffmentinbytes* muss innerhalb des Bereichs der Indikator Ressource liegen.
-   *pdebug* darf nicht NULL sein.
-   die *präquelle* darf nicht NULL sein.

Beachten Sie auch die folgenden Anwendungsfälle:

-   Wenn " *pcounterresource* " nicht angegeben wird, muss " *counteroffset tinbytes* " den Wert "0" aufweisen.
-   Wenn das RAW-Flag festgelegt ist, muss das Format das DXGI \_ -Format R32 aufweisen, \_ \_ und die UAV-Ressource muss ein Puffer sein.
-   Wenn *pcounterresource* nicht festgelegt ist, muss *counteroffsetinbytes* den Wert 0 aufweisen.
-   Wenn das RAW-Flag nicht festgelegt ist und *structurebytestride* = 0 ist, muss das Format ein gültiges UAV-Format aufweisen.

Direct3D 12 entfernt den Unterschied zwischen angefügenden und gegen-UAVs (obwohl der Unterschied in HLSL-Bytecode noch vorhanden ist).

Die Core-Laufzeit überprüft diese Einschränkungen in der Datei " [**" von "**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)".

Beim Zeichnen/verteilen muss die Counter-Ressource den Status [**D3D12 \_ Resource \_ State \_ unsortierter \_ Zugriff**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)aufweisen. Außerdem ist es innerhalb eines einzelnen Draw/Dispatch-Aufrufes nicht möglich, dass eine Anwendung über zwei separate UAV-Indikatoren auf denselben Speicherort mit 32-Bit-Speicher zugreifen kann. Die debugschicht gibt Fehler aus, wenn eine dieser Funktionen erkannt wird.

Es gibt keine "Set-Methode" oder "copystructurecount"-Methoden, da Apps einfach Daten direkt in den und aus dem Zählerwert kopieren können.

Dynamische Indizierung von UAVs mit Leistungsindikatoren wird unterstützt.

Wenn ein Shader versucht, auf den-Wert einer UAV zuzugreifen, der nicht über einen zugeordneten-Wert verfügt, wird von der debugschicht eine Warnung ausgegeben, und es tritt ein GPU-Seiten Fehler auf, der bewirkt, dass das Gerät der apps entfernt wird.

UAV-Indikatoren werden in allen Heap Typen unterstützt (Standard, Upload, Read Back).

## <a name="related-topics"></a>Verwandte Themen

* [Zähler und Abfragen](counters-and-queries.md)