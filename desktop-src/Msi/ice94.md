---
description: ICE94 überprüft die Verknüpfungs Tabelle, die Featuretabelle und die MsiAssembly-Tabelle und gibt eine Warnung aus, wenn nicht angekündigte Verknüpfungen vorhanden sind, die auf eine Assemblydatei im globalen Assemblycache verweisen.
ms.assetid: 9b1b25b5-b190-47c2-8d43-fa3964e87a6f
title: ICE94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ce52e88a31e246eb4d69defba77b64c2955eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217651"
---
# <a name="ice94"></a><span data-ttu-id="c3143-103">ICE94</span><span class="sxs-lookup"><span data-stu-id="c3143-103">ICE94</span></span>

<span data-ttu-id="c3143-104">ICE94 überprüft die Verknüpfungs [Tabelle](shortcut-table.md), die [Featuretabelle](feature-table.md)und die [MsiAssembly-Tabelle](msiassembly-table.md) und gibt eine Warnung aus, wenn nicht angekündigte Verknüpfungen vorhanden sind, die auf eine Assemblydatei im globalen Assemblycache verweisen.</span><span class="sxs-lookup"><span data-stu-id="c3143-104">ICE94 checks the [Shortcut table](shortcut-table.md), [Feature table](feature-table.md), and [MsiAssembly table](msiassembly-table.md) and posts a warning if there are any unadvertised shortcuts pointing to an assembly file in the global assembly cache.</span></span> <span data-ttu-id="c3143-105">Wenn der Eintrag im Feld Ziel der Verknüpfungs Tabelle kein Feature in der Featuretabelle ist, wird die Verknüpfung nicht angekündigt.</span><span class="sxs-lookup"><span data-stu-id="c3143-105">If the entry in the Target field of the Shortcut table is not a feature in the Feature table, the shortcut is unadvertised.</span></span> <span data-ttu-id="c3143-106">Wenn der Eintrag im Feld Komponente \_ der Verknüpfungs Tabelle auch in der Tabelle MsiAssembly aufgeführt ist, verweist die Verknüpfung auf eine Assemblydatei.</span><span class="sxs-lookup"><span data-stu-id="c3143-106">If the entry in the Component\_ field of the Shortcut table is also listed in the MsiAssembly table, the shortcut points to an assembly file.</span></span> <span data-ttu-id="c3143-107">Wenn der Eintrag im Feld "Datei \_ Anwendung" in der Tabelle "MsiAssembly" leer ist, befindet sich die Assemblydatei im globalen Assemblycache.</span><span class="sxs-lookup"><span data-stu-id="c3143-107">If the entry in the File\_Application field in the MsiAssembly table is empty, the assembly file is in the global assembly cache.</span></span>

## <a name="result"></a><span data-ttu-id="c3143-108">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="c3143-108">Result</span></span>

<span data-ttu-id="c3143-109">ICE94 gibt die folgende Warnung aus.</span><span class="sxs-lookup"><span data-stu-id="c3143-109">ICE94 posts the following warning.</span></span>



| <span data-ttu-id="c3143-110">ICE94-Warnung</span><span class="sxs-lookup"><span data-stu-id="c3143-110">ICE94 warning</span></span>                                                                                | <span data-ttu-id="c3143-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3143-111">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3143-112">Die nicht angekündigte Verknüpfung ' \[ 2 \] ' verweist auf eine Assemblydatei im globalen Assemblycache.</span><span class="sxs-lookup"><span data-stu-id="c3143-112">The non-advertised shortcut '\[2\]' points to an assembly file in the global assembly cache.</span></span> | <span data-ttu-id="c3143-113">Eine nicht angekündigte Verknüpfung verweist auf eine Assemblydatei im globalen Assemblycache.</span><span class="sxs-lookup"><span data-stu-id="c3143-113">An unadvertised shortcut is pointing to an assembly file in the global assembly cache.</span></span> |



 

## <a name="example"></a><span data-ttu-id="c3143-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c3143-114">Example</span></span>

<span data-ttu-id="c3143-115">ICE94 meldet den folgenden Fehler für das Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c3143-115">ICE94 reports the following error for the example:</span></span>

``` syntax
The non-advertised shortcut 'shortcut1' points to an assembly file in the global assembly cache.
```

<span data-ttu-id="c3143-116">Verknüpfungs [Tabelle](shortcut-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="c3143-116">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="c3143-117">Abkürzung</span><span class="sxs-lookup"><span data-stu-id="c3143-117">Shortcut</span></span>  | <span data-ttu-id="c3143-118">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="c3143-118">Component\_</span></span> | <span data-ttu-id="c3143-119">Ziel</span><span class="sxs-lookup"><span data-stu-id="c3143-119">Target</span></span>    |
|-----------|-------------|-----------|
| <span data-ttu-id="c3143-120">shortcut1</span><span class="sxs-lookup"><span data-stu-id="c3143-120">shortcut1</span></span> | <span data-ttu-id="c3143-121">c1</span><span class="sxs-lookup"><span data-stu-id="c3143-121">c1</span></span>          | <span data-ttu-id="c3143-122">\[file1\]</span><span class="sxs-lookup"><span data-stu-id="c3143-122">\[file1\]</span></span> |
| <span data-ttu-id="c3143-123">shortcut2</span><span class="sxs-lookup"><span data-stu-id="c3143-123">shortcut2</span></span> | <span data-ttu-id="c3143-124">c2</span><span class="sxs-lookup"><span data-stu-id="c3143-124">c2</span></span>          | <span data-ttu-id="c3143-125">Feature1</span><span class="sxs-lookup"><span data-stu-id="c3143-125">feature1</span></span>  |
| <span data-ttu-id="c3143-126">shortcut3</span><span class="sxs-lookup"><span data-stu-id="c3143-126">shortcut3</span></span> | <span data-ttu-id="c3143-127">c3</span><span class="sxs-lookup"><span data-stu-id="c3143-127">c3</span></span>          | <span data-ttu-id="c3143-128">\[file2\]</span><span class="sxs-lookup"><span data-stu-id="c3143-128">\[file2\]</span></span> |



 

<span data-ttu-id="c3143-129">[Funktions Tabelle](feature-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="c3143-129">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="c3143-130">Funktion</span><span class="sxs-lookup"><span data-stu-id="c3143-130">Feature</span></span>  |
|----------|
| <span data-ttu-id="c3143-131">Feature1</span><span class="sxs-lookup"><span data-stu-id="c3143-131">feature1</span></span> |



 

<span data-ttu-id="c3143-132">[MsiAssembly-Tabelle](msiassembly-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="c3143-132">[MsiAssembly Table](msiassembly-table.md) (partial)</span></span>



| <span data-ttu-id="c3143-133">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="c3143-133">Component\_</span></span> | <span data-ttu-id="c3143-134">Datei \_ Anwendung</span><span class="sxs-lookup"><span data-stu-id="c3143-134">File\_Application</span></span> |
|-------------|-------------------|
| <span data-ttu-id="c3143-135">c1</span><span class="sxs-lookup"><span data-stu-id="c3143-135">c1</span></span>          |                   |
| <span data-ttu-id="c3143-136">c2</span><span class="sxs-lookup"><span data-stu-id="c3143-136">c2</span></span>          |                   |
| <span data-ttu-id="c3143-137">c3</span><span class="sxs-lookup"><span data-stu-id="c3143-137">c3</span></span>          | <span data-ttu-id="c3143-138">fa1</span><span class="sxs-lookup"><span data-stu-id="c3143-138">fa1</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="c3143-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c3143-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3143-140">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="c3143-140">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



