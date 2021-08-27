---
description: 'Weitere Informationen finden Sie unter: Mehrwertige Sparsespalten'
title: Mehrwertige Sparsespalten
TOCTitle: Multi-Valued Sparse Columns
ms:assetid: 36e82a73-aad4-4e0d-a743-a2182c41fe9c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269225(v=EXCHG.10)
ms:contentKeyID: 32765527
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 21dbe18be8be26af9fe32d9b80cbd5744c172793e27701d46438df4d63dcf395
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115580"
---
# <a name="multi-valued-sparse-columns"></a>Mehrwertige Sparsespalten


_**Gilt für:** Windows | Windows Server_

## <a name="multi-valued-sparse-columns"></a>Mehrwertige Sparsespalten

Sparsespalten können eine feste oder variable Länge haben und eindeutig sein, da sie keinen Speicherplatz in einem Datensatz benötigen, wenn sie NULL sind oder ihren Standardwert verlassen. Sparsespalten, auch als markierte Spalten bezeichnet, können mehr als einen Wert in einem einzelnen Datensatz enthalten. Gekennzeichnete Spalten können alle Spaltentypen sein, die in den JET_coltyp [beschrieben](./jet-coltyp.md) werden. Sie werden erstellt, wenn die Spalte der Tabelle hinzugefügt wird, indem sie das JET_bitColumnTagged-Flag in der [JET_COLUMNDEF-Struktur](./jet-columndef-structure.md) im Aufruf von [JetAddColumn](./jetaddcolumn-function.md)oder in der [JET_COLUMNCREATE-Struktur](./jet-columncreate-structure.md) festlegen, die im Aufruf von [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) oder [JetCreateTableColumnIndex2 verwendet wird.](./jetcreatetablecolumnindex2-function.md) Spalten vom Typ JET_coltypLongText und JET_coltypLongBinary werden automatisch als markierte Spalten erstellt.

Nur markierte Spalten können mehrere Werte in einem Datensatz enthalten, Spalten mit fester oder variabler Länge dürfen nicht mehrere Werte enthalten. Es gibt zwei Typen von mehrwertigen Spalten:

  - Markierte Spalten sind standardmäßig mehrwertige Spalten. Wenn der Spalte ein zweiter Wert hinzugefügt wird, wird er automatisch mehrwertig.

  - Markierte Spalten, die mit der Option JET_bitColumnMultiValued in [der](./jet-columndef-structure.md) JET_COLUMNDEF struktur im Aufruf von [JetAddColumn erstellt werden.](./jetaddcolumn-function.md)

Die JET_bitColumnMultiValued option ändert die Art und Weise, wie die Spalte indiziert wird. Mehrwertige Spalten mit der JET_bitColumnMultiValued werden umfangreicher indiziert als markierte mehrwertige Spalten. Diese Spalten werden über alle Werte in der mehrwertigen Spalte indiziert, wohingegen markierte mehrwertige Spalten nur über den ersten Wert in der mehrwertigen Spalte indiziert werden. Stellen Sie sich beispielsweise eine mehrwertige Spalte vor, in der JET_bitColumnMultiValued Option festgelegt ist und dies die erste mehrwertige Spalte in einem Index ist. Diese Spalte enthält drei Werte: A, B und C. Ein Index für diese Spalte enthält Einträge für alle drei Werte A, B und C. Wenn die JET_bitColumnMultiValued nicht festgelegt wurde, enthält der Index für diese Spalte nur den ersten Wert, A, im Index.
