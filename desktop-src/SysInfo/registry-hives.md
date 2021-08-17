---
description: Eine Struktur ist eine logische Gruppe von Schlüsseln, Unterschlüsseln und Werten in der Registrierung, die über eine Reihe von unterstützenden Dateien verfügt, die Sicherungen ihrer Daten enthalten.
ms.assetid: fe517d88-7b03-4dc3-b3db-6a92665bca8e
title: Registrierungsstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11920a7b70a8aeb78b08aee2c25b89c4de5457b5cb96a480fc1f75fff6c6a35a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763627"
---
# <a name="registry-hives"></a>Registrierungsstrukturen

Eine *Struktur* ist eine logische Gruppe von Schlüsseln, Unterschlüsseln und Werten in der Registrierung, die über eine Reihe von unterstützenden Dateien verfügt, die beim Starten des Betriebssystems oder beim Anmelden eines Benutzers in den Arbeitsspeicher geladen werden.

Jedes Mal, wenn sich ein neuer Benutzer bei einem Computer anmeldet, wird eine neue Struktur für diesen Benutzer mit einer separaten Datei für das Benutzerprofil erstellt. Dies wird als *Benutzerprofilstruktur* bezeichnet. Die Struktur eines Benutzers enthält spezifische Registrierungsinformationen zu den Anwendungseinstellungen, Desktop, Umgebung, Netzwerkverbindungen und Druckern des Benutzers. Benutzerprofilstrukturen befinden sich unter dem **Schlüssel HKEY \_ USERS.**

Registrierungsdateien weisen die folgenden beiden Formate auf: standard und latest. Das Standardformat ist das einzige Format, das von Windows 2000 unterstützt wird. Sie wird aus Gründen der Abwärtskompatibilität auch von späteren Versionen von Windows unterstützt. Das neueste Format wird ab Windows XP unterstützt. In Versionen von Windows, die das neueste Format unterstützen, verwenden die folgenden Strukturen weiterhin das Standardformat: **HKEY \_ CURRENT \_ USER,** **HKEY \_ LOCAL MACHINE \_ \\ SAM,** **HKEY LOCAL MACHINE \_ \_ \\ Security** und **HKEY USERS \_ \\ . DEFAULT**; alle anderen Strukturen verwenden das neueste Format.

Die meisten unterstützenden Dateien für die Strukturen befinden sich im Verzeichnis %SystemRoot% \\ System32 \\ Config. Diese Dateien werden jedes Mal aktualisiert, wenn sich ein Benutzer anmeldet. Die Dateinamenerweiterungen der Dateien in diesen Verzeichnissen oder in einigen Fällen das Fehlen einer Erweiterung geben den Typ der enthaltenen Daten an. In der folgenden Tabelle sind diese Erweiterungen zusammen mit einer Beschreibung der Daten in der Datei aufgeführt.



| Durchwahl       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Keine<br/> | Eine vollständige Kopie der Hive-Daten.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| .alt<br/> | Eine Sicherungskopie der kritischen **HKEY \_ LOCAL MACHINE \_ \\ System-Struktur.** Nur der Systemschlüssel verfügt über eine ALT-Datei.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| .log<br/> | Ein Transaktionsprotokoll von Änderungen an den Schlüsseln und Werteinträgen in der Struktur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| .sav<br/> | Eine Sicherungskopie einer Struktur.<br/> **Windows Server 2003 und Windows XP/2000:** Kopien der Hive-Dateien am Ende der Textmodusphase im Setup. Das Setup umfasst zwei Phasen: Textmodus und Grafikmodus. Die Struktur wird nach der Textmodusphase des Setups in eine DATEI KOPIERT, um sie vor Fehlern zu schützen, die auftreten können, wenn die Grafikmodusphase des Setups fehlschlägt. Wenn das Setup während der Grafikmodusphase fehlschlägt, wird nur die Grafikmodusphase wiederholt, wenn der Computer neu gestartet wird. Die DATEI ".sav" wird verwendet, um die Hive-Daten wiederherzustellen.<br/> |



 

In der folgenden Tabelle sind die Standardstrukturen und ihre unterstützenden Dateien aufgeführt.



| Registrierungsstruktur                      | Unterstützende Dateien                           |
|------------------------------------|--------------------------------------------|
| **AKTUELLE \_ \_ HKEY-KONFIGURATION**          | System, System.alt, System.log, System.sav |
| **AKTUELLER \_ \_ HKEY-BENUTZER**            | Ntuser.dat, Ntuser.dat.log                 |
| **HKEY \_ LOCAL \_ MACHINE \\ SAM**      | Sam, Sam.log, Sam.sav                      |
| **HKEY \_ LOCAL \_ MACHINE \\ Security** | Security, Security.log, Security.sav       |
| **HKEY \_ LOCAL \_ MACHINE \\ Software** | Software, Software.log, Software.wild       |
| **HKEY \_ LOCAL \_ MACHINE \\ System**   | System, System.alt, System.log, System.sav |
| **HKEY \_ USERS \\ . Standard**          | Default, Default.log, Default.sav          |



 

 

 




