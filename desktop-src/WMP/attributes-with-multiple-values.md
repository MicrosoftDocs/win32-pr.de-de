---
title: Attribute mit mehreren Werten (Windows Media Player SDK)
description: Erfahren Sie mehr über Attribute mit mehreren Werten im Windows Media Player SDK. Einige Medienelementattribute können mehrere Werte haben.
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
keywords:
- Windows Media Player,Attribute für Medienelemente
- Windows Media Player Objektmodell,Attribute für Medienelemente
- Objektmodell,Attribute für Medienelemente
- Windows Media Player Mobile,Attribute für Medienelemente
- Windows Media Player ActiveX-Steuerelement,Attribute für Medienelemente
- Windows Media Player Mobile ActiveX-Steuerelement,Attribute für Medienelemente
- ActiveX-Steuerelement,Attribute für Medienelemente
- Windows Media Player Bibliothek,Attribute für Medienelemente
- Bibliothek,Attribute für Medienelemente
- Attribute,mehrere Werte
- Mehrere Attributwerte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16baf4bab47dc972ec7b043980dccb0f2aadd57
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262602"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a><span data-ttu-id="e624b-115">Attribute mit mehreren Werten (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="e624b-115">Attributes with Multiple Values (Windows Media Player SDK)</span></span>

<span data-ttu-id="e624b-116">Einige Medienelementattribute können mehrere Werte haben.</span><span class="sxs-lookup"><span data-stu-id="e624b-116">Some media item attributes can have multiple values.</span></span> <span data-ttu-id="e624b-117">Beispielsweise können die **Attribute Author**, **WM/Composer** und **WM/Genre** jeweils mehrere Werte haben.</span><span class="sxs-lookup"><span data-stu-id="e624b-117">For example, the **Author**, **WM/Composer**, and **WM/Genre** attributes can each have more than one value.</span></span> <span data-ttu-id="e624b-118">Der Datentyp solcher Attribute ist eine **mehrwertige Zeichenfolge.**</span><span class="sxs-lookup"><span data-stu-id="e624b-118">The data type of such attributes is **multi-valued string**.</span></span>

<span data-ttu-id="e624b-119">In Windows Media Player zeigt die Bibliothek mehrere Werte in einem einzelnen Feld an, indem die Werte durch Semikolons getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="e624b-119">In Windows Media Player, the library displays multiple values in a single field, separating the values with semicolons.</span></span> <span data-ttu-id="e624b-120">Jeder Wert ist jedoch tatsächlich ein separates Attribut im Windows Media-Element.</span><span class="sxs-lookup"><span data-stu-id="e624b-120">However, each value is actually a separate attribute in the Windows Media item.</span></span>

<span data-ttu-id="e624b-121">Sie können Code schreiben, der bestimmt, ob ein bestimmtes Attribut über mehrere Werte verfügt, und dann alle diese Werte abrufen.</span><span class="sxs-lookup"><span data-stu-id="e624b-121">You can write code that will determine whether a given attribute has multiple values and then retrieve all of those values.</span></span> <span data-ttu-id="e624b-122">Sie müssen Media *verwenden.* **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="e624b-122">You must use *Media*.**getItemInfoByType**.</span></span> <span data-ttu-id="e624b-123">Wenn Sie media *verwenden.* **getItemInfo-Methode** zum Abrufen eines mehrwertigen Attributs. Sie rufen nur den ersten Wert ab.</span><span class="sxs-lookup"><span data-stu-id="e624b-123">If you use the *Media*.**getItemInfo** method to retrieve a multi-valued attribute, you will only retrieve the first value.</span></span>

<span data-ttu-id="e624b-124">Im letzten Beispiel im Thema [Lesen von Attributwerten](reading-attribute-values.md) wird die Verwendung von *Media veranschaulicht.* **getAttributeCountByType und** *Media*. **getItemInfoByType-Methoden** zum Abrufen mehrerer Werte für ein bestimmtes Attribut.</span><span class="sxs-lookup"><span data-stu-id="e624b-124">The final example in the [Reading Attribute Values](reading-attribute-values.md) topic demonstrates the use of the *Media*.**getAttributeCountByType** and *Media*.**getItemInfoByType** methods to retrieve multiple values for a given attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e624b-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e624b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e624b-126">**Medienelementattribute**</span><span class="sxs-lookup"><span data-stu-id="e624b-126">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="e624b-127">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="e624b-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="e624b-128">**Lesen von Attributwerten von einer CD oder DVD**</span><span class="sxs-lookup"><span data-stu-id="e624b-128">**Reading Attribute Values from a CD or DVD**</span></span>](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




