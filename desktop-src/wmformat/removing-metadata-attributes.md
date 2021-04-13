---
title: Entfernen von Metadatenattributen
description: Entfernen von Metadatenattributen
ms.assetid: 44546091-406f-4ae6-914a-942d1b89e0e4
keywords:
- Windows Media-Format-SDK, Entfernen von Metadatenattributen
- Advanced Systems Format (ASF), Entfernen von Metadatenattributen
- ASF (Advanced Systems Format), Entfernen von Metadatenattributen
- Metadaten, Entfernen von Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b10176452dcc78cc3eca898b61c350a157e568
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104390050"
---
# <a name="removing-metadata-attributes"></a><span data-ttu-id="06bec-107">Entfernen von Metadatenattributen</span><span class="sxs-lookup"><span data-stu-id="06bec-107">Removing Metadata Attributes</span></span>

<span data-ttu-id="06bec-108">Sie können ein Metadatenattribut entfernen, indem Sie den Index und die streamnummer an die [**IWMHeaderInfo3::D eleteattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="06bec-108">You can remove a metadata attribute by passing its index and stream number to the [**IWMHeaderInfo3::DeleteAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) method.</span></span> <span data-ttu-id="06bec-109">Die Reihenfolge, in der die übrigen Attribute nach dem Entfernen eines Attributs indiziert werden, ändert sich nicht. alle verbleibenden Attribute, die ursprünglich einen Indexwert aufweisen, der größer als der entfernte Wert war, haben die Indexwerte um 1 reduziert.</span><span class="sxs-lookup"><span data-stu-id="06bec-109">The order in which the remaining attributes are indexed after removing an attribute does not change; all remaining attributes that originally had an index value greater than the one removed have their index values reduced by one.</span></span> <span data-ttu-id="06bec-110">Wenn Sie mehrere Attribute entfernen, führen Sie dies in absteigender Reihenfolge nach Index durch, um die Anpassung der Indizierung zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="06bec-110">When removing multiple attributes, do so in descending order by index to avoid having to calculate the adjustment in indexing.</span></span>

<span data-ttu-id="06bec-111">Der [**IWMHeaderInfo3:: getattributeindices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) -Methode gibt die Indexwerte in absteigender Reihenfolge zurück, um die Werte zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="06bec-111">For convenience in removing values, the [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) method returns the index values in descending order.</span></span>

> [!Note]  
> <span data-ttu-id="06bec-112">Indexwerte, die mit den Methoden von [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) abgerufen werden, sind nicht mit Indexwerten kompatibel, die mit den Methoden von [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="06bec-112">Index values obtained by using the methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) are not compatible with index values obtained by using the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span></span> <span data-ttu-id="06bec-113">Wenn Sie die Methoden einer Schnittstelle verwenden, um Attribute in einer Datei zu ändern, sollten Sie davon ausgehen, dass alle zuvor von der anderen Schnittstelle abgerufenen Indexwerte nicht mehr gültig sind und erneut abgerufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="06bec-113">If you use the methods of one interface to change attributes in a file, you should assume that any index values previously retrieved from the other interface are no longer valid and must be obtained again.</span></span> <span data-ttu-id="06bec-114">Vermeiden Sie die Verwendung der Methoden von **iwmheaderinfo** , wenn dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="06bec-114">You should avoid using the methods of **IWMHeaderInfo** if possible.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="06bec-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06bec-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06bec-116">**Arbeiten mit Metadaten**</span><span class="sxs-lookup"><span data-stu-id="06bec-116">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




