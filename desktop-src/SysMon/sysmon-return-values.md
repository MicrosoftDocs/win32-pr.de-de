---
title: Sysmon-Rückgabewerte
description: Im folgenden finden Sie eine Liste der System Monitor-Rückgabewerte, die in smonmsg. h definiert sind.
ms.assetid: f1cc7668-4a6f-4b70-9591-62bd447fe8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ce5678c20a1ab8df825a5e3bc5f725d255e459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390732"
---
# <a name="sysmon-return-values"></a>Sysmon-Rückgabewerte

Im folgenden finden Sie eine Liste der System Monitor-Rückgabewerte, die in smonmsg. h definiert sind.



| Rückgabewert                                       | BESCHREIBUNG                                                                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Smon- \_ Status- \_ Dupl-Counter- \_ \_ Pfad (0xc0001388)     | Die zählungssammlung enthält bereits den angegebenen Zählers.                                                                                                                                                                               |
| Smon- \_ Status \_ kein \_ Sysmon- \_ Objekt (0xc0001389)      | Die Einstellungen enthalten keine kompletten System Monitor-HTML-Objekte.                                                                                                                                                                        |
| Smon- \_ Status \_ zu \_ wenige \_ Beispiele (0xc000138a)       | Die angegebene Protokolldatei enthält weniger als zwei Daten Stichproben.                                                                                                                                                                                 |
| Größenbeschränkung für smon- \_ Status \_ Protokoll \_ Datei \_ \_ (0xc000138b)  | Die angegebene Protokolldatei überschreitet die Größenbeschränkungen des System Monitor-Steuer Elements. Wenn zurzeit eine Protokolldatei ausgewählt ist, wählen Sie aktuelle Aktivität als Datenquelle aus, um die aktuelle Protokolldatei zu entladen, und wählen Sie dann die angegebene Protokolldatei erneut aus. |
| Datenquelle für smon- \_ Status \_ Protokoll \_ Datei \_ \_ (0xc000138c) | Um der Datenquelle eine neue Protokolldatei hinzuzufügen, muss der Daten Quellentyp in einen anderen Typ als sysmonlogfiles geändert werden.                                                                                                                          |
| Pfad für den smon- \_ Status der \_ \_ Protokoll \_ Datei \_ (0xc000138d)   | Die Protokolldatei Sammlung enthält bereits die angegebene Protokolldatei.                                                                                                                                                                             |



 

Eine Beschreibung der zusätzlichen Rückgabewerte, die vom System Monitor zurückgegeben werden, finden Sie unter [System Fehlercodes](/windows/desktop/Debug/system-error-codes) und [Fehlercodes für Leistungsdaten](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).

 

 