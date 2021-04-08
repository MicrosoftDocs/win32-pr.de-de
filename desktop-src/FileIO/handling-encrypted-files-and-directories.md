---
description: Eine Datei, die als verschlüsselt gekennzeichnet ist, wird vom NTFS-Dateisystem mithilfe des aktuellen Verschlüsselungs Treibers verschlüsselt.
ms.assetid: 166bfb8c-b97d-4cc7-bf6b-399837cb8ad0
title: Behandeln von verschlüsselten Dateien und Verzeichnissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2718656a28eb678c10076e228e08a2a95cabd1fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960648"
---
# <a name="handling-encrypted-files-and-directories"></a>Behandeln von verschlüsselten Dateien und Verzeichnissen

Ein Programmierer oder Benutzer kann ein Verzeichnis oder eine Datei als verschlüsselt markieren. Eine Datei, die als verschlüsselt gekennzeichnet ist, wird vom NTFS-Dateisystem mithilfe des aktuellen Verschlüsselungs Treibers verschlüsselt. Wenn die Datei zu einem späteren Zeitpunkt als nicht verschlüsselt gekennzeichnet ist, wird sie entschlüsselt und in einem nur-Text-Zustand (unsicher) belassen.

Verzeichnisse werden nicht selbst verschlüsselt. In einem "verschlüsselten" Verzeichnis werden standardmäßig alle neuen Dateien im Verzeichnis bei der Erstellung verschlüsselt. Ein Benutzer muss den Status einer neuen Datei explizit ändern, um entschlüsselt zu werden, wenn der Benutzer nicht möchten, dass die Datei verschlüsselt wird. Ein verschlüsseltes Verzeichnis ist sichtbar. Verwenden Sie die Standardmethoden für die Zugriffs Steuerung, damit andere Benutzer nicht auf ein Verzeichnis zugreifen können.

Die Verschlüsselungsfunktionen können nicht mit der [Backup-API](/windows/desktop/Backup/backup)verwendet werden.

Verwenden Sie [**die Funktion "**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Funktion", um eine neue Datei zu verschlüsseln **. \_ \_** Verwenden Sie die Funktion " [**verschlüsseltfile**](/windows/desktop/api/WinBase/nf-winbase-encryptfilea) ", um eine vorhandene Datei zu verschlüsseln. Alle Datenströme in der Datei werden verschlüsselt. Wenn die Datei bereits verschlüsselt ist, führt " **verschlüsseltfile** " nichts aus, sondern gibt einen Wert ungleich 0 (null) zurück, was den Erfolg angibt. Wenn die Datei komprimiert ist, wird die Datei von **Verschlüsselungsdatei** vor der Verschlüsselung dekomprimiert.

Verwenden Sie die [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) -Funktion, um eine verschlüsselte Datei zu entschlüsseln. Wenn die Datei nicht verschlüsselt ist, führt **DecryptFile** keine Aktion aus, sondern gibt einen Wert ungleich NULL zurück, der den Erfolg angibt.

Die Funktion " [**verschlüsselungsdeaktivieren**](/windows/desktop/api/WinEfs/nf-winefs-encryptiondisable) " deaktiviert oder aktiviert die Verschlüsselung des bestimmten Verzeichnisses und der darin aufgeführten Dateien. Die Verschlüsselung von Unterverzeichnissen unter dem angegebenen Verzeichnis wird nicht beeinträchtigt.

Verwenden Sie die [**fileverschlüsseltionstatus**](/windows/desktop/api/WinBase/nf-winbase-fileencryptionstatusa) -Funktion, um den Verschlüsselungs Status einer Datei abzurufen. Rufen Sie alternativ die [**getfileattributfunktion**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) auf, und untersuchen Sie das **\_ Dateiattribut \_ verschlüsselte** Flag im Rückgabewert.

[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) und [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) versuchen, die Zieldatei mit den Schlüsseln zu verschlüsseln, die bei der Verschlüsselung der Quelldatei verwendet werden. Wenn dies nicht möglich ist, versuchen beide Funktionen, die Zieldatei mit Standard Schlüsseln zu verschlüsseln. Wenn beide Methoden nicht ausgeführt werden können, schlagen **CopyFile** und **CopyFileEx** mit einem Fehler bei der **Fehler \_ Verschlüsselung \_** fehl. Wenn Sie **möchten, dass** **CopyFileEx** den Kopiervorgang abschließt, auch wenn die Zieldatei nicht verschlüsselt werden kann, schließen Sie das Flag zum Zulassen des **\_ \_ \_ entschlüsselten \_ Ziels** in den Wert des Parameters dwcopyflags in den Wert des Parameters *dwcopyflags* ein.

 

 
