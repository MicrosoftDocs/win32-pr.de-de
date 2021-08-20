---
description: In Windows Vista und Windows Server 2008 und höher kann der Entwickler eines VSS-Writer oder einer VsS-Anwendung bestimmte Dateien von Schattenkopien ausschließen.
ms.assetid: 4fe1ae94-7b2f-421a-9009-3a7e88822458
title: Ausschließen von Dateien aus Schattenkopien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c39acf8c92d44bcf8786a880b6ae5eb6a88786809f5af1609dee1b342cd2fb65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122106"
---
# <a name="excluding-files-from-shadow-copies"></a>Ausschließen von Dateien aus Schattenkopien

In Windows Vista und Windows Server 2008 und höher kann der Entwickler eines VSS-Writer oder einer VsS-Anwendung bestimmte Dateien von Schattenkopien ausschließen.

Die Auswirkungen auf die Leistung und die Verwendung des Schattenkopiespeicherbereichs (auch als "Diff Area" bezeichnet) einer Datei in einer Schattenkopie stehen in direktem Zusammenhang mit der Menge der Änderungen am Inhalt der Datei, nachdem die Schattenkopie erstellt wurde. Darüber hinaus kann das Ausschließen von Dateien aus Schattenkopien die Erstellung von Schattenkopien verlangsamen.

Aus diesen Gründen sollte eine Datei nur dann von Schattenkopien ausgeschlossen werden, wenn sie groß ist, eine erhebliche Änderung zwischen einer Schattenkopie und der nächsten durchläuft und nicht sichern werden muss.

Sie sollten nur Dateien ausschließen, die zu Ihrer Anwendung gehören.

Wenn das VSS \_ VOLSNAP \_ ATTR \_ NO AUTORECOVERY-Flag im Schattenkopiekontext festgelegt ist, bedeutet dies, dass die automatische Wiederherstellung deaktiviert ist und keine Dateien aus der Schattenkopie ausgeschlossen werden \_ können. Weitere Informationen finden Sie in der [**\_ VSS \_ VOLUME \_ SNAPSHOT \_ ATTRIBUTES-Enumeration.**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

## <a name="using-the-addexcludefilesfromsnapshot-method"></a>Verwenden der AddExcludeFilesFromSnapshot-Methode

Ein VSS Writer kann Dateien wie folgt aus einer Schattenkopie ausschließen:

1.  Rufen Sie [**die IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) auf, um die auszuschließenden Dateien zu melden.
2.  Löschen Sie in der [**CVssWriter::OnPostSnapshot-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) des Writers die Dateien aus der Schattenkopie.

## <a name="using-the-filesnottosnapshot-registry-key"></a>Verwenden des Registrierungsschlüssels FilesNotToSnapshot

> [!Note]  
> Der Registrierungsschlüssel **FilesNotToSnapshot** sollte nur von Anwendungen verwendet werden. Benutzer, die versuchen, den Registrierungsschlüssel zu verwenden, erhalten Einschränkungen wie die folgenden:
>
> -   Es können keine Dateien aus einer Schattenkopie gelöscht werden, die unter Windows Server mit dem Feature „Vorherige Versionen“ erstellt wurden.
> -   Es können keine Dateien aus Schattenkopien für freigegebene Ordner gelöscht werden.
> -   Sie kann Dateien aus einer Schattenkopie löschen, die mit dem [Hilfsprogramm DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) erstellt wurde, aber keine Dateien aus einer Schattenkopie löschen, die mit dem [Vssadmin-Hilfsprogramm erstellt](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) wurde.
> -   Dateien werden auf Grundlage der besten Leistung aus einer Schattenkopie gelöscht. Das bedeutet, dass Sie nicht unbedingt gelöscht werden.

 

Eine VSS-Anwendung kann Dateien während der Erstellung von Schattenkopien mithilfe des folgenden Registrierungsschlüssels aus einer Schattenkopie löschen:

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ BackupRestore \\ FilesNotToSnapshot**

Dieser Registrierungsschlüssel verfügt über REG \_ MULTI \_ SZ-Werte für jede Anwendung, deren Dateien ausgeschlossen werden können. Die Dateien werden durch vollqualifizierte Pfade angegeben, die den \* Platzhalter enthalten können.

In allen Fällen wird der Eintrag ignoriert, wenn keine Dateien mit der Pfadzeichenfolge übereinstimmen.

Nachdem eine Datei dem entsprechenden Registrierungsschlüsselwert hinzugefügt wurde, wird sie während der Erstellung durch den Schattenkopie-Optimierungswriter aus der Schattenkopie gelöscht.

Wenn kein vollqualifizierter Pfad angegeben werden kann, kann ein Pfad auch mithilfe der Variablen $UserProfile$ oder $AllVolumes$ impliziert werden. Beispiel:

-   $UserProfile$ Directory \\ \\ Subdirectory \\ FileName.\*
-   $AllVolumes$ \\ TemporaryFiles \\ \* .\*

Um den Pfad rekursiv zu machen, fügen Sie "/s" am Ende an. Beispiel:

-   $UserProfile$ Directory \\ \\ Subdirectory \\ FileName. \* /s
-   $AllVolumes$ \\ TemporaryFiles \\ \* . \* /s

Die $UserProfile$-Variable bewirkt, dass die Pfadzeichenfolge auf alle Benutzerprofile auf dem Computer angewendet wird. Die Benutzerprofile werden mit dem folgenden Registrierungsschlüssel aufzählt:

**HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ ProfileList**

Die $AllVolumes$-Variable bewirkt, dass die Pfadzeichenfolge auf alle Schattenkopien auf dem Computer angewendet wird. Angenommen, der Pfad ist "$AllVolumes$ \\ TemporaryFiles \\ \* . \* /s", und der Computer verfügt über drei Volumes: C:, D:und E:. Wenn C: und E: den Pfad " TemporaryFiles " enthalten, und Volume D: nur den Pfad D: Daten enthält, wird die Verzeichnisstruktur C: TemporaryFiles aus Schattenkopien von C: gelöscht, und die Verzeichnisstruktur \\ \\ \\ \\ \\ \\ E: \\ TemporaryFiles wird aus Schattenkopien von \\ E: gelöscht.

Administratoren können die Erweiterung der variablen $UserProfile$ mithilfe des folgenden Registrierungsschlüssels deaktivieren:

**HKEY \_ LOCAL MACHINE System \_ \\ \\ CurrentControlSet \\ Services \\ vss \\ Einstellungen**

Geben Sie unter diesem Registrierungsschlüssel DisableUserProfileExpansion als Wertnamen, REG DWORD für den Werttyp und einen Wert ungleich 0 (null) für die \_ Wertdaten an.

## <a name="about-the-filesnottobackup-registry-key"></a>Informationen zum Registrierungsschlüssel "FilesNotToBackup"

Der **Registrierungsschlüssel FilesNotToBackup** kann verwendet werden, um die Namen der Dateien und Verzeichnisse anzugeben, die von Sicherungsanwendungen nicht gesichert oder wiederhergestellt werden sollen. Diese Dateien werden jedoch nicht von Schattenkopien ausgeschlossen. Weitere Informationen zu diesem Registrierungsschlüssel finden Sie unter [Registrierungsschlüssel und -werte für Sicherung und Wiederherstellung.](../backup/registry-keys-for-backup-and-restore.md)

 

 
