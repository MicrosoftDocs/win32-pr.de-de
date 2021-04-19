---
description: ICEM10 überprüft, ob ein Mergemodul nur Eigenschaften enthält, die in der Eigenschaften Tabelle zulässig sind.
ms.assetid: 9ac7a724-ea0e-4caa-bb4f-846bfb802037
title: ICEM10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80263e5033ec14bd669c5d046c7f3842d58e332f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349529"
---
# <a name="icem10"></a><span data-ttu-id="3b015-103">ICEM10</span><span class="sxs-lookup"><span data-stu-id="3b015-103">ICEM10</span></span>

<span data-ttu-id="3b015-104">ICEM10 überprüft, ob ein Mergemodul nur Eigenschaften enthält, die in der Eigenschaften [Tabelle](property-table.md)zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="3b015-104">ICEM10 verifies that a merge module contains only properties that are allowed in the [Property Table](property-table.md).</span></span> <span data-ttu-id="3b015-105">Die folgenden produktspezifischen Eigenschaften sind in der Eigenschaften Tabelle nicht zulässig:</span><span class="sxs-lookup"><span data-stu-id="3b015-105">The following product specific properties are not allowed in the Property Table:</span></span>

-   [<span data-ttu-id="3b015-106">**Productlanguage-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="3b015-106">**ProductLanguage Property**</span></span>](productlanguage.md)
-   [<span data-ttu-id="3b015-107">**ProductCode-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="3b015-107">**ProductCode Property**</span></span>](productcode.md)
-   [<span data-ttu-id="3b015-108">**ProductVersion-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="3b015-108">**ProductVersion Property**</span></span>](productversion.md)
-   [<span data-ttu-id="3b015-109">**ProductName-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="3b015-109">**ProductName Property**</span></span>](productname.md)
-   [<span data-ttu-id="3b015-110">**Manufacturer-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="3b015-110">**Manufacturer Property**</span></span>](manufacturer.md)

## <a name="result"></a><span data-ttu-id="3b015-111">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="3b015-111">Result</span></span>

<span data-ttu-id="3b015-112">ICEM10 gibt einen Fehler aus, wenn ein Mergemodul eine Eigenschaft enthält, die in der [Eigenschaften Tabelle](property-table.md)nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="3b015-112">ICEM10 posts an error when a merge module contains a property that is not allowed in the [Property Table](property-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="3b015-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3b015-113">Example</span></span>

<span data-ttu-id="3b015-114">ICEM10 gibt die folgenden Fehlermeldungen für ein Modul aus, das die angezeigten Datenbankeinträge enthält.</span><span class="sxs-lookup"><span data-stu-id="3b015-114">ICEM10 posts the following error messages for a module that contains the database entries shown.</span></span>

``` syntax
The property 'ProductLanguage' is not allowed in a merge module.

The property 'Manufacturer' is not allowed in a merge module.
```

<span data-ttu-id="3b015-115">In der folgenden Tabelle wird eine partielle [Eigenschaften Tabelle](property-table.md)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="3b015-115">The following table shows you a partial [Property Table](property-table.md).</span></span>



| <span data-ttu-id="3b015-116">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3b015-116">Property</span></span>                                   | <span data-ttu-id="3b015-117">Werte</span><span class="sxs-lookup"><span data-stu-id="3b015-117">Values</span></span>    |
|--------------------------------------------|-----------|
| <span data-ttu-id="3b015-118">Color</span><span class="sxs-lookup"><span data-stu-id="3b015-118">Color</span></span>                                      | <span data-ttu-id="3b015-119">Red</span><span class="sxs-lookup"><span data-stu-id="3b015-119">Red</span></span>       |
| [<span data-ttu-id="3b015-120">**Hersteller**</span><span class="sxs-lookup"><span data-stu-id="3b015-120">**Manufacturer**</span></span>](manufacturer.md)       | <span data-ttu-id="3b015-121">Microsoft</span><span class="sxs-lookup"><span data-stu-id="3b015-121">Microsoft</span></span> |
| [<span data-ttu-id="3b015-122">**Productlanguage**</span><span class="sxs-lookup"><span data-stu-id="3b015-122">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="3b015-123">1033</span><span class="sxs-lookup"><span data-stu-id="3b015-123">1033</span></span>      |



 

<span data-ttu-id="3b015-124">Im folgenden Verfahren wird gezeigt, wie Sie Fehler beheben.</span><span class="sxs-lookup"><span data-stu-id="3b015-124">The following procedure shows you how to fix errors.</span></span>

<span data-ttu-id="3b015-125">**So beheben Sie die Fehler**</span><span class="sxs-lookup"><span data-stu-id="3b015-125">**To fix the errors**</span></span>

1.  <span data-ttu-id="3b015-126">Entfernen Sie die Eigenschaft "[**Manufacturer**](manufacturer.md)" aus der [Eigenschaften Tabelle](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="3b015-126">Remove the '[**Manufacturer**](manufacturer.md)' property from the [Property Table](property-table.md).</span></span>
2.  <span data-ttu-id="3b015-127">Entfernen Sie die [**productlanguage**](productlanguage.md)-Eigenschaft aus der [Eigenschaften Tabelle](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="3b015-127">Remove the '[**ProductLanguage**](productlanguage.md)' property from the [Property Table](property-table.md).</span></span>

## <a name="table-used-during-execution"></a><span data-ttu-id="3b015-128">Während der Ausführung verwendete Tabelle</span><span class="sxs-lookup"><span data-stu-id="3b015-128">Table Used During Execution</span></span>

<span data-ttu-id="3b015-129">Die [Eigenschaften Tabelle](property-table.md) wird während der Ausführung verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b015-129">The [Property Table](property-table.md) is used during execution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b015-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3b015-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b015-131">Eisverweis für Mergemodul</span><span class="sxs-lookup"><span data-stu-id="3b015-131">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



