---
description: Weitere Informationen finden Sie unter Verwenden von Spalten in einer Tabelle.
title: Verwenden von Spalten in einer Tabelle
TOCTitle: Using Columns in a Table
ms:assetid: 064ac59e-d306-4335-a623-754a003f5ebc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269178(v=EXCHG.10)
ms:contentKeyID: 32765481
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 332cca1c64c851ded44951fc9bb7f68ebd9f6818030cefeb8406f965a1bd5d6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471300"
---
# <a name="using-columns-in-a-table"></a>Verwenden von Spalten in einer Tabelle


_**Gilt für:** Windows | Windows Server_

## <a name="using-columns-in-a-table"></a>Verwenden von Spalten in einer Tabelle

Eine Tabelle kann mit einem anfänglichen Satz von Spalten durch Aufrufen von [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) oder ohne Spalten durch Aufrufen von [JetCreateTable](./jetcreatetable-function.md)erstellt werden. Wenn die Tabelle mit einem anfänglichen Satz von Spalten im Aufruf von [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) oder [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)erstellt wird, enthält sie eine [JET_TABLECREATE](./jet-tablecreate-structure.md) -Struktur (oder [JET_TABLECREATE2](./jet-tablecreate2-structure.md)). Diese Strukturen enthalten ein Array von [JET_COLUMNCREATE](./jet-columncreate-structure.md) Strukturen, die den Satz von Spalten in der Tabelle definieren. Der **grbit-Member** legt die Optionen für die Spalte fest, und der **Coltypmember** legt den Datentyp fest, der in der Spalte festgelegt werden kann.

Wenn die Tabelle ohne Spalten erstellt wird, müssen sie durch Aufrufen von [JetAddColumn](./jetaddcolumn-function.md) mit der [JET_COLUMNDEF-Struktur](./jet-columndef-structure.md) hinzugefügt werden. Der **grbit-Member** der [JET_COLUMNDEF-Struktur](./jet-columndef-structure.md) legt die Optionen für die Spalte fest, und der **Coltypmember** legt den Datentyp fest, der in der Spalte festgelegt werden kann. Standardspaltenwerte werden im Aufruf von [JetAddColumn](./jetaddcolumn-function.md) festgelegt, indem ein Wert im *pvDefault-Parameter* und die Größe im *cbDefault-Parameter* angegeben werden. Eine Spalte ohne Standardwert weist effektiv den Standardwert NULL auf.

Die Werte in der Tabelle können nur im Kontext einer Transaktion festgelegt werden. Die Transaktion beginnt beim Aufruf von [JetBeginTransaction](./jetbegintransaction-function.md) und endet mit dem Aufruf von [JetCommitTransaction.](./jetcommittransaction-function.md) Innerhalb der Transaktion kann ein einzelner Spaltenwert durch Aufrufen von [JetSetColumn](./jetsetcolumn-function.md)festgelegt werden, oder mehrere Spaltenwerte können durch Aufrufen von [JetSetColumns](./jetsetcolumns-function.md)festgelegt werden. [JetSetColumns](./jetsetcolumns-function.md) verwendet ein Array von [JET_SETCOLUMN](./jet-setcolumn-structure.md) Strukturen, um mehrere Spalten in der Tabelle festzulegen. Die Daten sind im *pvData-Parameter* von [JetSetColumn](./jetsetcolumn-function.md)oder im **pvData-Member** in [JET_SETCOLUMN-Struktur](./jet-setcolumn-structure.md) enthalten.

Die [strukturen JET_COLUMNBASE](./jet-columnbase-structure.md), [JET_COLUMNLIST](./jet-columnlist-structure.md)und [JET_COLUMNDEF](./jet-columndef-structure.md) werden in den Aufrufen von [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)und [JetGetColumnInfo](./jetgetcolumninfo-function.md) abhängig vom Typ der abgerufenen Spalte zurückgegeben. Die [JET_COLUMNBASE-Struktur](./jet-columnbase-structure.md) beschreibt die Parameter der Basisspalte, und die [JET_COLUMNLIST](./jet-columnlist-structure.md) enthält die Informationen, die zum Durchlaufen der temporären Tabelle erforderlich sind, die von den [JetGetColumnInfo-](./jetgetcolumninfo-function.md) und [JetGetTableColumnInfo-Funktionen](./jetgettablecolumninfo-function.md) erstellt wird.
