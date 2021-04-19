---
description: ICE56 überprüft, ob die Verzeichnisstruktur der MSI-Datei ein einzelnes Stammverzeichnis, das Stammverzeichnis der TARGETDIR-Eigenschaft und der SourceDir-Eigenschafts Wert in der DefaultDir-Spalte der Verzeichnis Tabelle ist.
ms.assetid: 6fbb51ff-64fc-40b7-852f-490c93e592c0
title: ICE56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0b83dc20c8463b80375d325dd9225de8524742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366078"
---
# <a name="ice56"></a><span data-ttu-id="14194-103">ICE56</span><span class="sxs-lookup"><span data-stu-id="14194-103">ICE56</span></span>

<span data-ttu-id="14194-104">ICE56 überprüft, ob die Verzeichnisstruktur der MSI-Datei ein einzelnes Stammverzeichnis, das Stammverzeichnis der [**TARGETDIR**](targetdir.md) -Eigenschaft und der [**SourceDir**](sourcedir.md) -Eigenschafts Wert in der DefaultDir-Spalte der [Verzeichnis Tabelle](directory-table.md)ist.</span><span class="sxs-lookup"><span data-stu-id="14194-104">ICE56 validates that the directory structure of the .msi file has a single root directory, that the root is the [**TARGETDIR**](targetdir.md) property, and that the [**SourceDir**](sourcedir.md) property value is in the DefaultDir column of the [Directory table](directory-table.md).</span></span>

<span data-ttu-id="14194-105">Wenn eine MSI-Datei mehrere Stämme aufweist oder einen anderen Stamm als [**TARGETDIR**](targetdir.md)angibt, wird bei einer [administrativen Installation](administrative-installation.md) kein korrektes administratives Abbild erstellt.</span><span class="sxs-lookup"><span data-stu-id="14194-105">If a .msi file has multiple roots or specifies a root other than [**TARGETDIR**](targetdir.md), an [administrative installation](administrative-installation.md) does not create a correct administrative image.</span></span>

<span data-ttu-id="14194-106">Beachten Sie, dass leere Verzeichnisse von ICE56 nicht geprüft werden.</span><span class="sxs-lookup"><span data-stu-id="14194-106">Note that empty directories are not checked by ICE56.</span></span> <span data-ttu-id="14194-107">Die Verzeichnisstruktur übergibt die Validierung mit mehreren Stamm Verzeichnissen, wenn die zusätzlichen Verzeichnisse leer sind.</span><span class="sxs-lookup"><span data-stu-id="14194-107">The directory structure passes validation with multiple root directories if the extra directories are empty.</span></span>

## <a name="result"></a><span data-ttu-id="14194-108">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="14194-108">Result</span></span>

<span data-ttu-id="14194-109">ICE56 gibt einen Fehler aus, wenn die MSI-Dateien nicht über einen einzelnen Stamm ( [**TARGETDIR**](targetdir.md)) verfügt, oder wenn [**SourceDir**](sourcedir.md) nicht in der DefaultDir-Spalte der [Verzeichnis Tabelle](directory-table.md)angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="14194-109">ICE56 posts an error if the .msi does not have a single root, [**TARGETDIR**](targetdir.md), or if [**SourceDir**](sourcedir.md) is not specified in the DefaultDir column of the [Directory table](directory-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="14194-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="14194-110">Example</span></span>

<span data-ttu-id="14194-111">ICE56 meldet die folgenden Fehler für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="14194-111">ICE56 reports the following errors for the example shown.</span></span>

``` syntax
Directory 'TARGETDIR' has a bad DefaultDir value. 
Directory 'Root2' is an invalid root Directory.
```

[<span data-ttu-id="14194-112">Verzeichnis Tabelle</span><span class="sxs-lookup"><span data-stu-id="14194-112">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="14194-113">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="14194-113">Directory</span></span> | <span data-ttu-id="14194-114">Über \_ geordnetes Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="14194-114">Directory\_Parent</span></span> | <span data-ttu-id="14194-115">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="14194-115">DefaultDir</span></span> |
|-----------|-------------------|------------|
| <span data-ttu-id="14194-116">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="14194-116">TARGETDIR</span></span> |                   | <span data-ttu-id="14194-117">Temp</span><span class="sxs-lookup"><span data-stu-id="14194-117">Temp</span></span>       |
| <span data-ttu-id="14194-118">Root2</span><span class="sxs-lookup"><span data-stu-id="14194-118">Root2</span></span>     | <span data-ttu-id="14194-119">Root2</span><span class="sxs-lookup"><span data-stu-id="14194-119">Root2</span></span>             | <span data-ttu-id="14194-120">SourceDir</span><span class="sxs-lookup"><span data-stu-id="14194-120">SourceDir</span></span>  |



 

<span data-ttu-id="14194-121">Um den ersten Fehler zu beheben, sollte der [**TARGETDIR**](targetdir.md) -Stamm einen DefaultDir-Wert von [**SourceDir**](sourcedir.md)aufweisen.</span><span class="sxs-lookup"><span data-stu-id="14194-121">To fix the first error, the [**TARGETDIR**](targetdir.md) root should have a DefaultDir value of [**SourceDir**](sourcedir.md).</span></span> <span data-ttu-id="14194-122">SourceDir wird ebenfalls akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="14194-122">SOURCEDIR is also accepted.</span></span> <span data-ttu-id="14194-123">Möglicherweise ist es möglich, **TARGETDIR** das übergeordnete Element des zweiten Stamms zu machen und den Wert "." in der Spalte "DefaultDir" zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="14194-123">It may be possible to make **TARGETDIR** the parent of the second root, and use the '.' value in the DefaultDir column.</span></span> <span data-ttu-id="14194-124">Weitere Informationen finden Sie in der [Verzeichnis Tabelle](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="14194-124">See the [Directory table](directory-table.md) for more information.</span></span>

<span data-ttu-id="14194-125">Um den zweiten Fehler zu beheben, sollte die Verzeichnisstruktur nur einen Stamm namens [**TARGETDIR**](targetdir.md)aufweisen.</span><span class="sxs-lookup"><span data-stu-id="14194-125">To fix the second error, the Directory structure should have only one root called [**TARGETDIR**](targetdir.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="14194-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="14194-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14194-127">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="14194-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



