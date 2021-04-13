---
title: Attribute mit mehreren Werten (Windows Media Player SDK)
description: Attribute mit mehreren Werten
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
keywords:
- Windows Media Player, Attribute für Medienelemente
- Windows Media Player-Objektmodell, Attribute für Medienelemente
- Objektmodell, Attribute für Medienelemente
- Windows Media Player Mobile, Attribute für Medienelemente
- Windows Media Player ActiveX-Steuerelement, Attribute für Medienelemente
- Windows Media Player Mobile ActiveX-Steuerelement, Attribute für Medienelemente
- ActiveX-Steuerelement, Attribute für Medienelemente
- Windows Media Player-Bibliothek, Attribute für Medienelemente
- Bibliothek, Attribute für Medienelemente
- Attribute, mehrere Werte
- mehrere Attributwerte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad93c4025d09a234b1834a32e4ca3789bcaa4a35
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391442"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a><span data-ttu-id="1bf07-114">Attribute mit mehreren Werten (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="1bf07-114">Attributes with Multiple Values (Windows Media Player SDK)</span></span>

<span data-ttu-id="1bf07-115">Einige Medien Element Attribute können mehrere Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1bf07-115">Some media item attributes can have multiple values.</span></span> <span data-ttu-id="1bf07-116">Beispielsweise können die Attribute **Author**, **WM/Composer** und **WM/Genre** jeweils mehr als einen Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1bf07-116">For example, the **Author**, **WM/Composer**, and **WM/Genre** attributes can each have more than one value.</span></span> <span data-ttu-id="1bf07-117">Der Datentyp dieser Attribute ist eine **mehrwertige Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="1bf07-117">The data type of such attributes is **multi-valued string**.</span></span>

<span data-ttu-id="1bf07-118">In Windows Media Player werden in der Bibliothek mehrere Werte in einem einzelnen Feld angezeigt, wobei die Werte durch Semikolons getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="1bf07-118">In Windows Media Player, the library displays multiple values in a single field, separating the values with semicolons.</span></span> <span data-ttu-id="1bf07-119">Jeder Wert ist jedoch tatsächlich ein separates Attribut im Windows Media-Element.</span><span class="sxs-lookup"><span data-stu-id="1bf07-119">However, each value is actually a separate attribute in the Windows Media item.</span></span>

<span data-ttu-id="1bf07-120">Sie können Code schreiben, mit dem bestimmt wird, ob ein bestimmtes Attribut über mehrere Werte verfügt, und dann alle diese Werte abrufen.</span><span class="sxs-lookup"><span data-stu-id="1bf07-120">You can write code that will determine whether a given attribute has multiple values and then retrieve all of those values.</span></span> <span data-ttu-id="1bf07-121">Sie müssen- *Medien* verwenden. **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="1bf07-121">You must use *Media*.**getItemInfoByType**.</span></span> <span data-ttu-id="1bf07-122">Wenn Sie die *Medien* verwenden. **getiteminfo** -Methode zum Abrufen eines mehrwertigen Attributs wird nur der erste Wert abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1bf07-122">If you use the *Media*.**getItemInfo** method to retrieve a multi-valued attribute, you will only retrieve the first value.</span></span>

<span data-ttu-id="1bf07-123">Das abschließende Beispiel im Thema [Lesen von Attributwerten](reading-attribute-values.md) veranschaulicht die Verwendung des *Mediums*. **getattributezähltbytype** und *Medium*. **getItemInfoByType** -Methoden zum Abrufen mehrerer Werte für ein bestimmtes Attribut.</span><span class="sxs-lookup"><span data-stu-id="1bf07-123">The final example in the [Reading Attribute Values](reading-attribute-values.md) topic demonstrates the use of the *Media*.**getAttributeCountByType** and *Media*.**getItemInfoByType** methods to retrieve multiple values for a given attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bf07-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1bf07-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bf07-125">**Medien Element Attribute**</span><span class="sxs-lookup"><span data-stu-id="1bf07-125">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="1bf07-126">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="1bf07-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="1bf07-127">**Lesen von Attributwerten von einer CD oder DVD**</span><span class="sxs-lookup"><span data-stu-id="1bf07-127">**Reading Attribute Values from a CD or DVD**</span></span>](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




