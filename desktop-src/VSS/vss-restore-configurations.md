---
description: Die Dateiwiederherstellung auf einem laufenden System kann problematisch sein. Es ist wichtig, dass ausgestellte Anwendungen (Writer) angeben, was zu tun ist, wenn während der Wiederherstellung Probleme auftreten, beispielsweise, wenn die wieder herzustellende Datei zurzeit verwendet wird.
ms.assetid: 2cb963a8-7077-4419-96d8-cba0fd011e4f
title: VSS-Wiederherstellungs Konfigurationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f13acfc59f250a859e9c62f2df2e1b1b982608ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129293"
---
# <a name="vss-restore-configurations"></a>VSS-Wiederherstellungs Konfigurationen

Die Dateiwiederherstellung auf einem laufenden System kann problematisch sein. Es ist wichtig, dass ausgestellte Anwendungen (Writer) angeben, was zu tun ist, wenn während der Wiederherstellung Probleme auftreten, beispielsweise, wenn die wieder herzustellende Datei zurzeit verwendet wird.

Unter VSS haben Writer zwei ergänzende Möglichkeiten zur Verwaltung von [*Wiederherstellungen – Wiederherstellungsmethoden*](vssgloss-r.md) und [*Wiederherstellungs Ziele*](vssgloss-r.md).

Außerdem können Anforderer die Dateien an zuvor nicht angegebenen Speicherorten wiederherstellen und Writer Benachrichtigen (Weitere Informationen finden Sie unter [**IVssBackupComponents:: addnewtarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).

Die Restore-Methode (auch das ursprüngliche Wiederherstellungs Ziel) wird von einem Writer zum Zeitpunkt der Sicherung angegeben und legt eine Writer-weite Definition der Methode fest, die zum Wiederherstellen aller ihrer Komponenten in der Zukunft verwendet werden soll. Alle Dateien und Komponenten, die von einem Writer verwaltet werden, verwenden dieselbe Wiederherstellungsmethode.

Mit Wiederherstellungs Zielen können Writer die Art und Weise ändern, wie bestimmte Komponenten zum Zeitpunkt der Wiederherstellung wieder hergestellt werden. Im Gegensatz zu Restore-Methoden werden Wiederherstellungs Ziele für einen Komponenten Satz definiert.

Eine ausführliche Erläuterung der Verwendung von Wiederherstellungsmethoden und Wiederherstellungs Zielen finden Sie in den folgenden Themen:

-   [VSS-Wiederherstellungs Status](vss-restore-state.md)
-   [Festlegen von VSS-Wiederherstellungsmethoden](setting-vss-restore-methods.md)
-   [Festlegen von VSS-Wiederherstellungs Zielen](setting-vss-restore-targets.md)
-   [Festlegen der VSS-Wiederherstellungsoptionen](setting-vss-restore-options.md)

(Informationen zu Wiederherstellungen, bei denen diese Mechanismen nicht verwendet werden, finden Sie unter wieder [herstellen ohne Writer-Teilnahme](restores-without-writer-participation.md).)

 

 



