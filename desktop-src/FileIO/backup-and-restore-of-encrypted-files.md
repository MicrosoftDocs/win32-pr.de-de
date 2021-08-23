---
description: Die verschlüsselungsrohen Funktionen ermöglichen die Sicherung verschlüsselter Dateien.
ms.assetid: 00f9b00e-305d-4554-8b43-7061228c92c3
title: Sichern und Wiederherstellen verschlüsselter Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34308dbfc0f67a1fcf9a70f1f7a5878434018494fa1450d308fa493af78226ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766180"
---
# <a name="backup-and-restore-of-encrypted-files"></a>Sichern und Wiederherstellen verschlüsselter Dateien

Der verschlüsselndes Dateisystem (EFS) filtert das Öffnen einer verschlüsselten Datei so, dass die Anwendung, die die Datei geöffnet hat, Zugriff auf die unverschlüsselten Informationen erhält, vorausgesetzt, sie verfügt natürlich über die richtigen Anmeldeinformationen, um auf die Datei zuzugreifen und den Schlüssel abzurufen, der zum Entschlüsseln der Datei erforderlich ist. Nachfolgende Lesevorgänge für diese Datei ergeben unverschlüsselten Text. Dies ist für den typischen Zugriff auf verschlüsselte Dateien sehr wünschenswert und sorgt dafür, dass die Verschlüsselung und Entschlüsselung der Dateien transparent bleibt. Es wird jedoch die Sicherung verschlüsselter Dateien verhindert, da die gesicherten Dateien die Nur-Text-Version sind, wenn versucht wird, eine Sicherung mit den Standarddatei-E/A-Aufrufen wie [**CreateFile,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)und [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)durchzuführen.

Die verschlüsselungsrohen Funktionen werden bereitgestellt, um dieses Problem zu lösen. Sicherungsanwendungen sind ein primärer vorgesehener Benutzer für diese Funktionen. Unformatierte Verschlüsselungsfunktionen unterscheiden sich von anderen Dateisystemfunktionen darin, dass Open-, Read- und Write-Funktionen den Zugriff auf die verschlüsselten Rohdatenströme und auch das Lesen/Schreiben des $EFS Datenstroms ermöglichen. Daher benötigt der Aufrufer der verschlüsselungsrohen Funktionen keinen Zugriff auf die kryptografischen Schlüssel, die die Datei entschlüsseln. Die folgenden unformatierten Verschlüsselungs-APIs sind für die Verwendung mit Sicherungs- und Wiederherstellungsanwendungen verfügbar: 

| Raw Encryption API                                     | Beschreibung                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OpenEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)   | Öffnen Sie eine verschlüsselte Datei mit Zugriff auf Daten im verschlüsselten Format. Wenn der Aufrufer keinen Zugriff auf den Schlüssel für die Datei hat, benötigt der Aufrufer [SeBackupPrivilege,](/windows/desktop/SecAuthZ/authorization-constants) um verschlüsselte Dateien zu exportieren, oder SeRestorePrivilege, um verschlüsselte Dateien zu importieren. |
| [**CloseEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-closeencryptedfileraw) | Schließen einer verschlüsselten Datei, die mit [ **OpenEncryptedFileRaw** geöffnet wurde](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)                                                                                                                                                                                      |
| [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)   | Lesen einer verschlüsselten Datei, die ihre Daten im verschlüsselten Format zurücklässt                                                                                                                                                                                                                   |
| [**WriteEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw) | Schreiben einer verschlüsselten Datei, die ihre Daten im verschlüsselten Format zurücklässt                                                                                                                                                                                                                  |
| [**ImportCallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_import_func)               | Anwendungsdefinierte Rückrufe zur Verwendung mit [ **WriteEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw)                                                                                                                                                                              |
| [**ExportCallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_export_func)               | Anwendungsdefinierte Rückrufe zur Verwendung mit [ **ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)                                                                                                                                                                                |



 

 

 
