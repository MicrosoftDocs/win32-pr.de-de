---
description: Weitere Informationen zu Spalten mit langen Werten
title: Lange Wert Spalten
TOCTitle: Long Value Columns
ms:assetid: 0690f9d3-1a58-4e53-92e1-213630fc88f4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269179(v=EXCHG.10)
ms:contentKeyID: 32765482
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: bb5618227d49de9e246adf69868a3cb2dc498dca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041636"
---
# <a name="long-value-columns"></a>Lange Wert Spalten


_**Gilt für:** Windows | Windows Server_

## <a name="long-value-columns"></a>Lange Wert Spalten

Die ESE-Spaltentypen JET_coltypLongText und JET_coltypLongBinary werden als Long-Wert-Spaltentypen bezeichnet. Diese Spalten sind große Zeichen folgen und große binäre Objekte, die in separaten B +-Strukturen vom primären Index abgelegt werden können. Wenn lange Werte vom primären Datensatz getrennt gespeichert werden, werden Sie intern auf eine lange Wert-ID (LID) und einen Byte Offset (und als Datenstrom) zugegriffen. Lange Wert Spalten werden der Tabelle im " [jetaddcolumn](./jetaddcolumn-function.md) "-Befehl hinzugefügt, wobei der **colttmember** der [JET_COLUMNDEF](./jet-columndef-structure.md) -Struktur entweder auf "JET_coltypLongText" oder "JET_coltypLongBinary" festgelegt ist. Die maximal zulässige Größe für einen langen Text-oder Long-Binär Spaltenwert ist 2 GB-1.

ESE unterstützt Anfüge-, Byte Bereichs Überschreibungs-und Mengen Größen Vorgänge für Spalten mit langen Werten, um effiziente Streamimplementierungen für diese Spaltentypen zu unterstützen. Lange Wertdaten werden standardmäßig in einer separaten B +-Struktur gespeichert, wenn Sie größer als 1024 Byte ist, oder wenn der Datensatz nicht auf eine einzelne Datenbankseite passt, wenn die langen Wertdaten im Datensatz gespeichert werden. Die Anwendung hat die Möglichkeit, das Standardverhalten zu überschreiben, indem Optionen zum Speichern von Long-Wert-Daten im Datensatz (JET_bitSetIntrinsicLV) festgelegt werden oder die Speicherung in der separaten B +-Struktur (JET_bitSetIntrinsicLV) erzwungen wird. Diese Werte werden im *grbit* -Parameter in [jetsetcolumn](./jetsetcolumn-function.md)festgelegt, oder das **grbit** -Element [JET_SETCOLUMN](./jet-setcolumn-structure.md) im Aufrufen von [jetsetcolumns](./jetsetcolumns-function.md) wie folgt verwendet:

  - Anfügen: (JET_bitSetAppendLV)

  - Byte Bereichs Überschreibung: (JET_bitSetOverwriteLV)

  - Größe festlegen: (JET_bitSetSizeLV)

  - Separate erzwingen: (JET_bitSetSeparateLV)

  - In Datensatz speichern: (JET_bitSetIntrinsicLV)

Die Long-Wert-Daten werden festgelegt, indem der Offset im Long Value-BLOB und die Länge der Long Value-Daten im BLOB angegeben wird. Der Offset zum Long Value-BLOB wird im **iblongvalue** -Member von [JET_SETINFO](./jet-setinfo-structure.md) -Struktur (für [jetsetcolumn](./jetsetcolumn-function.md)) oder dem **iblongvalue** -Member der [JET_SETCOLUMN](./jet-setcolumn-structure.md) -Struktur (für [jetsetcolumns](./jetsetcolumns-function.md)) festgelegt. Der **pvData** -Member von [JET_SETCOLUMN](./jet-setcolumn-structure.md)und der *pvData* -Parameter im-Befehl von [jetsetcolumn](./jetsetcolumn-function.md) enthalten die Long-Wertdaten. Aktualisierungen an Spalten mit langen Werten müssen innerhalb einer Transaktion ausgeführt werden.

Die langen Wertdaten werden immer in einer separaten Tabelle gespeichert, wenn die Anwendung die JET_bitSetSeparateLV oder JET_bitSetIntrinsicLV festlegt; andernfalls wird Sie heuristisch beschlossen. ESE speichert den Long-Wert getrennt, wenn er größer als 1024 Byte ist oder wenn der Datensatz nicht auf eine einzelne Datenbankseite passt, wenn er im Datensatz gespeichert wird.

Im folgenden Diagramm werden die in einer separaten Tabelle gespeicherten Long-Value-Daten angezeigt. Wenn ein Long-Wert außerhalb des Datensatzes gespeichert wird, wird eine neue Long-Wert-ID erstellt, um auf ihren Wert zu verweisen. Dadurch können mehrere Datensätze auf denselben Spaltenwert verweisen. Verweis Zähler auf die Daten werden angehoben, wenn mehr als ein Datensatz in den Daten auf die gleichen Long-Wert-Daten verweist.

![ESE_Documentation_longvaluedtree2](images/Gg269179.ESE_Documentation_longvaluedtree2(EXCHG.10).gif "ESE_Documentation_longvaluedtree2")

ESE unterstützt auch eine Single Instance Store-Funktion, mit der mehrere Datensätze auf dasselbe große binäre Objekt verweisen können, so als ob jeder Datensatz über eine eigene Kopie der Informationen verfügt. Dadurch werden doppelte Kopien der Spaltenwert Daten vermieden. Diese Funktion ist im Befehl [jetprepareupdate](./jetprepareupdate-function.md) mit der Option JET_prepInsertCopy im *prep* -Parameter aktiviert.
