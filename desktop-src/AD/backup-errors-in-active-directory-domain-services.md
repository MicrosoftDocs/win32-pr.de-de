---
title: Sicherungsfehler in Active Directory Domain Services
description: In diesem Thema werden Rückgabewerte für Sicherungsfehler für Funktionen in Active Directory Domain Services.
ms.assetid: d042f189-1b86-42ca-bdb4-a8aaa96c9c65
ms.tgt_platform: multiple
keywords:
- Active Directory-Sicherungsfehler
- Active Directory-Domäne von Dienstsicherungsfehlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5038b1d3a7a1f24c2e3b8dbf137aa2722073650b878e1d6a1dfdec8cac399a94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024137"
---
# <a name="backup-errors-in-active-directory-domain-services"></a>Sicherungsfehler in Active Directory Domain Services

In diesem Thema werden Rückgabewerte für Sicherungsfehler für Funktionen in Active Directory Domain Services.



| Wert                                      | Beschreibung                                                                                                                                                                                  |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **hrNyi**<br/>                       | Die Funktion ist nicht implementiert.<br/>                                                                                                                                                  |
| **hrInvalidParam**<br/>              | Der Parameter ist ungültig.<br/>                                                                                                                                                       |
| **hrError**<br/>                     | Interner Fehler.<br/>                                                                                                                                                       |
| **hrInvalidHandle**<br/>             | Das Handle ist ungültig.<br/>                                                                                                                                                          |
| **hrRestoreInProgress**<br/>         | Der Wiederherstellungsvorgang wird in Bearbeitung.<br/>                                                                                                                                               |
| **hrAlreadyOpen**<br/>               | Die angegebene Datei ist geöffnet.<br/>                                                                                                                                                       |
| **hrInvalidRecips**<br/>             | Die Empfänger sind ungültig. <br/>                                                                                                                                                    |
| **hrCouldNotConnect**<br/>           | Sicherung nicht möglich. Eine Verbindung mit dem angegebenen Sicherungsserver wurde nicht erkannt, oder der Dienst, den Sie sichern möchten, wird nicht ausgeführt.<br/>                                       |
| **hrRestoreMapExists**<br/>          | Für die angegebene Komponente ist eine Wiederherstellungszuordnung vorhanden. Eine Wiederherstellungszuordnung kann beim Ausführen einer vollständigen Wiederherstellung angegeben werden.<br/>                                                                  |
| **hrIncrementalBackupDisabled**<br/> | Eine andere Anwendung hat die angegebene Windows NT/Windows 2000 Directory Service-Datenbank so geändert, dass alle nachfolgenden Sicherungen fehlschlagen. Führen Sie eine vollständige Sicherung durch, um dieses Problem zu beheben.<br/> |
| **hrLogFileNotFound**<br/>           | Eine inkrementelle Sicherung kann nicht ausgeführt werden, da eine Windows NT/Windows 2000-Verzeichnisdienst-Datenbankprotokolldatei nicht gefunden wurde.<br/>                                        |
| **hrCircularLogging**<br/>           | Die Windows NT/Windows 2000 Directory Service-Komponente ist für die Verwendung zirkulärer Datenbankprotokolle konfiguriert. Die Sicherung kann nicht inkrementell durchgeführt werden. Führen Sie eine vollständige Sicherung durch.<br/>       |
| **hrNoFullRestore**<br/>             | Die Datenbanken wurden auf diesem Computer nicht wiederhergestellt. Sie können eine inkrementelle Sicherung erst wiederherstellen, wenn eine vollständige Sicherung wiederhergestellt wurde.<br/>                                            |
| **hrCommunicationError**<br/>        | Beim Versuch, eine lokale Sicherung durchzuführen, ist ein Kommunikationsfehler aufgetreten.<br/>                                                                                                       |
| **hrFullBackupNotTaken**<br/>        | Sie müssen eine vollständige Sicherung durchführen, bevor Sie eine inkrementelle Sicherung ausführen können.<br/>                                                                                                      |
| **hrMissingExpiryToken**<br/>        | Das Ablauftoken fehlt. Die Wiederherstellung kann ohne die Ablaufdaten nicht wiederhergestellt werden.<br/>                                                                                                                  |
| **hrUnknownExpiryTokenFormat**<br/>  | Das Ablauftoken hat ein nicht erkennbares Format.<br/>                                                                                                                                      |
| **hrContentsExpired**<br/>           | DS-Inhalte in der Sicherung sind veraltet. Wiederherstellen mit einer aktuellen Kopie.<br/>                                                                                                            |



 

## <a name="see-also"></a>Weitere Informationen

[Erfolg](success.md), [Systemfehler in Active Directory Domain Services](system-errors-in-active-directory-domain-services.md), [Verzeichnis-Manager-Fehler](directory-manager-errors.md), Protokollierungs- und Wiederherstellungsfehler in Funktionen [in Active Directory Domain Services](logging-and-recovery-errors-in-functions-in-active-directory-domain-services.md), [Rückgabewerte für Funktionen in Active Directory Domain Services](return-values-for-functions-in-active-directory-domain-services.md)


 

 





