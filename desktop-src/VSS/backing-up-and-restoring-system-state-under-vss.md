---
description: Hinweis Dieses Thema gilt nur für Windows Server 2003 R2 und Windows Server 2003 mit Service Pack 1 (SP1).
ms.assetid: a192d9a7-1c65-4251-acb1-4df03ebfe910
title: Sichern und Wiederherstellen des System Status in Windows Server 2003 R2 und Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2fdb50e3f719a5208c2894f5659f927bcc922d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960737"
---
# <a name="backing-up-and-restoring-system-state-in-windows-server-2003-r2-and-windows-server-2003-sp1"></a>Sichern und Wiederherstellen des System Status in Windows Server 2003 R2 und Windows Server 2003 SP1

> [!Note]  
> Dieses Thema gilt nur für Windows Server 2003 R2 und Windows Server 2003 mit Service Pack 1 (SP1). Informationen zu anderen Betriebssystemversionen finden Sie unter [Sichern und Wiederherstellen des Systemstatus](locating-additional-system-files.md).

 

> [!Note]  
> Microsoft bietet keinen technischen Support für Entwickler oder IT-Experten für die Implementierung von Online-Systemstatus Wiederherstellungen unter Windows (alle Versionen). Weitere Informationen zur Verwendung von von Microsoft bereitgestellten APIs und Prozeduren zum Implementieren von Online-Systemstatus Wiederherstellungen finden Sie in den Communityressourcen im [MSDN Community Center](https://msdn.microsoft.com/community/default.aspx).

 

Beim Ausführen einer VSS-Sicherung oder-Wiederherstellung wird der Windows-Systemstatus als eine Sammlung mehrerer wichtiger Betriebssystem Elemente und der zugehörigen Dateien definiert. Diese Elemente sollten immer von Sicherungs-und Wiederherstellungs Vorgängen als Einheit behandelt werden.

In Windows Server 2003 R2 und Windows Server 2003 mit SP1 gibt es keine Windows-API, mit der diese Objekte als eins behandelt werden. Daher wird empfohlen, dass die anfordernde Personen über ein eigenes Systemstatus Objekt verfügen, damit diese Komponenten konsistent verarbeitet werden können.

Da VSS unter Versionen von Windows ausgeführt wird, auf denen der [*Systemdatei Schutz*](vssgloss-s.md) (WFP) Systemstatus Dateien vor Beschädigungen schützt, sind spezielle Schritte erforderlich, um den Systemstatus zu sichern und wiederherzustellen.

Der System Status besteht aus den folgenden Elementen:

-   Alle durch WFP geschützten Dateien, Startdateien einschließlich NTLDR-, ntdetect-und leistungsindikatorenkonfigurationen
-   Die Active Directory (ADSI) (auf Systemen, die Domänen Controller sind)
-   Der Ordner "System Volume" (SYSVOL), der vom Datei Replikations Dienst (File Replication Service, FRS) repliziert wird (auf Systemen mit Domänen Controllern
-   Zertifikat Server (auf Systemen, die eine Zertifizierungsstelle bereitstellen)
-   Cluster Datenbank (auf Systemen, die ein Knoten eines Windows-Clusters sind)
-   Registrierungsdienst
-   Com+-Klassen Registrierungsdatenbank

Der Systemstatus kann in beliebiger Reihenfolge gesichert werden.

Allerdings sollte die Wiederherstellung des Systemstatus zuerst Startdateien ersetzen und den System Abschnitt (Hive) der Registrierung als letzten Schritt im Prozess ausführen und kann in der folgenden Reihenfolge vorkommen:

1.  Stellen Sie die Startdateien wieder her.
2.  Com+-Klassen Registrierungsdatenbank
3.  Stellen Sie SYSVOL, den Zertifikat Server und die Cluster Datenbanken (falls erforderlich) wieder her.
4.  Restore Active Directory (falls erforderlich).
5.  Stellen Sie die Registrierung wieder her.

Einige Systemdienste, z. b. die Zertifizierungsstelle, haben konventionelle VSS-Writer und befolgen die VSS-Sicherungs-und-Wiederherstellungs Algorithmen. Andere, wie z. b. die Registrierung, erfordern benutzerdefinierte Sicherungs-oder Wiederherstellungs Vorgänge. Weitere Informationen finden Sie unter [benutzerdefinierte Sicherungen und](custom-backups-and-restores.md)Wiederherstellungen.

## <a name="vss-backup-and-restores-of-boot-and-system-files"></a>VSS-Sicherung und-Wiederherstellung von Start-und System Dateien

Die Start-und Systemdateien sollten nur als einzelne Entität gesichert und wieder hergestellt werden.

Ein Anforderer kann auf sichere Weise schattenkopierte Versionen dieser Dateien verwenden und muss sicherstellen, dass das System Volume und das Startgerät als [*Schatten kopiert*](vssgloss-s.md)werden.

Die System-und Startdateien umfassen Folgendes:

-   Die Core-Startdateien: <dl> NtLdr.exe  
    Boot.ini  
    NtDetect.com  
    NtBootDD.sys (sofern vorhanden)  
    </dl>
-   The WFP service catalog file must be backed up prior to backing up the WFP files, and it is found under: <dl> % SystemRoot% System32-Stammverzeichnis \\ \\ \\ {F750E6C3-38EE-11d1-85E5-00C04FC295EE} </dl>
-   Alle Dateien, die vom [*System Datei Schutz*](vssgloss-s.md) geschützt und durch [**SfcGetNextProtectedFile**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) aufgelistet werden (siehe VSS-Wiederherstellungs Vorgänge von WFP-geschützten Dateien) -   : <dl> % Systemroot% \\ system32 \\ perf? 00?. Hütte  
    % Systemroot% \\ system32 \\ perf? 00?. BAK </dl>
-   Falls vorhanden, sollte die Internet Information Server (IIS)-Metabasisdatei in Sicherungs-und Wiederherstellungs Vorgänge eingeschlossen werden, da Sie einen von Microsoft Exchange und anderen Netzwerkanwendungen verwendeten Status enthält. Diese Datei befindet sich unter: <dl> % Systemroot% \\ system32 \\ inetsrv \\ MetaBase. bin </dl>
-   Wenn die IIS-Metabasisdatei gesichert ist, sollten Schlüssel zum Aktivieren von Anwendungen zum Lesen bestimmter verschlüsselter Einträge als Teil des Systemstatus wieder hergestellt werden. Die Dateien finden Sie unter: <dl> % Systemroot% \\ system32 \\ Microsoft \\ Protect\\\*  
    % ALLUSERSPROFILE% \\ Microsoft \\ Crypto \\ RSA \\ MachineKeys\\\* </dl>
-Beim Sichern von Start-und Systemdateien ist es möglicherweise erforderlich, das DOS-Startgerät zu ermitteln, indem Sie die folgenden Schritte ausführen: 1. Suchen der Systempartition unter **HKEY \_ local \_ Machine** \\ **System** \\ **Setup** \\ **Systempartition**.
    2.  Übergeben Sie die System Stamm-Umgebungsvariable (% SystemRoot%). zum Abrufen des NT-Geräte namens an den Mount Manager.

## <a name="vss-restore-operations-of-wfp-protected-files"></a>VSS-Wiederherstellungs Vorgänge von WFP-geschützten Dateien

Der WFP-Dienst ist so konzipiert, dass die versehentliche oder schrittweise Ersetzung von Systemdateien verhindert wird. Daher müssen spezielle Schritte ausgeführt werden, um WFP-Daten wiederherzustellen.

Der bedeutet, dass der WFP-Writer beim Definieren seines Writer-Metadatendokuments die **VSS- \_ RME- \_ Wiederherstellung \_ beim \_** Wiederherstellen des Dokuments angeben soll. Wenn ein Anforderer feststellt, dass der WFP-Writer diese Wiederherstellungsmethode nicht angeben konnte, weist dies auf einen Writer-Fehler hin.

Ein Anforderer muss beim Neustart eine Wiederherstellungsmethode der **VSS- \_ RME- \_ Wiederherstellung \_ \_** implementieren, indem er die Win32-Funktion " [**muvefileex**](/windows/win32/api/winbase/nf-winbase-movefileexa) " mit dem Parameter "verzögertes Verschieben von" in " **muvefile \_ \_ \_** " Die wiederhergestellten Dateien werden erst nach dem Neustart des Systems in die eigentlichen System Dateiverzeichnisse kopiert. Das Überschreiben geschützter Systemdateien findet nur statt, wenn der Wert des folgenden Registrierungs Eintrags von **reg \_ Word** auf 1 festgelegt ist:

**HKEY \_ Lokaler \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager** \\ **allowprotectedrenames** = 1

Dieser Wert muss vor jedem Start festgelegt werden, bei dem geschützte Dateien über " [**muvefileex**](/windows/win32/api/winbase/nf-winbase-movefileexa) " ersetzt und nach dem Neustart gelöscht werden.

Das System-dllcache-Verzeichnis sollte auch mit der Sicherung und Wiederherstellung des Start Datentyps gesichert oder wieder hergestellt werden, und es befindet sich in dem Registrierungs Eintrag **reg \_ Expand \_ SZ** :

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **sfcdllcache**<dl> <dt>

                  Data type
</dt> <dd>                  REG \_ Expand \_ SZ</dd> </dl>

Der Inhalt des Verzeichnisses System dllcache wird mithilfe der Systemdatei Prüfung (SFC) an der Eingabeaufforderung neu erstellt:

-   Die Option **/scanonce** scannt alle geschützten Dateien beim nächsten Systemstart.
-   Die Option **/scannow** scannt alle geschützten Dateien sofort.

Alle geschützten Dateien werden überprüft, und alle ungültigen Versionen werden im Verzeichnis und im Dllcache-Speicherort ersetzt.

Es gibt vier Dateien, die Teil des WFP sind und nicht mit den WFP-Dateien wieder hergestellt werden können:

<dl> Ctl3dv2.dll  
DtcSetup.exe  
NtDll.dll  
Smss.exe  
</dl>

Diese Dateien helfen bei der Wiederherstellung der WFP-Dateien, sodass eine zirkuläre Abhängigkeit vorliegt. Zurzeit gibt es keine Möglichkeit, diese Dateien wiederherzustellen, außer um Windows neu zu installieren.

 

 
