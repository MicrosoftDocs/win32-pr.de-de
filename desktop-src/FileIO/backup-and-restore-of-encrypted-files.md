---
description: Die unformatierten Verschlüsselungsfunktionen ermöglichen die Sicherung verschlüsselter Dateien.
ms.assetid: 00f9b00e-305d-4554-8b43-7061228c92c3
title: Sichern und Wiederherstellen verschlüsselter Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fbc5d1babbbbb92cef9e78f9a0dade702fd63d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041895"
---
# <a name="backup-and-restore-of-encrypted-files"></a>Sichern und Wiederherstellen verschlüsselter Dateien

Der Verschlüsselndes Dateisystem (EFS) filtert das Öffnen einer verschlüsselten Datei so, dass die Anwendung, die die Datei geöffnet hat, Zugriff auf die unverschlüsselten Informationen erhält. der Grund dafür ist, dass Sie über die richtigen Anmelde Informationen für den Zugriff auf die Datei und den zum Entschlüsseln der Datei erforderlichen Schlüssel verfügt. Nachfolgende Lesevorgänge in dieser Datei führen zu unverschlüsseltem Text. Dies ist für den typischen Zugriff auf verschlüsselte Dateien sehr wünschenswert, und die Verschlüsselung und Entschlüsselung der Dateien bleibt transparent. Allerdings wird die Sicherung verschlüsselter Dateien verhindert, weil bei der Sicherung mit den standardmäßigen Datei-e/a-aufrufen wie z. b. " [**kreatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)", " [**Infofile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)" und " [**Write File**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)" die nur-Text-Version gesichert wird.

Um dieses Problem zu beheben, werden die unformatierten Verschlüsselungsfunktionen bereitgestellt. Sicherungs Anwendungen sind ein primärer Benutzer für diese Funktionen. Rohverschlüsselungs Funktionen unterscheiden sich von anderen Dateisystemfunktionen in, die Funktionen zum Öffnen, lesen und schreiben erlauben, den Zugriff auf die unformatierten Datenströme zuzulassen und auch das Lesen/Schreiben des $EFS Streams zuzulassen. Daher benötigt der Aufrufer der rohverschlüsselungs Funktionen keinen Zugriff auf die Kryptografieschlüssel, die die Datei entschlüsseln. Die folgenden unformatierten Verschlüsselungs-APIs stehen für die Verwendung mit Sicherungs-und Wiederherstellungs Anwendungen zur Verfügung: 

| Rohverschlüsselungs-API                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Openverschlüsseltedfileraw**](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)   | Öffnen Sie eine verschlüsselte Datei mit Zugriff auf Daten in verschlüsselter Form. Wenn der Aufrufer keinen Zugriff auf den Schlüssel für die Datei hat, benötigt der Aufrufer [SeBackupPrivilege](/windows/desktop/SecAuthZ/authorization-constants) , um verschlüsselte Dateien zu exportieren, oder SeRestorePrivilege, um verschlüsselte Dateien zu importieren. |
| [**Closeverschlüsseltedfileraw**](/windows/desktop/api/WinBase/nf-winbase-closeencryptedfileraw) | Schließt eine verschlüsselte Datei, die mit [ **openverschlüsseltedfileraw** geöffnet wurde.](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)                                                                                                                                                                                      |
| [**"Read verschlüsseltedfileraw"**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)   | Lesen einer verschlüsselten Datei, die Ihre Daten in verschlüsseltem Format verlässt                                                                                                                                                                                                                   |
| [**"Write teencryptedfileraw"**](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw) | Verschlüsselte Datei schreiben, um die Daten in verschlüsseltem Format zu belassen                                                                                                                                                                                                                  |
| [**Importcallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_import_func)               | Anwendungs definierter Rückruf für die Verwendung mit " [ **Write teencryptedfileraw** "](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw)                                                                                                                                                                              |
| [**Exportcallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_export_func)               | Anwendungs definierter Rückruf für die Verwendung mit " [ **getverschlüsseltedfileraw** "](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)                                                                                                                                                                                |



 

 

 
