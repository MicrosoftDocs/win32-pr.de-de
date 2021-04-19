---
description: Die folgenden Funktionen werden mit der Systemzeit verwendet.
ms.assetid: 3733f611-c6a1-4d48-b21e-ada3490c5de1
title: Zeitfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1187c029bac34411fdca28dd3b27322478de678
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356952"
---
# <a name="time-functions"></a>Zeitfunktionen

Die folgenden Funktionen werden mit der Systemzeit verwendet.



| Funktion                                                                   | BESCHREIBUNG                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**GetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtime)                                     | Ruft das aktuelle Systemdatum und die aktuelle Systemzeit im UTC-Format ab.                                              |
| [**GetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment)                 | Bestimmt, ob das System regelmäßige Zeit Anpassungen auf die Tageszeit anwendet.          |
| [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata)                                    | Formatiert eine Systemzeit als Zeit Zeichenfolge für ein angegebenes Gebiets Schema.                                         |
| [**Ntquerysystemtime**](/windows/desktop/api/Winternl/nf-winternl-ntquerysystemtime)                             | Gibt die Systemzeit zurück.                                                                               |
| [**Rtllocaltimesystemtime**](/windows/desktop/api/Winternl/nf-winternl-rtllocaltimetosystemtime)               | Konvertiert die angegebene lokale Zeit in die Systemzeit.                                                      |
| [**RtlTimeToSecondsSince1970**](/windows/desktop/api/Winternl/nf-winternl-rtltimetosecondssince1970)             | Konvertiert die angegebene Systemzeit in die Anzahl der Sekunden seit der ersten Sekunde des 1. Januar 1970. |
| [**SetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtime)                                     | Legt die aktuelle System Uhrzeit und das aktuelle Datum fest.                                                                 |
| [**Setsystemtimeadjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment)                 | Aktiviert oder deaktiviert periodische Zeit Anpassungen an der Tageszeit des Systems.                       |
| [**Fehler bei SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)                       | Konvertiert eine Systemzeit in eine Datei Zeit.                                                                 |
| [**Systemtimeumtzspecificlocaltime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime) | Konvertiert eine UTC-Zeit in die entsprechende Ortszeit der angegebenen Zeitzone.                               |
| [**Tzspecificlocaltimeumsystemtime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime) | Konvertiert eine lokale Uhrzeit in eine UTC-Zeit.                                                                   |



 

Die folgenden Funktionen werden mit der Ortszeit verwendet.



| Funktion                                                                                           | BESCHREIBUNG                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Enumdynamictimezoneinformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-enumdynamictimezoneinformation)                           | Listet Informationen zu dynamischen Sommerzeit Informationen auf, die in der Registrierung gespeichert sind.                                                             |
| [**Filetimetolocalfiletime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime)                                         | Konvertiert eine UTC-Dateizeit in eine lokale Datei Zeit.                                                                                                  |
| [**Getdynamictimezoneinformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation)                             | Ruft die aktuellen Zeit Zonen-und Einstellungen für die dynamische Sommerzeit ab.                                                                      |
| [**Getdynamictimezoneinformationeffectiveyears**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformationeffectiveyears) | Ruft einen Bereich ab, der in Jahren ausgedrückt wird, für den [**dynamische \_ Zeit \_ Zonen \_ Informationen**](/windows/win32/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information) gültige Einträge aufweisen. |
| [**Getlocaltime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlocaltime)                                                               | Ruft das aktuelle lokale Datum und die aktuelle Uhrzeit ab.                                                                                                      |
| [**GetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)                                           | Ruft die aktuellen Zeitzoneneinstellungen ab.                                                                                                       |
| [**Gettimezoneinformationforyear**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear)                             | Ruft die Zeitzoneneinstellungen für das angegebene Jahr und die angegebene Zeitzone ab.                                                                          |
| [**Rtllocaltimesystemtime**](/windows/desktop/api/Winternl/nf-winternl-rtllocaltimetosystemtime)                                       | Konvertiert die angegebene lokale Zeit in die Systemzeit.                                                                                               |
| [**Setdynamictimezoneinformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation)                             | Legt die aktuellen Zeit Zonen-und Einstellungen für die dynamische Sommerzeit fest.                                                                           |
| [**Setlocaltime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime)                                                               | Legt die aktuelle lokale Uhrzeit und das aktuelle Datum fest.                                                                                                           |
| [**Settimezoneinformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-settimezoneinformation)                                           | Legt die aktuellen Zeitzoneneinstellungen fest.                                                                                                            |
| [**Systemtimeumtzspecificlocaltime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)                         | Konvertiert eine UTC-Zeit in die entsprechende Ortszeit der angegebenen Zeitzone.                                                                        |
| [**Systemtimeumtzspecificlocaltimeex**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltimeex)                     | Konvertiert eine UTC-Zeit mit Einstellungen für die dynamische Sommerzeit in die entsprechende Ortszeit einer angegebenen Zeitzone.                             |
| [**Tzspecificlocaltimeumsystemtime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime)                         | Konvertiert eine lokale Uhrzeit in eine UTC-Zeit.                                                                                                            |
| [**Tzspecificlocaltimeumsystemtimeex**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtimeex)                     | Konvertiert eine Ortszeit mit Einstellungen für die dynamische Sommerzeit in die UTC-Zeit.                                                                   |



 

Die folgenden Funktionen werden mit der Dateizeit verwendet.



| Funktion                                                   | BESCHREIBUNG                                                                                                     |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**Comparefiletime**](/windows/desktop/api/FileAPI/nf-fileapi-comparefiletime)                 | Vergleicht zwei Datei Zeiten.                                                                                        |
| [**Filetimetolocalfiletime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime) | Konvertiert eine UTC-Dateizeit in eine lokale Datei Zeit.                                                                  |
| [**Filetimeto SYSTEMTIME**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)       | Konvertiert eine Datei Zeit in das Systemzeit Format.                                                                     |
| [**' GetFileTime '**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime)                         | Ruft den Zeitpunkt (Datum und Uhrzeit) ab, zu dem die angegebene Datei bzw. das angegebene Verzeichnis erstellt, auf den zuletzt zugegriffen wurde |
| [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) | Ruft das aktuelle Systemdatum und die aktuelle Systemzeit im UTC-Format ab.                                                       |
| [**Localfiletimeto FILETIME**](/windows/desktop/api/FileAPI/nf-fileapi-localfiletimetofiletime) | Konvertiert eine lokale Datei Zeit in eine Dateizeit, die auf UTC basiert.                                                         |
| [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime)                         | Legt das Datum und die Uhrzeit fest, zu der die angegebene Datei bzw. das angegebene Verzeichnis erstellt, auf den zuletzt zugegriffen wurde, oder zuletzt geändert       |
| [**Fehler bei SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)       | Konvertiert eine Systemzeit in eine Datei Zeit.                                                                          |



 

Die folgenden Funktionen werden mit MS-DOS-Datum und-Zeit verwendet.



| Funktion                                               | BESCHREIBUNG                                          |
|--------------------------------------------------------|------------------------------------------------------|
| [**Dosdatetimedefiletime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) | Konvertiert die Datums-und Uhrzeitwerte von MS-DOS in eine Dateizeit. |
| [**Filetimededosdatetime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) | Konvertiert eine Datei Zeit in MS-DOS-Datums-und Uhrzeitwerte. |



 

Die folgenden Funktionen werden mit der Windows-Zeit verwendet.



| Funktion                                 | BESCHREIBUNG                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) | Ruft Informationen zur Systemzeit Steuerung ab.                                                                  |
| [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount)     | Ruft die Anzahl der Millisekunden ab, die seit dem Start des Systems (bis zu 49,7 Tage) verstrichen sind. |
| [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) | Ruft die Anzahl der Millisekunden ab, die seit dem Start des Systems verstrichen sind.                  |



 

Die folgenden Funktionen werden mit Leistungsindikatoren mit hoher Auflösung verwendet.



| Funktion                                                              | BESCHREIBUNG                                                             |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)     | Ruft den aktuellen Wert des Leistungs Zählers mit hoher Auflösung ab. |
| [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) | Ruft die Häufigkeit des Leistungs Zählers mit hoher Auflösung ab.     |



 

Die folgenden Funktionen werden mit dem zusätzlichen Leistungs Bearbeiter verwendet.



| Funktion                                                                                           | BESCHREIBUNG                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Queryauxiliarycounterfrequency**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryauxiliarycounterfrequency)                           | Fragt die Häufigkeit des zusätzlichen Zählers ab.                                                                                                                                                                      |
| [**Convertauxiliarycountertoperformancecounter**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-convertauxiliarycountertoperformancecounter) | Konvertiert den angegebenen Wert des zusätzlichen Leistungs Zählers in den entsprechenden Leistungs Zählers. gibt optional den geschätzten Konvertierungs Fehler in Nanosekunden aufgrund von Latenzen und maximal möglichen Abweichungen an. |
| [**Convertperformancecounterumauxiliarycounter**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-convertperformancecountertoauxiliarycounter) | Konvertiert den angegebenen Leistungs Zählers Wert in den entsprechenden Wert des Wert Zählers. gibt optional den geschätzten Konvertierungs Fehler in Nanosekunden aufgrund von Latenzen und maximal möglichen Abweichungen an. |



 

Die folgende Funktion wird mit Interruptzeit verwendet.



| Funktion                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Queryinterrupttime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)                               | Ruft die aktuelle Anzahl der Interrupt-Zeiten ab.                                                                                                                                                                                                                |
| [**Queryinterrupttimepräzisen**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)                 | Ruft die aktuelle Interruptzeit-Anzahl in einer präziseren Form als [**queryinterrupttime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) ab.                                                                                                                             |
| [**Queryunbiasedinterrupttime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)               | Ruft die aktuelle Anzahl der nicht unausgewogenen Interruptzeit ab. Die Anzahl der unausgewogenen Interruptzeit umfasst nicht die Zeit, die das System im Standbymodus oder Ruhezustand verbringt.                                                                                                    |
| [**Queryunbiasedinterrupttimepräzisen**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) | Ruft die aktuelle Anzahl der nicht gleichwertigen Interruptzeit in einer präziseren Form als [**queryunbiasedinterrupttime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) ab. Die Anzahl der unausgewogenen Interruptzeit umfasst nicht die Zeit, die das System im Standbymodus oder Ruhezustand verbringt. |



 

 

 
