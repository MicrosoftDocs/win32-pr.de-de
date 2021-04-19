---
description: Das Verarbeiten einer der Dateigruppen einer Komponente erfordert möglicherweise, dass ein Anforderer eine Verzeichnisstruktur rekursiv durchläuft. Dies kann erfordern, dass die anfordernde Person bereitgestellte Ordner und Analyse Punkte (z. b. Verknüpfungen) verarbeiten kann, die auf Daten verweisen, die nicht auf dem aktuellen Volume gespeichert sind.
ms.assetid: d0e08598-a8a2-489b-9cb2-e989bed1ce53
title: Arbeiten mit bereitgestellten Ordnern und Analyse Punkten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a7aa88f39361f788f9aac882b4f9d337fd6f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353081"
---
# <a name="working-with-mounted-folders-and-reparse-points"></a>Arbeiten mit bereitgestellten Ordnern und Analyse Punkten

Das Verarbeiten einer der Dateigruppen einer Komponente erfordert möglicherweise, dass ein Anforderer eine Verzeichnisstruktur rekursiv durchläuft. Dies kann erfordern, dass die anfordernde Person bereitgestellte Ordner und Analyse Punkte (z. b. Verknüpfungen) verarbeiten kann, die auf Daten verweisen, die nicht auf dem aktuellen Volume gespeichert sind.

Anforderer soll beim Durchlaufen einer Verzeichnisstruktur den bereitgestellten Ordnern und Analyse Punkten folgen, und VSS verfügt über klar definierte Richtlinien für die Behandlung von Sicherungs-und Wiederherstellungs Vorgängen.

Um diese Richtlinien zu veranschaulichen, sehen Sie sich das folgende Beispiel an:

-   Das Volume \\ \\ ? \\ Volume {GUID \_ 1} weist den Laufwerk Buchstaben C: auf \\ .
-   Ein Dateisatz hat den Pfad C: \\ Schreibdaten.
-   Eine Datei Spezifikation \* . dat wird vom Datei Satz verwendet.
-   Die Rekursion des Datei Satzes ist auf **true** festgelegt.
-   Das Verzeichnis C: " \\ Schreibdaten" befindet sich auf dem Volume \\ \\ ? \\ Volume {GUID \_ 1}.
-   Das Verzeichnis C: \\ Schreibdaten \\ Archive ist ein bereitgestellter Ordner.
-   Das Volume \\ \\ ? \\ Volume "{GUID \_ 2}" ist dem bereitgestellten Ordner "C: \\ schreibdata Archive" zugeordnet \\ .

## <a name="handling-mounted-folders-and-reparse-points-during-backup"></a>Behandeln von bereitgestellten Ordnern und Analyse Punkten während der Sicherung

Die grundlegenden Regeln für die Behandlung von bereitgestellten Ordnern und Analyse Punkten unter VSS beim Ausführen einer rekursiven Sicherung können wie folgt zusammengefasst werden:

-   Pfade werden über eingebundene Ordner und Analyse Punkte hinweg befolgt.
-   Wenn ein bereitgestellter Ordner oder Analyse Punkt auf ein Volume verweist, sollte dieses Volume als Schatten kopiert werden.
-   Wenn ein Volume eingebundene Ordner oder Analyse Punkte enthält, werden diese in der Schatten Kopie des Volumes angezeigt.
-   Daten, die sich unter dem bereitgestellten Ordner oder Analyse Punkt befinden, werden in der Schatten Kopie des Volumes aufgezeichnet, auf das der bereitgestellte Ordner oder der Analyse Punkt verweist.

Zur Veranschaulichung der Verwendung des obigen Beispiels, da das rekursive Flag festgelegt ist, muss der Anforderer alle Daten unter "C: \\ beschreiterdata Archive" und "below" untersuchen \\ .

Der Anforderer muss das Volume mit dem Laufwerk Buchstaben "C:" hinzufügen: \\ ( \\ \\ ? \\ Volume {GUID \_ 1}) und das Volume, das dem bereitgestellten Ordner C: \\ Write Data \\ Archive zugeordnet ist ( \\ \\ ? \\ Volume {GUID \_ 2}) zum Schattenkopiesatz, der mithilfe von [**IVssBackupComponents:: addtosnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)festgelegt wurde.

Der eingebundene Ordner C: das \\ \\ Archiv Data Archive wird in der Schatten Kopie des Volumes angezeigt \\ \\ ? \\ Volume {GUID \_ 1} mit einem Geräte Objekt mit dem Namen deviceObject1.

VSS kopiert jedoch keine Daten in diesem bereitgestellten Ordner (Daten auf \\ \\ ? \\ Volume {GUID \_ 2}) für die Schatten Kopie, auf die von deviceObject1 verwiesen wird. Stattdessen werden die Daten in der Schatten Kopie von aufgezeichnet \\ \\ ? \\ Volume {GUID \_ 2} mit einem Geräte Objekt mit dem Namen deviceObject2.

Daher verwendet eine anfordernde Person, die Schatten Kopien von Dateien unter "c: Write Data" sichert, \\ den Pfad "deviceObject1 \\ schreibdata", um nach Dateien zu suchen, die mit "c: \\ beschreiterdata \\ \* . dat" übereinstimmen.

Zum Sichern von schattenkopierten Dateien unter C: \\ beschreiterdata \\ Archive verwendet die anfordernde Person den Pfad deviceObject2 (weil das Stammverzeichnis von \\ \\ ? \\ Volume {GUID \_ 2} wurde dem bereitgestellten Ordner c: \\ Writer \\ Archive zugeordnet), um nach Dateien zu suchen, die mit "c: \\ Write Data \\ Archive \\ \* . dat" übereinstimmen.

Beachten Sie, dass ein Analyse Punkt auf die gleiche Weise wie ein bereitgestellter Ordner verarbeitet wird. Der Analyse Punkt wird in der Schatten Kopie des ersten Volumes angezeigt. Die Daten unter dem Analyse Punkt werden in der Schatten Kopie des zweiten Volumes angezeigt.

Während der Sicherung sollten anfordernde Personen Informationen zu bereitgestellten Ordnern und den Ihnen zugeordneten Volumes sowie Analyse Punkte und deren Ziele speichern, um sicherzustellen, dass alle Daten ordnungsgemäß gesichert und wieder hergestellt werden.

## <a name="handling-mount-and-reparse-points-during-restore"></a>Behandeln von einbinden und Analyse Punkten während der Wiederherstellung

Beim Wiederherstellen von Dateien muss die anfordernde Person den Richtlinien folgen, die sich etwas von denen bei der Sicherung unterscheiden (z. b. die [*Zuordnung alternativer Speicherorte*](vssgloss-a.md) und [*neuer Ziel Speicherort*](vssgloss-n.md)):

-   Wenn Rekursion erforderlich ist, dann werden die Pfade über eingebundene Ordner und Analyse Punkte hinweg befolgt.
-   Eingebundene Ordner müssen wieder hergestellt werden.
-   Die Wiederherstellungs Orte von bereitgestellten Ordnern und Analyse Punkten werden durch ihre ursprünglichen Pfade bestimmt.

Wenn die Volumenamen zwischen der Sicherung und Wiederherstellung beibehalten werden – d. h., Sie erstellen die Volumes nicht neu – werden wiederhergestellte bereitgestellte Ordner und Analyse Punkte auf die richtigen Volumes verweisen.

Daher wird im obigen Beispiel, wenn der bereitgestellte Ordner C: \\ Write Data Archive in \\ ( \\ \\ ? \\ Volume {GUID \_ 1}) und das zuvor zugeordnete Volume wurden wieder hergestellt in ( \\ \\ ? \\ Volume {GUID \_ 2}), die wiederhergestellten Dateien und die Dateistruktur sind korrekt und konsistent.

Es kann vorkommen, dass Daten in einem System wieder hergestellt werden, in dem sich die Volumenamen geändert haben Dies kann auf Datenträger Abstürze zurückzuführen sein, bei denen möglicherweise eine manuelle Systemwiederherstellung durchgeführt und Volumes neu erstellt werden müssen. In einer solchen Situation sind eingebundene Ordner und Analyse Punkte nach der Wiederherstellung nicht mehr gültig. Zum erneuten Erstellen der Dateien und der Dateistruktur auf dem wiederhergestellten Volume müssen die wiederhergestellten Ordner und Analyse Punkte gelöscht und auf dem Datenträger neu erstellt werden. Es liegt an der Sicherungs Anwendung, zu entscheiden, ob dies angemessen ist.

Beachten Sie, dass es möglich ist, dass das Wiederherstellungs Ziel für einen bereitgestellten Ordner bereits belegt ist. Beispielsweise kann C: das \\ Archiv Data \\ Archive bereits einige Dateien enthalten. Es liegt in der Sicherungs Anwendung, zu entscheiden, wie diese Situation bewältigt werden soll.

 

 



