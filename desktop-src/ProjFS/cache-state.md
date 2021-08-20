---
title: Cachezustand im Virtualisierungsstamm
description: Beschreibt die verschiedenen Cachezustände einer Datei oder eines Verzeichnisses, die bzw. das vom Anbieter verwaltet wird.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 378973075017cc1ac06bf46840ea9d2d1058150a46587eb537374d501396ce30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792867"
---
# <a name="cache-state-in-the-virtualization-root"></a>Cachezustand im Virtualisierungsstamm

Der Anbieter verwendet das lokale Dateisystem unter dem Virtualisierungsstamm als Cache der elemente, die er verwaltet.  Ein Element (Datei oder Verzeichnis) kann sich im lokalen Dateisystem in einem von sechs Zuzuständen befinden:

* Virtuell

  Das Element ist nicht lokal auf dem Datenträger vorhanden.  Sie wird während Enumerationen des übergeordneten Verzeichnisses projiziert, d. h. synthetisiert.  Virtuelle Elemente werden mit allen Elementen zusammengeführt, die möglicherweise auf dem Datenträger vorhanden sind, um den vollständigen Inhalt des übergeordneten Verzeichnisses anzuzeigen.

* Platzhalter

  Für Dateien: Der Inhalt der Datei (primärer Datenstrom) ist auf dem Datenträger nicht vorhanden.  Die Metadaten der Datei (Name, Größe, Zeitstempel, Attribute usw.) werden auf dem Datenträger zwischengespeichert.
  
  Für Verzeichnisse: Einige oder alle unmittelbaren Nachfolger des Verzeichnisses (die Dateien und Verzeichnisse im Verzeichnis) sind auf dem Datenträger nicht vorhanden, d. h. sie sind noch virtuell.  Die Metadaten des Verzeichnisses (Name, Zeitstempel, Attribute usw.) werden auf dem Datenträger zwischengespeichert.

* Hydrated-Platzhalter

  Für Dateien: Der Inhalt und die Metadaten der Datei wurden auf dem Datenträger zwischengespeichert.  Wird auch als "Teildatei" bezeichnet.
  
  Für Verzeichnisse: Ein Verzeichnis, das auf dem Datenträger als Platzhalter erstellt wurde, wird nie zu einem verzeichnisierten Platzhalterverzeichnis.  Auf diese Weise kann der Anbieter dem Verzeichnis im zugehörigen Speicher Elemente hinzufügen oder daraus entfernen, und diese Änderungen werden im lokalen Cache widergespiegelt.

* Dirty placeholder (hydrated or not)

  Die Metadaten des Elements wurden lokal geändert und sind kein Cache des Zustands im Speicher des Anbieters mehr. Beachten Sie, dass das Erstellen oder Löschen einer Datei oder eines Verzeichnisses unter einem Platzhalterverzeichnis dazu führt, dass dieses Platzhalterverzeichnis verfeckt wird.

* Vollständige Datei/vollständiges Verzeichnis

  Für Dateien: Der Inhalt der Datei (primärer Datenstrom) wurde geändert.  Die Datei ist kein Cache ihres Zustands mehr im Speicher des Anbieters.  Dateien, die auf dem lokalen Dateisystem erstellt wurden (d.h. die im Speicher des Anbieters überhaupt nicht vorhanden sind), werden ebenfalls als vollständige Dateien betrachtet.
  
  Für Verzeichnisse: Verzeichnisse, die im lokalen Dateisystem erstellt wurden (d.h. die im Speicher des Anbieters überhaupt nicht vorhanden sind), werden als vollständige Verzeichnisse betrachtet.  Ein Verzeichnis, das auf dem Datenträger als Platzhalter erstellt wurde, wird nie zu einem vollständigen Verzeichnis.
  
* Tombstone

  Ein spezieller ausgeblendeter Platzhalter, der ein Element darstellt, das aus dem lokalen Dateisystem gelöscht wurde.  Wenn ein Verzeichnis aufzählt, führt ProjFS den Satz lokaler Elemente (Platzhalter, vollständige Dateien usw.) mit dem Satz von virtuellen projizierten Elementen zusammen.  Wenn ein Element sowohl in der lokalen als auch in der projizierten Sätze angezeigt wird, hat das lokale Element Vorrang.  Wenn eine Datei im lokalen Dateisystem nicht vorhanden ist, gibt es keinen lokalen Zustand, sodass sie in der -Enumeration angezeigt wird.  Wenn dieses Element jedoch gelöscht worden wäre, wäre es unerwartet, wenn es in der -Enumeration angezeigt würde.  Das Ersetzen eines gelöschten Elements durch einen Tombstone hat die folgenden Auswirkungen:

  * Enumerationen, die das Element nicht preis geben.
  * Die Datei wird geöffnet, bei der erwartet wird, dass das Element vorhanden ist, z. B. "Datei wurde nicht gefunden".
  * Die Datei erstellt , die nur dann erfolgreich ist, wenn das Element nicht vorhanden ist. ProjFS entfernt den Tombstone als Teil des Vorgangs.

Um die oben genannten Zustände zu veranschaulichen, betrachten Sie die folgende Sequenz, wenn ein ProjFS-Anbieter eine einzelne Datei "foo.txt" enthält, die sich im Virtualisierungsstamm C:\root befindet.

1. Eine App aufzählt C:\root.  Die virtuelle Datei wird als "foo.txt" betrachtet.  Da auf die Datei noch nicht zugegriffen wurde, ist die Datei auf dem Datenträger nicht vorhanden.
1. Die App öffnet ein Handle zum C:\root\foo.txt.  ProjFS weist den Anbieter an, einen Platzhalter dafür zu erstellen.
1. Die App liest den Inhalt der Datei.  Der Anbieter stellt den Dateiinhalt für ProjFS zur C:\root\foo.txt.  Die Datei ist jetzt ein hydratisierter Platzhalter.
1. Die App aktualisiert den Zeitstempel der letzten Änderung.  Die Datei ist jetzt ein Platzhalter mit Dirty Hydrated.
1. Die App öffnet ein Handle für den Schreibzugriff auf die Datei.  C:\root\foo.txt ist jetzt eine vollständige Datei.
1. Die App löscht C:\root\foo.txt.  ProjFS ersetzt die Datei durch einen Tombstone.  Wenn die App nun "C:\root" aufzählt, wird die foo.txt.  Wenn versucht wird, die Datei zu öffnen, schlägt das Öffnen mit ERROR_FILE_NOT_FOUND.
