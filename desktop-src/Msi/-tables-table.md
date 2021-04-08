---
description: Die Tabellen \_ Tabelle ist eine schreibgeschützte Systemtabelle, in der alle Tabellen in der Datenbank aufgelistet sind. Fragen Sie diese Tabelle ab, um herauszufinden, ob eine Tabelle vorhanden ist.
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: _Tables Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2dc3ebafd969a07676f64f674f76c3e16ebe059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864544"
---
# <a name="_tables-table"></a><span data-ttu-id="d4dc9-104">\_Tabelle Tabellen</span><span class="sxs-lookup"><span data-stu-id="d4dc9-104">\_Tables Table</span></span>

<span data-ttu-id="d4dc9-105">Die Tabellen \_ Tabelle ist eine schreibgeschützte Systemtabelle, in der alle Tabellen in der Datenbank aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="d4dc9-105">The \_Tables table is a read-only system table that lists all the tables in the database.</span></span> <span data-ttu-id="d4dc9-106">Fragen Sie diese Tabelle ab, um herauszufinden, ob eine Tabelle vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d4dc9-106">Query this table to find out if a table exists.</span></span>

<span data-ttu-id="d4dc9-107">Die \_ Tabelle Tabellen weist die folgende Spalte auf.</span><span class="sxs-lookup"><span data-stu-id="d4dc9-107">The \_Tables Table has the following column.</span></span>



| <span data-ttu-id="d4dc9-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="d4dc9-108">Column</span></span> | <span data-ttu-id="d4dc9-109">Typ</span><span class="sxs-lookup"><span data-stu-id="d4dc9-109">Type</span></span>             | <span data-ttu-id="d4dc9-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="d4dc9-110">Key</span></span> | <span data-ttu-id="d4dc9-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="d4dc9-111">Nullable</span></span> |
|--------|------------------|-----|----------|
| <span data-ttu-id="d4dc9-112">Name</span><span class="sxs-lookup"><span data-stu-id="d4dc9-112">Name</span></span>   | [<span data-ttu-id="d4dc9-113">Text</span><span class="sxs-lookup"><span data-stu-id="d4dc9-113">Text</span></span>](text.md) | <span data-ttu-id="d4dc9-114">J</span><span class="sxs-lookup"><span data-stu-id="d4dc9-114">Y</span></span>   | <span data-ttu-id="d4dc9-115">N</span><span class="sxs-lookup"><span data-stu-id="d4dc9-115">N</span></span>        |



 

## <a name="column"></a><span data-ttu-id="d4dc9-116">Column</span><span class="sxs-lookup"><span data-stu-id="d4dc9-116">Column</span></span>

<dl> <dt>

<span data-ttu-id="d4dc9-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen</span><span class="sxs-lookup"><span data-stu-id="d4dc9-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="d4dc9-118">Der Name einer der Tabellen.</span><span class="sxs-lookup"><span data-stu-id="d4dc9-118">Name of one of the tables.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4dc9-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4dc9-119">Remarks</span></span>

<span data-ttu-id="d4dc9-120">Da die \_ Tabellen Tabelle eine Systemtabelle ist, die nicht über SQL-Abfragen geändert werden kann, können Sie die Primärschlüssel nicht mit der [**msidatabasegetprimarykeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) -Funktion oder der [**primarykeys-Eigenschaft**](database-primarykeys.md)abrufen.</span><span class="sxs-lookup"><span data-stu-id="d4dc9-120">Because the \_Tables table is a system table that cannot be modified through SQL queries, you cannot obtain the primary keys with the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function or the [**PrimaryKeys property**](database-primarykeys.md).</span></span>

 

 



