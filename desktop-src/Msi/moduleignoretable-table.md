---
description: Wenn eine Tabelle im Mergemodul in der Tabelle "moduleignoretable" aufgeführt ist, wird Sie nicht in die MSI-Datei zusammengeführt.
ms.assetid: 9ff87993-74f6-4436-b0a9-d7ebed6555bd
title: Moduleignoretable-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7b0191f616eced187411a148e40e0ae6575cca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218004"
---
# <a name="moduleignoretable-table"></a><span data-ttu-id="07fc5-103">Moduleignoretable-Tabelle</span><span class="sxs-lookup"><span data-stu-id="07fc5-103">ModuleIgnoreTable Table</span></span>

<span data-ttu-id="07fc5-104">Wenn eine Tabelle im Mergemodul in der Tabelle "moduleignoretable" aufgeführt ist, wird Sie nicht in die MSI-Datei zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="07fc5-104">If a table in the merge module is listed in the ModuleIgnoreTable table, it is not merged into the .msi file.</span></span> <span data-ttu-id="07fc5-105">Wenn die Tabelle bereits in der MSI-Datei vorhanden ist, wird Sie nicht durch den Merge geändert.</span><span class="sxs-lookup"><span data-stu-id="07fc5-105">If the table already exists in the .msi file, it is not modified by the merge.</span></span> <span data-ttu-id="07fc5-106">Die Tabellen in der moduleignoretable können daher Daten enthalten, die nach dem Merge nicht benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="07fc5-106">The tables in the ModuleIgnoreTable can therefore contain data that is unneeded after the merge.</span></span>

<span data-ttu-id="07fc5-107">Die moduleignoretable-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="07fc5-107">The ModuleIgnoreTable table has the following columns.</span></span>



| <span data-ttu-id="07fc5-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="07fc5-108">Column</span></span> | <span data-ttu-id="07fc5-109">Typ</span><span class="sxs-lookup"><span data-stu-id="07fc5-109">Type</span></span>                         | <span data-ttu-id="07fc5-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="07fc5-110">Key</span></span> | <span data-ttu-id="07fc5-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="07fc5-111">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="07fc5-112">Tabelle</span><span class="sxs-lookup"><span data-stu-id="07fc5-112">Table</span></span>  | [<span data-ttu-id="07fc5-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="07fc5-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="07fc5-114">J</span><span class="sxs-lookup"><span data-stu-id="07fc5-114">Y</span></span>   | <span data-ttu-id="07fc5-115">Nein</span><span class="sxs-lookup"><span data-stu-id="07fc5-115">No</span></span>       |



 

## <a name="columns"></a><span data-ttu-id="07fc5-116">Spalten</span><span class="sxs-lookup"><span data-stu-id="07fc5-116">Columns</span></span>

<dl> <dt>

<span data-ttu-id="07fc5-117"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Glaub</span><span class="sxs-lookup"><span data-stu-id="07fc5-117"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="07fc5-118">Der Name der Tabelle im Mergemodul, die nicht in der MSI-Datei zusammengeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="07fc5-118">Name of the table in the merge module that is not to be merged into the .msi file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07fc5-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07fc5-119">Remarks</span></span>

<span data-ttu-id="07fc5-120">Um die Größe der MSM-Datei zu minimieren, wird empfohlen, dass Entwickler nicht verwendete Tabellen aus Modulen entfernen, die für die Verteilung vorgesehen sind, anstatt diese Tabellen in der Tabelle "moduleignoretable" aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="07fc5-120">To minimize the size of the .msm file, it is recommended that developers remove unused tables from modules intended for redistribution rather than listing these tables in the ModuleIgnoreTable table.</span></span>

 

 



