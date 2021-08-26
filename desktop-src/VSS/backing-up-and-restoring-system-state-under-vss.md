---
description: Hinweis Dieses Thema gilt nur für Windows Server 2003 R2 und Windows Server 2003 mit Service Pack 1 (SP1).
ms.assetid: a192d9a7-1c65-4251-acb1-4df03ebfe910
title: Sichern und Wiederherstellen des Systemstatus in Windows Server 2003 R2 und Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4803acc5981cc74084789064bd276baa28b35c0ffe225e49d2b65ba5485e51a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032950"
---
# <a name="backing-up-and-restoring-system-state-in-windows-server-2003-r2-and-windows-server-2003-sp1"></a>Sichern und Wiederherstellen des Systemstatus in Windows Server 2003 R2 und Windows Server 2003 SP1

> [!Note]  
> Dieses Thema gilt nur für Windows Server 2003 R2 und Windows Server 2003 mit Service Pack 1 (SP1). Informationen zu anderen Betriebssystemversionen finden Sie unter [Sichern und Wiederherstellen des Systemstatus](locating-additional-system-files.md).

 

> [!Note]  
> Microsoft bietet keinen technischen Support für Entwickler oder IT-Mitarbeiter bei der Implementierung von Online-Systemstatuswiederherstellungen auf Windows (alle Releases). Informationen zur Verwendung von von Microsoft bereitgestellten APIs und Verfahren zum Implementieren von Online-Systemstatuswiederherstellungen finden Sie in den Communityressourcen, die im [MSDN Community Center verfügbar sind.](https://msdn.microsoft.com/community/default.aspx)

 

Beim Ausführen einer VSS-Sicherung oder -Wiederherstellung wird der Windows-Systemstatus als Sammlung mehrerer wichtiger Betriebssystemelemente und ihrer Dateien definiert. Diese Elemente sollten immer von Sicherungs- und Wiederherstellungsvorgängen als Einheit behandelt werden.

In Windows Server 2003 R2 und Windows Server 2003 mit SP1 gibt es keine Windows-API, die diese Objekte als eins behandelt. Daher wird empfohlen, dass anfordernde Personen über ein eigenes Systemstatusobjekt verfügen, damit sie diese Komponenten konsistent verarbeiten können.

Da VSS in Versionen von Windows ausgeführt wird, bei denen [*systemdateischutz (System File Protection,*](vssgloss-s.md) WFP) Systemstatusdateien vor Beschädigungen schützt, sind spezielle Schritte zum Sichern und Wiederherstellen des Systemstatus erforderlich.

Der Systemstatus umfasst Folgendes:

-   Alle durch WFP geschützten Dateien, Startdateien einschließlich ntldr-, ntdetect- und Leistungsindikatorkonfigurationen
-   Active Directory (ADSI) (auf Systemen, die Domänencontroller sind)
-   Der Systemvolumeordner (SYSVOL), der vom Dateireplikationsdienst (File Replication Service, FRS) repliziert wird (auf Systemen, die Domänencontroller sind)
-   Zertifikatserver (auf Systemen, die die Zertifizierungsstelle bereitstellen)
-   Clusterdatenbank (auf Systemen, die ein Knoten eines Windows sind)
-   Registrierungsdienst
-   COM+-Klassenregistrierungsdatenbank

Der Systemstatus kann in beliebiger Reihenfolge sichern werden.

Die Wiederherstellung des Systemstatus sollte jedoch zuerst Startdateien ersetzen und den Systemabschnitt (Hive) der Registrierung als letzten Schritt im Prozess commiten. Dies kann in der folgenden Reihenfolge erfolgen:

1.  Wiederherstellen der Startdateien.
2.  COM+-Klassenregistrierungsdatenbank
3.  Stellen Sie bei Bedarf SYSVOL-, Zertifikatserver- und Clusterdatenbanken wieder her.
4.  Stellen Sie Active Directory wieder her (falls erforderlich).
5.  Stellen Sie die Registrierung wieder auf.

Einige Systemdienste, z. B. die Zertifizierungsstelle, verfügen über herkömmliche VSS Writer und folgen den VSS-Sicherungs- und -Wiederherstellungsalgorithmen. Andere, z. B. die Registrierung, erfordern benutzerdefinierte Sicherungs- oder Wiederherstellungsvorgänge. Weitere Informationen finden Sie unter [Benutzerdefinierte Sicherungen und Wiederherstellungen.](custom-backups-and-restores.md)

## <a name="vss-backup-and-restores-of-boot-and-system-files"></a>VSS-Sicherung und -Wiederherstellungen von Start- und Systemdateien

Die Start- und Systemdateien sollten nur als einzelne Entität sichern und wiederhergestellt werden.

Ein An anfordernde Benutzer kann schattenkopiert Versionen dieser Dateien sicher verwenden und sollte sicherstellen, dass das Systemvolumen und das Startgerät [*schattenkopiert werden.*](vssgloss-s.md)

Die System- und Startdateien umfassen Folgendes:

-   Die wichtigsten Startdateien: <dl> NtLdr.exe  
    Boot.ini  
    NtDetect.com  
    NtBootDD.sys (falls vorhanden)  
    </dl>
-   The WFP service catalog file must be backed up prior to backing up the WFP files, and it is found under: <dl> %SystemRoot% \\ System32 \\ CatRoot \\ {F750E6C3-38EE-11D1-85E5-00C04FC295EE} </dl>
-Alle Dateien, [](vssgloss-s.md) die durch systemdateischutzgeschützt und von [**SfcGetNextProtectedFile**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) aufzählt werden (siehe VSS-Wiederherstellungsvorgänge von WFP-geschützten Dateien) Die Konfigurationsdateien des - Leistungsindikators: <dl> %SystemRoot% \\ System32 \\ Perf?00?. Dat  
    %SystemRoot% \\ System32 \\ Perf?00?. Bak </dl>
-Falls vorhanden, sollte die IIS-Metabasisdatei (Internet Information Server) in Sicherungs- und Wiederherstellungsvorgänge eingeschlossen werden, da sie den Zustand enthält, der von Microsoft Exchange und anderen Netzwerkanwendungen verwendet wird. Diese Datei befindet sich unter: <dl> %SystemRoot% \\ System32 \\ InetSrv \\ Metabase.bin </dl>
-   Wenn die IIS-Metabasisdatei sicherungsbasiert ist, sollten Schlüssel, mit denen Anwendungen bestimmte verschlüsselte Einträge lesen können, als Teil des Systemstatus wiederhergestellt werden. Die Dateien finden Sie unter: <dl> %SystemRoot% \\ System32 \\ Microsoft \\ Protect\\\*  
    %AllUsersProfile% \\ Microsoft Crypto RSA \\ \\ \\ MachineKeys\\\* </dl>
-Beim Sichern von Start- und Systemdateien kann es erforderlich sein, das DOS-Startgerät wie folgt zu bestimmen: Suchen Sie die Systempartition unter 1. **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\  \\ **Setup SystemPartition**.
    2.  Übergeben Sie die Systemstammumgebungsvariable (%SystemRoot%) an den Bereitstellungs-Manager, um den NT-Gerätenamen zu erhalten.

## <a name="vss-restore-operations-of-wfp-protected-files"></a>VSS-Wiederherstellungsvorgänge von WFP-geschützten Dateien

Der WFP-Dienst ist darauf ausgelegt, versehentliche oder unbeabsichtigte Ersetzungen von Systemdateien zu verhindern. Daher müssen besondere Schritte durchgeführt werden, um WFP-Daten wiederherzustellen.

Bedeutet, dass der WFP-Writer die **VSS \_ RME \_ RESTORE AT \_ \_ REBOOT-Wiederherstellungsmethode** angeben sollte, wenn er sein Writer-Metadatendokument definiert. Wenn eine Anfordernde feststellt, dass der WFP-Writer diese Wiederherstellungsmethode nicht angeben konnte, weist dies auf einen Writerfehler hin.

Eine Anfordernde sollte eine Wiederherstellungsmethode von **VSS \_ RME \_ RESTORE AT \_ \_ REBOOT** implementieren, indem sie die Win32-Funktion [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) mit dem **MOVEFILE DELAY UNTIL \_ \_ \_ REBOOT-Parameter** verwendet, um Systemdateien zu ersetzen. Die wiederhergestellten Dateien werden erst nach dem Systemneustart in die eigentlichen Systemdateiverzeichnisse kopiert. Das Überschreiben geschützter Systemdateien erfolgt nur, wenn der Wert des folgenden **REG WORD-Registrierungseintrags \_** auf 1 festgelegt ist:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager** \\ **AllowProtected Steuerelement** = 1

Dieser Wert muss vor jedem Start festgelegt werden, bei dem geschützte Dateien über [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) ersetzt und nach dem Neustart gelöscht werden.

Das Dllcache-Systemverzeichnis sollte ebenfalls gesichert oder wiederhergestellt werden, mit Sicherung und Wiederherstellung des Startvolumens, und es wird durch Untersuchen des **Registrierungseintrags REG \_ EXPAND \_ SZ** gefunden:

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **WinLogon** \\ **SfcDllCache**<dl> <dt>

                  Data type
</dt> <dd>                  REG \_ EXPAND \_ SZ</dd> </dl>

Der Inhalt des Dllcache-Verzeichnisses des Systems wird mithilfe des Systemdatei-Überprüfungsprogramm (SFC) an der Eingabeaufforderung neu erstellt:

-   Mit **der Option /SCANONCE** werden alle geschützten Dateien beim nächsten Systemstart überprüft.
-   Mit **der Option /SCANNOW** werden alle geschützten Dateien sofort überprüft.

Alle geschützten Dateien werden überprüft, und alle ungültigen Versionen werden sowohl im Verzeichnis als auch im DLLCache-Speicherort ersetzt.

Es gibt vier Dateien, die Teil des WFP sind und nicht mit den WFP-Dateien wiederhergestellt werden können:

<dl> Ctl3dv2.dll  
DtcSetup.exe  
NtDll.dll  
Smss.exe  
</dl>

Diese Dateien helfen beim Wiederherstellen der WFP-Dateien, und daher besteht eine zirkuläre Abhängigkeit. Derzeit gibt es keine Möglichkeit, diese Dateien wiederherzustellen, mit ausnahme der Neuinstallation Windows.

 

 
