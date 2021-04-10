---
description: 'Die Windows Server 2003-Version der Volumeschattenkopie-Dienst enthält die folgenden neuen Funktionen:'
ms.assetid: 3dcfcc01-3e3c-43e9-a933-5c72f331da9a
title: Neue Funktionalität in Windows Server 2003 verfügbar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5782ef6b24f208f69e50cdb992e12ba3212c47f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131276"
---
# <a name="new-functionality-available-in-windows-server-2003"></a>Neue Funktionalität in Windows Server 2003 verfügbar

Die Windows Server 2003-Version der Volumeschattenkopie-Dienst enthält die folgenden neuen Funktionen:

-   Unterstützung für die [*Wiederherstellung von Wiederherstellungen*](vssgloss-s.md) zusätzlich zu und gleichermaßen mit [*selectlichkeit für die Sicherung*](vssgloss-s.md) (zuvor nur als "selekabilität" bezeichnet). Weitere Informationen finden Sie [unter Arbeiten mit selekabilität und logischen Pfaden](working-with-selectability-and-logical-paths.md) .
-   Einführung eines [*BackupShutdown*](vssgloss-b.md) -Ereignisses, das angibt, dass eine VSS-kompatible Sicherungs Anwendung (Requester) heruntergefahren wurde, ob der Sicherungs Versuch ordnungsgemäß abgeschlossen wurde oder nicht. Weitere Informationen finden Sie unter [Behandeln von BackupShutdown-Ereignissen](handling-backupshutdown-events.md) .
-   Unterstützung expliziter Writer-Komponenten Abhängigkeiten. Eine Möglichkeit zum beschreiben und unterstützen der Situationen, in denen eine von einem Writer verwaltete Komponente (und der von ihr festgelegte Komponenten Satz) nicht unabhängig von den von anderen Writern verwalteten Komponenten gesichert oder wieder hergestellt werden kann. Weitere Informationen finden Sie [unter Abhängigkeiten zwischen Komponenten, die von verschiedenen Writern verwaltet werden](dependencies-between-components-managed-by-different-writers.md) .
-   Vollständige Unterstützung für [*partielle Datei*](vssgloss-p.md) Vorgänge. Das Sichern und Wiederherstellen von Datei Segmenten durch Writer und Requestern wird jetzt vollständig unterstützt. Weitere Informationen zu partiellen Datei Vorgängen finden Sie unter [Arbeiten mit partiellen Dateien](working-with-partial-files.md) .
-   Einführung [*differenzierter Dateien*](vssgloss-d.md) zur Unterstützung inkrementeller Sicherungs-und Wiederherstellungs Vorgänge. Weitere Informationen finden Sie unter [inkrementelle und differenzielle Sicherungen](incremental-and-differential-backups.md) .
-   Einführung von Sicherungs Schemas als Konzept, das die Ebene der Writer-Unterstützung für Typen von Sicherungs Vorgängen angibt. Weitere Informationen finden Sie unter [**VSS- \_ Sicherungs \_ Schema**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) .
-   Unterstützung für die anfordererspezifikation neuer Datei Wiederherstellungs Ziele ([*neue Zielspeicher Orte*](vssgloss-n.md)) während Wiederherstellungs Vorgängen. Weitere Informationen finden Sie [unter Arbeiten mit neuen Zielen während der Wiederherstellung](working-with-new-targets-during-restore.md) .
-   Unterstützung für die bedingte Wiederherstellung beim Neustart. Weitere Informationen finden Sie unter VSS- \_ RME- \_ Wiederherstellung \_ beim \_ Neustart, \_ Wenn \_ nicht \_ ersetzen ([**VSE \_ restoremethod \_ enum**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)).
-   Die Definition eines Wiederherstellungs Zustands und des Wiederherstellungs Typs. Weitere Informationen finden Sie unter [**VSS- \_ \_ Wiederherstellungstyp**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) und [VSS-Wiederherstellungs Status](vss-restore-state.md) .
-   Unterstützung von Writer-Abfragen zum Status der Schatten Kopie. Weitere Informationen finden Sie unter [**CVssWriter:: GetContext**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcontext) und [**CVssWriter:: geznapshotdevicename**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename) .
-   Unterstützung für austauschen-Schatten Kopien in Windows Server 2003, Enterprise Edition und Windows Server 2003, Datacenter Edition. Weitere Informationen finden Sie unter [importieren transportable-Schattenkopievolumes](importing-transportable-shadow-copied-volumes.md).

 

 



