---
description: 'Weitere Informationen: Verwenden von Spalten in einer Tabelle'
title: Verwenden von Spalten in einer Tabelle
TOCTitle: Using Columns in a Table
ms:assetid: 064ac59e-d306-4335-a623-754a003f5ebc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269178(v=EXCHG.10)
ms:contentKeyID: 32765481
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: cd715b171162f63aaf0772ff6ec2e4a6d057a0d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350470"
---
# <a name="using-columns-in-a-table"></a>Verwenden von Spalten in einer Tabelle


_**Gilt für:** Windows | Windows Server_

## <a name="using-columns-in-a-table"></a>Verwenden von Spalten in einer Tabelle

Eine Tabelle kann mit einem anfänglichen Satz von Spalten erstellt werden, indem [jetcreatetablecolumnindex](./jetcreatetablecolumnindex-function.md) oder ohne Spalten aufgerufen wird, indem [jetcreatetable](./jetcreatetable-function.md)aufgerufen wird. Wenn die Tabelle mit einem anfänglichen Satz von Spalten im Aufrufen von [jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md) oder [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)erstellt wird, enthält Sie eine [JET_TABLECREATE](./jet-tablecreate-structure.md) Struktur (oder [JET_TABLECREATE2](./jet-tablecreate2-structure.md)Struktur). Diese Strukturen enthalten ein Array von [JET_COLUMNCREATE](./jet-columncreate-structure.md) Strukturen, die den Satz von Spalten in der Tabelle definieren. Der **grbit** -Member legt die Optionen für die Spalte fest, und der **colttmember** legt den Datentyp fest, der in der Spalte festgelegt werden kann.

Wenn die Tabelle ohne Spalten erstellt wird, müssen Sie durch Aufrufen von [jetaddcolumn](./jetaddcolumn-function.md) mit der [JET_COLUMNDEF](./jet-columndef-structure.md) -Struktur hinzugefügt werden. Der **grbit** -Member der [JET_COLUMNDEF](./jet-columndef-structure.md) Struktur legt die Optionen für die Spalte fest, und der **colttmember** legt den Datentyp fest, der in der Spalte festgelegt werden kann. Standard Spaltenwerte werden im Aufrufen von [jetaddcolumn](./jetaddcolumn-function.md) festgelegt, indem ein Wert im *pvdefault* -Parameter und die Größe im *cbdefault* -Parameter angegeben wird. Eine Spalte ohne Standardwert weist einen Standardwert von NULL auf.

Die Werte in der Tabelle können nur innerhalb des Kontexts einer Transaktion festgelegt werden. Die Transaktion beginnt im Aufrufen von [jetbegintransaction](./jetbegintransaction-function.md) und endet mit dem Aufrufen von [jetcommittransaction](./jetcommittransaction-function.md). Innerhalb der Transaktion kann ein einzelner Spaltenwert durch Aufrufen von [jetsetcolumn](./jetsetcolumn-function.md)festgelegt werden, oder es können mehrere Spaltenwerte durch Aufrufen von [jetsetcolumns](./jetsetcolumns-function.md)festgelegt werden. [Jetsetcolumns](./jetsetcolumns-function.md) verwendet ein Array von [JET_SETCOLUMN](./jet-setcolumn-structure.md) Strukturen, um mehrere Spalten in der Tabelle festzulegen. Die Daten sind im *pvData* -Parameter von [jetsetcolumn](./jetsetcolumn-function.md)oder dem **pvData** -Member in [JET_SETCOLUMN](./jet-setcolumn-structure.md) Struktur enthalten.

Die [JET_COLUMNBASE](./jet-columnbase-structure.md)-, [JET_COLUMNLIST](./jet-columnlist-structure.md)-und [JET_COLUMNDEF](./jet-columndef-structure.md) -Strukturen werden in den Aufrufen von [jetgettablecolumninfo](./jetgettablecolumninfo-function.md)und [jetgetcolumninfo](./jetgetcolumninfo-function.md) zurückgegeben, abhängig vom Typ der abgerufenen Spalte. Die [JET_COLUMNBASE](./jet-columnbase-structure.md) Struktur beschreibt die Parameter der Basis Spalte, und die [JET_COLUMNLIST](./jet-columnlist-structure.md) enthält die Informationen, die erforderlich sind, um die temporäre Tabelle zu durchlaufen, die von den Funktionen [jetgetcolumninfo](./jetgetcolumninfo-function.md) und [jetgettablecolumninfo](./jetgettablecolumninfo-function.md) erstellt wird.
