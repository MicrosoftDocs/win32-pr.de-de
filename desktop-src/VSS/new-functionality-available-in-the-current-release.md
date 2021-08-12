---
description: 'Das Windows Server 2003-Release des Volumeschattenkopie-Dienst enthält die folgenden neuen Funktionen:'
ms.assetid: 3dcfcc01-3e3c-43e9-a933-5c72f331da9a
title: Neue Funktionalität in Windows Server 2003 verfügbar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bc444a062fd2e1dae33af80feb88e1da52452064d8ed38c2db6fd5f7f3ae2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591391"
---
# <a name="new-functionality-available-in-windows-server-2003"></a>Neue Funktionalität in Windows Server 2003 verfügbar

Das Windows Server 2003-Release des Volumeschattenkopie-Dienst enthält die folgenden neuen Funktionen:

-   Unterstützung der [*Selektivität für die Wiederherstellung*](vssgloss-s.md) zusätzlich zu und auf gleiche Weise mit [*der Auswählbarkeit für die Sicherung*](vssgloss-s.md) (zuvor nur als Auswählbarkeit bezeichnet). Weitere Informationen finden Sie unter [Working with Selectability and Logical Paths (Arbeiten mit Selektivität und logischen Pfaden).](working-with-selectability-and-logical-paths.md)
-   Einführung eines [*BackupShutdown-Ereignisses,*](vssgloss-b.md) das angibt, dass eine VSS-kompatible Sicherungsanwendung (Anfordernde) heruntergefahren wurde, unabhängig davon, ob der Sicherungsversuch ordnungsgemäß abgeschlossen wurde oder nicht. Weitere Informationen finden Sie unter [Behandeln von BackupShutdown-Ereignissen.](handling-backupshutdown-events.md)
-   Unterstützung für explizite Abhängigkeiten von Writer-Komponenten. Ein Mittel zum Beschreiben und Unterstützen von Situationen, in denen eine Komponente (und die von ihr festgelegte Komponente), die von einem Writer verwaltet wird, nicht unabhängig von komponenten, die von anderen Writern verwaltet werden, gesichert oder wiederhergestellt werden kann. Weitere Informationen finden Sie unter [Abhängigkeiten zwischen Komponenten, die von verschiedenen Writern verwaltet werden.](dependencies-between-components-managed-by-different-writers.md)
-   Vollständige Unterstützung für [*Partielle Dateivorgänge.*](vssgloss-p.md) Die Sicherung und Wiederherstellung von Dateisegmenten durch Writer und Anforderer wird jetzt vollständig unterstützt. Weitere Informationen zu [partiellen](working-with-partial-files.md) Dateivorgängen finden Sie unter Arbeiten mit Teildateien.
-   Einführung [*differenzierter Dateien*](vssgloss-d.md) zur Unterstützung inkrementeller Sicherungs- und Wiederherstellungsvorgänge. Weitere Informationen finden Sie unter [Inkrementelle und differenzielle Sicherungen.](incremental-and-differential-backups.md)
-   Einführung von Sicherungsschemas als Konzept, das den Grad der Writerunterstützung für Arten von Sicherungsvorgängen angibt. Weitere Informationen finden Sie unter [**VSS \_ BACKUP \_ SCHEMA.**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
-   Unterstützung für die Anforderungsspezifikation neuer Dateiwiederherstellungsziele [*(neue Zielspeicherorte)*](vssgloss-n.md)während Wiederherstellungsvorgängen. Weitere Informationen finden Sie [unter Arbeiten mit neuen Zielen während der Wiederherstellung.](working-with-new-targets-during-restore.md)
-   Unterstützung für die bedingte Wiederherstellung zum Zeitpunkt des Neustarts. Weitere Informationen finden Sie unter \_ VSS RME \_ RESTORE AT REBOOT IF CANNOT REPLACE \_ \_ \_ \_ \_ [**(VSE \_ RESTOREMETHOD \_ ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)).
-   Definition eines Wiederherstellungsstatus und Wiederherstellungstyps. Weitere Informationen finden Sie unter [**VSS \_ RESTORE \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) und [VSS Restore State.](vss-restore-state.md)
-   Unterstützung für Writerabfragen zum Schattenkopiezustand. Weitere Informationen finden Sie unter [**CVssWriter::GetContext**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcontext) und [**CVssWriter::GetSnapshotDeviceName.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   Unterstützung für transportierbare Schattenkopien in Windows Server 2003, Enterprise Edition und Windows Server 2003, Datacenter Edition. Weitere Informationen finden Sie unter [Importieren von transportierbaren Schattenkopievolumes.](importing-transportable-shadow-copied-volumes.md)

 

 



