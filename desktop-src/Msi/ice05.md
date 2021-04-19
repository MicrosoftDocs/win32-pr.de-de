---
description: 'ICE05 überprüft, ob bestimmte Tabellen erforderliche Einträge enthalten. Dies umfasst, aber ist nicht darauf beschränkt, die Eigenschaften Tabelle auf die erforderlichen Eigenschaften zu überprüfen: ProductName, productlanguage, ProductVersion, ProductCode und Hersteller.'
ms.assetid: 90b35758-c9d9-4104-a352-f0b17b04b571
title: ICE05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9710a81eca3da7ac947afb90a1d6788c0ddd74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349944"
---
# <a name="ice05"></a><span data-ttu-id="49d09-104">ICE05</span><span class="sxs-lookup"><span data-stu-id="49d09-104">ICE05</span></span>

<span data-ttu-id="49d09-105">ICE05 überprüft, ob bestimmte Tabellen erforderliche Einträge enthalten.</span><span class="sxs-lookup"><span data-stu-id="49d09-105">ICE05 validates that certain tables contain required entries.</span></span> <span data-ttu-id="49d09-106">Dies umfasst, aber ist nicht darauf beschränkt, die Eigenschaften [Tabelle](property-table.md) auf die erforderlichen Eigenschaften zu überprüfen: [**ProductName**](productname.md), [**productlanguage**](productlanguage.md), [**ProductVersion**](productversion.md), [**ProductCode**](productcode.md)und [**Hersteller**](manufacturer.md).</span><span class="sxs-lookup"><span data-stu-id="49d09-106">This includes, but is not restricted to, checking the [Property table](property-table.md) for the required properties: [**ProductName**](productname.md), [**ProductLanguage**](productlanguage.md), [**ProductVersion**](productversion.md), [**ProductCode**](productcode.md), and [**Manufacturer**](manufacturer.md).</span></span>

## <a name="result"></a><span data-ttu-id="49d09-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="49d09-107">Result</span></span>

<span data-ttu-id="49d09-108">ICE05 gibt einen Fehler aus, wenn ein erforderlicher Eintrag fehlt.</span><span class="sxs-lookup"><span data-stu-id="49d09-108">ICE05 posts an error if a required entry is missing.</span></span>

## <a name="example"></a><span data-ttu-id="49d09-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="49d09-109">Example</span></span>

<span data-ttu-id="49d09-110">Im gezeigten Beispiel meldet ICE05, dass der Eintrag "ProductVersion" in der Tabelle "Property" erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="49d09-110">For the example shown, ICE05 would report that the entry: 'ProductVersion' is required in the 'Property' table.</span></span>

<span data-ttu-id="49d09-111">[Eigenschaften Tabelle](property-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="49d09-111">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="49d09-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="49d09-112">Property</span></span>                           | <span data-ttu-id="49d09-113">Wert</span><span class="sxs-lookup"><span data-stu-id="49d09-113">Value</span></span>     |
|------------------------------------|-----------|
| [<span data-ttu-id="49d09-114">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="49d09-114">**ProductName**</span></span>](productname.md) | <span data-ttu-id="49d09-115">MyProduct</span><span class="sxs-lookup"><span data-stu-id="49d09-115">MyProduct</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="49d09-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="49d09-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49d09-117">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="49d09-117">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



