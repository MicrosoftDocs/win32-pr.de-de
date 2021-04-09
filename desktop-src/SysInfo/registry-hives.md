---
description: Eine Hive ist eine logische Gruppe von Schlüsseln, unter Schlüsseln und Werten in der Registrierung, die eine Reihe unterstützender Dateien enthält, die Datensicherungen enthalten.
ms.assetid: fe517d88-7b03-4dc3-b3db-6a92665bca8e
title: Registrierungs Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05f942a275855c710de53a0d93df0b4654dd596f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865703"
---
# <a name="registry-hives"></a>Registrierungs Strukturen

Eine *Hive* ist eine logische Gruppe von Schlüsseln, unter Schlüsseln und Werten in der Registrierung, bei der eine Reihe von unterstützenden Dateien in den Arbeitsspeicher geladen werden, wenn das Betriebssystem gestartet oder ein Benutzer sich anmeldet.

Jedes Mal, wenn sich ein neuer Benutzer an einem Computer anmeldet, wird eine neue Hive für diesen Benutzer mit einer separaten Datei für das Benutzerprofil erstellt. Dies wird als *Benutzerprofil-Hive* bezeichnet. Die Hive eines Benutzers enthält bestimmte Registrierungsinformationen in Bezug auf die Anwendungseinstellungen des Benutzers, den Desktop, die Umgebung, die Netzwerkverbindungen und die Drucker. Benutzerprofil Strukturen befinden sich unter dem Schlüssel **HKEY \_ Users** .

Registrierungsdateien haben die folgenden zwei Formate: Standard und latest. Das Standardformat ist das einzige von Windows 2000 unterstützte Format. Sie wird auch von neueren Versionen von Windows aus Gründen der Abwärtskompatibilität unterstützt. Das neueste Format wird ab Windows XP unterstützt. In Windows-Versionen, die das neueste Format unterstützen, verwenden die folgenden Strukturen weiterhin das Standardformat: **HKEY \_ Current \_ User**, **HKEY \_ local \_ Machine \\ Sam**, **HKEY \_ local \_ Machine \\ Security** und **HKEY \_ Users \\ . Standard** Wert; alle anderen Strukturen verwenden das neueste Format.

Die meisten der unterstützenden Dateien für die Strukturen befinden sich im Verzeichnis% systemroot% \\ system32 \\ config. Diese Dateien werden jedes Mal aktualisiert, wenn sich ein Benutzer anmeldet. Die Dateinamen Erweiterungen der Dateien in diesen Verzeichnissen oder in einigen Fällen, in denen eine Erweiterung fehlt, geben den Typ der darin enthaltenen Daten an. In der folgenden Tabelle werden diese Erweiterungen zusammen mit einer Beschreibung der Daten in der Datei aufgelistet.



| Durchwahl       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| none<br/> | Eine komplette Kopie der Hive-Daten.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| . alt<br/> | Eine Sicherungskopie der wichtigen HKEY-System Struktur für den **\_ lokalen \_ Computer \\** . Nur der System Schlüssel hat eine alt-Datei.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| .log<br/> | Ein Transaktionsprotokoll mit Änderungen an den Schlüsseln und Wert Einträgen in der Hive.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| . sav<br/> | Eine Sicherungskopie einer Struktur.<br/> **Windows Server 2003 und Windows XP/2000:** Kopien der Hive-Dateien, wenn Sie sich am Ende der Textmodusphase beim Setup angeschaut haben. Setup verfügt über zwei Phasen: Textmodus und Grafikmodus. Die Hive-Datei wird nach der textmodusephase des Setups in eine. sav-Datei kopiert, um Sie vor Fehlern zu schützen, die auftreten können, wenn die Grafikmodus-Phase des Setups fehlschlägt. Wenn Setup während der Grafikmodus-Stufe fehlschlägt, wird nur die Grafikmodus-Stufe wiederholt, wenn der Computer neu gestartet wird. die Datei ". SAV" wird verwendet, um die Hive-Daten wiederherzustellen.<br/> |



 

In der folgenden Tabelle werden die Standard Strukturen und deren unterstützende Dateien aufgelistet.



| Registrierungs Struktur                      | Unterstützende Dateien                           |
|------------------------------------|--------------------------------------------|
| **aktuelle HKEY- \_ \_ Konfiguration**          | System, System. alt, System. log, System. sav |
| **Aktueller HKEY- \_ \_ Benutzer**            | Ntuser. dat, Ntuser. dat. log                 |
| **HKEY \_ local \_ Machine \\ Sam**      | Sam, Sam. log, Sam. sav                      |
| **Sicherheit des lokalen HKEY-Computers \_ \_ \\** | Sicherheit, Security. log, Security. sav       |
| **Lokale HKEY- \_ \_ Computer \\ Software** | Software, Software. log, Software. sav       |
| **Lokales HKEY- \_ \_ Computer \\ System**   | System, System. alt, System. log, System. sav |
| **HKEY- \_ Benutzer \\ . Vorgegebene**          | Default, Default. log, Default. sav          |



 

 

 




