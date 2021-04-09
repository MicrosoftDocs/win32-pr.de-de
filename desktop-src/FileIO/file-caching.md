---
description: Windows speichert Datei Daten, die von Datenträgern gelesen und auf Datenträger geschrieben werden.
ms.assetid: 0865c741-63e3-4246-ba69-801b02153e4a
title: Dateizwischenspeicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a14fb668af16cfb8a4e42b59b25b73ecefbb7cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868248"
---
# <a name="file-caching"></a>Dateizwischenspeicherung

Standardmäßig speichert Windows Dateidaten zwischen, die von Datenträgern gelesen und auf Datenträger geschrieben werden. Dies bedeutet, dass Lesevorgänge Datei Daten aus einem Bereich im Systemspeicher lesen, der als Systemdatei Cache bezeichnet wird, und nicht vom physischen Datenträger. Entsprechend schreiben Schreibvorgänge Dateidaten in den Systemdateicache statt auf den Datenträger, und diese Art von Cache wird als Zurückschreibcache bezeichnet. Zwischenspeichern wird auf Dateiobjektbasis verwaltet.

Das Caching erfolgt in der Richtung des *Cache-Managers*, der fortlaufend ausgeführt wird, während Windows ausgeführt wird. Datei Daten im Systemdatei Cache werden in durch das Betriebssystem festgelegter Intervallen auf den Datenträger geschrieben, und der zuvor von diesen Datei Daten verwendete Arbeitsspeicher wird freigegeben – dies *wird als leeren* des Caches bezeichnet. Die Richtlinie, das Schreiben der Daten in die Datei zu verzögern und im Cache zu speichern, bis der Cache geleert wird, wird als lazy writing bezeichnet und wird durch den Cache-Manager in einem bestimmten Zeitintervall ausgelöst. Die Zeit, zu der ein Dateidatenblock geleert wird, basiert teilweise auf dem Zeitraum, für den er im Cache gespeichert wurde, und auf der Zeit, die seit dem letzten Zugriff auf die Daten in einem Lesevorgang verstrichen ist. Dadurch wird sichergestellt, dass die Möglichkeit des Zugriffs auf häufig gelesene Dateidaten im Systemdateicache für eine maximale Zeitspanne erhalten bleibt.

Dieser Vorgang der Datei Datenspeicherung wird in der folgenden Abbildung veranschaulicht.

![Zwischenspeichern von Datei Daten](images/fig3.png)

Wie von den voll tonpfeilen in der vorherigen Abbildung dargestellt, wird ein Bereich von 256 KB-Daten in einen Slot-Slot von 256 KB in den System Adressraum eingelesen, wenn er während eines Datei Lesevorgangs erstmalig vom Cache-Manager angefordert wird. Ein Benutzermodusprozess kopiert die Daten in diesem Slot dann in seinen eigenen Adressraum. Wenn der Prozess den Datenzugriff abgeschlossen hat, schreibt er die geänderten Daten wieder in denselben Slot im Systemcache, wie mit dem gestrichelten Pfeil zwischen den Adressraum des Prozesses und dem Systemcache dargestellt. Wenn der Cache-Manager festgestellt hat, dass die Daten für einen bestimmten Zeitraum nicht mehr benötigt werden, werden die geänderten Daten in die Datei auf dem Datenträger zurückgeschrieben, wie durch den gepunkteten Pfeil zwischen dem System Cache und dem Datenträger dargestellt.

Der Umfang der e/a-Leistungsverbesserung, den das Zwischenspeichern von Datei Daten bietet, hängt von der Größe des gelesenen oder geschriebenen Datei Datenblocks ab. Wenn große Blöcke von Datei Daten gelesen und geschrieben werden, ist es wahrscheinlicher, dass Lese-und Schreibvorgänge für Datenträger erforderlich sind, um den e/a-Vorgang abzuschließen. Die e/a-Leistung wird immer stärker beeinträchtigt, da diese Art von e/a-Vorgängen auftritt.

In diesen Fällen kann das Zwischenspeichern deaktiviert werden. Dies erfolgt zu dem Zeitpunkt, zu dem die Datei geöffnet wird, indem Sie das **\_ Dateiflag \_ keine \_ Pufferung** als Wert für den *dwflagsandattributsparameter* von " [**kreatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)" übergibt. Wenn das Caching deaktiviert ist, greifen alle Lese-und Schreibvorgänge direkt auf den physischen Datenträger zu. Die Datei Metadaten werden jedoch möglicherweise weiterhin zwischengespeichert. Verwenden Sie die [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) -Funktion, um die Metadaten auf den Datenträger zu leeren.

Die Häufigkeit, mit der die Leerung erfolgt, ist ein wichtiger Aspekt, der die Systemleistung mit der Systemzuverlässigkeit ausgeglichen. Wenn das System den Cache zu häufig leert, wird die Systemleistung durch die Anzahl von leeren Schreibvorgängen bei Schreibvorgängen erheblich beeinträchtigt. Wenn das System nicht oft genug geleert wird, ist die Wahrscheinlichkeit größer, dass entweder der System Arbeitsspeicher durch den Cache erschöpft ist, oder es kommt zu einem plötzlichen Systemausfall (z. b. ein Stromausfall des Computers), der vor dem leeren erfolgt. In der letzteren Instanz gehen die zwischengespeicherten Daten verloren.

Um sicherzustellen, dass die richtige Menge an leeren erfolgt, erzeugt der Cache-Manager jede Sekunde einen Prozess, der als Lazy Writer bezeichnet wird. Der Lazy Writer-Prozess fügt ein Achtel der Seiten ein, die nicht vor kurzem geleert wurden, um auf den Datenträger geschrieben zu werden. Es wertet ständig die Menge der Daten aus, die für eine optimale Systemleistung geleert werden, und wenn mehr Daten geschrieben werden müssen, werden mehr Daten in die Warteschlange eingereiht. Verzögerte Writer leeren keine temporären Dateien, da davon ausgegangen wird, dass Sie von der Anwendung oder dem System gelöscht werden.

Einige Anwendungen, z. b. Viren Überprüfungs Software, erfordern, dass Ihre Schreibvorgänge sofort auf den Datenträger geleert werden. Windows bietet diese Möglichkeit durch das Zwischenspeichern von Schreibvorgängen. Ein Prozess ermöglicht das Zwischenspeichern von Lesevorgängen für einen bestimmten e/a-Vorgang, indem das **\_ Dateiflag zum \_ schreiben \_ durch** das Flag in seinen Aufrufen von " [**kreatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)" übergeht. Wenn das Write-Through-Caching aktiviert ist, werden die Daten weiterhin in den Cache geschrieben, aber der Cache-Manager schreibt die Daten sofort auf den Datenträger, anstatt eine Verzögerung mithilfe des Lazy Writer-Diensts zu verursachen. Ein Prozess kann auch das Leeren einer Datei erzwingen, die er durch Aufrufen der [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) -Funktion geöffnet hat.

Dateisystem Metadaten werden immer zwischengespeichert. Um Metadatenänderungen auf dem Datenträger zu speichern, muss die Datei daher entweder geleert oder mit einem **\_ Dateiflag \_ mit \_ Schreib** Zugriff geöffnet werden.

 

 



