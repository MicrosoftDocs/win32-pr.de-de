---
description: Die odbingtribute-Tabelle enthält Informationen zu den Attributen der Open Database Connectivity (ODBC)-Treiber und-Konvertierer.
ms.assetid: 82fd83d4-22dd-4641-807b-d2b263918e4c
title: Odbingtribute-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e76a52dd63bdc8eb969324f7891e7359be7caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130285"
---
# <a name="odbcattribute-table"></a><span data-ttu-id="40590-103">Odbingtribute-Tabelle</span><span class="sxs-lookup"><span data-stu-id="40590-103">ODBCAttribute Table</span></span>

<span data-ttu-id="40590-104">Die odbingtribute-Tabelle enthält Informationen zu den Attributen der Open Database Connectivity (ODBC)-Treiber und-Konvertierer.</span><span class="sxs-lookup"><span data-stu-id="40590-104">The ODBCAttribute table contains information about the attributes of Open Database Connectivity (ODBC) drivers and translators.</span></span>

<span data-ttu-id="40590-105">Die odbingtribute-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="40590-105">The ODBCAttribute table has the following columns.</span></span>



| <span data-ttu-id="40590-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="40590-106">Column</span></span>    | <span data-ttu-id="40590-107">Typ</span><span class="sxs-lookup"><span data-stu-id="40590-107">Type</span></span>                         | <span data-ttu-id="40590-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="40590-108">Key</span></span> | <span data-ttu-id="40590-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="40590-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="40590-110">Treiber\_</span><span class="sxs-lookup"><span data-stu-id="40590-110">Driver\_</span></span>  | [<span data-ttu-id="40590-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="40590-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="40590-112">J</span><span class="sxs-lookup"><span data-stu-id="40590-112">Y</span></span>   | <span data-ttu-id="40590-113">N</span><span class="sxs-lookup"><span data-stu-id="40590-113">N</span></span>        |
| <span data-ttu-id="40590-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="40590-114">Attribute</span></span> | [<span data-ttu-id="40590-115">Text</span><span class="sxs-lookup"><span data-stu-id="40590-115">Text</span></span>](text.md)             | <span data-ttu-id="40590-116">J</span><span class="sxs-lookup"><span data-stu-id="40590-116">Y</span></span>   | <span data-ttu-id="40590-117">N</span><span class="sxs-lookup"><span data-stu-id="40590-117">N</span></span>        |
| <span data-ttu-id="40590-118">Wert</span><span class="sxs-lookup"><span data-stu-id="40590-118">Value</span></span>     | [<span data-ttu-id="40590-119">Großformatige</span><span class="sxs-lookup"><span data-stu-id="40590-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="40590-120">N</span><span class="sxs-lookup"><span data-stu-id="40590-120">N</span></span>   | <span data-ttu-id="40590-121">J</span><span class="sxs-lookup"><span data-stu-id="40590-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="40590-122">Spalten</span><span class="sxs-lookup"><span data-stu-id="40590-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="40590-123"><span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Trei\_</span><span class="sxs-lookup"><span data-stu-id="40590-123"><span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Driver\_</span></span>
</dt> <dd>

<span data-ttu-id="40590-124">Interner Tokenname für einen Treiber.</span><span class="sxs-lookup"><span data-stu-id="40590-124">Internal token name for a driver.</span></span> <span data-ttu-id="40590-125">Ein Primärschlüssel für die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="40590-125">A primary key for the table.</span></span> <span data-ttu-id="40590-126">Ein Fremdschlüssel in der [odbcdriver-Tabelle](odbcdriver-table.md).</span><span class="sxs-lookup"><span data-stu-id="40590-126">A foreign key into the [ODBCDriver table](odbcdriver-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="40590-127"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Versehen</span><span class="sxs-lookup"><span data-stu-id="40590-127"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="40590-128">Der Name des Treiber Attributs.</span><span class="sxs-lookup"><span data-stu-id="40590-128">Name of the driver attribute.</span></span> <span data-ttu-id="40590-129">Ein Primärschlüssel für die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="40590-129">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="40590-130"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert</span><span class="sxs-lookup"><span data-stu-id="40590-130"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="40590-131">Lokalisier barer Zeichen folgen Wert für das Attribut.</span><span class="sxs-lookup"><span data-stu-id="40590-131">Localizable string value for attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40590-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40590-132">Remarks</span></span>

<span data-ttu-id="40590-133">Die Informationen in dieser Tabelle werden durch die [installlodbc](installodbc-action.md) -und [removeodbc](removeodbc-action.md) -Aktionen in [*Sequenz Tabellen*](s-gly.md) verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="40590-133">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="40590-134">Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="40590-134">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="40590-135">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="40590-135">Validation</span></span>

<dl>

[<span data-ttu-id="40590-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="40590-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="40590-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="40590-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="40590-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="40590-138">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="40590-139">ICE46</span><span class="sxs-lookup"><span data-stu-id="40590-139">ICE46</span></span>](ice46.md)  
</dl>

 

 



