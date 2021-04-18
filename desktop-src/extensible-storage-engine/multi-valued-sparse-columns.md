---
description: 'Weitere Informationen: mehrwertige Spalten mit geringer Dichte'
title: Mehrwertige Spalten mit geringer Dichte
TOCTitle: Multi-Valued Sparse Columns
ms:assetid: 36e82a73-aad4-4e0d-a743-a2182c41fe9c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269225(v=EXCHG.10)
ms:contentKeyID: 32765527
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 21448d50e17881517086c1b258dcce02e84286a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359096"
---
# <a name="multi-valued-sparse-columns"></a>Mehrwertige Spalten mit geringer Dichte


_**Gilt für:** Windows | Windows Server_

## <a name="multi-valued-sparse-columns"></a>Mehrwertige Spalten mit geringer Dichte

Spalten mit geringer Dichte können eine fest-oder Variablen Länge aufweisen und sind insofern eindeutig, als Sie keinen Speicherplatz in einem Datensatz belegen, wenn Sie NULL sind oder bis zum Standardwert liegen. Sparsespalten (auch als markierte Spalten bezeichnet) können mehr als einen Wert in einem einzelnen Datensatz enthalten. Markierte Spalten können einer der Spaltentypen sein, die in den [JET_coltyp](./jet-coltyp.md) Konstanten beschrieben werden. Sie werden erstellt, wenn die Spalte der Tabelle hinzugefügt wird, indem das JET_bitColumnTagged-Flag in der [JET_COLUMNDEF](./jet-columndef-structure.md) Struktur im Aufrufen von [jetaddcolumn](./jetaddcolumn-function.md)festgelegt wird, oder in der [JET_COLUMNCREATE](./jet-columncreate-structure.md) Struktur, die im Aufrufen von [jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md) oder [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)verwendet wird. Spalten vom Typ JET_coltypLongText und JET_coltypLongBinary werden automatisch als markierte Spalten erstellt.

Nur markierte Spalten können mehrere Werte in einem Datensatz enthalten, Spalten mit fester oder variabler Länge dürfen nicht mehrere Werte enthalten. Es gibt zwei Typen von mehrwertigen Spalten:

  - Markierte Spalten sind standardmäßig mehr wertig. Wenn der Spalte ein zweiter Wert hinzugefügt wird, wird dieser automatisch mehr wertig.

  - Markierte Spalten, die mit der Option JET_bitColumnMultiValued in der [JET_COLUMNDEF](./jet-columndef-structure.md) Struktur im Befehl [jetaddcolumn](./jetaddcolumn-function.md)erstellt werden.

Die Option JET_bitColumnMultiValued ändert die Art und Weise, in der die Spalte indiziert wird. Mehrwertige Spalten mit der JET_bitColumnMultiValued-Option werden ausführlicher indiziert als markierte mehrwertige Spalten. Diese Spalten werden über alle Werte in der mehrwertigen Spalte indiziert, während markierte mehrwertige Spalten nur über den ersten Wert in der mehrwertigen Spalte indiziert werden. Stellen Sie sich beispielsweise eine mehrwertige Spalte vor, in der die JET_bitColumnMultiValued-Option festgelegt ist und die erste mehrwertige Spalte in einem Index ist. Diese Spalte enthält drei Werte: A, B und C. Ein Index für diese Spalte enthält Einträge für alle drei Werte A, B und C. Wenn die JET_bitColumnMultiValued-Option nicht festgelegt wurde, enthält der Index für diese Spalte nur den ersten Wert (A) im Index.
