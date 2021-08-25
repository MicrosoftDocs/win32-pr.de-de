---
description: PGM-Absender werden mit bestimmten Standardeinstellungen bereitgestellt, die sich auf die Leistung der Datenübertragung auswirken, und wie lange Daten gepuffert werden, um Paketverluste und zugeordnete PGM-Client-Neuübertragungsanforderungen zu berücksichtigen.
ms.assetid: 56b15eac-ea0d-4d18-b5f6-2f1a7b1bb25f
title: Optionen für PGM-Absender
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04bce19e096f269207a22f8e3078643fefd9a7ced31482305c2caeb0ae8b7749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857907"
---
# <a name="pgm-sender-options"></a>Optionen für PGM-Absender

PGM-Absender werden mit bestimmten Standardeinstellungen bereitgestellt, die sich auf die Leistung der Datenübertragung auswirken, und wie lange Daten gepuffert werden, um Paketverluste und zugeordnete PGM-Client-Neuübertragungsanforderungen zu berücksichtigen. In den folgenden Absätzen werden diese Standardeinstellungen beschrieben.

## <a name="window-size-and-transmission-rate"></a>Fenstergröße und Übertragungsrate

Die Funktion zum Festlegen von Fenstergröße und Übertragungsrate ermöglicht Es Anwendungen, die Datenmenge der Transportpuffer für die neu übertragene Übertragung und die Rate, mit der der Bytestream übertragen wird, zu steuern.

Neuübertragungsdaten werden in einer Datei gespeichert. Daher wird die maximale Fenstergröße durch den Speicherplatz beschränkt, der vom Transport verwendet werden kann. Die Standardfenstergröße beträgt 10 MB. Obwohl es möglich ist, dass eine Sende- oder Nachrichtengröße das Fenster oder die Puffergröße überschreitet, bleibt der Datenstrom unterbrechungsfrei. wird so lange gesendet, bis alle Daten gesendet wurden.

> [!Note]  
> Der maximale Pufferspeicherplatz wird durch die maximale Anzahl von Paketen begrenzt, die zu einem beliebigen Zeitpunkt im Fenster gehalten werden können, was 2^31 – 1 entspricht.

 

Die Übertragungsrate ist der kombinierte Abfluss von ursprünglichen Datenpaketen (ODATA), neu übertragenen Datenpaketen (RDATA) und transportspezifischen Buchhaltungspaketen (SPMs), ausgedrückt pro Sekunde. Wenn das Ratenlimit standardmäßig auf 56 Kilobits pro Sekunde festgelegt ist. Die Standardfenstergröße beträgt 10 Megabyte mit einer Standardrate von 56 Kilobits pro Sekunde. Aufgrund der Beziehung zwischen den drei Membern der [**RM \_ SEND \_ WINDOW-Struktur**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window) beträgt die Standardfenstergröße daher 1428 Sekunden. Weitere Informationen finden Sie unter **RM \_ SEND \_ WINDOW.**

## <a name="window-advance-rate"></a>Fenstervorlaufrate

Die Vorabrate des Fensters wird durch die RM [ \_ SENDER WINDOW \_ \_ ADV \_ RATE-Socketoption](socket-options.md) festgelegt. Mit dieser Option können Anwendungen das Inkrement angeben, bei dem das Fenster des PGM-Absenders erweitert wird, ausgedrückt als Prozentwert ungleich 0 (null) der Fenstergröße. Der Standardwert ist 15 %, und die maximale Rate beträgt 50 %. Wenn für den PGM-Absender Reparaturdaten ausstehen, die in den Bereich des Inkrementfensters fallen, wird das Fenster teilweise erweitert, wenn jedes Reparaturpaket im Fenster gesendet wird.

## <a name="forward-error-correction-fec"></a>Vorwärtsfehlerkorrektur (FORWARD Error Correction, FEC)

Die Korrektur von Vorwärtsfehlern wird mithilfe der RM \_ USE \_ FEC-Socketoption festgelegt. Diese Socketoption ermöglicht dem PGM-Absender das Senden von Reparaturpaketen als Paritätspakete anstelle von regulären Datenpaketen. Dadurch wird die Anzahl von Reparaturpaketen minimiert, die gesendet werden, um verschiedene Sequenzen zu reparieren, die von mehreren Empfängern innerhalb derselben Datengruppe verloren gegangen sind. Das Aktivieren von FEC ist nur für den PGM-Absender festgelegt. PGM-Empfänger folgen automatisch der vom Absender festgelegten Richtlinie. Eine ausführliche Erläuterung zu FEC finden Sie im PGM RFC auf der [IETF-Website.](https://www.ietf.org/)

 

 



