---
description: 'Bei jedem Sicherungs Vorgang, bei dem versucht wird, ein vollständiges und stabiles Image eines Systems zu kopieren, müssen folgende Aspekte berücksichtigt werden:'
ms.assetid: 8ccdba6d-1097-4c1c-982c-f3d9cbdf06cd
title: Häufige Probleme bei der Volumesicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f10433e0a695c11f7e61a258c3256baa651dc27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349701"
---
# <a name="common-volume-backup-issues"></a>Häufige Probleme bei der Volumesicherung

Bei jedem Sicherungs Vorgang, bei dem versucht wird, ein vollständiges und stabiles Image eines Systems zu kopieren, müssen folgende Aspekte berücksichtigt werden:

-   Nicht zugängliche Dateien während einer Sicherung. Beim Ausführen von Anwendungen müssen Dateien häufig im exklusiven Modus während einer Sicherung geöffnet bleiben, sodass Sicherungs Programme nicht kopiert werden können.
-   Inkonsistenter Dateistatus Selbst wenn die Dateien einer Anwendung nicht im exklusiven Modus geöffnet sind, ist es möglich – aufgrund der begrenzten Zeit, die zum Öffnen, sichern und Schließen einer Datei erforderlich ist –, dass Dateien, die auf die Speichermedien kopiert wurden, nicht alle denselben Anwendungs Zustand widerspiegeln.
-   Sie müssen Dienstunterbrechungen minimieren. Um den Zugriff auf die Datei und die Integrität der zu sichernden Daten sicherzustellen, sind die Unterbrechung und/oder Beendigung aller ausgeführten Programme während der Volumesicherung erforderlich. Bei großen Datenträgern kann dies Stunden lang dauern.

    Vor kurzem haben einige Speicher Anbieter versucht, diese Probleme zu beheben, indem Sie einen Volumen Erfassungs Mechanismus bereitstellen – ein Mittel zum Erfassen eines Abbilds der Dateien auf dem Datenträger zu einem bestimmten Zeitpunkt – entweder mithilfe eines Copy-on-Write-oder "Split Mirror"-Mechanismus. Diese Lösungen verursachen jedoch eigene Schwierigkeiten:

    -   Nicht kompatible Hersteller Implementierungen der volumeerfassung. Viele Anbieter von RAID-Geräten stellen Volumen Erfassungs Mechanismen bereit. Jeder Anbieter verfügt jedoch über eine eigene Oberfläche und muss von den Sicherungs Anbietern Unterstützung für die Volumen Erfassungs Schnittstellen erhalten. Dies bedeutet, dass die Anbieter von Sicherungs Anwendungen mehrere Volumen Aufzeichnungs Implementierungen unterstützen müssen, was nicht erwünscht ist.
    -   Fehlende Anwendungs Koordination. Viele Geräte, die eine volumeerfassung unterstützen, bieten keine Unterstützung für die Koordination der Ausführung von Anwendungen mit dem Einfrieren von Daten auf dem Datenträger. Bei Geräten, die wie bei den Sicherungs Anwendungen Vorgehen, verfügt jeder Anbieter über eine andere Schnittstelle.
    -   Eingeschränkte Unterstützung für nicht-RAID-Geräte. Wenige, wenn herkömmliche Datenträger Hersteller Unterstützung für eine beliebige Art von Volumen Erfassung in ihren Gerätetreibern bieten. Dies bedeutet, dass Aufzeichnungs Mechanismen auf bestimmte Datenträger Systeme beschränkt sind und in der Regel nicht die Sicherung von Systembereichen unterstützt werden.
    -   Updates auf dem Datenträger müssen während der volumeerfassung behandelt werden. Die vom Speicher Anbieter bereitgestellten Volumen Erfassungs Mechanismen können den Zustand der Daten auf dem Datenträger fixieren, aber Sie interagieren nicht immer mit den laufenden Anwendungen. Dies bedeutet häufig, dass Daten verloren gehen können, die an das Volume gesendet werden, während ein Speichergerät die volumeerfassung durchläuft.
    -   Konsistente multivolumesicherung. Das Speichergerät führt diese Volumen Erfassungen aus, sodass es im Allgemeinen keinen Mechanismus gibt, um die zeitliche Steuerung der Daten Sperrung zu koordinieren. Dies trifft vor allem dann zu, wenn die Geräte von separaten Anbietern stammen. Wenn also mehrere Speichervolumes an einer Sicherung mit einer volumeerfassung beteiligt sind, ist das für jedes Volume beibehaltene Zeit Abbild möglicherweise nicht konsistent.

 

 



