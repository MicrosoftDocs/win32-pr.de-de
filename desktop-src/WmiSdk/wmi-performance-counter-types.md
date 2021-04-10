---
description: Der Leistungs indikatorentyp legt eine Formel fest, die zum Abrufen berechneter Leistungsindikatoren erforderlich ist. Dabei handelt es sich um die gleichen bei der Windows-Leistungsüberwachung verwendeten Leistungstypen.
ms.assetid: d4a9feca-80a2-4ce5-b4d7-4e83ef951c08
ms.tgt_platform: multiple
title: WMI-Leistungsdaten Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ac0d2c8afb1499fec44c983364b5e3278b864
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131148"
---
# <a name="wmi-performance-counter-types"></a>WMI-Leistungsdaten Typen

Der Leistungs [indikatorentyp](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) legt eine Formel fest, die zum Abrufen berechneter Leistungsindikatoren erforderlich ist. Dabei handelt es sich um die gleichen bei der Windows- [Leistungsüberwachung verwendeten Leistungs](/windows/desktop/PerfCtrs/performance-counters-portal)Typen. In WMI-Leistungsklassen stammen die Rohdaten für die Counter Type-Formel aus einer [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klasse, und das berechnete Ergebnis ist in der gleichnamigen Eigenschaft einer entsprechenden [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) -Klasse enthalten.

Indikator Typen werden als **CounterType** -Qualifizierer für Eigenschaften in [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klassen und als **cookingtype** -Qualifizierer für Eigenschaften in [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) -Klassen angezeigt.

Beispielsweise ist die **avgdiskbytesperread** -Eigenschaft in der [**Win32 \_ perfrawdata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) -Klasse die Rohdaten Quelle für die **avgdiskbytesperread** -Eigenschaft in der Klasse [**Win32 \_ perfformatteddata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), die die gleichen Daten wie im System Monitor enthält.

In der folgenden Liste werden die zähtertyp Beschreibungen nach Funktionstyp organisiert:

-   [Basis-Counter-Typen](base-counter-types.md)
-   [Grundlegende algorithmuscounter-Typen](basic-algorithm-counter-types.md)
-   [Gegen Typen von Algorithmus-Algorithmus](counter-algorithm-counter-types.md)
-   [Nicht-Berechnungs-Counter-Typen](noncomputational-counter-types.md)
-   [Zähler Typen für Genauigkeits Geber Algorithmen](precision-timer-algorithm-counter-types.md)
-   [Algorithmustypen der Warteschlangen Länge](queue-length-algorithm-counter-types.md)
-   [Statistische Counter-Typen](statistical-counter-types.md)
-   [Zähler Typen für Timer-Algorithmus](timer-algorithm-counter-types.md)

 

 
