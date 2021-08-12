---
description: Nicht berechnete Indikatortypen verfügen nicht über eine zugeordnete Formel. Der Rohwert ist direkt aussagekräftig.
ms.assetid: 2a6bb3a3-0aec-437a-881a-c4e14fcff6da
ms.tgt_platform: multiple
title: Nicht berechnete Indikatortypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a05da34058ceeb99ab60d8cc3d4f72cb3eec85194e48bb707a929eb2f68aa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555160"
---
# <a name="noncomputational-counter-types"></a>Nicht berechnete Indikatortypen

Nicht berechnete Indikatortypen verfügen nicht über eine zugeordnete Formel. Der Rohwert ist direkt aussagekräftig.

Die **FilesToBeIndexed-Eigenschaft** in der [**Win32 \_ PerfRawData \_ ContentIndex \_ IndexingService-Klasse**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) ist ein Beispiel für den **PERF \_ COUNTER \_ RAWCOUNT-Indikatortyp.** Sie enthält die Anzahl der Dateien, die nicht indiziert wurden.

Indikatortypen werden durch die in Winperf.h definierte Konstante festgelegt, die sich im Microsoft Windows Software Development Kit (SDK) befindet. In der folgenden Tabelle sind die nicht berechneten Indikatortypen aufgeführt, die bereitgestellt werden.



| Countertype                                                                                                 | Beschreibung                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [PERF \_ \_INDIKATORTEXT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Dezimalzahl 2816<br/>                | Dieser Indikatortyp zeigt eine Textzeichenfolge variabler Länge in Unicode an. Berechnete Werte werden nicht angezeigt.               |
| [PERF \_ COUNTER \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Dezimalzahl 65536<br/>           | Unformatierte Indikatorwerte, die keine Berechnungen erfordern, und stellt eine Stichprobe dar, die nur der letzte beobachtete Wert ist. |
| [PERF \_ COUNTER \_ LARGE \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792<br/>    | Identisch mit **PERF \_ COUNTER \_ RAWCOUNT,** aber eine 64-Bit-Darstellung für größere Werte.                                    |
| [PERF \_ INDIKATOR \_ RAWCOUNT \_ HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0<br/>                  | Zuletzt beobachteter Wert im Hexadezimalformat. Er zeigt keinen Durchschnittswert an.                                    |
| [PERF \_ COUNTER \_ LARGE \_ RAWCOUNT \_ HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 256<br/> | Identisch mit **PERF \_ COUNTER \_ RAWCOUNT \_ HEX**, aber eine 64-Bit-Darstellung in Hexadezimal für die Verwendung mit großen Werten.        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Leistungsindikatortypen](wmi-performance-counter-types.md)
</dt> </dl>

 

