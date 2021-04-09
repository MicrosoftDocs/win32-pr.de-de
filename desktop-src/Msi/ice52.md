---
description: ICE52 prüft, ob private Eigenschaften in der AppSearch-Tabelle angezeigt werden. Siehe Informationen zu Eigenschaften.
ms.assetid: 18d1489e-666a-488d-ae12-5dbe60885a2e
title: ICE52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785dd468aaa637df02b9eb432dd77f9226d828a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867291"
---
# <a name="ice52"></a><span data-ttu-id="06dcd-104">ICE52</span><span class="sxs-lookup"><span data-stu-id="06dcd-104">ICE52</span></span>

<span data-ttu-id="06dcd-105">ICE52 prüft, ob private Eigenschaften in der [AppSearch-Tabelle](appsearch-table.md)angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="06dcd-105">ICE52 checks for private properties in the [AppSearch table](appsearch-table.md).</span></span> <span data-ttu-id="06dcd-106">Siehe [Informationen zu Eigenschaften](about-properties.md).</span><span class="sxs-lookup"><span data-stu-id="06dcd-106">See [About Properties](about-properties.md).</span></span>

<span data-ttu-id="06dcd-107">Bei Verwendung von Windows 2000 müssen alle Eigenschaften, die in der Eigenschafts Spalte der AppSearch-Tabelle festgelegt sind, öffentliche Eigenschaften sein.</span><span class="sxs-lookup"><span data-stu-id="06dcd-107">When using Windows 2000 all properties set in the Property column of the AppSearch table must be public properties.</span></span>

## <a name="result"></a><span data-ttu-id="06dcd-108">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="06dcd-108">Result</span></span>

<span data-ttu-id="06dcd-109">ICE52 gibt eine Warnung aus, wenn in der AppSearch-Tabelle eine private-Eigenschaft vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="06dcd-109">ICE52 posts a warning if there is a private property in the AppSearch table.</span></span>

## <a name="example"></a><span data-ttu-id="06dcd-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="06dcd-110">Example</span></span>

<span data-ttu-id="06dcd-111">ICE52 gibt die folgende Warnung für das gezeigte Beispiel aus.</span><span class="sxs-lookup"><span data-stu-id="06dcd-111">ICE52 posts the following warning for the example shown.</span></span>

``` syntax
Property 'Property2' in AppSearch row 'Property2'.'Signature2' 
    is not public. It should be all uppercase.
```

[<span data-ttu-id="06dcd-112">AppSearch-Tabelle</span><span class="sxs-lookup"><span data-stu-id="06dcd-112">AppSearch Table</span></span>](appsearch-table.md)



| <span data-ttu-id="06dcd-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="06dcd-113">Property</span></span>  | <span data-ttu-id="06dcd-114">Signatur</span><span class="sxs-lookup"><span data-stu-id="06dcd-114">Signature</span></span>  |
|-----------|------------|
| <span data-ttu-id="06dcd-115">Eigenschaft1</span><span class="sxs-lookup"><span data-stu-id="06dcd-115">PROPERTY1</span></span> | <span data-ttu-id="06dcd-116">Signature1</span><span class="sxs-lookup"><span data-stu-id="06dcd-116">Signature1</span></span> |
| <span data-ttu-id="06dcd-117">Eigenschaft2</span><span class="sxs-lookup"><span data-stu-id="06dcd-117">Property2</span></span> | <span data-ttu-id="06dcd-118">Signature2</span><span class="sxs-lookup"><span data-stu-id="06dcd-118">Signature2</span></span> |



 

<span data-ttu-id="06dcd-119">Um diese Warnung zu beheben, ändern Sie die benutzerdefinierte öffentliche Eigenschaft: Eigenschaft2.</span><span class="sxs-lookup"><span data-stu-id="06dcd-119">To fix this warning change to the custom public property: PROPERTY2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06dcd-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06dcd-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06dcd-121">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="06dcd-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



