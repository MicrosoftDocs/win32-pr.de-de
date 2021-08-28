---
description: Die Verarbeitung eines Dateisets einer Komponente erfordert möglicherweise, dass ein Anforderer eine Verzeichnisstruktur rekursiv durchläuft. Dies kann erfordern, dass der Anforderer bereitgestellte Ordner und Auswertungspunkte (z. B. Links) behandelt, die auf Daten verweisen, die sich nicht auf dem aktuellen Volume befinden.
ms.assetid: d0e08598-a8a2-489b-9cb2-e989bed1ce53
title: Arbeiten mit bereitgestellten Ordnern und Wiederholungspunkten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1162d1d7da5869f588ae61d9235ec3d5827265c5eb9deaa23c38b8b9e85db68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905060"
---
# <a name="working-with-mounted-folders-and-reparse-points"></a>Arbeiten mit bereitgestellten Ordnern und Wiederholungspunkten

Die Verarbeitung eines Dateisets einer Komponente erfordert möglicherweise, dass ein Anforderer eine Verzeichnisstruktur rekursiv durchläuft. Dies kann erfordern, dass der Anforderer bereitgestellte Ordner und Auswertungspunkte (z. B. Links) behandelt, die auf Daten verweisen, die sich nicht auf dem aktuellen Volume befinden.

Von Anforderern wird erwartet, dass sie beim Durchlaufen einer Verzeichnisstruktur bereitgestellte Ordner und Nachverfolgungspunkte befolgen, und VSS verfügt über klar definierte Richtlinien für deren Behandlung für Sicherungs- und Wiederherstellungsvorgänge.

Betrachten Sie das folgende Beispiel, um diese Richtlinien zu veranschaulichen:

-   Das Volume \\ \\ ? \\ Volume{GUID \_ 1} hat den Laufwerkbuchstaben C: \\ .
-   Ein Dateisatz weist den Pfad C: \\ WriterData auf.
-   Eine Dateispezifikation \* .dat wird vom Dateisatz verwendet.
-   Die Rekursion des Dateisatzes ist auf **TRUE** festgelegt.
-   Das Verzeichnis C: \\ WriterData befindet sich auf dem Volume \\ \\ ? \\ Volume{GUID \_ 1}.
-   Das Verzeichnis C: \\ WriterData \\ Archive ist ein eingebundener Ordner.
-   Das Volume \\ \\ ? \\ Volume{GUID \_ 2} ist dem eingebundenen Ordner C: \\ WriterData \\ Archive zugeordnet.

## <a name="handling-mounted-folders-and-reparse-points-during-backup"></a>Behandeln von bereitgestellten Ordnern und Wiederholungspunkten während der Sicherung

Die grundlegenden Regeln für die Behandlung von bereitgestellten Ordnern und Wiederholungspunkten unter VSS beim Ausführen einer rekursiven Sicherung können wie folgt zusammengefasst werden:

-   Pfade werden über bereitgestellte Ordner und Reparsepunkte hinweg verfolgt.
-   Wenn ein bereitgestellter Ordner oder Ein Wiederholungspunkt auf ein Volume verweist, sollte dieses Volume schattenkopiert werden.
-   Wenn ein Volume bereitgestellte Ordner oder Wiederholungspunkte enthält, werden diese in der Schattenkopie des Volumes angezeigt.
-   Daten, die sich unter dem bereitgestellten Ordner oder Dementepunkt befinden, werden in der Schattenkopie des Volumes erfasst, auf das der bereitgestellte Ordner oder Der Auswertungspunkt zeigt.

Um die Verwendung des obigen Beispiels zu veranschaulichen, da das rekursive Flag festgelegt ist, muss der Anforderer alle Daten unter C: \\ WriterData \\ Archive und darunter untersuchen.

Der Anforderer muss das Volume mit Laufwerkbuchstaben C: \\ ( \\ \\ ? \\ Volume{GUID \_ 1}) und das Volume, das dem eingebundenen Ordner C: \\ WriterData \\ Archive ( \\ \\ ? \\ Volume{GUID \_ 2}) für das Schattenkopieset mithilfe von [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).

Der bereitgestellte Ordner C: \\ WriterData \\ Archive wird in der Schattenkopie des Volumes \\ \\ angezeigt? \\ Volume{GUID \_ 1}, das über ein Geräteobjekt mit dem Namen deviceObject1 verfügt.

VSS kopiert jedoch keine Daten in diesen bereitgestellten Ordner (Daten in \\ \\ ? \\ Volume{GUID \_ 2}) für die Schattenkopie, auf die von deviceObject1 verwiesen wird. Stattdessen werden diese Daten in der Schattenkopie von \\ \\ erfasst. \\ Volume{GUID \_ 2}, das über ein Geräteobjekt mit dem Namen deviceObject2 verfügt.

Daher verwendet ein Anforderer, der Schattenkopiendateien unter C: WriterData gesichert, \\ den Pfad deviceObject1 \\ WriterData, um nach Dateien zu suchen, die C: \\ WriterData \\ \* .dat entsprechen.

Um Schattenkopiendateien unter C: WriterData Archive zu \\ \\ sichern, verwendet der Anforderer den Pfad deviceObject2 (da das Stammverzeichnis \\ \\ von ? \\ Volume{GUID \_ 2} wurde dem eingebundenen Ordner C: \\ Writer Archive \\ zugeordnet, um nach Dateien zu suchen, die C: \\ WriterData Archive \\ \\ \* .dat entsprechen.

Beachten Sie, dass ein Wiederholungspunkt auf die gleiche Weise wie ein bereitgestellter Ordner behandelt wird. Der Wiederholungspunkt wird in der Schattenkopie des ersten Volumes angezeigt. Die Daten unter dem Auswertungspunkt werden in der Schattenkopie des zweiten Volumes angezeigt.

Während der Sicherung sollten Anforderer Informationen zu bereitgestellten Ordnern und den zugeordneten Volumes sowie Dies sind Dies sind die Fehlerpunkte und ihre Ziele, um sicherzustellen, dass alle Daten ordnungsgemäß gesichert und wiederhergestellt werden.

## <a name="handling-mount-and-reparse-points-during-restore"></a>Behandeln von Bereitstellungs- und Wiederholungspunkten während der Wiederherstellung

Beim Wiederherstellen von Dateien muss der Anforderer andere Richtlinien befolgen als die, die während der Sicherung verwendet wurden (wobei Probleme wie [*die Zuordnung alternativer Speicherorte*](vssgloss-a.md) und [*neuer Zielspeicherort*](vssgloss-n.md)ignoriert werden):

-   Wenn eine Rekursion erforderlich ist, werden wie zuvor Pfade über bereitgestellte Ordner und Wiederholungspunkte hinweg verfolgt.
-   Bereitgestellte Ordner müssen wiederhergestellt werden.
-   Die Wiederherstellungsspeicherorte der bereitgestellten Ordner und Derortierungspunkte werden durch ihre ursprünglichen Pfade bestimmt.

Wenn die Volumenamen zwischen Sicherung und Wiederherstellung beibehalten werden , d. h., Sie erstellen die Volumes nicht neu, sollten wiederhergestellte bereitgestellte Ordner und Fehlerpunkte auf die richtigen Volumes verweisen.

Aus diesem Grund wurde im oben beschriebenen Beispiel der bereitgestellte Ordner C: \\ WriterData \\ Archive in ( \\ \\ ? \\ Volume{GUID \_ 1}) und das zuvor zugeordnete Volume wurden auf ( \\ \\ ? \\ Volume{GUID \_ 2}), die wiederhergestellten Dateien und die Dateistruktur wären richtig und konsistent.

Es kann vorkommen, dass Daten in einem System wiederhergestellt werden, in dem sich Volumenamen geändert haben. Dies kann auf Datenträgerabstürze zurückzuführen sein, bei denen Sie möglicherweise eine manuelle Systemwiederherstellung durchführen und Volumes neu erstellen müssen. In dieser Art von Situation sind bereitgestellte Ordner und Überprüfungspunkte nach der Wiederherstellung nicht mehr gültig. Um die Dateien und die Dateistruktur auf dem wiederhergestellten Volume neu zu erstellen, müssen die wiederhergestellten bereitgestellten Ordner gelöscht und Die Punkte neu erstellt und auf dem Datenträger neu erstellt werden. Die Sicherungsanwendung muss entscheiden, ob dies geeignet ist.

Beachten Sie, dass das Wiederherstellungsziel für einen eingebundenen Ordner möglicherweise bereits belegt ist. Beispielsweise enthält C: \\ WriterData \\ Archive möglicherweise bereits einige Dateien. Die Sicherungsanwendung muss entscheiden, wie diese Situation behandelt werden soll.

 

 



