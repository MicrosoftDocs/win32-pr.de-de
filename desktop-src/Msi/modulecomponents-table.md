---
description: Die modulecomponents-Tabelle enthält eine Liste der Komponenten, die im Mergemodul gefunden werden.
ms.assetid: def96d52-c9fa-4fac-b575-f9de8eb82d1c
title: Modulecomponents-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea2f47418b0387c7fa9d289d156fb0369f53adf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349624"
---
# <a name="modulecomponents-table"></a><span data-ttu-id="8ee03-103">Modulecomponents-Tabelle</span><span class="sxs-lookup"><span data-stu-id="8ee03-103">ModuleComponents Table</span></span>

<span data-ttu-id="8ee03-104">Die modulecomponents-Tabelle enthält eine Liste der Komponenten, die im Mergemodul gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="8ee03-104">The ModuleComponents table contains a list of the components found in the merge module.</span></span>

<span data-ttu-id="8ee03-105">Die modulecomponents-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="8ee03-105">The ModuleComponents table has the following columns.</span></span>



| <span data-ttu-id="8ee03-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="8ee03-106">Column</span></span>    | <span data-ttu-id="8ee03-107">Typ</span><span class="sxs-lookup"><span data-stu-id="8ee03-107">Type</span></span>                         | <span data-ttu-id="8ee03-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="8ee03-108">Key</span></span> | <span data-ttu-id="8ee03-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="8ee03-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="8ee03-110">Komponente</span><span class="sxs-lookup"><span data-stu-id="8ee03-110">Component</span></span> | [<span data-ttu-id="8ee03-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="8ee03-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="8ee03-112">J</span><span class="sxs-lookup"><span data-stu-id="8ee03-112">Y</span></span>   | <span data-ttu-id="8ee03-113">N</span><span class="sxs-lookup"><span data-stu-id="8ee03-113">N</span></span>        |
| <span data-ttu-id="8ee03-114">ModuleID</span><span class="sxs-lookup"><span data-stu-id="8ee03-114">ModuleID</span></span>  | [<span data-ttu-id="8ee03-115">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="8ee03-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="8ee03-116">J</span><span class="sxs-lookup"><span data-stu-id="8ee03-116">Y</span></span>   | <span data-ttu-id="8ee03-117">N</span><span class="sxs-lookup"><span data-stu-id="8ee03-117">N</span></span>        |
| <span data-ttu-id="8ee03-118">Sprache</span><span class="sxs-lookup"><span data-stu-id="8ee03-118">Language</span></span>  | [<span data-ttu-id="8ee03-119">Integer</span><span class="sxs-lookup"><span data-stu-id="8ee03-119">Integer</span></span>](integer.md)       | <span data-ttu-id="8ee03-120">J</span><span class="sxs-lookup"><span data-stu-id="8ee03-120">Y</span></span>   | <span data-ttu-id="8ee03-121">N</span><span class="sxs-lookup"><span data-stu-id="8ee03-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8ee03-122">Spalten</span><span class="sxs-lookup"><span data-stu-id="8ee03-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8ee03-123"><span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Zulieferern</span><span class="sxs-lookup"><span data-stu-id="8ee03-123"><span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Component</span></span>
</dt> <dd>

<span data-ttu-id="8ee03-124">Ein Bezeichner, der auf eine Komponente im Mergemodul verweist.</span><span class="sxs-lookup"><span data-stu-id="8ee03-124">An identifier referring to a component in the merge module.</span></span> <span data-ttu-id="8ee03-125">Die Komponenten Spalte ist ein Fremdschlüssel für die [Komponenten Tabelle](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="8ee03-125">The Component column is a foreign key to the [Component table](component-table.md).</span></span> <span data-ttu-id="8ee03-126">Der Eintrag in der Component-Spalte muss der Benennungs Konvention unter [Benennen von primär Schlüsseln in mergemoduldatenbanken](naming-primary-keys-in-merge-module-databases.md)entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8ee03-126">The entry in the Component column must follow the naming convention in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ee03-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="8ee03-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="8ee03-128">Der Bezeichner für das Mergemodul.</span><span class="sxs-lookup"><span data-stu-id="8ee03-128">The identifier for the merge module.</span></span> <span data-ttu-id="8ee03-129">Dies ist ein Fremdschlüssel für die [ModuleSignature-Tabelle](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8ee03-129">This is a foreign key to the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ee03-130"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Kurse</span><span class="sxs-lookup"><span data-stu-id="8ee03-130"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="8ee03-131">Der Sprachen Bezeichner beschreibt die Standardsprache für das Mergemodul.</span><span class="sxs-lookup"><span data-stu-id="8ee03-131">The Language identifier describes the default language for the merge module.</span></span> <span data-ttu-id="8ee03-132">Der sprach Bezeichner weist das Dezimal Format auf, z. b. US-Englisch ist 1033.</span><span class="sxs-lookup"><span data-stu-id="8ee03-132">The language identifier is in decimal format, for example, U.S. English is 1033.</span></span> <span data-ttu-id="8ee03-133">Fremdschlüssel für die [ModuleSignature-Tabelle](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8ee03-133">Foreign key to the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ee03-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ee03-134">Remarks</span></span>

<span data-ttu-id="8ee03-135">Sprach Transformationen müssen in der Lage sein, diese Tabelle zu aktualisieren, wenn das Mergemodul mehrere Sprachen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ee03-135">Language transforms must be able to update this table if the merge module supports multiple languages.</span></span>

 

 



