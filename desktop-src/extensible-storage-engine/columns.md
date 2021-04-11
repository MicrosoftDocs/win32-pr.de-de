---
description: 'Weitere Informationen: Spalten'
title: Spalten
TOCTitle: Columns
ms:assetid: bc16ca4c-e3c9-43db-ac16-284d7cc0926d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294073(v=EXCHG.10)
ms:contentKeyID: 32765688
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 86f7d2bbb3925434ddbfff52e987b6e408af9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130208"
---
# <a name="columns"></a>Spalten


_**Gilt für:** Windows | Windows Server_

## <a name="columns"></a>Spalten

Eine Tabelle kann entweder mit einem anfänglichen Satz von Spalten erstellt werden, indem [jetcreatetablecolumnindex](./jetcreatetablecolumnindex-function.md) aufgerufen wird, oder ohne eine anfängliche Gruppe von Spalten durch Aufrufen von [jetcreatetable](./jetcreatetable-function.md). Tabellen in ESE können bis zu 127 Spalten fester Länge, 128 Spalten variabler Länge und 64.993 markierte Spalten enthalten. Spalten werden anhand ihres Namens und ihrer ID identifiziert und können der Tabelle mit [jetaddcolumn](./jetaddcolumn-function.md)dynamisch hinzugefügt werden. Spalten werden mit einem bestimmten Datentyp und einem optionalen Satz von Attributen erstellt, z. b. ob die Spalte eine festgelegte Länge hat oder ob Sie NULL sein darf oder nicht.

Der Typ einer Spalte bestimmt die Daten, die in der Spalte gespeichert werden können, sowie viele der Eigenschaften der Spalte, einschließlich der Reihenfolge der Indizierung. ESE unterstützt eine breite Palette von Spaltentypen mit einer Größe von 1 bis 2 GB (2146483647 ASCII-Zeichen oder 1073741823 Unicode-Zeichen). Eine umfassende Liste der Spaltendatentypen, die von ESE unterstützt werden, finden Sie im [JET_COLTYP](./jet-coltyp.md) Thema. In den folgenden Themen werden einige der Spaltentypen erläutert, die von ESE unterstützt werden:

  - [Markierte, fixierte und Variablen Spalten](./tagged-fixed-and-variable-columns.md)

  - [Versions-, automatische Inkrement-und hinterlegte Spalten](./version-auto-increment-and-escrow-columns.md)

  - [Lange Wert Spalten](./long-value-columns.md)

  - [Mehrwertige Spalten mit geringer Dichte](./multi-valued-sparse-columns.md)

  - [Benutzerdefinierte Spalten](./user-defined-columns.md)

  - [Verwenden von Spalten in einer Tabelle](./using-columns-in-a-table.md)
