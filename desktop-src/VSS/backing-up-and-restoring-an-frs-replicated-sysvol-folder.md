---
description: In diesem Thema wird erläutert, wie Sie bestimmen, ob ein SYSVOL-Ordner von DFSR oder FSR repliziert wird, und wie Sie einen FRS-replizierten SYSVOL-Ordner sichern und wiederherstellen.
ms.assetid: 32d8a5bd-eeb4-4db6-8129-b5cd3508a7e5
title: Sichern und Wiederherstellen eines FRS-Replicated SYSVOL-Ordners
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d841f64bab62114824847f91876ba8bbffbb0166db942c0f3cb9d010b72f106
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124600"
---
# <a name="backing-up-and-restoring-an-frs-replicated-sysvol-folder"></a>Sichern und Wiederherstellen eines FRS-Replicated SYSVOL-Ordners

Der Ordner Systemvolume (SYSVOL) bietet einen Standardspeicherort zum Speichern wichtiger Elemente Gruppenrichtlinie [Objekten](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)) und Skripts. Auf jedem Domänencontroller in einer Domäne ist eine Kopie des Ordners SYSVOL vorhanden. Der SYSVOL-Ordner wird entweder von verteiltes Dateisystem [Replikation (DFSR)](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) oder dem [Dateireplikationsdienst (File Replication Service, FRS) repliziert.](/previous-versions/windows/it-pro/windows-server-2003/cc781582(v=ws.10)) In diesem Thema wird erläutert, wie Sie bestimmen, ob ein SYSVOL-Ordner von DFSR oder FSR repliziert wird, und wie Sie einen FRS-replizierten SYSVOL-Ordner sichern und wiederherstellen.

FRS kann SYSVOL-Inhalte auf andere Domänencontroller innerhalb der Domäne kopieren. FRS überwacht den SYSVOL-Ordner und repliziert die geänderte Datei automatisch in die SYSVOL-Ordner auf den anderen Domänencontrollern in der Domäne, wenn eine Änderung an einer im ORDNER SYSVOL gespeicherten Datei auftritt.

> [!Note]  
> Nur die Gruppenrichtlinie-Vorlage wird repliziert, indem der Inhalt des SYSVOL-Ordners repliziert wird. Der Gruppenrichtlinie container wird über die Active Directory-Replikation repliziert. Damit Gruppenrichtlinie funktioniert, müssen sowohl die Gruppenrichtlinie-Vorlage als auch der Gruppenrichtlinie-Container auf einem Domänencontroller verfügbar sein.

 

In diesem Thema werden die folgenden Themen behandelt:

-   [Bestimmen, ob der SYSVOL-Ordner eines Domänencontrollers von DFSR oder FRS repliziert wird](#determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs)
-   [Sichern eines DFSR-Replicated SYSVOL-Ordners](#backing-up-a-dfsr-replicated-sysvol-folder)
-   [Sichern eines FRS-Replicated SYSVOL-Ordners auf einer Windows Server 2008- oder Windows Server 2003-Domäne](#backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain)
-   [Frs Writer-Beispielmetadatendokument](#sample-frs-writer-metadata-document)
-   [Festlegen von Registrierungsschlüsseln für eine Wiederherstellung eines FRS-Replicated SYSVOL-Ordners](#setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder)
-   [Ausführen einer nicht authentifizierten Wiederherstellung eines FRS-Replicated SYSVOL-Ordners](#performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder)
-   [Ausführen einer autoritativen Wiederherstellung eines FRS-Replicated SYSVOL-Ordners](#performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder)

## <a name="determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs"></a>Bestimmen, ob der SYSVOL-Ordner eines Domänencontrollers von DFSR oder FRS repliziert wird

In der folgenden Tabelle wird zusammengefasst, wie Sie bestimmen, ob der SYSVOL-Ordner eines Domänencontrollers von [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) oder FRS repliziert wird.

| Wenn der Domänencontroller ausgeführt wird                                                                                                                  | SYSVOL wird von repliziert. |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| Windows Server 2008 + Domänenfunktionsebene von Windows Server 2008 + [SYSVOL-Migration](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) abgeschlossen | DFSR                    |
| Windows Server 2008 + Domänenfunktionsebene unter Windows Server 2008                                                                              | Frs                     |
| Windows Server 2003                                                                                                                                  | Frs                     |



 

Wenn die Funktionsebene der Domäne Windows Server 2008 ist und die Domäne der [SYSVOL-Migration](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx)unterzogen wurde, wird [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) zum Replizieren des SYSVOL-Ordners verwendet. [](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10)) Wenn der erste Domänencontroller in der Domäne direkt auf die Windows Server [](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))2008-Funktionsebene hinaus 2008 promotet wurde, wird DFSR automatisch für die SYSVOL-Replikation verwendet. In solchen Fällen ist keine Migration der SYSVOL-Replikation von FRS zu DFSR erforderlich. Wenn die Domäne auf Windows Server 2008-Funktionsebene aktualisiert wurde, wird FRS für die SYSVOL-Replikation verwendet, bis der Migrationsprozess von FRS zu DFSR abgeschlossen ist. [](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10)) [](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx)

Um zu bestimmen, ob DFSR oder FRS auf einem Domänencontroller verwendet wird, auf dem Windows Server 2008 ausgeführt wird, überprüfen Sie den Wert des SysVols Migrating Sysvols LocalState registry-Unterschlüssels des **HKEY \_ LOCAL \_** \\ **MACHINE-Systems** \\ **CurrentControlSet** \\ **Services** \\ **DFSR** Parameters \\  \\ **SysVols** \\ **Migrating Sysvols** \\ **LocalState** registry . Wenn dieser Registrierungsunterschlüssel vorhanden ist und sein Wert auf 3 (ELIMINATED) festgelegt ist, wird [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) verwendet. Wenn der Unterschlüssel nicht vorhanden ist oder über einen anderen Wert verfügt, wird FRS verwendet.

## <a name="backing-up-a-dfsr-replicated-sysvol-folder"></a>Sichern eines DFSR-Replicated SYSVOL-Ordners

Wenn der SYSVOL-Ordner von [DFSR repliziert](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)wird, kann der DFSR VSS Writer zum Sichern verwendet werden. Weitere Informationen zum DFSR VSS Writer finden Sie unter [DFSR Replicated Folders](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders).

## <a name="backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain"></a>Sichern eines FRS-Replicated SYSVOL-Ordners auf einer Windows Server 2008- oder Windows Server 2003-Domäne

Auf einem Domänencontroller, auf dem Windows Server 2008 oder Windows Server 2003 ausgeführt wird, ist die VSS-Infrastruktur vorhanden. Daher kann der FRS VSS Writer zum Sichern des SYSVOL-Ordners und der FRS-Komponenten verwendet werden.

Das Writer-Metadatendokument des FRS VSS-Writers enthält Informationen zum Speicherort des Ordners SYSVOL und zu den Ausschlusslisten für den Writer. Basierend auf diesen Informationen kann eine VSS-Sicherungsanwendung (Anfordernde) den SYSVOL-Ordner mithilfe der regulären VSS-basierten Sicherungstechniken sichern.

Das Writer-Metadatendokument enthält Informationen über den Writer, die Daten, die der Writer besitzt, und wie diese Daten wiederhergestellt werden. Dies ist ein schreibgeschütztes Dokument, das von der Sicherungsanwendung abgerufen werden kann, bevor eine Sicherung erstellt wird. Das [DiskShadow-Tool](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) kann zum Anzeigen des Writermetadatendokuments des FRS VSS-Writer verwendet werden. Der [Befehl DiskShadow list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) enthält Informationen zu den Writern, die im System vorhanden sind. Diese Liste enthält Informationen zum FRS Writer auf Domänencontrollern, die FRS für die SYSVOL-Replikation verwenden, oder auf Dateiservern, die FRS für die Replikation von [DFS-Linkzielen verwenden.](/previous-versions/windows/it-pro/windows-server-2003/cc782417(v=ws.10))

Der folgende Abschnitt Frs Writer-Metadatendokument zeigt ein Frs Writer-Beispielmetadatendokument für einen Domänencontroller mit dem Ordner SYSVOL auf D: \\ Windows \\ Sysvol. Der im Abschnitt "Ausgeschlossene Dateien" angezeigte Pfad ist identisch mit dem Pfad, der beim Abfragen des SysVol-Registrierungsschlüssels des **Netlogon-Diensts** ermittelt wurde:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NetLogon** \\ **Parameters** \\ **SysVol**

Die einzige Ausnahme von dieser Regel tritt auf, wenn sich der Domänencontroller im Zustand UMGELEITET der [SYSVOL-Migration befindet.](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) In diesem Zustand melden die Writer, die sowohl FRS als auch dem [DFSR-Dienst](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) entspricht, ihre jeweiligen Kopien des SYSVOL-Ordners. Allerdings ist die Kopie des SYSVOL-Ordners (in der Regel ein Ordner namens SYSVOL DFSR) des [DFSR-Diensts](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) der, der vom Domänencontroller gemeinsam genutzt wird. Auf diesen Pfad verweist der \_ **SysVol-Registrierungsschlüssel.**

Der FRS VSS Writer erfordert eine benutzerdefinierte Wiederherstellungsmethode. Dies bedeutet, dass beim Wiederherstellen von Dateien, die von FRS repliziert werden, bestimmte benutzerdefinierte Schritte ausgeführt werden müssen. Weitere Informationen finden Sie unter Ausführen einer nicht authentifizierten Wiederherstellung eines FRS-Replicated SYSVOL-Ordners.

> [!Note]  
> Systemstatussicherungen für Windows-Domänencontroller enthalten nicht die FRS-Datenbank, die Zustandsinformationen für den FRS-Dienst in Bezug auf die Dateien im Ordner SYSVOL und andere Inhaltssätze verwaltet. Die [FRS-Datenbank,](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) Debugprotokolle, Stagingbereichsdateien und Dateien im bereits vorhandenen Datenordner werden von einer Systemstatussicherung ausgeschlossen. Die folgende FRS Writer-Beispielspezifikation enthält die Ausschlussliste im Abschnitt "Ausgeschlossene Dateien".

 

## <a name="sample-frs-writer-metadata-document"></a>Frs Writer-Beispielmetadatendokument

Im Folgenden finden Sie ein Frs Writer-Beispielmetadatendokument für einen Domänencontroller, dessen SYSVOL-Ordnerpfad D: \\ Windows \\ Sysvol ist.

``` syntax
* WRITER "FRS Writer"
    - Writer ID   = {d76f5a28-3092-4589-ba48-2958fb88ce29}
    - Writer Instance ID = {07ae58e5-6977-4e34-9dfe-399bbd2cbe40}
    - Supports restore events = FALSE
    - Writer restore conditions = VSS_WRE_NEVER
    - Restore method = VSS_RME_CUSTOM
    - Requires reboot after restore = FALSE

    - Excluded files:
       - Exclude: Path = d:\windows\ntfrs\jet, Filespec = *
       - Exclude: Path = d:\Windows\debug\NtFrs, Filespec = NtFrs*
       - Exclude: Path = d:\windows\sysvol\domain\DO_NOT_REMOVE_NtFrs_PreInstall_Directory, Filespec = *
       - Exclude: Path = d:\windows\sysvol\domain\NtFrs_PreExisting___See_EventLog, Filespec = *
       - Exclude: Path = d:\windows\sysvol\staging\domain, Filespec = NTFRS_*

    - Component "FRS Writer:\SYSVOL\da45368c-b2d3-4cf0-bdc338a2cde15a7b"
       - Name: 'da45368c-b2d3-4cf0-bdc338a2cde15a7b'
       - Logical Path: 'SYSVOL'
       - Full Path: '\SYSVOL\da45368c-b2d3-4cf0-bdc338a2cde15a7b'
       - Caption: ''
       - Type: VSS_CT_FILEGROUP [2]
       - Is Selectable: 'TRUE'
       - Is top level: 'TRUE'
       - Notify on backup complete: 'TRUE'
       - Components:
       - File List: Path = d:\windows\sysvol, Filespec = *
       - Affected paths by this component:
         - d:\windows\sysvol
       - Affected volumes by this component:
         - \\?\Volume{da897ba5-5840-11db-93c1-806e6f6e6963}\ [D:\]
       - Component Dependencies:
```

## <a name="setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder"></a>Festlegen von Registrierungsschlüsseln für eine Wiederherstellung eines FRS-Replicated SYSVOL-Ordners

Mit **dem Registrierungsschlüssel "AuthFlags"** werden autoritative oder nicht authentifizierte Wiederherstellungen auf FRS-Mitgliedern von DFS- oder SYSVOL-Replikatgruppen erstellt. Der globale (computerweite) **MüssenFlags-Registrierungsschlüssel** enthält REG DWORD-Werte und befindet sich an folgendem \_ Speicherort in der Registrierung:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** Parameters \\  \\ **Backup/Restore** \\ **Process at Startup**

Die gängigsten Werte für den **-Registrierungsschlüssel sind:**

-   D2, auch als Wiederherstellung im nicht authentifizierten Modus bezeichnet.
-   D4, auch als Wiederherstellung im autoritativen Modus bezeichnet.

Es gibt globale und replikatgruppenspezifische **MüssenFlags-Registrierungsschlüssel.** Durch das Festlegen des **globalen Registrierungsschlüssels "Führungsflags"** werden alle Replikatgruppen, die das Mitglied enthält, erneut initialisiert. Dieser globale Schlüssel sollte festgelegt werden, wenn der Server nur eine Replikatgruppe enthält oder wenn die replikatgruppen, die er enthält, relativ wenige und kleine Replikatgruppen sind. Wenn der Server z. B. ein Domänencontroller ist, der keine Inhaltssätze hosten kann, die mithilfe von FRS repliziert werden, mit einem anderen Namen als dem SYSVOL-Ordner, kann der globale **Registrierungsschlüssel "BirFlags"** festgelegt werden.

Der globale **MussFlags-Registrierungsschlüssel** befindet sich an folgendem Speicherort in der Registrierung:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** Parameters \\ **Backup/Restore** \\ **Process** at \\ **Startup**

Im Gegensatz zum globalen **MüssenFlags-Schlüssel** ermöglicht der Replikatgruppen-spezifische **Schlüssel "Replikatgruppe"** die erneute Initialisierung diskreter, einzelner Replikatgruppen, sodass fehlerfreie Replikationssätze intakt bleiben können.

Replikatgruppenspezifische **MüssenFlags-Registrierungsschlüssel** können gefunden werden, indem die GUID für diese bestimmte Replikatgruppe bestimmt wird.

Im folgenden Verfahren wird beschrieben, wie Ermittelt wird, welche GUID einer bestimmten Replikatgruppe entspricht, und wie eine Wiederherstellung konfiguriert wird.

**So bestimmen Sie, welche GUID einer bestimmten Replikatgruppe entspricht, und konfigurieren sie eine Wiederherstellung**

1.  Beenden Sie den FRS-Dienst.
2.  So bestimmen Sie die GUID, die eine bestimmte Replikatgruppe darstellt:
    1.  Suchen Sie den folgenden Schlüssel in der Registrierung.

        **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **Parameters Replica** \\ **Sets**

    2.  Unter dem **Unterschlüssel Replikatgruppen** befinden sich mindestens ein Unterschlüssel, die jeweils durch eine GUID identifiziert werden.
    3.  Der **Stammwert der Replikatgruppe** für jede GUID ist ein Dateisystempfad, der die Replikatgruppe angibt, die durch diese GUID dargestellt wird.
    4.  Iterieren Sie diese Liste der GUIDs, bis die gewünschte Replikatgruppe gefunden wird. Notieren Sie sich die entsprechende GUID.

3.  Suchen Sie den folgenden Unterschlüssel in der Registrierung:

    **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **Parameters Cumulative** Replica \\ **Sets**

4.  Suchen Sie unter diesem Unterschlüssel nach der gleichen GUID, die Sie sich in Schritt 2 notiert haben. Erstellen Sie unterhalb des GUID-Unterschlüssels einen Eintrag für den **Schlüssel "KeyFlags".**
5.  Starten Sie den FRS-Dienst neu.

## <a name="performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder"></a>Ausführen einer nicht authentifizierten Wiederherstellung eines FRS-Replicated SYSVOL-Ordners

Die nicht authentifizierte Wiederherstellung ist die gängigste Methode zum erneuten Initialisieren der SYSVOL-Replikation auf einzelnen Domänencontrollern. Domänencontroller, die nicht authentifiziert wiederhergestellt werden, müssen über eingehende Verbindungen von anderen funktionierenden Domänencontrollern verfügen, die an der Active Directory- und FRS-Replikation teilnehmen. In einer großen Bereitstellungsumgebung, die aus vielen Domänencontrollern besteht, können die verbleibenden Domänencontroller mithilfe einer nicht authentifizierten Moduswiederherstellung unter den folgenden Bedingungen wiederhergestellt werden:

-   Es muss mindestens ein bekanntes gutes Replikatmitglied (ein Domänencontroller mit einem fehlerfreien SYSVOL-Ordner) sein.
-   Die anderen Domänencontroller müssen in der Reihenfolge der direkten Replikationspartner erneut initialisiert werden.

Im folgenden Verfahren wird beschrieben, wie sie eine nicht authentifizierte Wiederherstellung durchführen.

**So führen Sie eine nicht authentifizierte Wiederherstellung aus**

1.  Beenden Sie den FRS-Dienst.
2.  Stellen Sie die gesicherten Daten im Ordner SYSVOL wieder her.
3.  Konfigurieren Sie den **BurFlags-Registrierungsschlüssel,** indem Sie den Wert des folgenden Registrierungsschlüssels auf den DWORD-Wert D2 festlegen.

    **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **Parameters** \\ **Backup/Restore** Process at \\ **Startup** \\ **BurFlags**

4.  Starten Sie den FRS-Dienst neu.

Wenn der FRS-Dienst neu gestartet wird, werden die folgenden Aktionen ausgeführt:

-   Der Wert des **BurFlags-Registrierungsschlüssels** wird auf 0 (null) zurückgesetzt.
-   Dateien in den erneut initialisierten FRS-Ordnern werden in einen bereits vorhandenen Ordner verschoben.
-   Ereignis 13565 wird im FRS-Ereignisprotokoll protokolliert, um zu signalisieren, dass eine nicht authentifizierte Wiederherstellung gestartet wurde.
    > [!Note]  
    > FRS-Ereigniscodes sind in "Fehlercodes des FRS-Ereignisprotokolls" im Knowledge Base Hilfe und Support unter dokumentiert. <https://go.microsoft.com/fwlink/p/?linkid=117779>

     

-   Die FRS-Datenbank wird neu erstellt.
-   Der Member führt einen ersten Join der Replikatgruppe von einem Upstreampartner oder von dem Computer aus, der im Registrierungsschlüssel des **übergeordneten Replikatsatzes** angegeben ist, wenn für SYSVOL-Replikatgruppen ein übergeordnetes Element angegeben wurde.
-   Der neu initialisierte Computer führt eine vollständige Replikation der betroffenen Replikatgruppen aus, wenn der entsprechende Replikationszeitplan beginnt.
-   Wenn der Prozess abgeschlossen ist, wird ein Ereignis 13516 protokolliert, um zu signalisieren, dass FRS betriebsbereit ist. Wenn das Ereignis nicht protokolliert wird, liegt ein Problem mit der FRS-Konfiguration vor.

> [!Note]  
> Die Platzierung von Dateien im [bereits vorhandenen](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) Ordner auf erneut initialisierten Membern ist ein Schutz in FRS, der dazu dient, versehentlichen Datenverlust zu verhindern. Alle Dateien, die für das Replikat bestimmt sind und nur im lokalen bereits vorhandenen Ordner vorhanden sind und nach der ersten Replikation repliziert wurden, können dann in den entsprechenden Ordner kopiert werden. Wenn die ausgehende Replikation erfolgt ist, können Dateien im bereits vorhandenen Ordner gelöscht werden, um zusätzlichen Speicherplatz auf dem Laufwerk frei zu machen.

 

## <a name="performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder"></a>Ausführen einer autoritativen Wiederherstellung eines FRS-Replicated SYSVOL-Ordners

Autoritative Wiederherstellungen werden als letzte Möglichkeit in kritischen Situationen verwendet, z. B. bei Abweichungen der Daten im Inhaltssatz, die durch Verzeichniskonflikte verursacht werden. Beispielsweise kann eine autoritative Wiederherstellung erforderlich sein, um eine FRS-Replikatgruppe wiederherzustellen, bei der die Replikation vollständig beendet wurde und eine Neuerstellung von Grund auf erforderlich ist.

Wenn Sie eine autoritative Wiederherstellung des SYSVOL-Ordners durchführen müssen, beachten Sie, dass es sich um einen sehr komplizierten Prozess handelt. Umfassende Richtlinien, in denen die Vorgänge beschrieben werden, die für eine autoritative Wiederherstellung des Inhalts des SYSVOL-Ordners ausgeführt werden müssen, finden Sie im Hilfe- und Support-Knowledge Base unter unter "How to rebuild the SYSVOL tree and its content in a domain" (Neu erstellen der SYSVOL-Struktur und deren Inhalt in einer Domäne). <https://go.microsoft.com/fwlink/p/?linkid=117780>

Die folgenden Anforderungen müssen erfüllt sein, bevor eine autoritative FRS-Wiederherstellung ausgeführt wird:

1.  Der FRS-Dienst muss auf allen Downstreamreplikationspartnern (direkt und transitiv) für den erneut initialisierten SYSVOL-Ordner deaktiviert werden, bevor die autoritative Wiederherstellung konfiguriert wurde.
2.  Die Ereignisse 13553 und 13516 wurden im FRS-Ereignisprotokoll protokolliert. Diese Ereignisse deuten darauf hin, dass die Mitgliedschaft der SYSVOL-Replikatgruppe auf dem Domänencontroller eingerichtet wurde, der für die autoritative Wiederherstellung konfiguriert ist.
    > [!Note]  
    > FRS-Ereigniscodes sind in "Fehlercodes des FRS-Ereignisprotokolls" im Knowledge Base Hilfe und Support unter dokumentiert. <https://go.microsoft.com/fwlink/p/?linkid=117779>

     

3.  Der Domänencontroller, der für die autoritative Wiederherstellung konfiguriert ist, ist für alle SYSVOL-Daten autoritativ konfiguriert, die auf den verbleibenden Domänencontrollern repliziert werden sollen.
4.  Alle anderen Partner in der Replikatgruppe müssen mit einer nicht authentifizierten Wiederherstellung erneut initialisiert werden.

 

 
