---
description: 'Weitere Informationen finden Sie hier: Transaktionen (Windows-Ereignisse)'
title: Transaktionen (Windows-Ereignisse)
TOCTitle: Transactions
ms:assetid: 1ceb362c-1efe-439b-b10a-016c8a54f27b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269197(v=EXCHG.10)
ms:contentKeyID: 32765500
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 90b5b566f5ff961ce7b0ae3725f580e1f39c041d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346958"
---
# <a name="transactions-windows-events"></a>Transaktionen (Windows-Ereignisse)


_**Gilt für:** Windows | Windows Server_

## <a name="transactions"></a>Transaktionen

ESE-Transaktionen sind logische Verarbeitungseinheiten, mit denen gesteuert wird, wie eine Anwendung Zeilen in der Datenbank sieht und bearbeitet. Die Anwendung kann Transaktions Speicherpunkte verwenden, um zu bestimmen, ob ein bestimmter Satz von Änderungen an der Datenbank beibehalten oder verworfen werden soll. Alle Transaktionen in ESE sind atomarisch, konsistent, isoliert und dauerhaft (ACID), wie im folgenden beschrieben:

  - **Atomarisch:** Alle Updates in der Transaktion werden entweder in der Datenbank angezeigt, oder Sie werden verworfen.

<!-- end list -->

  - **Konsistent:** Die Datenbank wird immer in einem gültigen Zustand gestartet und endet immer mit einem anderen rechtlichen Zustand. Bei ESE-Anwendungen steuert die Datenbank-Engine einige einfache Einschränkungen, z. b. die Eindeutigkeit eines eindeutigen Indexes, aber die Anwendung selbst definiert fast alle anderen Aspekte der Bedeutung, die für die Datenbank in einem rechtlichen Zustand vorliegen.

<!-- end list -->

  - **Isolation:** Transaktionen werden von Updates durch andere Sitzungen isoliert. Eine Transaktion erhält nie einen partiellen Satz von Änderungen, die von einer anderen Transaktion vorgenommen wurden.

<!-- end list -->

  - Permanent **:** Nachdem die Datenbank-Engine bestätigt hat, dass für eine Transaktion ein Commit ausgeführt wurde, werden die Änderungen in der Datenbank persistent gespeichert. Die Dauerhaftigkeit einer Transaktion kann aus Leistungsgründen optional aufgehoben werden.

Transaktionen werden innerhalb der Grenzen der Aufrufe von [jetbegintransaction](./jetbegintransaction-function.md) und [jetcommittransaction](./jetcommittransaction-function.md) oder [jetrollback](./jetrollback-function.md)durchgeführt. Wenn die Anwendung in die Transaktion eintritt, wird die Datenbank bei der Instanz fixiert, wenn die Transaktion beginnt. Dies wird als Momentaufnahme Isolation bezeichnet. Wenn die Transaktion durch Aufrufen von [jetrollback](./jetrollback-function.md)beendet wird, wird keiner der Vorgänge, die in der Transaktion ausgeführt werden, an die Datenbank übertragen. Wenn der Prozess oder der Computer abstürzt, bevor [jetcommittransaction](./jetcommittransaction-function.md) aufgerufen wird, entspricht er dem Aufruf von [jetrollback](./jetrollback-function.md).

Diese Prozedur zeigt, wie Sie eine Transaktion starten und ausführen, die Daten in einer-Datenbank liest und aktualisiert.

### <a name="to-start-and-commit-a-transaction"></a>So starten Sie eine Transaktion und commitden Commit

1.  Aufrufen von [jetbegintransaction](./jetbegintransaction-function.md) oder [JetBeginTransaction2](./jetbegintransaction2-function.md) mit der Sitzungs-ID, um die Transaktion zu starten.

2.  Bewegen Sie den Cursor in den gewünschten Datensatz, indem Sie [jetmove](./jetmove-function.md) mit JET_MoveFirst aufrufen, die im Parameter " *cRow* " angegeben sind. Weitere Informationen zum Verschieben des Cursors finden Sie im Thema [Indizierung in der Tabelle](./indexing-in-the-table.md) .

3.  Rufen Sie [jetgettablecolumninfo](./jetgettablecolumninfo-function.md) für den aktuellen Datensatz mit JET_ColInfo im *infolevel* -Parameter fest, um die Spalten-ID für die Spalte abzurufen. Die Spalten-ID wird in der [JET_COLUMNDEF](./jet-columndef-structure.md) Struktur zurückgegeben.

4.  Aufrufen von [jetsetcolumn](./jetsetcolumn-function.md) mit der Sitzungs-ID, der Tabellen-ID und der Spalten-ID der aktualisierten Spalte. Die Spaltendaten sind im *pvData* -Parameter enthalten.

5.  Ruft [jetcommittransaction](./jetcommittransaction-function.md) auf, um die Transaktion an die Datenbank zu übergeben.

Die Art und Weise, in der ein ESE-Datenbankmodul die Momentaufnahme Isolation implementiert, hat einige wichtige Unterschiede zu herkömmlichen relationalen Daten Bank Isolations- Wenn eine Transaktion eine Zeile liest, kann Sie immer auf die Zeile zugreifen, ohne dass ein Fehler auftritt oder darauf gewartet wird, dass andere Sitzungen eine Sperre freigeben. Wenn eine Transaktion versucht, eine Zeile zu aktualisieren, wird Sie erfolgreich ausgeführt, wenn Sie die erste Sitzung zum Aktualisieren dieser Zeile ist, d. h., der erste Writer gewinnt. Wenn die Sitzung nicht der erste Writer ist, wird Sie sofort mit einem Fehler beim Schreiben eines Konflikts fehlschlagen. Die Sitzung muss dann die Transaktion abbrechen, (in der Regel über eine zufällige Verzögerung) warten, bis die andere Transaktion einen Commit für die Änderungen durchführen und dann die Transaktion wiederholen. Die Datenbank-Engine führt nicht automatisch dazu, dass die Sitzung wartet, bis die Aktualisierung der anderen Transaktion abgeschlossen ist. Normalerweise testet eine Transaktion, ob eine Zeile innerhalb des [jetupdate](./jetupdate-function.md) -Aufrufes aktualisiert werden kann. Wenn die Zeile für das Update nicht gesperrt werden kann, schlägt [jetupdate](./jetupdate-function.md) mit JET_errWriteConflict fehl.

Sitzungen sind auf einen Thread ab dem Zeitpunkt beschränkt, zu dem die Transaktion mit dem Ende der Transaktion beginnt. Es wird empfohlen, alle Update-und Abruf Vorgänge in einer Transaktion durchzuführen. ESE unterstützt auch Schema Änderungen wie das Erstellen von Tabellen und das Hinzufügen von Spalten innerhalb der Transaktion. Sowohl Update-als auch Schema Änderungen können in der gleichen Transaktion ausgeführt werden. Nachdem die Transaktion mit [jetcommittransaction](./jetcommittransaction-function.md)abgeschlossen wurde, wird das Update in der Transaktionsprotokoll Datei protokolliert. Diese Dateien können verwendet werden, um einen logisch konsistenten Zustand zu gewährleisten, wenn eine unerwartete Beendigung des Prozesses oder das Herunterfahren des Systems auftritt.

Transaktionen können bis zu 7 Ebenen geschachtelt werden, wobei die Aufrufe von [jetbegintransaction](./jetbegintransaction-function.md) und [jetcommittransaction](./jetcommittransaction-function.md) oder [jetrollback](./jetrollback-function.md) ineinander geschachtelt sind. Dadurch kann die Anwendung einen Teil der Transaktion zurücksetzen, ohne dass die gesamte Transaktion zurückgesetzt werden muss. Der von [jetcommittransaction eingefügte pecommittransaction](./jetcommittransaction-function.md) -Befehl bedeutet, dass diese Verarbeitungs Ebene abgeschlossen ist. die Transaktion wird jedoch erst dann an die Datenbank übergeben, wenn der äußerste Anrufe den Commit der Transaktion mit [jetcommittransaction](./jetcommittransaction-function.md)durchläuft.

Escrow-Update Spalten können gleichzeitig durch mehrere Sitzungen aktualisiert werden, ohne dass Jet_errWriteConflict fehlschlägt. Die [jetescrowupdate](./jetescrowupdate-function.md) -Funktion kann nur für hinterlegte Spalten, Spalten, die mit Jet_bitColumnEscrowUpdate erstellt wurden, aufgerufen werden.
