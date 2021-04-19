---
description: Die \_ columns-Tabelle ist eine schreibgeschützte Systemtabelle, die den Spalten Katalog enthält. Sie listet die Spalten für alle Tabellen auf. Sie können diese Tabelle Abfragen, um herauszufinden, ob eine bestimmte Spalte vorhanden ist.
ms.assetid: 1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf
title: _Columns Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d896f330e5fc2e13b5f172581341eb11a09617d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356117"
---
# <a name="_columns-table"></a><span data-ttu-id="a9f02-105">\_Columns-Tabelle</span><span class="sxs-lookup"><span data-stu-id="a9f02-105">\_Columns Table</span></span>

<span data-ttu-id="a9f02-106">Die \_ columns-Tabelle ist eine schreibgeschützte Systemtabelle, die den Spalten Katalog enthält.</span><span class="sxs-lookup"><span data-stu-id="a9f02-106">The \_Columns table is a read-only system table that contains the column catalog.</span></span> <span data-ttu-id="a9f02-107">Sie listet die Spalten für alle Tabellen auf.</span><span class="sxs-lookup"><span data-stu-id="a9f02-107">It lists the columns for all the tables.</span></span> <span data-ttu-id="a9f02-108">Sie können diese Tabelle Abfragen, um herauszufinden, ob eine bestimmte Spalte vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a9f02-108">You can query this table to find out if a given column exists.</span></span>

<span data-ttu-id="a9f02-109">Die \_ Spalten Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="a9f02-109">The \_Columns table has the following columns.</span></span>



| <span data-ttu-id="a9f02-110">Spalte</span><span class="sxs-lookup"><span data-stu-id="a9f02-110">Column</span></span> | <span data-ttu-id="a9f02-111">Typ</span><span class="sxs-lookup"><span data-stu-id="a9f02-111">Type</span></span>                   | <span data-ttu-id="a9f02-112">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="a9f02-112">Key</span></span> | <span data-ttu-id="a9f02-113">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="a9f02-113">Nullable</span></span> |
|--------|------------------------|-----|----------|
| <span data-ttu-id="a9f02-114">Tabelle</span><span class="sxs-lookup"><span data-stu-id="a9f02-114">Table</span></span>  | [<span data-ttu-id="a9f02-115">Text</span><span class="sxs-lookup"><span data-stu-id="a9f02-115">Text</span></span>](text.md)       | <span data-ttu-id="a9f02-116">J</span><span class="sxs-lookup"><span data-stu-id="a9f02-116">Y</span></span>   | <span data-ttu-id="a9f02-117">N</span><span class="sxs-lookup"><span data-stu-id="a9f02-117">N</span></span>        |
| <span data-ttu-id="a9f02-118">Number</span><span class="sxs-lookup"><span data-stu-id="a9f02-118">Number</span></span> | [<span data-ttu-id="a9f02-119">Integer</span><span class="sxs-lookup"><span data-stu-id="a9f02-119">Integer</span></span>](integer.md) | <span data-ttu-id="a9f02-120">J</span><span class="sxs-lookup"><span data-stu-id="a9f02-120">Y</span></span>   | <span data-ttu-id="a9f02-121">N</span><span class="sxs-lookup"><span data-stu-id="a9f02-121">N</span></span>        |
| <span data-ttu-id="a9f02-122">Name</span><span class="sxs-lookup"><span data-stu-id="a9f02-122">Name</span></span>   | [<span data-ttu-id="a9f02-123">Text</span><span class="sxs-lookup"><span data-stu-id="a9f02-123">Text</span></span>](text.md)       | <span data-ttu-id="a9f02-124">N</span><span class="sxs-lookup"><span data-stu-id="a9f02-124">N</span></span>   | <span data-ttu-id="a9f02-125">N</span><span class="sxs-lookup"><span data-stu-id="a9f02-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a9f02-126">Spalten</span><span class="sxs-lookup"><span data-stu-id="a9f02-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a9f02-127"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Glaub</span><span class="sxs-lookup"><span data-stu-id="a9f02-127"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="a9f02-128">Der Name der Tabelle, die die Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="a9f02-128">The name of the table that contains the column.</span></span>

</dd> <dt>

<span data-ttu-id="a9f02-129"><span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Einigen</span><span class="sxs-lookup"><span data-stu-id="a9f02-129"><span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Number</span></span>
</dt> <dd>

<span data-ttu-id="a9f02-130">Die Reihenfolge der Spalte in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a9f02-130">The order of the column within the table.</span></span>

</dd> <dt>

<span data-ttu-id="a9f02-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen</span><span class="sxs-lookup"><span data-stu-id="a9f02-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="a9f02-132">Der Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="a9f02-132">The name of the column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9f02-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9f02-133">Remarks</span></span>

<span data-ttu-id="a9f02-134">Da die \_ columns-Tabelle eine Systemtabelle ist, die nicht über SQL-Abfragen geändert werden kann, können Sie die Primärschlüssel nicht mit der [**msidatabasegetprimarykeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) -Funktion oder der [**primarykeys-Eigenschaft**](database-primarykeys.md)abrufen.</span><span class="sxs-lookup"><span data-stu-id="a9f02-134">Because the \_Columns table is a system table that cannot be modified through SQL queries, you cannot obtain the primary keys with the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function or the [**PrimaryKeys property**](database-primarykeys.md).</span></span>

<span data-ttu-id="a9f02-135">Nur persistente Spalten werden in der \_ Spalten Tabelle gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a9f02-135">Only persistent columns are stored in the \_Columns table.</span></span> <span data-ttu-id="a9f02-136">Wenn Sie ermitteln möchten, ob eine temporäre Spalte vorhanden ist, müssen Sie eine Sicht mit einer SELECT- \* Anweisung für die Tabelle erstellen und dann alle Felder in einem Datensatz durchlaufen, der von der [**msiviewgetcolumninfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) -Funktion mit der msicolinfo Names-Option zurückgegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="a9f02-136">To determine if a temporary column exists one would need to create a view using a SELECT \* statement against the table, then loop through all fields in a record returned by the [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) function with the MSICOLINFO\_NAMES option.</span></span>

 

 



