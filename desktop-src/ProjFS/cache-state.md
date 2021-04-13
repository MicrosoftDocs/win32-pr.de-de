---
title: Cache Status im virtualisierungsstamm
description: Beschreibt die verschiedenen Cache Zustände, die eine vom Anbieter verwaltete Datei oder ein Verzeichnis aufweisen kann.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 43d62ceb1f5ef5bf07000666f336077270b1e86a
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/22/2020
ms.locfileid: "104389729"
---
# <a name="cache-state-in-the-virtualization-root"></a>Cache Status im virtualisierungsstamm

Der Anbieter verwendet das lokale Dateisystem unter dem virtualisierungsstamm als Cache der Elemente, die er verwaltet.  Ein Element (Datei oder Verzeichnis) kann sich in einem von sechs Zuständen im lokalen Dateisystem befinden:

* Virtuell

  Das Element ist nicht lokal auf dem Datenträger vorhanden.  Sie wird bei Enumerationen des übergeordneten Verzeichnisses projiziert, d. h. synthetisiert.  Virtuelle Elemente werden mit allen Elementen zusammengeführt, die möglicherweise auf dem Datenträger vorhanden sind, um den gesamten Inhalt des übergeordneten Verzeichnisses anzuzeigen.

* Platzhalter

  Für Dateien: der Inhalt der Datei (primärer Datenstrom) ist auf dem Datenträger nicht vorhanden.  Die Metadaten der Datei (Name, Größe, Zeitstempel, Attribute usw.) werden auf dem Datenträger zwischengespeichert.
  
  Für Verzeichnisse: einige oder alle unmittelbaren Nachfolger des Verzeichnisses (die Dateien und Verzeichnisse im Verzeichnis) sind nicht auf dem Datenträger vorhanden, d. h., Sie sind weiterhin virtuell.  Die Metadaten des Verzeichnisses (Name, Zeitstempel, Attribute usw.) werden auf dem Datenträger zwischengespeichert.

* Platzhalter

  Für Dateien: der Inhalt und die Metadaten der Datei wurden auf dem Datenträger zwischengespeichert.  Wird auch als "Partielle Datei" bezeichnet.
  
  Für Verzeichnisse: ein Verzeichnis, das auf dem Datenträger als Platzhalter erstellt wurde, wird nie zu einem Platzhalter Verzeichnis.  Dadurch kann der Anbieter Elemente aus dem Verzeichnis im Sicherungs Speicher hinzufügen oder daraus entfernen und diese Änderungen im lokalen Cache widerspiegeln.

* Geänderter Platzhalter (mit Feuchtigkeit oder nicht)

  Die Metadaten des Elements wurden lokal geändert, und es handelt sich nicht mehr um einen Cache seines Zustands im Speicher des Anbieters. Beachten Sie, dass das Erstellen oder Löschen einer Datei oder eines Verzeichnisses in einem Platzhalter Verzeichnis dazu führt, dass dieses Platzhalter Verzeichnis geändert wird.

* Vollständige Datei/Verzeichnis

  Für Dateien: der Inhalt der Datei (primärer Datenstrom) wurde geändert.  Die Datei ist kein Cache Ihres Zustands mehr im Speicher des Anbieters.  Dateien, die im lokalen Dateisystem erstellt wurden (d. h. nicht im Speicher des Anbieters vorhanden sind), werden auch als vollständige Dateien angesehen.
  
  Für Verzeichnisse: Verzeichnisse, die im lokalen Dateisystem erstellt wurden (d. h., die im Speicher des Anbieters nicht vorhanden sind), werden als vollständige Verzeichnisse betrachtet.  Ein Verzeichnis, das auf dem Datenträger als Platzhalter erstellt wurde, wird nie zu einem vollständigen Verzeichnis.
  
* Tombstone

  Ein spezieller ausgeblendeter Platzhalter, der ein Element darstellt, das aus dem lokalen Dateisystem gelöscht wurde.  Wenn ein Verzeichnis aufgelistet wird, führt projfs den Satz lokaler Elemente (Platzhalter, vollständige Dateien usw.) mit dem Satz der virtuellen projizierten Elemente zusammen.  Wenn ein Element sowohl in den lokalen als auch in den projizierten Sätzen vorkommt, hat das lokale Element Vorrang.  Wenn eine Datei im lokalen Dateisystem nicht vorhanden ist, gibt es keinen lokalen Zustand, sodass Sie in der-Enumeration angezeigt wird.  Wenn das Element jedoch gelöscht wurde, wäre es unerwartet, wenn es in der-Enumeration angezeigt wird.  Das Ersetzen eines gelöschten Elements durch einen Tombstone-Element führt zu folgenden Auswirkungen:

  * Enumerationen, um das Element nicht anzuzeigen.
  * Die Datei wird geöffnet, die davon ausgehen, dass das Element vorhanden ist, z. b. "Datei nicht gefunden".
  * Datei erstellt, die nur erfolgreich ausgeführt werden kann, wenn das Element nicht vorhanden ist. Projfs entfernt das Tombstone als Teil des Vorgangs.

Um die oben genannten Zustände zu veranschaulichen, sollten Sie die folgende Sequenz beachten, wenn Sie einen projfs-Anbieter haben, der über eine einzelne Datei "foo.txt" im virtualisierungsstamm "c:\Root" verfügt.

1. Eine APP listet c:\rootauf.  Die virtuelle Datei "foo.txt" wird angezeigt.  Da auf die Datei noch nicht zugegriffen wurde, ist die Datei nicht auf dem Datenträger vorhanden.
1. Die APP öffnet ein Handle für die C:\root\foo.txt.  Projfs weist den Anbieter an, einen Platzhalter dafür zu erstellen.
1. Die APP liest den Inhalt der Datei.  Der Anbieter stellt den Dateiinhalt für projfs bereit und wird in C:\root\foo.txt zwischengespeichert.  Die Datei ist jetzt ein Platzhalter.
1. Die APP aktualisiert den Zeitstempel der letzten Änderung.  Die Datei ist jetzt ein geänderter Platzhalter.
1. Die APP öffnet ein Handle für den Schreibzugriff auf die Datei.  C:\root\foo.txt ist nun eine vollständige Datei.
1. Die APP löscht C:\root\foo.txt.  Projfs ersetzt die Datei durch einen Tombstone.  Wenn die App nun c:\Root auflistet, wird foo.txt nicht angezeigt.  Wenn versucht wird, die Datei zu öffnen, schlägt das Öffnen mit ERROR_FILE_NOT_FOUND fehl.
