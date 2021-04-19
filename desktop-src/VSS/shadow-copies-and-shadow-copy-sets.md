---
description: Eine Schatten Kopie ist eine Momentaufnahme eines Volumes, bei dem alle Daten, die auf diesem Volume gespeichert sind, zu einem bestimmten Zeitpunkt dupliziert werden. VSS identifiziert jede Schatten Kopie durch eine persistente GUID.
ms.assetid: 8ef2478a-c8bc-4517-9a14-e1d9226ec4cd
title: Schatten Kopien und schattenkopiesätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18709842b1fb0fbf6d6cce2557b51042dfb024ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367871"
---
# <a name="shadow-copies-and-shadow-copy-sets"></a>Schatten Kopien und schattenkopiesätze

Eine [*Schatten Kopie*](vssgloss-s.md) ist eine Momentaufnahme eines Volumes, bei dem alle Daten, die auf diesem Volume gespeichert sind, zu einem bestimmten Zeitpunkt dupliziert werden. VSS identifiziert jede Schatten Kopie durch eine persistente GUID.

Ein [*Schattenkopiesatz*](vssgloss-s.md) ist eine Sammlung von Schatten Kopien verschiedener Volumes, die alle gleichzeitig erstellt wurden. VSS identifiziert jede Schatten Kopie, die durch eine persistente GUID festgelegt ist.

Die Art und Weise, wie sich ein bestimmter Hardware-oder Softwarehersteller für die Implementierung von Schatten Kopien entscheidet, ist vollständig Nachdem eine Schatten Kopie erstellt wurde, sind tatsächlich zwei Images des schattenkopierten Volumes für das System verfügbar: das ursprüngliche Volume, auf das konventionell zugegriffen werden kann. und den kopierten Daten, auf die über die VSS-API zugegriffen werden kann.

Dadurch können zwei Gruppen von Aktivitäten gleichzeitig stattfinden:

-   Normale Anwendungen im System können mit dem ursprünglichen Volume schnell fortfahren oder fortgesetzt werden, indem die Daten auf dem Datenträger aktualisiert werden.
-   Anwendungen, die die VSS-Anforderer-API verwenden, um auf das schattenkopierte Volume zuzugreifen, können Sicherungen oder ähnliche Vorgänge ausführen.

Schatten Kopien müssen nicht auf die gleiche Weise für alle Dateien, Verzeichnisse oder Volumes implementiert werden. Verschiedene Implementierungen des schattenkopiemechanismus ([*Anbieter*](vssgloss-p.md)) können unterschiedliche Ansätze zum Erstellen einer Schatten Kopie verwenden. Für alle Anwendungen, die die VSS-API verwenden, sollten allerdings alle Schatten Kopien identisch angezeigt werden.

Weitere Informationen zur Standard Implementierung des Windows-Anbieters finden Sie unter [System Anbieter](providers.md).

## <a name="default-shadow-copy-state"></a>Standardmäßiger schattenkopiestatus

Obwohl das Dateisystem vor dem Erstellen einer Schatten Kopie alle e/a-Puffer geleert hat, wird dadurch nicht sichergestellt, dass unvollständige e/a-Vorgänge ordnungsgemäß verarbeitet werden.

Wenn das System keine VSS-fähigen Anwendungen hat, werden die Daten in einer Schatten Kopie daher in einem [*Absturz konsistenten Zustand*](vssgloss-c.md)angezeigt. Eine Schatten Kopie in einem Absturz konsistenten Zustand enthält ein Abbild des Datenträgers, das mit dem übereinstimmt, das nach einem schwerwiegenden Herunterfahren des Systems vorhanden wäre. Alle geöffneten Dateien sind weiterhin auf dem Volume vorhanden, aber Sie sind nicht garantiert, dass unvollständige e/a-Vorgänge oder Daten beschädigt sind.

Während der Absturz konsistente Zustand alle Probleme im Zusammenhang mit der Definition eines stabilen Sicherungs Satzes (siehe häufige Probleme mit der [Volumesicherung](common-volume-backup-issues.md)) nicht vollständig behandelt, bietet er mehrere Vorteile gegenüber dem Sicherungs Satz, der von herkömmlichen Sicherungs Vorgängen verwendet werden müsste:

-   Ein Volume, das in einer Schatten Kopie enthalten ist, selbst in einem Absturz konsistenten Zustand, enthält weiterhin alle Dateien. Ein Sicherungs Satz, der ohne eine Schatten Kopie erstellt wurde, enthält nicht alle Dateien, die zum Zeitpunkt der Sicherung geöffnet waren. Dateien, die zum Zeitpunkt des Sicherungs Vorgangs geöffnet gehalten wurden, werden von der Sicherung ausgeschlossen.
-   Die Schatten Kopie des Volumes wird zu einem Zeitpunkt erstellt, nicht durch das Durchlaufen eines aktiven Dateisystems, das in der Regel viel mehr Zeit erfordert.

Anwendungen auf einem System, die nicht VSS-fähig sind – Word-Prozessoren, Editoren usw. – haben wahrscheinlich, dass Ihre Dateien in einem Absturz konsistenten Zustand verbleiben. VSS-fähige Anwendungen (Writer) können Ihre Aktionen jedoch koordinieren, sodass der Zustand Ihrer Dateien in der Schatten Kopie wohl definiert und konsistent ist.

## <a name="shadow-copy-freeze-and-thaw"></a>Einfrieren von Schatten Kopien und durch das durch täuschen

Die Erstellung jedes VSS-schattenkopievorgangs wird durch [*Freeze*](vssgloss-f.md) -und [*Thaw*](vssgloss-t.md) -Ereignisse in Klammern gesetzt, die Writer verwenden, um Ihre Dateien vor dem Schatten kopieren in einen stabilen Zustand zu versetzen.

Die Verwendung von Freeze-und Thaw-Ereignissen als Teil des VSS-Modells bedeutet Folgendes:

-   Das Behandeln des Freeze-Ereignisses bedeutet, dass Benutzer, die Writer entwickeln, einen klar abgeglichen Punkt im Sicherungs Zeitraum aufweisen müssen, in dem Sie sicherstellen, dass alle Schreibvorgänge auf dem Datenträger beendet werden und dass sich die Dateien in einem klar definierten Zustand für die Sicherung befinden.
-   Wenn Sie das Ereignis Thaw verarbeiten, können Writer Schreibvorgänge auf dem Datenträger fortsetzen und temporäre Dateien oder andere temporäre Zustandsinformationen bereinigen, die in der Zuordnung zur Schatten Kopie erstellt wurden.
-   Das Standardfenster zwischen den Freeze-und den thaw-Ereignissen ist kurz (in der Regel 60 Sekunden); Daher kann die tatsächliche Unterbrechung eines Diensts, den ein Writer bereitstellt, minimiert werden.
-   Durch die Verarbeitung anderer Ereignisse (z. b. prepareforsnapshot) vor und nach den Ereignissen zum Einfrieren bzw. nachverfolgen wird die erforderliche Flexibilität bereitgestellt, damit Writer komplizierte Vorgänge ausführen können, um Schatten Kopien zu unterstützen.

 

 



