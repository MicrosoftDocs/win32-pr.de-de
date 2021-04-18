---
description: PGM-Sender werden mit bestimmten Standardeinstellungen bereitgestellt, die sich auf die Leistung der Datenübertragung auswirken, und darüber, wie lange Daten gepuffert werden, um Paketverluste und zugeordnete PGM-Client Neuübertragungs Anforderungen zu berücksichtigen.
ms.assetid: 56b15eac-ea0d-4d18-b5f6-2f1a7b1bb25f
title: PGM-Sender Optionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c2e83ec7b098b9a82f74d4a3e0b6aa3ab03b63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345058"
---
# <a name="pgm-sender-options"></a>PGM-Sender Optionen

PGM-Sender werden mit bestimmten Standardeinstellungen bereitgestellt, die sich auf die Leistung der Datenübertragung auswirken, und darüber, wie lange Daten gepuffert werden, um Paketverluste und zugeordnete PGM-Client Neuübertragungs Anforderungen zu berücksichtigen. In den folgenden Abschnitten werden diese Standardeinstellungen beschrieben.

## <a name="window-size-and-transmission-rate"></a>Fenstergröße und Übertragungs Rate

Die Möglichkeit zum Festlegen der Fenstergröße und der Übertragungsrate ermöglicht es Anwendungen, die Menge der Daten zu steuern, die der Transport Puffer für die erneute Übertragung bietet, und die Rate, mit der der Bytestream übertragen wird.

Neuübertragungs Daten werden in einer Datei gespeichert, daher ist die maximale Fenstergröße durch den vom Transport nutzbaren Speicherplatz beschränkt. Die Standardfenster Größe beträgt 10 MB. Obwohl es möglich ist, dass eine Sende-oder Nachrichtengröße das Fenster oder die Puffergröße überschreitet, bleibt der Datenstrom ununterbrochen erhalten. der Sendevorgang wird durchgeführt, bis alle Daten gesendet wurden.

> [!Note]  
> Der maximale Pufferspeicher wird durch die maximale Anzahl von Paketen beschränkt, die zu einem beliebigen Zeitpunkt im Fenster aufbewahrt werden können. Dies entspricht 2 ^ 31 – 1.

 

Bei der Übertragungsrate handelt es sich um den kombinierten Durchsatz von ursprünglichen Datenpaketen (odata), erneut übertragene Datenpakete (rdata) und Transport spezifische Buchhaltungs Pakete (SPMs), die pro Sekunde ausgedrückt werden. Wenn das Raten Limit standardmäßig auf 56 Kbit pro Sekunde festgelegt ist. Die Standardfenster Größe beträgt 10 Megabyte. der Standardwert ist 56 Kbit pro Sekunde. Aufgrund der Beziehung zwischen den drei Membern der [**RM- \_ Sende \_ Fenster**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window) Struktur ist die Standardfenster Größe somit 1428 Sekunden. Weitere Informationen finden **Sie unter RM- \_ Sende \_ Fenster** .

## <a name="window-advance-rate"></a>Vorlauf Rate für Fenster

Die Vorlauf Rate des Fensters wird durch die Option " [RM- \_ Sender \_ Fenster \_ ADV \_ Rate](socket-options.md) Socket" festgelegt. Diese Option ermöglicht es Anwendungen, das Inkrement anzugeben, in dem das Fenster des PGM-Absenders erweitert wird, ausgedrückt als Prozentwert ungleich 0 (null) der Fenstergröße. Der Standardwert ist 15%, und die maximale Rate beträgt 50%. Wenn für den PGM-Absender ausstehende Reparatur Daten im Bereich des Inkrement-Fensters liegen, wird das Fenster teilweise erweitert, da jedes reparaturpaket im Fenster versendet wird.

## <a name="forward-error-correction-fec"></a>Forward Error Korrektur (FEC)

Die Vorwärts Fehlerkorrektur wird durch die Verwendung der Option "RM \_ use \_ FEC Socket" festgelegt. Diese Socketoption ermöglicht dem PGM-Sender das Senden von Reparatur Paketen als Paritäts Pakete anstelle von regulären Datenpaketen. Dadurch wird die Anzahl der reparierenden Reparatur Pakete minimiert, um verschiedene Sequenzen zu reparieren, die von mehreren Empfängern innerhalb derselben Datengruppe verloren gehen. Das Aktivieren von FEC wird nur für den PGM-Absender festgelegt. PGM-Empfänger befolgen automatisch die vom Absender festgelegte Richtlinie. Eine ausführliche Erläuterung zu FEC finden Sie in der PGM-RFC auf der [IETF](https://www.ietf.org/) -Website.

 

 



