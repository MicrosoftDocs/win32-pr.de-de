---
description: Im folgenden finden Sie Hinweise zur ordnungsgemäßen Interaktion mit verschiedenen Dateisystem-und Sicherheitsfeatures, die in Windows Vista und Windows Server 2008 eingeführt wurden.
ms.assetid: 3e8a1fd2-59e5-4f18-aafc-0ce5ac1e1cfa
title: Arbeiten mit Datei System-und Sicherheits Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12903599beb7ed153965f4b803ad8147fd32067a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129272"
---
# <a name="working-with-file-system-and-security-features"></a>Arbeiten mit Datei System-und Sicherheits Features

Im folgenden finden Sie Hinweise zur ordnungsgemäßen Interaktion mit verschiedenen Dateisystem-und Sicherheitsfeatures, die in Windows Vista und Windows Server 2008 eingeführt wurden.

## <a name="interoperability-with-transactions"></a>Interoperabilität mit Transaktionen

Zur Unterstützung von Transaktionen stellt VSS sicher, dass sowohl der Kerneltransaktions-Manager (KTM) als auch der Distributed Transaction Coordinator (DTC) vor der Erstellung von Volumeschattenkopien eingefroren werden. Wenn das System das Einfrieren von KTM oder DTC nicht durchführt, können die folgenden Timeout Fehler von der [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) -Methode zurückgegeben werden:

<dl> VSS \_ E \_ Transaction \_ Freeze \_ Timeout  
Timeout für VSS \_ E- \_ Transaktions- \_ Thaw \_  
</dl>

Wenn der Anforderer einen dieser Fehlercodes erhält, muss er die Erstellung der Schatten Kopie wiederholen.

Registrierungs-und Dateisystem Vorgänge können ebenfalls transaktiv sein. Im Fall der Registrierung ist der Registrierungs Schreiber für die Sicherstellung der Transaktions Konsistenz verantwortlich. Bei Transaktions-NTFS-Dateisystem Vorgängen (Transaktions NTFS, TxF) ist der Systemanbieter für die Sicherstellung der Transaktions Konsistenz verantwortlich. Dies erfolgt durch Bereitstellen der Schatten Kopie als Lese-/Schreibzugriff, nachdem Sie erstellt wurde, um eine automatische Wiederherstellung zu ermöglichen. Während der automatischen Wiederherstellungs Phase führt KTM ein Rollback für unvollständige Transaktionen aus.

## <a name="identifying-and-creating-hard-links"></a>Identifizieren und Erstellen von Hardlinks

Beim Sichern von Dateien muss eine Sicherungs Anwendung alle festen Links zu jeder Datei identifizieren, um zu vermeiden, dass dieselbe Datei mehrmals gesichert wird. Zum Auflisten von festen Links stehen zwei neue Funktionen zur Verfügung: [**findfirstdateinamew**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) und [**FindNextFile amew**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew).

Ebenso muss die Sicherungs Anwendung beim Wiederherstellen von Dateien feste Verknüpfungen [**mithilfe der Funktion**](/windows/win32/api/winbase/nf-winbase-createhardlinka) "-Funktion" (Funktion) wiederherstellen.

Sicherungs Anwendungen müssen in der \_ \_ Sicherungs Phase und \_ in der Wiederherstellungs Phase auch den Namen der SE Backup Name-Berechtigung bestätigen \_ .

## <a name="permissions-and-privileges-required-by-backup-applications"></a>Von Sicherungs Anwendungen benötigte Berechtigungen und Berechtigungen

Sicherungs Anwendungen, die Systemdateien wiederherstellen, benötigen die folgenden Berechtigungen:

<dl> Name der SE- \_ Sicherung \_  
SE \_ Restore \_ Name  
Name der SE- \_ Sicherheit \_  
Name der SE \_ \_ Besitz Besitz \_  
</dl>

Sicherungs Anwendungen müssen \_ während der Wiederherstellungs Phase auch Schreib Besitzer-Zugriffsrechte anfordern.

## <a name="windows-media-digital-rights-management"></a>Digitales Windows Media-Rights Management

Der DRM-Client (Windows Media Digital Rights Management) unterhält ein Verzeichnis mit sensiblen Zustands-und Lizenzdateien im Verzeichnis% Program Data% \\ Microsoft \\ Windows \\ DRM. Die Dateien in diesem Verzeichnis sollten zur gleichen Zeit wie temporäre Dateien und Cache Dateien gelöscht werden. Um sicherzustellen, dass der Windows-DRM-Client in einem konsistenten Zustand bleibt, müssen Sie die Sicherung oder Wiederherstellung dieser Dateien vermeiden. Dieses Verzeichnis ist im Registrierungsschlüssel "FilesNotToBackup" aufgeführt. Weitere Informationen zum Schlüssel FilesNotToBackup finden Sie unter [Erstellen eines Sicherungs Satzes](generating-a-backup-set.md).

## <a name="user-account-control"></a>Benutzerkontensteuerung

Die Einführung der Benutzerkontensteuerung (User Account Control, UAC) in Windows Vista bedeutet, dass Anwendungen unter einem Standardbenutzer Konto ausgeführt werden müssen, sofern nicht anders angegeben. Außerdem ändert die Datei-und registrierungsvirtualisierungsfunktion von UAC die Speicherorte, an denen die Benutzerdaten gespeichert werden. Weitere Informationen zum Arbeiten mit UAC und der Datei-und Registrierungsvirtualisierung finden Sie in den folgenden Referenzen:

<dl>

[Windows Vista und Windows Server 2008 Developer Story: Windows Vista Anwendungs Entwicklungsanforderungen für die Benutzerkontensteuerung (User Account Control, UAC)](/previous-versions/aa905330(v=msdn.10))  
[Windows Vista-Anwendungs Entwicklungsanforderungen für die Kompatibilität mit der Benutzerkontensteuerung](/previous-versions/dotnet/articles/bb530410(v=msdn.10))  
[Patching der Benutzerkontensteuerung (User Account Control, UAC)](../msi/user-account-control--uac--patching.md)  
</dl>

## <a name="bitlocker-drive-encryption"></a>BitLocker-Laufwerkverschlüsselung

BitLocker-Laufwerkverschlüsselung ist ein neues Feature in Windows Vista Enterprise, Windows Vista Ultimate und Windows Server 2008, das eine sichere Start-und vollständige Volumeverschlüsselung bietet. Das Verständnis dieser Funktion ist für Entwickler von Sicherungs Anwendungen wichtig, die Offline Wiederherstellungen durchführen, bei denen Daten möglicherweise auf einem verschlüsselten Laufwerk wieder hergestellt werden müssen.

Führen Sie die folgenden Schritte aus, um Daten auf einem verschlüsselten Laufwerk wiederherzustellen:

1.  Entsperren Sie das Laufwerk.
2.  Deaktivieren Sie BitLocker-Laufwerkverschlüsselung.
3.  Führen Sie die Wiederherstellung aus.
4.  Starten Sie das wiederhergestellte Betriebssystem, und schalten Sie BitLocker-Laufwerkverschlüsselung ein.

Ausführliche Informationen zu BitLocker-Laufwerkverschlüsselung, einschließlich einer Schritt-für-Schritt-Anleitung, finden Sie auf der Microsoft TechNet Windows Vista-Website unter [BitLocker-Laufwerkverschlüsselung](https://www.microsoft.com/technet/windowsvista/security/bitlockr.mspx) . Weitere Informationen zum BitLocker-Laufwerkverschlüsselung WMI-Anbieter finden Sie unter [BitLocker-Laufwerkverschlüsselung Provider](../secprov/bitlocker-drive-encryption-provider.md).

 

 
