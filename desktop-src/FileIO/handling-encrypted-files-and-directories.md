---
description: Eine als verschlüsselt markierte Datei wird vom NTFS-Dateisystem mithilfe des aktuellen Verschlüsselungstreibers verschlüsselt.
ms.assetid: 166bfb8c-b97d-4cc7-bf6b-399837cb8ad0
title: Behandeln verschlüsselter Dateien und Verzeichnisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1a3a7b4a2d38aa2f4e012ccb96d01712f280879ff578afdb5c69392ab826a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927790"
---
# <a name="handling-encrypted-files-and-directories"></a>Behandeln verschlüsselter Dateien und Verzeichnisse

Ein Programmierer oder Benutzer kann ein Verzeichnis oder eine Datei als verschlüsselt markieren. Eine als verschlüsselt markierte Datei wird vom NTFS-Dateisystem mithilfe des aktuellen Verschlüsselungstreibers verschlüsselt. Wenn die Datei zu einem späteren Zeitpunkt als nicht verschlüsselt markiert ist, wird sie entschlüsselt und in einem (ungesicherten) Nur-Text-Zustand zurückgelassen.

Verzeichnisse werden nicht selbst verschlüsselt. Stattdessen werden in einem "verschlüsselten" Verzeichnis standardmäßig alle neuen Dateien im Verzeichnis bei der Erstellung verschlüsselt. Ein Benutzer muss den Status einer neuen Datei explizit in entschlüsselt ändern, wenn der Benutzer nicht möchte, dass die Datei verschlüsselt wird. Ein verschlüsseltes Verzeichnis ist sichtbar. Um anderen Benutzern den Zugriff auf ein Verzeichnis zu ermöglichen, verwenden Sie die Standardmethoden der Zugriffssteuerung.

Die Verschlüsselungsfunktionen können nicht mit der [Sicherungs-API verwendet werden.](/windows/desktop/Backup/backup)

Um eine neue Datei zu verschlüsseln, verwenden Sie die [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) mit dem **FILE ATTRIBUTE \_ \_ ENCRYPTED-Flag.** Verwenden Sie zum Verschlüsseln einer vorhandenen Datei die [**EncryptFile-Funktion.**](/windows/desktop/api/WinBase/nf-winbase-encryptfilea) Alle Datenströme in der Datei werden verschlüsselt. Wenn die Datei bereits verschlüsselt ist, **führt EncryptFile** nichts aus, sondern gibt einen Wert ungleich 0 (null) zurück, der auf Erfolg hinweist. Wenn die Datei komprimiert ist, dekomprimiert **EncryptFile** die Datei, bevor sie verschlüsselt wird.

Verwenden Sie zum Entschlüsseln einer verschlüsselten Datei die [**DecryptFile-Funktion.**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) Wenn die Datei nicht verschlüsselt ist, **führt DecryptFile** nichts aus, sondern gibt einen Wert ungleich 0 (null) zurück, der den Erfolg angibt.

Die [**EncryptionDisable-Funktion**](/windows/desktop/api/WinEfs/nf-winefs-encryptiondisable) deaktiviert oder aktiviert die Verschlüsselung des angegebenen Verzeichnisses und der dateien in diesem Verzeichnis. Dies wirkt sich nicht auf die Verschlüsselung von Unterverzeichnissen unterhalb des angegebenen Verzeichnisses aus.

Verwenden Sie die [**FileEncryptionStatus-Funktion,**](/windows/desktop/api/WinBase/nf-winbase-fileencryptionstatusa) um den Verschlüsselungsstatus einer Datei abzurufen. Rufen Sie alternativ die [**GetFileAttributes-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) auf, und untersuchen Sie das **FILE ATTRIBUTE \_ \_ ENCRYPTED-Flag** im Rückgabewert.

[**CopyFile und**](/windows/desktop/api/WinBase/nf-winbase-copyfile) [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) versuchen, die Zieldatei mit den Schlüsseln zu verschlüsseln, die bei der Verschlüsselung der Quelldatei verwendet werden. Wenn dies nicht möglich ist, versuchen beide Funktionen, die Zieldatei mit Standardschlüsseln zu verschlüsseln. Wenn beide Methoden nicht durchgeführt werden können, **tritt bei CopyFile** und **CopyFileEx** der **Fehler ERROR ENCRYPTION \_ \_ FAILED** auf. Wenn **CopyFileEx** den Kopiervorgang auch dann abschließen soll, wenn die Zieldatei nicht verschlüsselt werden kann, fügen Sie das **FLAG COPY FILE ALLOW \_ \_ \_ DECRYPTED \_ DESTINATION** in den Wert des *dwCopyFlags-Parameters* in Den Aufruf von **CopyFileEx ein.**

 

 
