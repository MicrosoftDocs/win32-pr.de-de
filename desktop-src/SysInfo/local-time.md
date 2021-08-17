---
description: Während das System intern DIE UTC-basierte Zeit verwendet, zeigt Ihre Anwendungen in der Regel die Ortszeit an, d. h. datums- und tageszeit für Ihre Zeitzone.
ms.assetid: a6570ec5-ac77-427a-86d9-32cbecc62e37
title: Ortszeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95835b76f09ae328c3e1509da68e0fbd989286b2e2669efc9f2280dbce72e35a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763999"
---
# <a name="local-time"></a>Ortszeit

Während das System intern UTC-basierte Zeit verwendet, zeigt Ihre Anwendungen in der Regel die **Ortszeit** an, d. h. datums- und tageszeit für Ihre Zeitzone. Um korrekte Ergebnisse sicherzustellen, müssen Sie daher beachten, ob eine Funktion eine UTC-basierte Zeit oder eine Ortszeit erwartet und ob die Funktion eine UTC-basierte Zeit oder eine Ortszeit zurückgibt.

Die aktuellen Zeitzoneneinstellungen steuern, wie das System zwischen UTC und Ortszeit konvertiert. Sie können die aktuellen Zeitzoneneinstellungen mithilfe der [**GetTimeZoneInformation-Funktion**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformation) abrufen. Die Funktion kopiert das Ergebnis in eine [**TIME \_ ZONE \_ INFORMATION-Struktur**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) und gibt einen Wert zurück, der angibt, ob die Ortszeit derzeit in der Standardzeit oder der Sommerzeit (DST) liegt. Sie können die Zeitzoneneinstellungen mithilfe der [**SetTimeZoneInformation-Funktion**](/windows/win32/api/timezoneapi/nf-timezoneapi-settimezoneinformation) festlegen. Verwenden Sie die Funktionen [**GetTimeZoneInformationForYear,**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear) [**GetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation) und [**SetDynamicTimeZoneInformation,**](/windows/win32/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation) um Die Sommerzeitgrenzen zu unterstützen, die sich von Jahr zu Jahr ändern.

Verwenden Sie die [**GetLocalTime-Funktion,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlocaltime) um die lokale Zeit abzurufen. **GetLocalTime** konvertiert die Systemzeit basierend auf den aktuellen Zeitzoneneinstellungen in eine lokale Zeit und kopiert das Ergebnis in eine [**SYSTEMTIME-Struktur.**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) Sie können die Systemzeit mithilfe der [**SetLocalTime-Funktion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime) festlegen. **SetLocalTime** geht davon aus, dass Sie eine ortslokale Zeit angegeben haben und vor dem Festlegen der Systemzeit in UTC konvertiert werden.

Wenn Sie [**SetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime)aufrufen, verwendet das System die aktuellen Zeitzoneninformationen, einschließlich der Sommerzeiteinstellung, um die Konvertierung durchzuführen. Beachten Sie, dass das System die Sommerzeiteinstellung der aktuellen Zeit verwendet, nicht die neue Zeit, die Sie festlegen. Um das richtige Ergebnis sicherzustellen, rufen Sie daher **SetLocalTime** ein zweites Mal auf, nachdem der erste Aufruf die Einstellung für die Sommerzeit aktualisiert hat.

Verwenden Sie die [**SystemTimeToTzSpecificLocalTime-Funktion,**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime) um eine UTC-basierte Zeit in eine Ortszeit zu konvertieren. Verwenden Sie die [**TzSpecificLocalTimeToSystemTime-Funktion,**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime) um eine Ortszeit in eine UTC-basierte Zeit zu konvertieren.

 

 
