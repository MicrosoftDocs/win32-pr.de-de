---
description: Die productlanguage-Eigenschaft muss auf den numerischen sprach Bezeichner (langid) für die neue Sprache aktualisiert werden.
ms.assetid: e00ef69b-c54b-41de-9230-a7582b260891
title: Aktualisieren von productlanguage-und ProductCode-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a7537cdb0295075fbfd1b8b58e45a051610cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360835"
---
# <a name="updating-productlanguage-and-productcode-properties"></a><span data-ttu-id="41d83-103">Aktualisieren von productlanguage-und ProductCode-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41d83-103">Updating ProductLanguage and ProductCode Properties</span></span>

<span data-ttu-id="41d83-104">Die [**productlanguage**](productlanguage.md) -Eigenschaft muss auf den numerischen sprach Bezeichner (langid) für die neue Sprache aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="41d83-104">The [**ProductLanguage**](productlanguage.md) property must be updated to the numeric language identifier (LANGID) for the new language.</span></span> <span data-ttu-id="41d83-105">Im Beispiel für die Lokalisierung muss der Wert der **productlanguage** -Eigenschaft von der langid für Englisch (1033) in die langid für Französisch (1036) in der [Eigenschaften Tabelle](property-table.md)geändert werden.</span><span class="sxs-lookup"><span data-stu-id="41d83-105">In the case of the localization example, the value of the **ProductLanguage** property must be changed from the LANGID for English (1033) to the LANGID for French (1036) in the [Property table](property-table.md).</span></span>

<span data-ttu-id="41d83-106">Der Wert der [**ProductCode**](productcode.md) -Eigenschaft in der [Eigenschaften Tabelle](property-table.md) muss beim Lokalisieren einer Datenbank in einen neuen, eindeutigen Wert geändert werden, da ein lokalisiertes Produkt als anderes Produkt angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="41d83-106">The value of the [**ProductCode**](productcode.md) property in the [Property table](property-table.md) must be changed to a new, unique value when localizing a database because a localized product is considered a different product.</span></span> <span data-ttu-id="41d83-107">Beispielsweise werden die deutsche und die englische Version einer Anwendung als zwei verschiedene Produkte betrachtet und müssen über unterschiedliche Produktcodes verfügen.</span><span class="sxs-lookup"><span data-stu-id="41d83-107">For example, the German and English versions of an application are considered two different products and must have different product codes.</span></span> <span data-ttu-id="41d83-108">Siehe [Produkt Codes](product-codes.md).</span><span class="sxs-lookup"><span data-stu-id="41d83-108">See [Product Codes](product-codes.md).</span></span>

<span data-ttu-id="41d83-109">Verwenden Sie den Datenbanktabellen-Editor, um die Werte der ProductCode-Eigenschaft und der productlanguage-Eigenschaft in der Eigenschaften Tabelle zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="41d83-109">Use your database table editor to update the values of the ProductCode and ProductLanguage properties in the Property table.</span></span> <span data-ttu-id="41d83-110">Verwenden Sie nicht die GUID, die angezeigt wird, wenn Sie dieses Beispiel kopieren.</span><span class="sxs-lookup"><span data-stu-id="41d83-110">Do not reuse the GUID shown if you copy this example.</span></span>

[<span data-ttu-id="41d83-111">Eigenschaften Tabelle</span><span class="sxs-lookup"><span data-stu-id="41d83-111">Property Table</span></span>](property-table.md)



| <span data-ttu-id="41d83-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="41d83-112">Property</span></span>                                   | <span data-ttu-id="41d83-113">Wert</span><span class="sxs-lookup"><span data-stu-id="41d83-113">Value</span></span>                                  |
|--------------------------------------------|----------------------------------------|
| [<span data-ttu-id="41d83-114">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="41d83-114">**ProductCode**</span></span>](productcode.md)         | <span data-ttu-id="41d83-115">{EE389960-E426-4EEA-B669-AD8129249881}</span><span class="sxs-lookup"><span data-stu-id="41d83-115">{EE389960-E426-4EEA-B669-AD8129249881}</span></span> |
| [<span data-ttu-id="41d83-116">**Productlanguage**</span><span class="sxs-lookup"><span data-stu-id="41d83-116">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="41d83-117">1036</span><span class="sxs-lookup"><span data-stu-id="41d83-117">1036</span></span>                                   |



 

[<span data-ttu-id="41d83-118">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="41d83-118">Continue</span></span>](updating-a-summary-information-stream.md)

 

 



