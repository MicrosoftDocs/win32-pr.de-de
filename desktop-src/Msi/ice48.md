---
description: ICE48 sucht nach Verzeichnissen, die auf lokale Pfade in der Eigenschaften Tabelle hart codiert sind.
ms.assetid: 9dcc2475-23a3-4f77-8828-4d0a036670d4
title: ICE48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c9c9ace086d044109e5f9b91bbc471c37094de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363562"
---
# <a name="ice48"></a><span data-ttu-id="56749-103">ICE48</span><span class="sxs-lookup"><span data-stu-id="56749-103">ICE48</span></span>

<span data-ttu-id="56749-104">ICE48 sucht nach Verzeichnissen, die auf lokale Pfade in der [Eigenschaften Tabelle](property-table.md)hart codiert sind.</span><span class="sxs-lookup"><span data-stu-id="56749-104">ICE48 checks for directories that are hard-coded to local paths in the [Property table](property-table.md).</span></span>

<span data-ttu-id="56749-105">Verwenden Sie keine hart Codierung von Verzeichnis Pfaden zu lokalen Laufwerken, da sich die Computer in der Einrichtung des lokalen Laufwerks unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="56749-105">Do not hard-code directory paths to local drives because computers differ in the setup of the local drive.</span></span> <span data-ttu-id="56749-106">Diese Vorgehensweise ist möglicherweise akzeptabel, wenn eine Anwendung auf einer großen Anzahl von Computern bereitgestellt wird, auf denen die relevanten Teile der Laufwerke identisch sind.</span><span class="sxs-lookup"><span data-stu-id="56749-106">This practice may be acceptable if deploying an application to a large number of computers on which the relevant portions of the drives are all the same.</span></span>

## <a name="result"></a><span data-ttu-id="56749-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="56749-107">Result</span></span>

<span data-ttu-id="56749-108">ICE48 gibt eine Fehlermeldung aus, wenn ein Verzeichnis vorhanden ist, das in einem lokalen Pfad in der Eigenschaften Tabelle hart codiert ist.</span><span class="sxs-lookup"><span data-stu-id="56749-108">ICE48 posts an error message if there is a directory that is hard-coded to a local path in the Property table.</span></span>

## <a name="example"></a><span data-ttu-id="56749-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="56749-109">Example</span></span>

<span data-ttu-id="56749-110">ICE48 würde die folgende Warnung für das gezeigte Beispiel melden.</span><span class="sxs-lookup"><span data-stu-id="56749-110">ICE48 would report the following warning for the example shown.</span></span>

``` syntax
Directory 'Dir1' appears to be hardcoded in the property 
    table to a local drive.
```

<span data-ttu-id="56749-111">[Verzeichnis Tabelle](directory-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="56749-111">[Directory Table](directory-table.md) (partial)</span></span>



| <span data-ttu-id="56749-112">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="56749-112">Directory</span></span> | <span data-ttu-id="56749-113">Über \_ geordnetes Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="56749-113">Directory\_Parent</span></span> | <span data-ttu-id="56749-114">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="56749-114">DefaultDir</span></span> |
|-----------|-------------------|------------|
| <span data-ttu-id="56749-115">Dir1</span><span class="sxs-lookup"><span data-stu-id="56749-115">Dir1</span></span>      |                   | <span data-ttu-id="56749-116">SourceDir</span><span class="sxs-lookup"><span data-stu-id="56749-116">SourceDir</span></span>  |



 

<span data-ttu-id="56749-117">[Eigenschaften Tabelle](property-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="56749-117">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="56749-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="56749-118">Property</span></span> | <span data-ttu-id="56749-119">Wert</span><span class="sxs-lookup"><span data-stu-id="56749-119">Value</span></span>      |
|----------|------------|
| <span data-ttu-id="56749-120">Dir1</span><span class="sxs-lookup"><span data-stu-id="56749-120">Dir1</span></span>     | <span data-ttu-id="56749-121">d: \\ Quelle</span><span class="sxs-lookup"><span data-stu-id="56749-121">d:\\source</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="56749-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56749-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56749-123">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="56749-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



