---
description: Die Dateiwiederherstellung auf einem ausgeführten System kann problematisch sein. Es ist wichtig, dass ausgeführte Anwendungen (Writer) angeben, was zu tun ist, wenn probleme während der Wiederherstellung auftreten, z. B. wenn die wiederhergestellte Datei derzeit verwendet wird.
ms.assetid: 2cb963a8-7077-4419-96d8-cba0fd011e4f
title: VSS-Wiederherstellungskonfigurationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48b3486128c6a91f601a89d697a4db9d8ab27fe9d3ac4cbef28dc870928d37d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344199"
---
# <a name="vss-restore-configurations"></a>VSS-Wiederherstellungskonfigurationen

Die Dateiwiederherstellung auf einem ausgeführten System kann problematisch sein. Es ist wichtig, dass ausgeführte Anwendungen (Writer) angeben, was zu tun ist, wenn probleme während der Wiederherstellung auftreten, z. B. wenn die wiederhergestellte Datei derzeit verwendet wird.

Unter VSS verfügen Writer über zwei sich ergänzende Methoden zum Verwalten von Wiederherstellungen:[*Wiederherstellungsmethoden*](vssgloss-r.md) und [*Wiederherstellungsziele.*](vssgloss-r.md)

Darüber hinaus können Anforderer Dateien an zuvor nicht angegebenen Speicherorten wiederherstellen und Writer benachrichtigen (siehe [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).

Die Wiederherstellungsmethode (auch das ursprüngliche Wiederherstellungsziel aufrufen) wird von einem Writer zu einem Sicherungszeitpunkt angegeben und legt eine writerweite Definition der Methode fest, die in Zukunft zum Wiederherstellen aller komponenten verwendet werden soll. Alle Dateien und Komponenten, die von einem Writer verwaltet werden, verwenden dieselbe Wiederherstellungsmethode.

Mit Wiederherstellungszielen können Writer ändern, wie bestimmte Komponenten zum Zeitpunkt der Wiederherstellung wiederhergestellt werden sollen. Im Gegensatz zu Wiederherstellungsmethoden werden Wiederherstellungsziele für einen Komponentensatz definiert.

Eine ausführliche Erläuterung der Verwendung von Wiederherstellungsmethoden und Wiederherstellungszielen finden Sie in den unten aufgeführten Themen:

-   [VSS-Wiederherstellungsstatus](vss-restore-state.md)
-   [Festlegen von VSS-Wiederherstellungsmethoden](setting-vss-restore-methods.md)
-   [Festlegen von VSS-Wiederherstellungszielen](setting-vss-restore-targets.md)
-   [Festlegen von VSS-Wiederherstellungsoptionen](setting-vss-restore-options.md)

(Informationen zu Wiederherstellungen, die diese Mechanismen nicht verwenden, finden Sie unter [Wiederherstellungen ohne Schreibteilnahme.)](restores-without-writer-participation.md)

 

 



