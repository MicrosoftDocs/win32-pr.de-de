---
description: Die odbcsourceattribute-Tabelle enthält Informationen zu den Attributen von Datenquellen.
ms.assetid: 8ee50fd7-507e-484f-9a16-de5449470562
title: Odbcsourceattribute-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52dd9636ac19eae0fb3a9e41d1a1c8389753e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525772"
---
# <a name="odbcsourceattribute-table"></a><span data-ttu-id="f2352-103">Odbcsourceattribute-Tabelle</span><span class="sxs-lookup"><span data-stu-id="f2352-103">ODBCSourceAttribute Table</span></span>

<span data-ttu-id="f2352-104">Die odbcsourceattribute-Tabelle enthält Informationen zu den Attributen von Datenquellen.</span><span class="sxs-lookup"><span data-stu-id="f2352-104">The ODBCSourceAttribute table contains information about the attributes of data sources.</span></span>

<span data-ttu-id="f2352-105">Die odbcsourceattribute-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="f2352-105">The ODBCSourceAttribute table has the following columns.</span></span>



| <span data-ttu-id="f2352-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="f2352-106">Column</span></span>       | <span data-ttu-id="f2352-107">Typ</span><span class="sxs-lookup"><span data-stu-id="f2352-107">Type</span></span>                         | <span data-ttu-id="f2352-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="f2352-108">Key</span></span> | <span data-ttu-id="f2352-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="f2352-109">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="f2352-110">DataSource\_</span><span class="sxs-lookup"><span data-stu-id="f2352-110">DataSource\_</span></span> | [<span data-ttu-id="f2352-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="f2352-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="f2352-112">J</span><span class="sxs-lookup"><span data-stu-id="f2352-112">Y</span></span>   | <span data-ttu-id="f2352-113">N</span><span class="sxs-lookup"><span data-stu-id="f2352-113">N</span></span>        |
| <span data-ttu-id="f2352-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="f2352-114">Attribute</span></span>    | [<span data-ttu-id="f2352-115">Text</span><span class="sxs-lookup"><span data-stu-id="f2352-115">Text</span></span>](text.md)             | <span data-ttu-id="f2352-116">J</span><span class="sxs-lookup"><span data-stu-id="f2352-116">Y</span></span>   | <span data-ttu-id="f2352-117">N</span><span class="sxs-lookup"><span data-stu-id="f2352-117">N</span></span>        |
| <span data-ttu-id="f2352-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f2352-118">Value</span></span>        | [<span data-ttu-id="f2352-119">Großformatige</span><span class="sxs-lookup"><span data-stu-id="f2352-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="f2352-120">N</span><span class="sxs-lookup"><span data-stu-id="f2352-120">N</span></span>   | <span data-ttu-id="f2352-121">J</span><span class="sxs-lookup"><span data-stu-id="f2352-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f2352-122">Spalten</span><span class="sxs-lookup"><span data-stu-id="f2352-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f2352-123"><span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>DataSource\_</span><span class="sxs-lookup"><span data-stu-id="f2352-123"><span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>DataSource\_</span></span>
</dt> <dd>

<span data-ttu-id="f2352-124">Interner Tokenname für die Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="f2352-124">Internal token name for data source.</span></span> <span data-ttu-id="f2352-125">Ein Primärschlüssel für die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f2352-125">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="f2352-126"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Versehen</span><span class="sxs-lookup"><span data-stu-id="f2352-126"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="f2352-127">Name des Datenquellen Attributs.</span><span class="sxs-lookup"><span data-stu-id="f2352-127">Name of data source attribute.</span></span> <span data-ttu-id="f2352-128">Ein Primärschlüssel für die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f2352-128">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="f2352-129"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert</span><span class="sxs-lookup"><span data-stu-id="f2352-129"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="f2352-130">Der lokalisierbare Zeichen folgen Wert für das Attribut.</span><span class="sxs-lookup"><span data-stu-id="f2352-130">The localizable string value for the attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2352-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2352-131">Remarks</span></span>

<span data-ttu-id="f2352-132">Die Informationen in dieser Tabelle werden durch die [installlodbc](installodbc-action.md) -und [removeodbc](removeodbc-action.md) -Aktionen in [*Sequenz Tabellen*](s-gly.md) verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f2352-132">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="f2352-133">Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f2352-133">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="f2352-134">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="f2352-134">Validation</span></span>

<dl>

[<span data-ttu-id="f2352-135">ICE03</span><span class="sxs-lookup"><span data-stu-id="f2352-135">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f2352-136">ICE06</span><span class="sxs-lookup"><span data-stu-id="f2352-136">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f2352-137">ICE32</span><span class="sxs-lookup"><span data-stu-id="f2352-137">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="f2352-138">ICE46</span><span class="sxs-lookup"><span data-stu-id="f2352-138">ICE46</span></span>](ice46.md)  
</dl>

 

 



