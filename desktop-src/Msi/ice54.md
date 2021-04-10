---
description: ICE54 prüft auf Komponenten, die eine Begleit Datei als Schlüssel Pfad verwenden.
ms.assetid: 94fcabfe-4500-42f2-acea-13b9a6681ca6
title: ICE54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99df2ba90ccb44e33b67aaf8ecdcadc723e8d2fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865476"
---
# <a name="ice54"></a><span data-ttu-id="5d164-103">ICE54</span><span class="sxs-lookup"><span data-stu-id="5d164-103">ICE54</span></span>

<span data-ttu-id="5d164-104">ICE54 prüft auf Komponenten, die eine Begleit Datei als Schlüssel Pfad verwenden.</span><span class="sxs-lookup"><span data-stu-id="5d164-104">ICE54 checks for components that use a companion file as their key path.</span></span>

<span data-ttu-id="5d164-105">Die Schlüssel Pfad Datei einer Komponente darf nicht von einer anderen Datei abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="5d164-105">The key path file of a component must not derive its version from a different file.</span></span> <span data-ttu-id="5d164-106">Dies kann dazu führen, dass einige Dateien nicht installiert werden.</span><span class="sxs-lookup"><span data-stu-id="5d164-106">This can cause some files to fail to install.</span></span> <span data-ttu-id="5d164-107">Weitere Informationen zu Begleit Dateien finden Sie in der [Dateitabelle](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5d164-107">See the [File table](file-table.md) for more information about companion files.</span></span>

## <a name="result"></a><span data-ttu-id="5d164-108">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="5d164-108">Result</span></span>

<span data-ttu-id="5d164-109">ICE54 gibt eine Warnung aus, wenn eine Komponente über eine Schlüssel Pfad Datei verfügt, die Ihre Version von einer anderen Datei ableitet.</span><span class="sxs-lookup"><span data-stu-id="5d164-109">ICE54 posts a warning if any component has a key path file that derives its version from another file.</span></span>

## <a name="example"></a><span data-ttu-id="5d164-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5d164-110">Example</span></span>

<span data-ttu-id="5d164-111">ICE54 gibt die folgende Warnung für das gezeigte Beispiel zurück.</span><span class="sxs-lookup"><span data-stu-id="5d164-111">ICE54 returns the following warning for the example shown.</span></span>

``` syntax
Component 'Component1' uses file 'File1' as its KeyPath, but the file's version is provided by the file 'File2'.
```

<span data-ttu-id="5d164-112">[Komponenten Tabelle](component-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="5d164-112">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="5d164-113">Komponente</span><span class="sxs-lookup"><span data-stu-id="5d164-113">Component</span></span>  | <span data-ttu-id="5d164-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="5d164-114">Attribute</span></span> | <span data-ttu-id="5d164-115">KEYPATH</span><span class="sxs-lookup"><span data-stu-id="5d164-115">KeyPath</span></span> |
|------------|-----------|---------|
| <span data-ttu-id="5d164-116">Component1</span><span class="sxs-lookup"><span data-stu-id="5d164-116">Component1</span></span> | <span data-ttu-id="5d164-117">0</span><span class="sxs-lookup"><span data-stu-id="5d164-117">0</span></span>         | <span data-ttu-id="5d164-118">Datei1</span><span class="sxs-lookup"><span data-stu-id="5d164-118">File1</span></span>   |



 

<span data-ttu-id="5d164-119">[Dateitabelle](file-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="5d164-119">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="5d164-120">File</span><span class="sxs-lookup"><span data-stu-id="5d164-120">File</span></span>  | <span data-ttu-id="5d164-121">Version</span><span class="sxs-lookup"><span data-stu-id="5d164-121">Version</span></span> | <span data-ttu-id="5d164-122">Sprache</span><span class="sxs-lookup"><span data-stu-id="5d164-122">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="5d164-123">Datei1</span><span class="sxs-lookup"><span data-stu-id="5d164-123">File1</span></span> | <span data-ttu-id="5d164-124">Datei2</span><span class="sxs-lookup"><span data-stu-id="5d164-124">File2</span></span>   |          |
| <span data-ttu-id="5d164-125">Datei2</span><span class="sxs-lookup"><span data-stu-id="5d164-125">File2</span></span> | <span data-ttu-id="5d164-126">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="5d164-126">1.0.0.0</span></span> | <span data-ttu-id="5d164-127">1033</span><span class="sxs-lookup"><span data-stu-id="5d164-127">1033</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="5d164-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5d164-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d164-129">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="5d164-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



