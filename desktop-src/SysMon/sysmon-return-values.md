---
title: SYSMON-Rückgabewerte
description: Im Folgenden finden Sie eine Liste der Rückgabewerte des Systemmonitors, die in Smonmsg.h definiert sind.
ms.assetid: f1cc7668-4a6f-4b70-9591-62bd447fe8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ce526a64132cef51338a83b387aa8e9bfd58ce0ef0b99a1fb7db0dce4c15ef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956446"
---
# <a name="sysmon-return-values"></a>SYSMON-Rückgabewerte

Im Folgenden finden Sie eine Liste der Rückgabewerte des Systemmonitors, die in Smonmsg.h definiert sind.



| Rückgabewert                                       | BESCHREIBUNG                                                                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SMON \_ STATUS \_ DUPL COUNTER PATH \_ \_ (0XC0001388)     | Die Indikatorsammlung enthält bereits den angegebenen Zähler.                                                                                                                                                                               |
| SMON \_ STATUS \_ NO \_ SYSMON OBJECT \_ (0xC0001389)      | Die Einstellungen enthalten keine vollständigen HTML-Objekte des Systemmonitors.                                                                                                                                                                        |
| SMON \_ STATUS TOO FEW SAMPLES \_ \_ \_ (0XC000138A)       | Die angegebene Protokolldatei enthält weniger als zwei Datenbeispiele.                                                                                                                                                                                 |
| SMON \_ STATUS LOG FILE SIZE LIMIT \_ \_ \_ \_ (0XC000138B)  | Die angegebene Protokolldatei überschreitet die Größenbeschränkungen des Systemmonitor-Steuerelements. Wenn derzeit eine Protokolldatei ausgewählt ist, wählen Sie die aktuelle Aktivität als Datenquelle aus, um die aktuelle Protokolldatei zu entladen, und wählen Sie dann die angegebene Protokolldatei erneut aus. |
| SMON \_ STATUS LOG FILE DATA SOURCE \_ \_ \_ \_ (0XC000138C) | Um der Datenquelle eine neue Protokolldatei hinzuzufügen, muss der Datenquellentyp in einen anderen Typ als sysmonLogFiles geändert werden.                                                                                                                          |
| SMON \_ STATUS \_ DUPL LOG FILE PATH \_ \_ \_ (0XC000138D)   | Die Protokolldateisammlung enthält bereits die angegebene Protokolldatei.                                                                                                                                                                             |



 

Eine Beschreibung zusätzlicher Rückgabewerte, die vom Systemmonitor zurückgegeben werden, finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes) und Fehlercodes des [Leistungsdaten-Hilfssystems.](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values)

 

 