---
description: Der Leistungsindikatortyp gibt eine Formel an, die zum Abrufen berechneter Leistungsindikatoren erforderlich ist. Dies sind die gleichen Leistungsindikatortypen, die von Windows Leistungsüberwachung verwendet werden.
ms.assetid: d4a9feca-80a2-4ce5-b4d7-4e83ef951c08
ms.tgt_platform: multiple
title: WMI-Leistungsindikatortypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3338f67b457b3f28bc94ed38c79c17b30286aa73ec867842154d436a6696cee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118106964"
---
# <a name="wmi-performance-counter-types"></a>WMI-Leistungsindikatortypen

Der [Leistungsindikatortyp gibt](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) eine Formel an, die zum Abrufen berechneter Leistungsindikatoren erforderlich ist. Dies sind die gleichen Indikatortypen, die von Windows [Leistungsüberwachung verwendet werden.](/windows/desktop/PerfCtrs/performance-counters-portal) In WMI-Leistungsklassen stammen die Rohdaten für die Formel des Indikatortyps aus einer [**Win32 \_ PerfRawData-Klasse,**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) und das berechnete Ergebnis befindet sich in der gleichen benannten Eigenschaft einer entsprechenden [**Win32 \_ PerfFormattedData-Klasse.**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)

Indikatortypen werden als CounterType-Qualifizierer für Eigenschaften in [**Win32 \_ PerfRawData-Klassen**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) und als Qualifizierer **für Eigenschaften** in [**Win32 \_ PerfFormattedData-Klassen**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) angezeigt. 

Beispielsweise ist die **AvgDiskBytesPerRead-Eigenschaft** in der [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk-Klasse**](./retrieving-raw-and-formatted-performance-data.md) die Rohdatenquelle für die **AvgDiskBytesPerRead-Eigenschaft** in der [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk-Klasse,**](./retrieving-raw-and-formatted-performance-data.md)die die gleichen Daten wie im Systemmonitor enthält.

In der folgenden Liste sind Indikatortypbeschreibungen nach Funktionstyp organisiert:

-   [Basiszählertypen](base-counter-types.md)
-   [Grundlegende Algorithmuszählertypen](basic-algorithm-counter-types.md)
-   [Indikatortypen für Zähleralgorithmen](counter-algorithm-counter-types.md)
-   [Nichtcomputational Counter Types (Nichtcomputational Counter Types)](noncomputational-counter-types.md)
-   [Genauigkeits-Timeralgorithmus-Indikatortypen](precision-timer-algorithm-counter-types.md)
-   [Algorithmuszählertypen mit Warteschlangenlänge](queue-length-algorithm-counter-types.md)
-   [Statistische Indikatortypen](statistical-counter-types.md)
-   [Indikatortypen des Timeralgorithmus](timer-algorithm-counter-types.md)

 

 
