---
title: Albumittelalbumartist-Attribut
description: Das albuminalbumartist-Attribut ist ein eindeutiger Bezeichner für das Album.
ms.assetid: beaa8d01-1722-4545-8705-6b3d130113b1
keywords:
- Albuminalbumartist-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- AlbumIDAlbumArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1925f40a50b15efcd339ad949d5d54ddb915cbe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371695"
---
# <a name="albumidalbumartist-attribute"></a><span data-ttu-id="34493-104">Albumittelalbumartist-Attribut</span><span class="sxs-lookup"><span data-stu-id="34493-104">AlbumIDAlbumArtist Attribute</span></span>

<span data-ttu-id="34493-105">Das **albuminalbumartist** -Attribut ist ein eindeutiger Bezeichner für das Album.</span><span class="sxs-lookup"><span data-stu-id="34493-105">The **AlbumIDAlbumArtist** attribute is a unique identifier for the album.</span></span>

## <a name="applies-to"></a><span data-ttu-id="34493-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="34493-106">Applies To</span></span>

-   [<span data-ttu-id="34493-107">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="34493-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="34493-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34493-108">Remarks</span></span>

<span data-ttu-id="34493-109">Dieses Attribut ist nur in der-Bibliothek gespeichert.</span><span class="sxs-lookup"><span data-stu-id="34493-109">This attribute is stored only in the library.</span></span>

<span data-ttu-id="34493-110">Der eindeutige Bezeichner ist eine Kombination aus dem Albumtitel und dem Namen des Album-Künstlers.</span><span class="sxs-lookup"><span data-stu-id="34493-110">The unique identifier is a combination of the album title and the album artist name.</span></span> <span data-ttu-id="34493-111">In diesem Attribut kommt der Name des Album-Künstlers zunächst vor.</span><span class="sxs-lookup"><span data-stu-id="34493-111">In this attribute, the album artist name comes first.</span></span> <span data-ttu-id="34493-112">Wenn Sie die [mediacollection. getAttributeStringCollection](mediacollection-getattributestringcollection.md) -Methode verwenden, um ein **StringCollection** -Objekt mithilfe dieses Attributs zu erhalten, werden die Werte nach dem Namen des Album-Künstlers sortiert.</span><span class="sxs-lookup"><span data-stu-id="34493-112">When you use the [MediaCollection.getAttributeStringCollection](mediacollection-getattributestringcollection.md) method to get a **StringCollection** object using this attribute, the values are sorted by album artist name.</span></span>

<span data-ttu-id="34493-113">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="34493-113">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="34493-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34493-114">Requirements</span></span>



| <span data-ttu-id="34493-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34493-115">Requirement</span></span> | <span data-ttu-id="34493-116">Wert</span><span class="sxs-lookup"><span data-stu-id="34493-116">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="34493-117">Version</span><span class="sxs-lookup"><span data-stu-id="34493-117">Version</span></span><br/> | <span data-ttu-id="34493-118">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="34493-118">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34493-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34493-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34493-120">**AlbumId-Attribut**</span><span class="sxs-lookup"><span data-stu-id="34493-120">**AlbumID Attribute**</span></span>](albumid-attribute.md)
</dt> <dt>

[<span data-ttu-id="34493-121">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="34493-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





