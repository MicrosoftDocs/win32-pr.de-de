---
description: In Windows Vista und Windows Server 2008 und höher kann der Entwickler einer VSS Writer oder Anwendung bestimmte Dateien aus Schatten Kopien ausschließen.
ms.assetid: 4fe1ae94-7b2f-421a-9009-3a7e88822458
title: Ausschließen von Dateien aus Schatten Kopien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52546c8ddc6da62433dc610f2bf4fc2c46c5e53f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218321"
---
# <a name="excluding-files-from-shadow-copies"></a>Ausschließen von Dateien aus Schatten Kopien

In Windows Vista und Windows Server 2008 und höher kann der Entwickler einer VSS Writer oder Anwendung bestimmte Dateien aus Schatten Kopien ausschließen.

Der Speicherbereich "Leistung und Schatten Kopie" (auch als "diff Area" bezeichnet) der Verwendung einer Datei in einer Schatten Kopie hängt direkt mit der Menge der Änderungen im Inhalt der Datei zusammen, nachdem die Schatten Kopie erstellt wurde. Außerdem kann das Ausschließen von Dateien aus Schatten Kopien die Erstellung von Schatten Kopien verlangsamen.

Aus diesen Gründen sollte eine Datei nur dann aus Schatten Kopien ausgeschlossen werden, wenn Sie groß ist, eine bedeutende Änderung zwischen einer Schatten Kopie und der nächsten besteht und nicht gesichert werden muss.

Sie sollten nur Dateien ausschließen, die zu Ihrer Anwendung gehören.

Wenn VSS \_ Volsnap \_ attr \_ kein \_ AutoRecovery-Flag im schattenkopieskontext festgelegt ist, bedeutet dies, dass die automatische Wiederherstellung deaktiviert ist und keine Dateien aus der Schatten Kopie ausgeschlossen werden können. Weitere Informationen finden Sie unter [**\_ VSS \_ Volume \_ Snapshot \_ Attribute**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) Enumeration.

## <a name="using-the-addexcludefilesfromsnapshot-method"></a>Verwenden der addexcludefilesfromsnapshot-Methode

Mit einem VSS Writer können Dateien wie folgt aus einer Schatten Kopie ausgeschlossen werden:

1.  Aufrufen der [**IVssCreateWriterMetadataEx:: addexcludefilesfromsnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) -Methode, um die auszuschließenden Dateien zu melden.
2.  Löschen Sie in der [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) -Methode des Writers die Dateien aus der Schatten Kopie.

## <a name="using-the-filesnottosnapshot-registry-key"></a>Verwenden des Registrierungsschlüssels "filesnottosnapshot"

> [!Note]  
> Der Registrierungsschlüssel **FilesNotToSnapshot** sollte nur von Anwendungen verwendet werden. Benutzer, die versuchen, den Registrierungsschlüssel zu verwenden, erhalten Einschränkungen wie die folgenden:
>
> -   Es können keine Dateien aus einer Schattenkopie gelöscht werden, die unter Windows Server mit dem Feature „Vorherige Versionen“ erstellt wurden.
> -   Es können keine Dateien aus Schattenkopien für freigegebene Ordner gelöscht werden.
> -   Es können Dateien aus einer Schatten Kopie gelöscht werden, die mit dem Hilfsprogramm [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) erstellt wurde, aber es können keine Dateien aus einer Schatten Kopie gelöscht werden, die mit dem Hilfsprogramm [vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) erstellt wurde.
> -   Dateien werden auf Grundlage der besten Leistung aus einer Schattenkopie gelöscht. Das bedeutet, dass Sie nicht unbedingt gelöscht werden.

 

Eine VSS-Anwendung kann Dateien aus einer Schatten Kopie während der Erstellung von Schatten Kopien löschen, indem der folgende Registrierungsschlüssel verwendet wird:

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ backuprestore \\ filesnottosnapshot**

Dieser Registrierungsschlüssel enthält reg \_ \_ MultiSZ-Werte für jede Anwendung, deren Dateien ausgeschlossen werden können. Die Dateien werden durch voll qualifizierte Pfade angegeben, die den Platzhalter enthalten können \* .

In allen Fällen wird der Eintrag ignoriert, wenn keine Dateien vorhanden sind, die der Pfad Zeichenfolge entsprechen.

Nachdem eine Datei zum entsprechenden Wert des Registrierungsschlüssels hinzugefügt wurde, wird Sie aus der Schatten Kopie bei der Erstellung vom schattenkopieoptimierungs-Writer auf der Grundlage der besten Leistung gelöscht.

Wenn kein voll qualifizierter Pfad angegeben werden kann, kann ein Pfad auch mit der Variablen $USERPROFILE $ oder $AllVolumes $ impliziert werden. Beispiel:

-   $UserProfile $ \\ Directory- \\ Unterverzeichnis \\ Dateiname.\*
-   $AllVolumes $ \\ TemporaryFiles \\ \* .\*

Um den Pfad rekursiv zu machen, fügen Sie am Ende "/s" an. Beispiel:

-   $UserProfile $ \\ Directory \\ Unterverzeichnis \\ Dateiname. \* /s
-   $AllVolumes $ \\ TemporaryFiles \\ \* . \* /s

Die Variable $USERPROFILE $ bewirkt, dass die Pfad Zeichenfolge auf alle Benutzerprofile auf dem Computer angewendet wird. Die Benutzerprofile werden durch Untersuchen des folgenden Registrierungsschlüssels aufgelistet:

**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ProfileList**

Die Variable $AllVolumes $ bewirkt, dass die Pfad Zeichenfolge auf alle Schatten Kopien auf dem Computer angewendet wird. Angenommen, der Pfad lautet "$AllVolumes $ \\ TemporaryFiles \\ \* . \* /s ", und der Computer hat drei Volumes: C:, D: und e:. Wenn C: und E: den Pfad " \\ TemporaryFiles \\ " enthalten und Volume D: nur den Pfad "D: Data" enthält \\ \\ , wird die Verzeichnisstruktur "c: \\ TemporaryFiles" \\ aus den Schatten Kopien von "c:" gelöscht, und die Verzeichnisstruktur "E: \\ TemporaryFiles" \\ wird aus den Schatten Kopien von "e:" gelöscht.

Administratoren können die Erweiterung der Variablen "$USERPROFILE $" mithilfe des folgenden Registrierungsschlüssels deaktivieren:

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ VSS- \\ Einstellungen**

Geben Sie unter diesem Registrierungsschlüssel den Wert "disableuserprofileexpansion" für den Wert "Name", "reg \_ DWORD" für den Werttyp und einen Wert ungleich NULL für die Wertdaten an.

## <a name="about-the-filesnottobackup-registry-key"></a>Informationen zum Registrierungsschlüssel "FilesNotToBackup"

Der Registrierungsschlüssel **FilesNotToBackup** kann verwendet werden, um die Namen der Dateien und Verzeichnisse anzugeben, die von Sicherungs Anwendungen nicht gesichert oder wieder hergestellt werden sollen. Diese Dateien werden jedoch nicht aus Schatten Kopien ausgeschlossen. Weitere Informationen zu diesem Registrierungsschlüssel finden Sie unter [Registrierungsschlüssel und-Werte für die Sicherung und Wiederherstellung](../backup/registry-keys-for-backup-and-restore.md).

 

 
