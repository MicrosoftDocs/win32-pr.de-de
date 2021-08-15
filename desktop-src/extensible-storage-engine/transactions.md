---
description: Weitere Informationen finden Sie unter Transaktionen (Windows Ereignisse).
title: Transaktionen (Windows-Ereignisse)
TOCTitle: Transactions
ms:assetid: 1ceb362c-1efe-439b-b10a-016c8a54f27b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269197(v=EXCHG.10)
ms:contentKeyID: 32765500
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: e223c95d7f8af5a4350786891d58b72c508443e459990d413d5b46bc2e12a2d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107055"
---
# <a name="transactions-windows-events"></a>Transaktionen (Windows-Ereignisse)


_**Gilt für:** Windows | Windows Server_

## <a name="transactions"></a>Transaktionen

ESE-Transaktionen sind logische Verarbeitungseinheiten, die steuern, wie eine Anwendung Zeilen in der Datenbank sieht und bearbeitet. Ihre Anwendung kann Transaktionsspeicherpunkte verwenden, um zu bestimmen, ob eine bestimmte Gruppe von Änderungen an der Datenbank beibehalten oder verworfen werden soll. Alle Transaktionen in ESE sind atomisch, konsistent, isoliert und dauerhaft (ACID), wie unten beschrieben:

  - **Atomar:** Alle Updates in der Transaktion werden entweder in der Datenbank angezeigt oder verworfen.

<!-- end list -->

  - **Konsistent:** Die Datenbank wird immer in einem rechtlichen Zustand gestartet und endet immer in einem anderen rechtlichen Zustand. Bei ESE-Anwendungen steuert die Datenbank-Engine einige einfache Einschränkungen, z. B. eindeutigkeit eines eindeutigen Indexes, aber die Anwendung selbst definiert fast alle anderen Aspekte, was es bedeutet, dass sich die Datenbank in einem rechtlichen Zustand befindet.

<!-- end list -->

  - **Isolation:** Transaktionen werden von Updates durch andere Sitzungen isoliert. Eine Transaktion wird nie einen Teilsatz von Änderungen sehen, die von einer anderen Transaktion vorgenommen wurden.

<!-- end list -->

  - **Dauerhaft:** Nachdem die Datenbank-Engine bestätigt hat, dass für eine Transaktion ein Commit ausgeführt wurde, sind die Änderungen in der Datenbank persistent. Die Dauerhaftigkeit einer Transaktion kann aus Leistungsgründen optional aufgehoben werden.

Transaktionen werden innerhalb der Grenzen der Aufrufe von [JetBeginTransaction](./jetbegintransaction-function.md) und [JetCommitTransaction](./jetcommittransaction-function.md) oder [JetRollback](./jetrollback-function.md)ausgeführt. Wenn die Anwendung in die Transaktion eintritt, wird die Datenbank zu dem Zeitpunkt, zu dem die Transaktion beginnt, auf der Instanz fixiert angezeigt. Dies wird als Momentaufnahmeisolation bezeichnet. Wenn die Transaktion durch Aufrufen von [JetRollback](./jetrollback-function.md)beendet wird, wird keiner der in der Transaktion ausgeführten Vorgänge an die Datenbank übertragen. Wenn der Prozess oder der Computer abstürzt, bevor [JetCommitTransaction](./jetcommittransaction-function.md) aufgerufen wird, entspricht er dem Aufruf von [JetRollback.](./jetrollback-function.md)

In diesem Verfahren wird gezeigt, wie Sie eine Transaktion starten und committen, die Daten in einer Datenbank liest und aktualisiert.

### <a name="to-start-and-commit-a-transaction"></a>So starten Sie eine Transaktion und committen sie

1.  Rufen Sie [JetBeginTransaction](./jetbegintransaction-function.md) oder [JetBeginTransaction2](./jetbegintransaction2-function.md) mit der Sitzungs-ID auf, um die Transaktion zu starten.

2.  Bewegen Sie den Cursor auf den gewünschten Datensatz, indem [Sie JetMove](./jetmove-function.md) mit JET_MoveFirst aufrufen, die im *cRow-Parameter* angegeben sind. Weitere Informationen zum Verschieben des Cursors finden Sie im Thema [Indizierung in der Tabelle.](./indexing-in-the-table.md)

3.  Rufen Sie [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) für den aktuellen Datensatz mit JET_ColInfo auf, die im *InfoLevel-Parameter* angegeben sind, um die Spalten-ID für die Spalte abzurufen. Die Spalten-ID wird in der [JET_COLUMNDEF-Struktur](./jet-columndef-structure.md) zurückgegeben.

4.  Rufen Sie [JetSetColumn](./jetsetcolumn-function.md) mit der Sitzungs-ID, der Tabellen-ID und der Spalten-ID der aktualisierten Spalte auf. Die Spaltendaten sind im *pvData-Parameter* enthalten.

5.  Rufen Sie [JetCommitTransaction](./jetcommittransaction-function.md) auf, um die Transaktion an die Datenbank zu committen.

Die Art und Weise, in der eine ESE-Datenbank-Engine die Momentaufnahmeisolation implementiert, weist einige wichtige Unterschiede zu herkömmlichen Isolations- und Sperrmodellen für relationale Datenbanken auf. Wenn eine Transaktion eine Zeile liest, kann sie immer auf die Zeile zugreifen, ohne dass ein Fehler eintritt oder darauf gewartet wird, dass andere Sitzungen eine Sperre freigeben. Wenn eine Transaktion versucht, eine Zeile zu aktualisieren, ist sie erfolgreich, wenn es sich um die erste Sitzung handelt, die diese Zeile aktualisiert, d.h. der erste Writer gewinnt. Wenn die Sitzung nicht der erste Writer ist, tritt sofort ein Schreibkonfliktfehler auf. Die Sitzung muss dann ihre Transaktion abbrechen, warten (in der Regel über eine zufällige Verzögerung), bis die andere Transaktion ihre Änderungen committen kann, und dann die Transaktion wiederholen. Die Datenbank-Engine bewirkt nicht automatisch, dass diese Sitzung wartet, bis die aktualisierung der anderen Transaktion abgeschlossen ist. In der Regel teste eine Transaktion, ob sie eine Zeile innerhalb des [JetUpdate-Aufrufs](./jetupdate-function.md) aktualisieren kann. Wenn die Zeile für das Update nicht gesperrt werden kann, schlägt [JetUpdate](./jetupdate-function.md) mit JET_errWriteConflict fehl.

Sitzungen sind auf einen Thread von dem Zeitpunkt an beschränkt, zu dem die Transaktion bis zum Ende der Transaktion beginnt. Es wird empfohlen, alle Aktualisierungs- und Abrufvorgänge in einer Transaktion auszuführen. ESE unterstützt auch Schemaänderungen wie das Erstellen von Tabellen und das Hinzufügen von Spalten innerhalb der Transaktion. Sowohl Update- als auch Schemaänderungen können in derselben Transaktion ausgeführt werden. Nachdem die Transaktion mit [JetCommitTransaction](./jetcommittransaction-function.md)abgeschlossen wurde, wird das Update in der Transaktionsprotokolldatei protokolliert. Diese Dateien können verwendet werden, um einen logisch konsistenten Zustand im Falle einer unerwarteten Prozessbeendigung oder des Herunterfahrens des Systems beizubehalten.

Transaktionen können bis zu 7 Ebenen geschachtelt sein, wobei übereinstimmende Aufrufe von [JetBeginTransaction](./jetbegintransaction-function.md) und [JetCommitTransaction](./jetcommittransaction-function.md) oder [JetRollback](./jetrollback-function.md) miteinander geschachtelt sind. Dies ermöglicht der Anwendung, ein Rollback für einen Teil der Transaktion auszuführen, ohne aus der gesamten Transaktion ein Rollback ausführen zu müssen. Der geschachtelte Aufruf von [JetCommitTransaction](./jetcommittransaction-function.md) gibt an, dass diese Verarbeitungsebene abgeschlossen ist. allerdings wird für die Transaktion erst ein Commit an die Datenbank ausgeführt, wenn der äußere größte Aufruf zum Committen der Transaktion mit [JetCommitTransaction](./jetcommittransaction-function.md)erfolgt.

Escrow update columns can be updated concurrently by multiple sessions without failing with Jet_errWriteConflict. Die [JetEscrowUpdate-Funktion](./jetescrowupdate-function.md) kann nur für Spalten aufgerufen werden, die mit Jet_bitColumnEscrowUpdate erstellt wurden.
