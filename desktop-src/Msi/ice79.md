---
description: ICE79 überprüft die Verweise auf Komponenten und Funktionen, die in den Datenbankfeldern eingegeben wurden, mithilfe des Bedingungs Datentyps.
ms.assetid: f0a8ceac-084a-4693-b27d-f610eec4702a
title: ICE79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9081297f2bf2f11283380c0f057bd0fbec417975
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129965"
---
# <a name="ice79"></a><span data-ttu-id="85817-103">ICE79</span><span class="sxs-lookup"><span data-stu-id="85817-103">ICE79</span></span>

<span data-ttu-id="85817-104">ICE79 überprüft die Verweise auf Komponenten und Funktionen, die in den Datenbankfeldern eingegeben wurden, [mithilfe des Bedingungs](condition.md) Datentyps.</span><span class="sxs-lookup"><span data-stu-id="85817-104">ICE79 validates the references to components and features entered in the database fields using the [Condition](condition.md) data type.</span></span>

## <a name="result"></a><span data-ttu-id="85817-105">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="85817-105">Result</span></span>

<span data-ttu-id="85817-106">ICE79 gibt zwei Warnungen aus.</span><span class="sxs-lookup"><span data-stu-id="85817-106">ICE79 posts two warnings.</span></span>



| <span data-ttu-id="85817-107">ICE79-Warnung</span><span class="sxs-lookup"><span data-stu-id="85817-107">ICE79 warning</span></span>                                                                      | <span data-ttu-id="85817-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85817-108">Description</span></span>                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="85817-109">Die Validierungs Tabelle der Datenbank fehlt \_ .</span><span class="sxs-lookup"><span data-stu-id="85817-109">Database is missing \_Validation table.</span></span> <span data-ttu-id="85817-110">Eigenschaftsnamen konnten nicht vollständig überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="85817-110">Could not completely check property names.</span></span> | <span data-ttu-id="85817-111">Die [ \_ Validierungs Tabelle](-validation-table.md)der Datenbank fehlt.</span><span class="sxs-lookup"><span data-stu-id="85817-111">Database is missing [\_Validation table](-validation-table.md).</span></span> |
| <span data-ttu-id="85817-112">Fehler beim Abrufen von Werten aus Spalte \[ 2 \] in Tabelle \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="85817-112">Error retrieving values from column \[2\] in table \[1\].</span></span> <span data-ttu-id="85817-113">Die Spalte wird übersprungen.</span><span class="sxs-lookup"><span data-stu-id="85817-113">Skipping Column.</span></span>         | <span data-ttu-id="85817-114">Fehler beim Abrufen des Werts.</span><span class="sxs-lookup"><span data-stu-id="85817-114">Error retrieving value.</span></span>                                          |



 

<span data-ttu-id="85817-115">ICE79 gibt zwei Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="85817-115">ICE79 posts two errors.</span></span>



| <span data-ttu-id="85817-116">ICE79-Fehler</span><span class="sxs-lookup"><span data-stu-id="85817-116">ICE79 error</span></span>                                                          | <span data-ttu-id="85817-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85817-117">Description</span></span>                               |
|----------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="85817-118">Auf die '% ls '-Komponente wurde in der '% s '-Spalte verwiesen. ' '% s ' der Zeile '% s ' ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="85817-118">Component '%ls' referenced in column '%s'.'%s' of row %s is invalid.</span></span> | <span data-ttu-id="85817-119">Es wurde ein ungültiger Komponenten Verweis gefunden.</span><span class="sxs-lookup"><span data-stu-id="85817-119">An invalid component reference was found.</span></span> |
| <span data-ttu-id="85817-120">Auf das Feature "% ls" wurde in der Spalte "% s" verwiesen. '% s ' der Zeile '% s ' ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="85817-120">Feature '%ls' referenced in column '%s'.'%s' of row %s is invalid.</span></span>   | <span data-ttu-id="85817-121">Es wurde ein ungültiger Funktions Verweis gefunden.</span><span class="sxs-lookup"><span data-stu-id="85817-121">An invalid feature reference was found</span></span>    |



 

## <a name="example"></a><span data-ttu-id="85817-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="85817-122">Example</span></span>

<span data-ttu-id="85817-123">ICE79 meldet die folgenden Fehler für das Beispiel:</span><span class="sxs-lookup"><span data-stu-id="85817-123">ICE79 reports the following errors for the example:</span></span>

``` syntax
Component 'NoSuchComponent' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom2 is invalid.
Feature 'NoSuchFeature' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom1 is invalid.
```

<span data-ttu-id="85817-124">In diesem Beispiel fehlt nosuchcomponent in der Component- [Tabelle](component-table.md) , und nosuchfeature ist in der Featuretabelle nicht vorhanden. [](feature-table.md)</span><span class="sxs-lookup"><span data-stu-id="85817-124">In this example, NoSuchComponent is absent from the [Component table](component-table.md) and NoSuchFeature is absent from the [Feature table](feature-table.md).</span></span>

<span data-ttu-id="85817-125">[InstallExecuteSequence-Tabelle](installexecutesequence-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="85817-125">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="85817-126">Aktion</span><span class="sxs-lookup"><span data-stu-id="85817-126">Action</span></span>  | <span data-ttu-id="85817-127">Bedingung</span><span class="sxs-lookup"><span data-stu-id="85817-127">Condition</span></span>                                |
|---------|------------------------------------------|
| <span data-ttu-id="85817-128">Custom1</span><span class="sxs-lookup"><span data-stu-id="85817-128">Custom1</span></span> | <span data-ttu-id="85817-129">TestAction = 1046 und &nosuchfeature>2</span><span class="sxs-lookup"><span data-stu-id="85817-129">TESTACTION=1046 AND &NoSuchFeature>2</span></span>  |
| <span data-ttu-id="85817-130">Custom2</span><span class="sxs-lookup"><span data-stu-id="85817-130">Custom2</span></span> | <span data-ttu-id="85817-131">TestAction = 146 und $NoSuchComponent>2</span><span class="sxs-lookup"><span data-stu-id="85817-131">TESTACTION=146 AND $NoSuchComponent>2</span></span> |



 

<span data-ttu-id="85817-132">Um diese Fehler zu beheben, geben Sie in den Funktions-und Komponenten Tabellen gültige Datensätze für nosuchfeature und nosuchcomponent ein.</span><span class="sxs-lookup"><span data-stu-id="85817-132">To fix these errors, enter valid records for NoSuchFeature and NoSuchComponent in the Feature and Component tables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85817-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="85817-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85817-134">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="85817-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



