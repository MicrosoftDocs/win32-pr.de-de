---
title: AlbumId-Attribut
description: Das albumId-Attribut ist ein eindeutiger Bezeichner für das Album.
ms.assetid: 0412d91a-11a7-434c-8717-a71d85655679
keywords:
- Fenster Media Player "albumId"-Attribut
topic_type:
- apiref
api_name:
- AlbumID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339253c82554579fa549371e2ebe4cb2f1926cc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367153"
---
# <a name="albumid-attribute"></a><span data-ttu-id="87d01-104">AlbumId-Attribut</span><span class="sxs-lookup"><span data-stu-id="87d01-104">AlbumID Attribute</span></span>

<span data-ttu-id="87d01-105">Das **albumId** -Attribut ist ein eindeutiger Bezeichner für das Album.</span><span class="sxs-lookup"><span data-stu-id="87d01-105">The **AlbumID** attribute is a unique identifier for the album.</span></span>

## <a name="applies-to"></a><span data-ttu-id="87d01-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="87d01-106">Applies To</span></span>

-   [<span data-ttu-id="87d01-107">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="87d01-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="87d01-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87d01-108">Remarks</span></span>

<span data-ttu-id="87d01-109">Dieses Attribut ist nur in der-Bibliothek gespeichert.</span><span class="sxs-lookup"><span data-stu-id="87d01-109">This attribute is stored only in the library.</span></span>

<span data-ttu-id="87d01-110">Der eindeutige Bezeichner ist eine Kombination aus dem Albumtitel und dem Namen des Album-Künstlers.</span><span class="sxs-lookup"><span data-stu-id="87d01-110">The unique identifier is a combination of the album title and the album artist name.</span></span> <span data-ttu-id="87d01-111">In diesem Attribut kommt der Titel des Albums zuerst vor.</span><span class="sxs-lookup"><span data-stu-id="87d01-111">In this attribute, the album title comes first.</span></span> <span data-ttu-id="87d01-112">Wenn Sie die [mediacollection. getAttributeStringCollection](mediacollection-getattributestringcollection.md) -Methode verwenden, um ein **StringCollection** -Objekt mit diesem Attribut zu erhalten, werden die Werte nach dem Titel des Albums sortiert.</span><span class="sxs-lookup"><span data-stu-id="87d01-112">When you use the [MediaCollection.getAttributeStringCollection](mediacollection-getattributestringcollection.md) method to get a **StringCollection** object using this attribute, the values are sorted by album title.</span></span>

<span data-ttu-id="87d01-113">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="87d01-113">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="87d01-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87d01-114">Requirements</span></span>



| <span data-ttu-id="87d01-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87d01-115">Requirement</span></span> | <span data-ttu-id="87d01-116">Wert</span><span class="sxs-lookup"><span data-stu-id="87d01-116">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="87d01-117">Version</span><span class="sxs-lookup"><span data-stu-id="87d01-117">Version</span></span><br/> | <span data-ttu-id="87d01-118">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="87d01-118">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="87d01-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87d01-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87d01-120">**Albumittelalbumartist-Attribut**</span><span class="sxs-lookup"><span data-stu-id="87d01-120">**AlbumIDAlbumArtist Attribute**</span></span>](albumidalbumartist-attribute.md)
</dt> <dt>

[<span data-ttu-id="87d01-121">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="87d01-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





