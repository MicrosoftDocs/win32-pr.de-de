---
title: Sicherungs Fehler in Active Directory Domain Services
description: In diesem Thema werden die Rückgabewerte von Sicherungs Fehlern für Funktionen in Active Directory Domain Services aufgeführt.
ms.assetid: d042f189-1b86-42ca-bdb4-a8aaa96c9c65
ms.tgt_platform: multiple
keywords:
- Active Directory Sicherungs Fehler
- Active Directory-Domäne von Dienst Sicherungs Fehlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9b38ba9f28e47fd95e69a923e953d59fdd4d37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470772"
---
# <a name="backup-errors-in-active-directory-domain-services"></a>Sicherungs Fehler in Active Directory Domain Services

In diesem Thema werden die Rückgabewerte von Sicherungs Fehlern für Funktionen in Active Directory Domain Services aufgeführt.



| Wert                                      | BESCHREIBUNG                                                                                                                                                                                  |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **hrnyi**<br/>                       | Die Funktion ist nicht implementiert.<br/>                                                                                                                                                  |
| **hrinvalidparam**<br/>              | Der Parameter ist ungültig.<br/>                                                                                                                                                       |
| **hrError**<br/>                     | Interner Fehler.<br/>                                                                                                                                                       |
| **hrinvalidhandle**<br/>             | Das Handle ist ungültig.<br/>                                                                                                                                                          |
| **hrrestoreingeprogress**<br/>         | Der Wiederherstellungs Vorgang wird ausgeführt.<br/>                                                                                                                                               |
| **hralleseryopen**<br/>               | Die angegebene Datei ist geöffnet.<br/>                                                                                                                                                       |
| **hrinvalidrecips**<br/>             | Die Empfänger sind ungültig. <br/>                                                                                                                                                    |
| **hrcouldnotconnect**<br/>           | Die Sicherung kann nicht ausgeführt werden. Es wurde keine Verbindung mit dem angegebenen Sicherungs Server erkannt, oder der Dienst, den Sie sichern möchten, wird nicht ausgeführt.<br/>                                       |
| **hrrestoremapist vorhanden.**<br/>          | Für die angegebene Komponente ist eine Wiederherstellungs Zuordnung vorhanden. Eine Restore Map kann beim Ausführen einer vollständigen Wiederherstellung angegeben werden.<br/>                                                                  |
| **hrincrementalbackupdeaktiviert**<br/> | Eine andere Anwendung hat die angegebene Windows NT/Windows 2000-Verzeichnisdienst Datenbank so geändert, dass alle nachfolgenden Sicherungen fehlschlagen. Um dieses Problem zu beheben, führen Sie eine vollständige Sicherung aus.<br/> |
| **hrlogfile-found**<br/>           | Eine inkrementelle Sicherung kann nicht ausgeführt werden, weil eine erforderliche Windows NT/Windows 2000-Verzeichnisdienst-Daten Bank Protokolldatei nicht gefunden wurde.<br/>                                        |
| **hrcircularlogging**<br/>           | Die angegebene Windows NT/Windows 2000-Verzeichnisdienst Komponente ist so konfiguriert, dass zirkuläre Daten Bank Protokolle verwendet werden. Sie kann nicht inkrementell gesichert werden. Führen Sie eine vollständige Sicherung aus.<br/>       |
| **hrnofullrestore**<br/>             | Die Datenbanken wurden nicht auf diesem Computer wieder hergestellt. Eine inkrementelle Sicherung kann erst wieder hergestellt werden, wenn eine vollständige Sicherung wieder hergestellt wurde<br/>                                            |
| **hrcommunicationerror**<br/>        | Kommunikationsfehler beim Versuch, eine lokale Sicherung auszuführen.<br/>                                                                                                       |
| **hrfullbackupnottaken**<br/>        | Sie müssen eine vollständige Sicherung durchführen, bevor Sie eine inkrementelle Sicherung ausführen können.<br/>                                                                                                      |
| **hrmissingexpirytoken**<br/>        | Das Ablauf Token fehlt. Ohne die Ablaufdaten kann nicht wieder hergestellt werden.<br/>                                                                                                                  |
| **hrunknownexpirytokenformat**<br/>  | Das Ablauf Token liegt in einem nicht erkennbaren Format vor.<br/>                                                                                                                                      |
| **hrcontentsexpired**<br/>           | Der DS-Inhalt in der Sicherung ist veraltet. Stellen Sie mit einer aktuellen Kopie wieder her.<br/>                                                                                                            |



 

## <a name="see-also"></a>Weitere Informationen

[Erfolg](success.md), [System Fehler in Active Directory Domain Services](system-errors-in-active-directory-domain-services.md), [Verzeichnis-Manager-Fehler](directory-manager-errors.md), [Protokollierungs-und Wiederherstellungs Fehler in Funktionen in Active Directory Domain Services](logging-and-recovery-errors-in-functions-in-active-directory-domain-services.md), [Rückgabewerte für Funktionen in Active Directory Domain Services](return-values-for-functions-in-active-directory-domain-services.md)


 

 





