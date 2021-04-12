---
description: In diesem Thema wird erläutert, wie Sie feststellen können, ob ein SYSVOL-Ordner von DFSR oder FSR repliziert wird, und es wird erläutert, wie Sie einen FRS-replizierten SYSVOL-Ordner sichern
ms.assetid: 32d8a5bd-eeb4-4db6-8129-b5cd3508a7e5
title: Sichern und Wiederherstellen eines FRS-Replicated SYSVOL-Ordners
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea83ccbc156182a4a3b84c758cb22153f4f7110f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347228"
---
# <a name="backing-up-and-restoring-an-frs-replicated-sysvol-folder"></a>Sichern und Wiederherstellen eines FRS-Replicated SYSVOL-Ordners

Der Ordner "System Volume" (SYSVOL) ist ein Standard Speicherort zum Speichern wichtiger Elemente von [Gruppenrichtlinie](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)) Objekten und Skripts. Auf jedem Domänen Controller in einer Domäne ist eine Kopie des Ordners SYSVOL vorhanden. Der SYSVOL-Ordner wird entweder von [verteiltes Dateisystem Replikation (DFSR)](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) oder vom [Datei Replikations Dienst (File Replication Service, FRS)](/previous-versions/windows/it-pro/windows-server-2003/cc781582(v=ws.10))repliziert. In diesem Thema wird erläutert, wie Sie feststellen können, ob ein SYSVOL-Ordner von DFSR oder FSR repliziert wird, und es wird erläutert, wie Sie einen FRS-replizierten SYSVOL-Ordner sichern

FRS kann SYSVOL-Inhalte auf andere Domänen Controller innerhalb der Domäne kopieren. FRS überwacht den SYSVOL-Ordner. Wenn eine Änderung an einer im SYSVOL-Ordner gespeicherten Datei vorgenommen wird, wird die geänderte Datei von FRS automatisch in den SYSVOL-Ordnern auf den anderen Domänen Controllern in der Domäne repliziert.

> [!Note]  
> Nur die Gruppenrichtlinie Vorlage wird repliziert, indem der Inhalt des Ordners "SYSVOL" repliziert wird. Der Gruppenrichtlinie-Container wird durch Active Directory Replikation repliziert. Damit Gruppenrichtlinie erfolgreich funktioniert, müssen sowohl die Gruppenrichtlinie Vorlage als auch der Gruppenrichtlinie Container auf einem Domänen Controller verfügbar sein.

 

In diesem Thema werden die folgenden Themen behandelt:

-   [Ermitteln, ob der SYSVOL-Ordner eines Domänen Controllers von DFSR oder FRS repliziert wird](#determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs)
-   [Sichern eines DFSR-Replicated SYSVOL-Ordners](#backing-up-a-dfsr-replicated-sysvol-folder)
-   [Sichern eines FRS-Replicated SYSVOL-Ordners in einer Windows Server 2008-oder Windows Server 2003-Domäne](#backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain)
-   [Metadatendokument für das Beispiel-FRS](#sample-frs-writer-metadata-document)
-   [Festlegen von Registrierungs Schlüsseln für eine Wiederherstellung eines FRS-Replicated SYSVOL-Ordners](#setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder)
-   [Ausführen einer nicht autoritativen Wiederherstellung eines FRS-Replicated SYSVOL-Ordners](#performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder)
-   [Ausführen einer autorisierenden Wiederherstellung eines FRS-Replicated SYSVOL-Ordners](#performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder)

## <a name="determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs"></a>Ermitteln, ob der SYSVOL-Ordner eines Domänen Controllers von DFSR oder FRS repliziert wird

In der folgenden Tabelle wird zusammengefasst, wie Sie bestimmen können, ob der SYSVOL-Ordner eines Domänen Controllers von [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) oder FRS repliziert wird.

| Wenn der Domänen Controller ausgeführt wird                                                                                                                  | SYSVOL wird repliziert von |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| Windows Server 2008 + Domänen Funktionsebene von Windows Server 2008 + [SYSVOL-Migration](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) abgeschlossen | DFSR                    |
| Windows Server 2008 +-Domänen Funktionsebene unterhalb von Windows Server 2008                                                                              | Fr                     |
| Windows Server 2003                                                                                                                                  | Fr                     |



 

Wenn die [Funktionsebene](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10)) der Domäne Windows Server 2008 ist und die Domäne der [SYSVOL-Migration](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx)unterzogen wurde, wird [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) zum Replizieren des Ordners SYSVOL verwendet. Wenn der erste Domänen Controller in der Domäne direkt in die Windows Server 2008- [Funktionsebene](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))herauf gestuft wurde, wird DFSR automatisch für die SYSVOL-Replikation verwendet. In solchen Fällen ist die Migration der SYSVOL-Replikation von FRS zu DFSR nicht erforderlich. Wenn die Domäne auf Windows Server 2008- [Funktionsebene](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))aktualisiert wurde, wird FRS für die SYSVOL-Replikation verwendet, bis der [Migrations](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) Prozess von FRS zu DFSR beendet ist.

Um zu ermitteln, ob DFSR oder FRS auf einem Domänen Controller mit Windows Server 2008 verwendet wird, überprüfen Sie den Wert des **\_ lokalen \_ HKEY**-Computers \\  \\ **CurrentControlSet** \\ **Services** \\ **DFSR**- \\ **Parameter** \\ **sysvols** \\ **Migrieren von sysvols** \\ **localstate** Registry unter Key. Wenn dieser Registrierungs Unterschlüssel vorhanden ist und der Wert auf 3 (eliminiert) festgelegt ist, wird [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) verwendet. Wenn der Unterschlüssel nicht vorhanden ist, oder wenn er einen anderen Wert aufweist, wird FRS verwendet.

## <a name="backing-up-a-dfsr-replicated-sysvol-folder"></a>Sichern eines DFSR-Replicated SYSVOL-Ordners

Wenn der SYSVOL-Ordner von [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)repliziert wird, kann der DFSR-VSS Writer verwendet werden, um ihn zu sichern. Weitere Informationen zum DFSR-VSS Writer finden Sie unter von [DFSR replizierte Ordner](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders).

## <a name="backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain"></a>Sichern eines FRS-Replicated SYSVOL-Ordners in einer Windows Server 2008-oder Windows Server 2003-Domäne

Auf einem Domänen Controller, auf dem Windows Server 2008 oder Windows Server 2003 ausgeführt wird, ist die VSS-Infrastruktur vorhanden. Daher kann der FRS-VSS Writer zum Sichern des Ordners SYSVOL und FRS verwendet werden.

Das Writer-Metadatendokument des FRS-VSS Writer enthält Informationen über den Speicherort des Ordners SYSVOL und die Ausschluss Listen für den Writer. Basierend auf diesen Informationen kann eine VSS-Sicherungs Anwendung (Requester) den SYSVOL-Ordner mithilfe der regulären VSS-basierten Sicherungs Techniken sichern.

Das Writer-Metadatendokument enthält Informationen zum Writer, zu den Daten, die der Writer besitzt, und zur Wiederherstellung dieser Daten. Dies ist ein Schreib geschütztes Dokument, das von der Sicherungs Anwendung abgerufen werden kann, bevor eine Sicherung durch genommen wird. Das [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) -Tool kann verwendet werden, um das Writer-Metadatendokument des FRS-VSS Writer anzuzeigen. Der [DiskShadow List Writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) -Befehl enthält Informationen zu den im System vorhandenen Writern. Diese Liste enthält Informationen zum FRS-Writer auf Domänen Controllern, die FRS für die SYSVOL-Replikation verwenden, oder auf Dateiservern, die FRS für die Replikation von [DFS-linkzielen](/previous-versions/windows/it-pro/windows-server-2003/cc782417(v=ws.10))verwenden.

Der folgende Beispiel-Metadatendokument-Abschnitt zeigt ein Metadatendokument für den FRS-Eintrag für einen Domänen Controller, der den SYSVOL-Ordner unter D: \\ Windows \\ SYSVOL enthält. Der im Abschnitt "ausgeschlossene Dateien" angezeigte Pfad ist identisch mit dem, der beim Abfragen des **SYSVOL** -Registrierungsschlüssels des Anmelde Diensts abgerufen wurde:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **Netlogon** \\ **Parameters** \\ **SYSVOL**

Die einzige Ausnahme von dieser Regel tritt auf, wenn sich der Domänen Controller im umgeleiteten Status der [SYSVOL-Migration](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx)befindet. In diesem Zustand melden die Writer, die sowohl dem FRS-als auch dem [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) -Dienst entsprechen, ihre entsprechenden Kopien des Ordners "SYSVOL". Allerdings ist der [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) -Dienst eine Kopie des Ordners SYSVOL (in der Regel ein Ordner namens SYSVOL \_ DFSR), der vom Domänen Controller gemeinsam verwendet wird. dieser Pfad ist der Pfad, auf den der **SYSVOL** -Registrierungsschlüssel verweist.

Das FRS-VSS Writer erfordert eine benutzerdefinierte Wiederherstellungsmethode. Dies bedeutet, dass beim Wiederherstellen von Dateien, die von FRS repliziert werden, bestimmte benutzerdefinierte Schritte ausgeführt werden müssen. Weitere Informationen finden Sie unter Durchführen einer nicht autorisierenden Wiederherstellung eines FRS-Replicated SYSVOL-Ordners.

> [!Note]  
> System Status Sicherungen für Windows-Domänen Controller enthalten nicht die FRS-Datenbank, die Zustandsinformationen für den FRS-Dienst für die Dateien im SYSVOL-Ordner und andere Inhalts Sätze verwaltet. Die FRS-Datenbank, Debugprotokolle, stagingbereichsdateien und Dateien im [bereits vorhandenen Datenordner](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) werden aus einer Systemstatus Sicherung ausgeschlossen. Die folgende Beispiel Spezifikation für den FRS-Writer enthält die Ausschlussliste im Abschnitt "ausgeschlossene Dateien".

 

## <a name="sample-frs-writer-metadata-document"></a>Metadatendokument für das Beispiel-FRS

Im folgenden finden Sie ein Beispiel eines FRS-Metadatendokuments für einen Domänen Controller, dessen SYSVOL-Ordner Pfad D: \\ Windows \\ SYSVOL lautet.

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

## <a name="setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder"></a>Festlegen von Registrierungs Schlüsseln für eine Wiederherstellung eines FRS-Replicated SYSVOL-Ordners

Der **BurFlags** -Registrierungsschlüssel wird verwendet, um autorisierende oder nicht autoritative Wiederherstellungen für FRS-Member von DFS-oder SYSVOL-Replikat Sätzen Der globale (Computer weite) **BurFlags** -Registrierungsschlüssel enthält die reg \_ DWORD-Werte und befindet sich an folgendem Speicherort in der Registrierung:

**HKEY \_ Lokaler \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NTFRS** \\  \\ **-Parameter Sicherungs-/Wiederherstellungsprozess** \\ **beim Start**

Die gängigsten Werte für den **BurFlags** -Registrierungsschlüssel lauten:

-   D2, auch als nicht autoritative Wiederherstellung bezeichnet.
-   D4, auch als autoritative Modus-Wiederherstellung bezeichnet.

Es gibt globale und Replikat gruppenspezifische **BurFlags** -Registrierungsschlüssel. Durch Festlegen des globalen **BurFlags** -Registrierungsschlüssels werden alle Replikat Gruppen erneut initialisiert, die der Member enthält. Dieser globale Schlüssel sollte festgelegt werden, wenn der Server nur eine Replikat Gruppe enthält oder wenn das Replikat, das es enthält, relativ wenig groß und kleiner ist. Wenn der Server z. b. ein Domänen Controller ist, der keine Inhalts Sätze hostet, die mit einem anderen FRS als dem SYSVOL-Ordner repliziert werden, kann der globale **BurFlags** -Registrierungsschlüssel festgelegt werden.

Der globale **BurFlags** -Registrierungsschlüssel befindet sich an folgendem Speicherort in der Registrierung:

**HKEY \_ Lokaler \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NTFRS** \\  \\ **-Parameter Sicherungs-/Wiederherstellungsprozess** \\ **beim Start**

Im Gegensatz zum globalen **BurFlags** -Schlüssel ermöglicht der Replikat gruppenspezifische **BurFlags** -Schlüssel die erneute Initialisierung diskreter, einzelner Replikat Gruppen, sodass fehlerfreie Replikations Sätze unverändert bleiben.

Replikat gruppenspezifische **BurFlags** -Registrierungsschlüssel können gefunden werden, indem die GUID für die jeweilige Replikat Gruppe bestimmt wird.

Im folgenden Verfahren wird beschrieben, wie Sie bestimmen, welche GUID einer bestimmten Replikat Gruppe entspricht, und wie Sie eine Wiederherstellung konfigurieren.

**So bestimmen Sie die GUID, die einer bestimmten Replikat Gruppe entspricht, und um eine Wiederherstellung zu konfigurieren**

1.  Der FRS-Dienst wird beendet.
2.  So bestimmen Sie die GUID, die eine bestimmte Replikat Gruppe darstellt:
    1.  Suchen Sie den folgenden Schlüssel in der Registrierung.

        **HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NTFRS**- \\ **Parameter** \\ **Replikat Sätze**

    2.  Unterhalb des unter Schlüssels der **Replikat Gruppen** gibt es einen oder mehrere Unterschlüssel, die jeweils durch eine GUID identifiziert werden.
    3.  Der Stamm Wert der **Replikat Gruppe** für jede GUID ist ein Dateisystempfad, der die Replikat Gruppe angibt, die durch diese GUID dargestellt wird.
    4.  Iterieren Sie diese Liste von GUIDs, bis die gewünschte Replikat Gruppe gefunden wurde. Notieren Sie sich die entsprechende GUID.

3.  Suchen Sie in der Registrierung nach dem folgenden Unterschlüssel:

    **HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NTFRS**- \\ **Parameter** \\ **kumulative Replikat Sätze**

4.  Suchen Sie unter diesem Unterschlüssel die gleiche GUID, die Sie in Schritt 2 notiert haben. Erstellen Sie unterhalb des unter Schlüssels GUID einen Eintrag für den **BurFlags** -Schlüssel.
5.  Starten Sie den FRS-Dienst neu.

## <a name="performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder"></a>Ausführen einer nicht autoritativen Wiederherstellung eines FRS-Replicated SYSVOL-Ordners

Die nicht autoritative Wiederherstellung ist die gängigste Methode zum erneuten Initialisieren der SYSVOL-Replikation auf einzelnen Domänen Controllern. Domänen Controller, die nicht autoritativ wieder hergestellt werden, müssen eingehende Verbindungen von anderen funktionierenden Domänen Controllern aufweisen, die an Active Directory-und FRS-Replikation beteiligt sind. In einer großen Bereitstellungs Umgebung, die aus vielen Domänen Controllern besteht, können die verbleibenden Domänen Controller unter den folgenden Bedingungen mithilfe einer nicht autorisierenden Wiederherstellung wieder hergestellt werden:

-   Es muss mindestens ein bekanntes, gutes Replikat Mitglied vorhanden sein (ein Domänen Controller mit einem fehlerfreien SYSVOL-Ordner).
-   Die anderen Domänen Controller müssen in der Reihenfolge der direkt Replikations Partner erneut initialisiert werden.

Im folgenden Verfahren wird beschrieben, wie eine nicht autoritative Wiederherstellung durchgeführt wird.

**So führen Sie eine nicht autoritative Wiederherstellung aus**

1.  Der FRS-Dienst wird beendet.
2.  Stellen Sie die gesicherten Daten im SYSVOL-Ordner wieder her.
3.  Konfigurieren Sie den **BurFlags** -Registrierungsschlüssel, indem Sie den Wert des folgenden Registrierungsschlüssels auf den DWORD-Wert D2 festlegen.

    **HKEY \_ Lokaler \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NTFRS** \\  \\ **-Parameter Sicherungs-/Wiederherstellungsprozess** \\ **beim Starten von** \\ **BurFlags**

4.  Starten Sie den FRS-Dienst neu.

Wenn der FRS-Dienst neu gestartet wird, treten die folgenden Aktionen auf:

-   Der Wert des **BurFlags** -Registrierungsschlüssels wird auf 0 (null) zurückgesetzt.
-   Dateien in den erneut initialisierten FRS-Ordnern werden in einen bereits vorhandenen Ordner verschoben.
-   Das Ereignis 13565 wird im FRS-Ereignisprotokoll protokolliert, um zu signalisieren, dass eine nicht autoritative Wiederherstellung gestartet wurde.
    > [!Note]  
    > FRS-Ereignis Codes sind in der Hilfe-und Support-Wissensdatenbank unter "FRS-Ereignisprotokoll-Fehlercodes" dokumentiert. <https://go.microsoft.com/fwlink/p/?linkid=117779>

     

-   Die FRS-Datenbank wird neu erstellt.
-   Der-Member führt einen anfänglichen Join der Replikat Gruppe von einem upstreampartner oder von dem Computer aus, der im übergeordneten Registrierungsschlüssel **Replikat Gruppe** angegeben ist, wenn ein übergeordnetes Element für SYSVOL-Replikat Gruppen angegeben wurde.
-   Der neu initialisierte Computer führt eine vollständige Replikation der betroffenen Replikat Gruppen durch, wenn der relevante Replikations Zeitplan beginnt.
-   Wenn der Prozess beendet ist, wird ein Ereignis 13516 protokolliert, das signalisiert, dass FRS betriebsbereit ist. Wenn das Ereignis nicht protokolliert wird, liegt ein Problem mit der FRS-Konfiguration vor.

> [!Note]  
> Die Platzierung von Dateien im [bereits vorhandenen](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) Ordner bei erneut initialisierten Membern ist eine Absicherung in FRS, die so konzipiert ist, dass versehentliche Datenverluste vermieden werden. Alle für das Replikat vorgesehenen Dateien, die nur im lokalen Ordner vorhanden sind und nach der ersten Replikation repliziert wurden, können dann in den entsprechenden Ordner kopiert werden. Wenn die ausgehende Replikation stattgefunden hat, können Dateien im bereits vorhandenen Ordner gelöscht werden, um zusätzlichen Speicherplatz freizugeben.

 

## <a name="performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder"></a>Ausführen einer autorisierenden Wiederherstellung eines FRS-Replicated SYSVOL-Ordners

Autorisierende Wiederherstellungen werden als letztes Mittel für kritische Situationen verwendet, z. b. Abweichungen von Daten im Inhalts Satz, die durch Verzeichnis Kollisionen verursacht werden. Beispielsweise kann eine autoritative Wiederherstellung erforderlich sein, um eine FRS-Replikat Gruppe wiederherzustellen, bei der die Replikation vollständig beendet wurde und eine Neuerstellung von Grund auf

Wenn Sie eine autoritative Wiederherstellung des Ordners SYSVOL ausführen müssen, beachten Sie, dass es sich um einen sehr komplizierten Prozess handelt. Umfassende Richtlinien mit Informationen zu den Vorgängen, die für eine autoritative Wiederherstellung des Inhalts des Ordners "SYSVOL" ausgeführt werden müssen, finden Sie unter "Gewusst wie: Neuerstellen der SYSVOL-Struktur und des zugehörigen Inhalts in einer Domäne" in der Hilfe-und Support Knowledge Base unter <https://go.microsoft.com/fwlink/p/?linkid=117780> .

Die folgenden Anforderungen müssen erfüllt sein, bevor eine autoritative FRS-Wiederherstellung durchgeführt wird:

1.  Der FRS-Dienst muss für alle downstreamreplikations Partner (direkt und transitiv) für den neu initialisierten SYSVOL-Ordner deaktiviert werden, bevor die autorisierende Wiederherstellung konfiguriert wurde.
2.  Die Ereignisse 13553 und 13516 wurden im FRS-Ereignisprotokoll protokolliert. Diese Ereignisse zeigen an, dass die Mitgliedschaft der SYSVOL-Replikat Gruppe auf dem Domänen Controller eingerichtet wurde, der für die autoritative Wiederherstellung konfiguriert wurde.
    > [!Note]  
    > FRS-Ereignis Codes sind in der Hilfe-und Support-Wissensdatenbank unter "FRS-Ereignisprotokoll-Fehlercodes" dokumentiert. <https://go.microsoft.com/fwlink/p/?linkid=117779>

     

3.  Der für die autorisierende Wiederherstellung konfigurierte Domänen Controller ist so konfiguriert, dass er für alle SYSVOL-Daten, die auf die übrigen Domänen Controller repliziert werden sollen, autorisierend ist.
4.  Alle anderen Partner in der Replikat Gruppe müssen mit einer nicht autorisierenden Wiederherstellung erneut initialisiert werden.

 

 
