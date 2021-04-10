---
description: Die folgenden Funktionen werden mit Kommunikationsressourcen verwendet.
ms.assetid: ba7d1a9e-6906-4923-a8eb-db58050ba699
title: Kommunikationsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64853bf2b0c42d4e7ca607fbbe624995cfe1a249
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214154"
---
# <a name="communications-functions"></a>Kommunikationsfunktionen

Die folgenden Funktionen werden mit Kommunikationsressourcen verwendet.



| Funktion                                                   | BESCHREIBUNG                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**BuildCommDCB**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcba)                       | Füllt eine angegebene [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) -Struktur mit Werten, die in einer Zeichenfolge für den Geräte Steuerelement angegeben sind.                           |
| [**Buildcommdcbandtimeouts**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcbandtimeoutsa) | Übersetzt eine Geräte Definitions Zeichenfolge in entsprechende Geräte Steuerungs Block Codes und platziert Sie in einem Geräte Kontroll Block. |
| [**Clearcommbreak**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak)                   | Stellt die Zeichen Übertragung für ein angegebenes Kommunikationsgerät wieder her und versetzt die Übertragungs Zeile in den Zustand "nicht Umbruch".    |
| [**Clearcommerror**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror)                   | Ruft Informationen zu einem Kommunikationsfehler ab und meldet den aktuellen Status eines kommunikationsgeräts.                  |
| [**Commconfigdialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga)               | Zeigt ein vom Treiber bereitgestelltes Konfigurations Dialogfeld an.                                                                           |
| [**Escapecommfunction**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction)           | Weist ein angegebenes Kommunikationsgerät an, eine erweiterte Funktion auszuführen.                                                     |
| [**Getcommconfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig)                     | Ruft die aktuelle Konfiguration eines kommunikationsgeräts ab.                                                                |
| [**Getcommmask**](/windows/desktop/api/Winbase/nf-winbase-getcommmask)                         | Ruft den Wert der Ereignis Maske für ein angegebenes Kommunikationsgerät ab.                                                   |
| [**Getcommmudemstatus**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus)           | Ruft Modem Steuerelement-Registerwerte ab.                                                                                       |
| [**Getcommproperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties)             | Ruft Informationen zu den Kommunikations Eigenschaften für ein angegebenes Kommunikationsgerät ab.                               |
| [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate)                       | Ruft die aktuellen Steuerelement Einstellungen für ein angegebenes Kommunikationsgerät ab.                                                  |
| [**Getcommtimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts)                 | Ruft die Timeout Parameter für alle Lese-und Schreibvorgänge auf einem angegebenen Kommunikationsgerät ab.                      |
| [**Getdefaultcommconfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga)       | Ruft die Standardkonfiguration für das angegebene Kommunikationsgerät ab.                                                   |
| [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm)                             | Verwirft alle Zeichen aus der Ausgabe oder dem Eingabepuffer einer angegebenen Kommunikations Ressource.                                |
| [**Setcommbreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak)                       | Hält die Zeichen Übertragung für ein angegebenes Kommunikationsgerät an und versetzt die Übertragungs Zeile in einen unterbrecherzustand.       |
| [**Setcommconfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig)                     | Legt die aktuelle Konfiguration eines kommunikationsgeräts fest.                                                                     |
| [**Setcommmask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask)                         | Gibt eine Gruppe von Ereignissen an, die für ein Kommunikationsgerät überwacht werden sollen.                                                         |
| [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate)                       | Konfiguriert ein Kommunikationsgerät entsprechend den Spezifikationen in einem Geräte Steuerungs Block.                                  |
| [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts)                 | Legt die Timeout Parameter für alle Lese-und Schreibvorgänge auf einem angegebenen Kommunikationsgerät fest.                           |
| [**Setdefaultcommconfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga)       | Legt die Standardkonfiguration für ein Kommunikationsgerät fest.                                                                    |
| [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm)                             | Initialisiert die Kommunikationsparameter für ein angegebenes Kommunikationsgerät.                                               |
| [**Transmitcommchar**](/windows/desktop/api/Winbase/nf-winbase-transmitcommchar)               | Überträgt ein angegebenes Zeichen vor allen ausstehenden Daten im Ausgabepuffer des angegebenen kommunikationsgeräts.         |
| [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent)                     | Wartet, bis ein Ereignis für ein bestimmtes Kommunikationsgerät auftritt.                                                             |



 

 

 



