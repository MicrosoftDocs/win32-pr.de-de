---
description: 'Weitere Informationen zu: Spalten'
title: Spalten
TOCTitle: Columns
ms:assetid: bc16ca4c-e3c9-43db-ac16-284d7cc0926d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294073(v=EXCHG.10)
ms:contentKeyID: 32765688
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 8cc7e3921c1904cdae3a09432d6a17eae3953251d3bd39c288cb6d6ffe184ffc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118982700"
---
# <a name="columns"></a>Spalten


_**Gilt für:** Windows | Windows Server_

## <a name="columns"></a>Spalten

Eine Tabelle kann entweder mit einem anfänglichen Satz von Spalten durch Aufrufen von [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) oder ohne einen anfänglichen Satz von Spalten durch Aufrufen von [JetCreateTable](./jetcreatetable-function.md)erstellt werden. Tabellen in ESE können bis zu 127 Spalten fester Länge, 128 Spalten variabler Länge und 64.993 markierte Spalten enthalten. Spalten werden anhand ihres Namens und ihrer ID identifiziert und können der Tabelle mit [JetAddColumn](./jetaddcolumn-function.md)dynamisch hinzugefügt werden. Spalten werden mit einem bestimmten Datentyp und einem optionalen Satz von Attributen erstellt, z. B. ob die Spalte eine feste Länge aufweist oder null sein kann.

Der Typ einer Spalte bestimmt die Daten, die in der Spalte gespeichert werden können, sowie viele der Eigenschaften der Spalte, einschließlich ihrer Reihenfolge für die Indizierung. ESE unterstützt eine Vielzahl von Spaltentypen mit einer Größe von 1 Bit bis 2 GB (2146483647 ASCII-Zeichen oder 1073741823 Unicode-Zeichen). Eine vollständige Liste der von ESE unterstützten Spaltendatentypen finden Sie im [Thema JET_COLTYP.](./jet-coltyp.md) In den folgenden Themen werden einige der spaltentypen erläutert, die von ESE unterstützt werden:

  - [Markierte, feste und variable Spalten](./tagged-fixed-and-variable-columns.md)

  - [Spalten "Version", "Auto-Increment" und "Escrow"](./version-auto-increment-and-escrow-columns.md)

  - [Spalten mit langen Werten](./long-value-columns.md)

  - [Mehrwertige Sparsespalten](./multi-valued-sparse-columns.md)

  - [Benutzerdefinierte Spalten](./user-defined-columns.md)

  - [Verwenden von Spalten in einer Tabelle](./using-columns-in-a-table.md)
