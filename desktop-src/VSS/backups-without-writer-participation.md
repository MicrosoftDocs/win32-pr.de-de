---
description: Wenn ein VSS-Sicherungs Vorgang ohne Beteiligung eines Writers durchgeführt wird, kann die Erstellung von Schatten Kopien weiterhin stattfinden.
ms.assetid: 2058e894-bde5-4690-a7aa-849d2e9cdc71
title: Sicherungen ohne Writer-Teilnahme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9a782fbcb9afe532f2f123151dc7998307157b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360871"
---
# <a name="backups-without-writer-participation"></a>Sicherungen ohne Writer-Teilnahme

Wenn ein VSS-Sicherungs Vorgang ohne Beteiligung eines Writers durchgeführt wird, kann die Erstellung von Schatten Kopien weiterhin stattfinden.

Wie an anderer Stelle angegeben (siehe [Standard schattenkopiestatus](shadow-copies-and-shadow-copy-sets.md)), ist das Ergebnis dieser Art von Schatten Kopie ein Volume, das den Zustand eines Datenträgers zum Zeitpunkt der Schatten Kopie widerspiegelt: die Daten auf dem schattenkopierten Volume spiegeln möglicherweise unvollständige oder partielle e/a-Vorgänge wider und werden so beschrieben, dass Sie sich in einem [*Absturz konsistenten Zustand*](vssgloss-c.md)befinden.

Es gibt mehrere Situationen, in denen eine Sicherungs Anwendung für Absturz konsistente Schatten Kopien von Daten erforderlich ist:

-   **Daten werden von VSS-abhängigen Anwendungen verwaltet.**

    Fast jedes System verfügt über einige Anwendungen – Text-Editoren, e-Mail-Reader, Word-Prozessoren usw. –, die VSS nicht wissen, ist es wahrscheinlich, dass einige der Daten auf einer Schatten Kopie als in einem Absturz konsistenten Zustand angesehen werden müssen.

    Bei dieser Art von Daten handelt es sich in der Regel nicht um System-oder Dienst kritische Daten, sodass die Sicherung nicht problematisch oder zumindest bei einer herkömmlichen Sicherung nicht problematisch sein sollte.

    Wie bei der Vorbereitung für konventionelle Sicherungen sollten Sicherungs Operatoren nach Möglichkeit versuchen, solche Anwendungen anzuhalten oder zu beenden, bevor Sie einen VSS-Sicherungsauftrag starten.

-   **System ohne VSS-kompatible Writer**

    Diese Situation kann relativ selten auftreten, da die meisten Systeme, die durch eine VSS-Sicherungs Anwendung gesichert werden können, über eine VSS-fähige Windows-Version verfügen, die Writer enthalten sollte.

    Es gibt jedoch bestimmte Situationen, in denen dieses Problem auftreten kann – z. b. Wenn Sie ein System ohne VSS-Unterstützung sichern, aber das System ein VSS-fähiges Netzwerkgerät für seine Speicherung verwendet.

    Obwohl das Sichern des Systemstatus von einem Absturz konsistenten Abbild nicht optimal ist, kann es für einen Computer ausreichend sein, den Betriebsstatus neu zu starten. In vielen Fällen wird der Computer von unvollständigen e/a-Vorgängen in den Dateisystemen wieder hergestellt und wird normal ausgeführt.

-   **Ein Anforderer, der sich entscheidet, nicht mit den System Autoren zu arbeiten**

    Dieser Umstand tritt auf, wenn ein Anforderer sich entschieden hat, keine Writer-Komponenten hinzuzufügen oder alle Writer zu deaktivieren.

    Das Ausführen von Sicherungen auf diese Weise wird im Allgemeinen nicht empfohlen. Obwohl das zu sichernde schattenkopierte Volume ausreichen kann, um ein System in der Ausführung wiederherzustellen, ist es nicht wünschenswert. Tatsache, dass die Schreiber, die auf dem System ausgeführt werden, mit Funktionen für die Zusammenarbeit mit VSS und Schatten Kopien entworfen wurden, kann die Sicherung Ihrer Daten auf diese Weise zu einer Instabilität führen.

 

 



