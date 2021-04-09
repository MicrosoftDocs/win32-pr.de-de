---
description: Während das System die UTC-basierte Zeit intern verwendet, zeigen ihre Anwendungen im Allgemeinen die Ortszeit an, die das Datum und die Uhrzeit für die Zeitzone ist.
ms.assetid: a6570ec5-ac77-427a-86d9-32cbecc62e37
title: Ortszeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c60eb9ca53245a12eba1bc0096b522eae97de75a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862995"
---
# <a name="local-time"></a>Ortszeit

Während das System die UTC-basierte Zeit intern verwendet, zeigen ihre Anwendungen im Allgemeinen die **Ortszeit** an, die das Datum und die Uhrzeit für die Zeitzone ist. Um korrekte Ergebnisse sicherzustellen, müssen Sie daher wissen, ob eine Funktion einen UTC-basierten Zeitpunkt oder eine Ortszeit erwartet und ob die Funktion eine UTC-basierte Zeit oder eine lokale Zeit zurückgibt.

Die aktuellen Zeitzoneneinstellungen steuern, wie das System zwischen UTC und Ortszeit konvertiert. Sie können die aktuellen Zeitzoneneinstellungen mithilfe der [**GetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformation) -Funktion abrufen. Die-Funktion kopiert das Ergebnis in eine [**Zeit \_ Zonen \_ Informations**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) Struktur und gibt einen Wert zurück, der angibt, ob Ortszeit Normalzeit oder Sommerzeit (DST) ist. Die Zeitzoneneinstellungen können mithilfe der [**settimezoneinformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-settimezoneinformation) -Funktion festgelegt werden. Um Grenzen für die Sommerzeit zu unterstützen, die sich von Jahr zu Jahr ändern, verwenden Sie die Funktionen [**gettimezoneinformationforyear**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear), [**getdynamictimezoneinformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation) und [**setdynamictimezoneinformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation) .

Verwenden Sie die [**getlocaltime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlocaltime) -Funktion, um die lokale Zeit abzurufen. **Getlocaltime** konvertiert die Systemzeit auf Grundlage der aktuellen Zeitzoneneinstellungen in eine lokale Zeit und kopiert das Ergebnis in eine [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) -Struktur. Sie können die Systemzeit mithilfe der [**setlocaltime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime) -Funktion festlegen. **Setlocaltime** geht davon aus, dass Sie vor dem Festlegen der Systemzeit eine lokale Uhrzeit angegeben und in UTC konvertiert haben.

Wenn Sie [**setlocaltime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime)aufrufen, verwendet das System die aktuellen Zeitzoneninformationen, einschließlich der Einstellung für die Sommerzeit, um die Konvertierung auszuführen. Beachten Sie, dass das System die Sommerzeit Einstellung der aktuellen Uhrzeit verwendet, nicht die neue Zeit, die Sie festlegen. Um das richtige Ergebnis zu gewährleisten, müssen Sie **setlocaltime** ein zweites Mal aufrufen, nachdem der erste Aufruf die Sommerzeit Einstellung aktualisiert hat.

Verwenden Sie die [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime) -Funktion, um eine UTC-basierte Zeit in eine lokale Zeit zu konvertieren. Verwenden Sie die Funktion " [**tzspecificlocaltimetosystemtime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime) ", um eine Ortszeit in eine UTC-basierte Zeit zu konvertieren.

 

 
