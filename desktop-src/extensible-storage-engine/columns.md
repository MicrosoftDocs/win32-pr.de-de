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
# <a name="columns"></a><span data-ttu-id="c8699-103">Spalten</span><span class="sxs-lookup"><span data-stu-id="c8699-103">Columns</span></span>


<span data-ttu-id="c8699-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c8699-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="columns"></a><span data-ttu-id="c8699-105">Spalten</span><span class="sxs-lookup"><span data-stu-id="c8699-105">Columns</span></span>

<span data-ttu-id="c8699-106">Eine Tabelle kann entweder mit einem anfänglichen Satz von Spalten erstellt werden, indem [jetcreatetablecolumnindex](./jetcreatetablecolumnindex-function.md) aufgerufen wird, oder ohne eine anfängliche Gruppe von Spalten durch Aufrufen von [jetcreatetable](./jetcreatetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="c8699-106">A table can be created either with an initial set of columns by calling [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) or without an initial set of columns by calling [JetCreateTable](./jetcreatetable-function.md).</span></span> <span data-ttu-id="c8699-107">Tabellen in ESE können bis zu 127 Spalten fester Länge, 128 Spalten variabler Länge und 64.993 markierte Spalten enthalten.</span><span class="sxs-lookup"><span data-stu-id="c8699-107">Tables in ESE can contain up to 127 fixed-length columns, 128 variable-length columns, and 64,993 tagged columns.</span></span> <span data-ttu-id="c8699-108">Spalten werden anhand ihres Namens und ihrer ID identifiziert und können der Tabelle mit [jetaddcolumn](./jetaddcolumn-function.md)dynamisch hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c8699-108">Columns are identified by their name and ID and can be dynamically added to the table with [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="c8699-109">Spalten werden mit einem bestimmten Datentyp und einem optionalen Satz von Attributen erstellt, z. b. ob die Spalte eine festgelegte Länge hat oder ob Sie NULL sein darf oder nicht.</span><span class="sxs-lookup"><span data-stu-id="c8699-109">Columns are created with a specific data type and an optional set of attributes, such as whether the column is fixed-length or whether it can be NULL or not.</span></span>

<span data-ttu-id="c8699-110">Der Typ einer Spalte bestimmt die Daten, die in der Spalte gespeichert werden können, sowie viele der Eigenschaften der Spalte, einschließlich der Reihenfolge der Indizierung.</span><span class="sxs-lookup"><span data-stu-id="c8699-110">The type of a column determines the data that may be stored in the column and many of the properties of the column, including its order for indexing.</span></span> <span data-ttu-id="c8699-111">ESE unterstützt eine breite Palette von Spaltentypen mit einer Größe von 1 bis 2 GB (2146483647 ASCII-Zeichen oder 1073741823 Unicode-Zeichen).</span><span class="sxs-lookup"><span data-stu-id="c8699-111">ESE supports a wide range of column types, ranging in size from 1 bit to 2 GB (2146483647 ASCII characters or 1073741823 Unicode characters).</span></span> <span data-ttu-id="c8699-112">Eine umfassende Liste der Spaltendatentypen, die von ESE unterstützt werden, finden Sie im [JET_COLTYP](./jet-coltyp.md) Thema.</span><span class="sxs-lookup"><span data-stu-id="c8699-112">For a complete list of the column data types supported by ESE, see the [JET_COLTYP](./jet-coltyp.md) topic.</span></span> <span data-ttu-id="c8699-113">In den folgenden Themen werden einige der Spaltentypen erläutert, die von ESE unterstützt werden:</span><span class="sxs-lookup"><span data-stu-id="c8699-113">The topics below discuss a few of the columns types supported by ESE:</span></span>

  - [<span data-ttu-id="c8699-114">Markierte, fixierte und Variablen Spalten</span><span class="sxs-lookup"><span data-stu-id="c8699-114">Tagged, Fixed and Variable Columns</span></span>](./tagged-fixed-and-variable-columns.md)

  - [<span data-ttu-id="c8699-115">Versions-, automatische Inkrement-und hinterlegte Spalten</span><span class="sxs-lookup"><span data-stu-id="c8699-115">Version, Auto-Increment and Escrow Columns</span></span>](./version-auto-increment-and-escrow-columns.md)

  - [<span data-ttu-id="c8699-116">Lange Wert Spalten</span><span class="sxs-lookup"><span data-stu-id="c8699-116">Long Value Columns</span></span>](./long-value-columns.md)

  - [<span data-ttu-id="c8699-117">Mehrwertige Spalten mit geringer Dichte</span><span class="sxs-lookup"><span data-stu-id="c8699-117">Multi-Valued Sparse Columns</span></span>](./multi-valued-sparse-columns.md)

  - [<span data-ttu-id="c8699-118">Benutzerdefinierte Spalten</span><span class="sxs-lookup"><span data-stu-id="c8699-118">User Defined Columns</span></span>](./user-defined-columns.md)

  - [<span data-ttu-id="c8699-119">Verwenden von Spalten in einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="c8699-119">Using Columns in a Table</span></span>](./using-columns-in-a-table.md)
