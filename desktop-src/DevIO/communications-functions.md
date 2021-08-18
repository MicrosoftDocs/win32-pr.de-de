---
description: Die folgenden Funktionen werden mit Kommunikationsressourcen verwendet.
ms.assetid: ba7d1a9e-6906-4923-a8eb-db58050ba699
title: Kommunikationsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1f49efccf2ff93ea18710ea4d6647e45f1135cf8a5fed542a65192f0abda6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768960"
---
# <a name="communications-functions"></a>Kommunikationsfunktionen

Die folgenden Funktionen werden mit Kommunikationsressourcen verwendet.



| Funktion                                                   | Beschreibung                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**BuildCommDCB**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcba)                       | Füllt eine angegebene [**DCB-Struktur**](/windows/desktop/api/Winbase/ns-winbase-dcb) mit Werten aus, die in einer Gerätesteuerungszeichenfolge angegeben sind.                           |
| [**BuildCommDCBAndTimeouts**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcbandtimeoutsa) | Übersetzt eine Gerätedefinitionszeichenfolge in entsprechende Gerätesteuerungsblockcodes und platziert sie in einem Gerätesteuerungsblock. |
| [**ClearCommBreak**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak)                   | Stellt die Zeichenübertragung für ein angegebenes Kommunikationsgerät wieder auf und platziert die Übertragungsleitung in einen nicht bruchfreien Zustand.    |
| [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror)                   | Ruft Informationen zu einem Kommunikationsfehler ab und meldet den aktuellen Status eines Kommunikationsgeräts.                  |
| [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga)               | Zeigt ein vom Treiber bereitgestelltes Konfigurationsdialogfeld an.                                                                           |
| [**EscapeCommFunction**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction)           | Leitet ein angegebenes Kommunikationsgerät an, eine erweiterte Funktion durchzuführen.                                                     |
| [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig)                     | Ruft die aktuelle Konfiguration eines Kommunikationsgeräts ab.                                                                |
| [**GetCommMask**](/windows/desktop/api/Winbase/nf-winbase-getcommmask)                         | Ruft den Wert der Ereignismaske für ein angegebenes Kommunikationsgerät ab.                                                   |
| [**GetCommModemStatus**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus)           | Ruft Die Werte des Modem-Kontrollregisters ab.                                                                                       |
| [**GetCommProperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties)             | Ruft Informationen zu den Kommunikationseigenschaften für ein angegebenes Kommunikationsgerät ab.                               |
| [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate)                       | Ruft die aktuellen Steuerelementeinstellungen für ein angegebenes Kommunikationsgerät ab.                                                  |
| [**GetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts)                 | Ruft die Time out-Parameter für alle Lese- und Schreibvorgänge auf einem angegebenen Kommunikationsgerät ab.                      |
| [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga)       | Ruft die Standardkonfiguration für das angegebene Kommunikationsgerät ab.                                                   |
| [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm)                             | Verwirft alle Zeichen aus der Ausgabe oder dem Eingabepuffer einer angegebenen Kommunikationsressource.                                |
| [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak)                       | Unterbricht die Zeichenübertragung für ein angegebenes Kommunikationsgerät und platziert die Übertragungsleitung in einen Unterbrechungszustand.       |
| [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig)                     | Legt die aktuelle Konfiguration eines Kommunikationsgeräts fest.                                                                     |
| [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask)                         | Gibt einen Satz von Ereignissen an, die für ein Kommunikationsgerät überwacht werden sollen.                                                         |
| [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate)                       | Konfiguriert ein Kommunikationsgerät gemäß den Spezifikationen in einem Gerätesteuerungsblock.                                  |
| [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts)                 | Legt die Time out-Parameter für alle Lese- und Schreibvorgänge auf einem angegebenen Kommunikationsgerät fest.                           |
| [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga)       | Legt die Standardkonfiguration für ein Kommunikationsgerät fest.                                                                    |
| [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm)                             | Initialisiert die Kommunikationsparameter für ein angegebenes Kommunikationsgerät.                                               |
| [**TransmitCommChar**](/windows/desktop/api/Winbase/nf-winbase-transmitcommchar)               | Überträgt ein angegebenes Zeichen vor allen ausstehenden Daten im Ausgabepuffer des angegebenen Kommunikationsgeräts.         |
| [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent)                     | Wartet, bis ein Ereignis für ein angegebenes Kommunikationsgerät eintritt.                                                             |



 

 

 



