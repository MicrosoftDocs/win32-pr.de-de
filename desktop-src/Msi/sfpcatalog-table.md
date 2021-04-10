---
description: Die sfpcatalog-Tabelle enthält die von Windows Me verwendeten Kataloge.
ms.assetid: e9dc65a9-4ec9-4310-b03a-a2c38720ca8c
title: Sfpcatalog-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe887644faf6cf0a5cda626bbf757e9f448ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214858"
---
# <a name="sfpcatalog-table"></a><span data-ttu-id="e216d-103">Sfpcatalog-Tabelle</span><span class="sxs-lookup"><span data-stu-id="e216d-103">SFPCatalog Table</span></span>

<span data-ttu-id="e216d-104">Die sfpcatalog-Tabelle enthält die von Windows Me verwendeten Kataloge.</span><span class="sxs-lookup"><span data-stu-id="e216d-104">The SFPCatalog table contains the catalogs used by Windows Me.</span></span>

<span data-ttu-id="e216d-105">Die sfpcatalog-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="e216d-105">The SFPCatalog table has the following columns.</span></span>



| <span data-ttu-id="e216d-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="e216d-106">Column</span></span>     | <span data-ttu-id="e216d-107">Typ</span><span class="sxs-lookup"><span data-stu-id="e216d-107">Type</span></span>                       | <span data-ttu-id="e216d-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e216d-108">Key</span></span> | <span data-ttu-id="e216d-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="e216d-109">Nullable</span></span> |
|------------|----------------------------|-----|----------|
| <span data-ttu-id="e216d-110">Sfpcatalog</span><span class="sxs-lookup"><span data-stu-id="e216d-110">SFPCatalog</span></span> | [<span data-ttu-id="e216d-111">Filename</span><span class="sxs-lookup"><span data-stu-id="e216d-111">Filename</span></span>](filename.md)   | <span data-ttu-id="e216d-112">J</span><span class="sxs-lookup"><span data-stu-id="e216d-112">Y</span></span>   | <span data-ttu-id="e216d-113">N</span><span class="sxs-lookup"><span data-stu-id="e216d-113">N</span></span>        |
| <span data-ttu-id="e216d-114">Katalog</span><span class="sxs-lookup"><span data-stu-id="e216d-114">Catalog</span></span>    | [<span data-ttu-id="e216d-115">Binär (Binary)</span><span class="sxs-lookup"><span data-stu-id="e216d-115">Binary</span></span>](binary.md)       | <span data-ttu-id="e216d-116">N</span><span class="sxs-lookup"><span data-stu-id="e216d-116">N</span></span>   | <span data-ttu-id="e216d-117">N</span><span class="sxs-lookup"><span data-stu-id="e216d-117">N</span></span>        |
| <span data-ttu-id="e216d-118">Abhängigkeit</span><span class="sxs-lookup"><span data-stu-id="e216d-118">Dependency</span></span> | [<span data-ttu-id="e216d-119">Großformatige</span><span class="sxs-lookup"><span data-stu-id="e216d-119">Formatted</span></span>](formatted.md) | <span data-ttu-id="e216d-120">N</span><span class="sxs-lookup"><span data-stu-id="e216d-120">N</span></span>   | <span data-ttu-id="e216d-121">J</span><span class="sxs-lookup"><span data-stu-id="e216d-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e216d-122">Spalten</span><span class="sxs-lookup"><span data-stu-id="e216d-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e216d-123"><span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>Sfpcatalog</span><span class="sxs-lookup"><span data-stu-id="e216d-123"><span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog</span></span>
</dt> <dd>

<span data-ttu-id="e216d-124">Der kurze Dateiname für den Katalog.</span><span class="sxs-lookup"><span data-stu-id="e216d-124">The short file name for the catalog.</span></span> <span data-ttu-id="e216d-125">Da Kataloge keine Version aufweisen, kann der in dieser Spalte angegebene Katalog einen Katalog überschreiben, der denselben Namen hat und bereits auf dem lokalen System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e216d-125">Because catalogs have no version, the catalog specified in this column can overwrite a catalog that has the same name and is already installed on the local system.</span></span> <span data-ttu-id="e216d-126">Weitere Informationen finden Sie [im Thema zur Datei Versions](neither-file-has-a-version.md)Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="e216d-126">See the file versioning topic [Neither File Has a Version](neither-file-has-a-version.md).</span></span>

</dd> <dt>

<span data-ttu-id="e216d-127"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Sieren</span><span class="sxs-lookup"><span data-stu-id="e216d-127"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span>
</dt> <dd>

<span data-ttu-id="e216d-128">Binärdaten für den Katalog.</span><span class="sxs-lookup"><span data-stu-id="e216d-128">Binary data for the catalog.</span></span>

</dd> <dt>

<span data-ttu-id="e216d-129"><span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Gkeit</span><span class="sxs-lookup"><span data-stu-id="e216d-129"><span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Dependency</span></span>
</dt> <dd>

<span data-ttu-id="e216d-130">Der in diesem Feld angegebene Katalog ist das übergeordnete Element des abhängigen Katalogs, der im Feld sfpcatalog angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e216d-130">The catalog specified in this field is the parent of the dependent catalog specified in the SFPCatalog field.</span></span> <span data-ttu-id="e216d-131">Geben Sie den kurzen Dateinamen des übergeordneten Katalogs in das Abhängigkeits Feld ein.</span><span class="sxs-lookup"><span data-stu-id="e216d-131">Enter the short file name of the parent catalog into the Dependency field.</span></span> <span data-ttu-id="e216d-132">Dieses Feld ist ein Schlüssel zurück in die sfpcatalog-Spalte.</span><span class="sxs-lookup"><span data-stu-id="e216d-132">This field is a key back into the SFPCatalog column.</span></span> <span data-ttu-id="e216d-133">Bei der Abhängigkeit wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="e216d-133">The dependency match is case sensitive.</span></span>

<span data-ttu-id="e216d-134">Wenn das Abhängigkeits Feld auf einen anderen Datensatz in dieser sfpcatalog-Tabelle verweist, wird der übergeordnete Katalog vor dem abhängigen Katalog installiert.</span><span class="sxs-lookup"><span data-stu-id="e216d-134">If the Dependency field references another record in this SFPCatalog table, the parent catalog is installed before the dependent catalog.</span></span>

<span data-ttu-id="e216d-135">Wenn das Abhängigkeits Feld auf einen übergeordneten Katalog verweist, der im Feld sfpcatalog der Tabelle nicht vorhanden ist, und wenn der übergeordnete Katalog nicht bereits installiert ist, tritt bei der Installation ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="e216d-135">If the Dependency field references a parent catalog that is not present in the SFPCatalog field of this table, and if the parent catalog is not already installed, the installation fails.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e216d-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e216d-136">Remarks</span></span>

<span data-ttu-id="e216d-137">Mit der [Aktion installsfpcatalogfile](installsfpcatalogfile-action.md) werden die [Komponenten Tabelle](component-table.md), die [Dateitabelle](file-table.md), die [filesfpcatalog-Tabelle](filesfpcatalog-table.md) und die sfpcatalog-Tabelle abgefragt.</span><span class="sxs-lookup"><span data-stu-id="e216d-137">The [InstallSFPCatalogFile action](installsfpcatalogfile-action.md) queries the [Component table](component-table.md), [File table](file-table.md), [FileSFPCatalog table](filesfpcatalog-table.md) and SFPCatalog table.</span></span>

## <a name="validation"></a><span data-ttu-id="e216d-138">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="e216d-138">Validation</span></span>

<dl>

[<span data-ttu-id="e216d-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="e216d-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e216d-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="e216d-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e216d-141">ICE29</span><span class="sxs-lookup"><span data-stu-id="e216d-141">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="e216d-142">ICE32</span><span class="sxs-lookup"><span data-stu-id="e216d-142">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="e216d-143">ICE46</span><span class="sxs-lookup"><span data-stu-id="e216d-143">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="e216d-144">ICE66</span><span class="sxs-lookup"><span data-stu-id="e216d-144">ICE66</span></span>](ice66.md)  
</dl>

 

 



