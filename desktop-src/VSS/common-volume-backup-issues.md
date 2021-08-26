---
description: 'Bei jedem Sicherungsvorgang, bei dem versucht wird, ein vollständiges und stabiles Image eines Systems zu kopieren, müssen die folgenden Aspekte berücksichtigt werden:'
ms.assetid: 8ccdba6d-1097-4c1c-982c-f3d9cbdf06cd
title: Häufige Probleme bei der Volumesicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16275c0d8e9128110736dd5feb51c75d2977b77c746b56cda487eed3aec86c34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032890"
---
# <a name="common-volume-backup-issues"></a>Häufige Probleme bei der Volumesicherung

Bei jedem Sicherungsvorgang, bei dem versucht wird, ein vollständiges und stabiles Image eines Systems zu kopieren, müssen die folgenden Aspekte berücksichtigt werden:

-   Während einer Sicherung kann nicht auf Dateien zugegriffen werden. Bei ausgeführten Anwendungen müssen Dateien während einer Sicherung häufig im exklusiven Modus geöffnet bleiben, sodass Sicherungsprogramme sie nicht kopieren können.
-   Inkonsistenter Dateizustand. Auch wenn die Dateien einer Anwendung nicht im exklusiven Modus geöffnet sind, ist es möglich– aufgrund der begrenzten Zeit, die zum Öffnen, Sichern und Schließen einer Datei erforderlich ist –, dass dateien, die auf Speichermedien kopiert werden, möglicherweise nicht alle denselben Anwendungszustand aufweisen.
-   Sie müssen Dienstunterbrechungen minimieren. Um den Dateizugriff und die Integrität der zu sichernden Daten sicherzustellen, kann die Unterbrechung und/oder Beendigung aller ausgeführten Programme während einer Volumesicherung erforderlich sein. Bei großen Datenträgersystemen kann dies eine Dauer von Stunden sein.

    In letzter Zeit haben einige Speicheranbieter versucht, diese Probleme zu beheben, indem sie einen Volumeerfassungsmechanismus (ein Mittel zum Erfassen eines Images der Dateien auf dem Datenträger zu einem bestimmten Zeitpunkt) mithilfe eines Kopier-bei-Schreib-Mechanismus oder eines "Split Mirror"-Mechanismus bereitstellen. Diese Lösungen bringen jedoch eigene Schwierigkeiten mit sich:

    -   Inkompatible Anbieterimplementierungen der Volumeerfassung. Viele Anbieter von RAID-Geräten bieten Volumeerfassungsmechanismen. Jeder Anbieter verfügt jedoch über eine eigene Schnittstelle, und jeder anbieter muss Unterstützung von den Sicherungsanbietern für seine Volumeerfassungsschnittstellen erhalten. Dies bedeutet, dass Anbieter von Sicherungsanwendungen mehrere Volumeerfassungsimplementierungen unterstützen müssen, was nicht erwünscht ist.
    -   Fehlende Anwendungskoordinierung. Viele Geräte, die eine Volumeerfassung unterstützen, unterstützen nicht die Koordination ausgeführter Anwendungen mit dem Einfrieren von Daten auf dem Datenträger. Für die Geräte, die dies tun, wie bei den Sicherungsanwendungen, verfügt jeder Anbieter über eine andere Schnittstelle.
    -   Eingeschränkte Unterstützung für Nicht-RAID-Geräte. Nur wenige herkömmliche Datenträgeranbieter bieten Unterstützung für jede Art von Volumeerfassung in ihren Gerätetreibern. Dies bedeutet, dass Erfassungsmechanismen auf bestimmte Datenträgersysteme beschränkt sind und in der Regel die Sicherung von Systembereichen nicht unterstützen können.
    -   Aktualisierungen des Datenträgers müssen während der Volumeerfassung behandelt werden. Obwohl die vom Speicheranbieter bereitgestellten Volumeerfassungsmechanismen den Zustand von Daten auf dem Datenträger einfrieren können, können sie nicht immer mit ausgeführten Anwendungen zusammenarbeiten. Dies bedeutet häufig, dass Daten, die an das Volume gesendet werden, während ein Speichergerät eine Volumeerfassung durchläuft, möglicherweise verloren gegangen sind.
    -   Konsistente Multivolume-Sicherung. Das Speichergerät führt diese Volumeerfassungen aus, sodass es im Allgemeinen keinen Mechanismus gibt, um den Zeitpunkt des Einfrierens der Daten zu koordinieren. Dies gilt insbesondere, wenn die Geräte von separaten Anbietern stammen. Wenn also mehrere Speichervolumes an einer Sicherung mit einer Volumeerfassung beteiligt sind, ist das für jedes Volume beibehaltene Zeitimage möglicherweise nicht konsistent.

 

 



