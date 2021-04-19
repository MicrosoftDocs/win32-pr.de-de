---
title: LIBRARYID-Attribut
description: Das LIBRARYID-Attribut ist der Bezeichner der Bibliothek, zu der das Element gehört.
ms.assetid: 680d9374-8729-4258-8672-b4b93b65e20a
keywords:
- LIBRARYID-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- LibraryID Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ae9e5ad097bc188b8de1e76a09448c57aa9b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368418"
---
# <a name="libraryid-attribute"></a><span data-ttu-id="23561-104">LIBRARYID-Attribut</span><span class="sxs-lookup"><span data-stu-id="23561-104">LibraryID Attribute</span></span>

<span data-ttu-id="23561-105">Das **LIBRARYID** -Attribut ist der Bezeichner der Bibliothek, zu der das Element gehört.</span><span class="sxs-lookup"><span data-stu-id="23561-105">The **LibraryID** attribute is the identifier of the library that the item belongs to.</span></span>

## <a name="applies-to"></a><span data-ttu-id="23561-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="23561-106">Applies To</span></span>

-   [<span data-ttu-id="23561-107">**Audioelemente**</span><span class="sxs-lookup"><span data-stu-id="23561-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="23561-108">**Foto Elemente**</span><span class="sxs-lookup"><span data-stu-id="23561-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="23561-109">**Wiedergabelisten Elemente**</span><span class="sxs-lookup"><span data-stu-id="23561-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="23561-110">**Video Elemente**</span><span class="sxs-lookup"><span data-stu-id="23561-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="23561-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23561-111">Remarks</span></span>

<span data-ttu-id="23561-112">Ein Medien Element kann der lokalen Bibliothek des aktuellen Benutzers angehören, oder es kann einer Bibliothek angehören, die von einem anderen Benutzer im Heimnetzwerk oder im Internet zur Verfügung gestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="23561-112">A media item might belong to the current user's local library or it might belong to a library that has been made available by another user on the home network or the Internet.</span></span>

<span data-ttu-id="23561-113">Der Wert dieses Attributs entspricht dem Wert, der von der [**IWMPLibrary2:: getiteminfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="23561-113">The value of this attribute is the same as the value returned by the [**IWMPLibrary2::getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="23561-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23561-114">Requirements</span></span>



| <span data-ttu-id="23561-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23561-115">Requirement</span></span> | <span data-ttu-id="23561-116">Wert</span><span class="sxs-lookup"><span data-stu-id="23561-116">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="23561-117">Version</span><span class="sxs-lookup"><span data-stu-id="23561-117">Version</span></span><br/> | <span data-ttu-id="23561-118">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="23561-118">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="23561-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23561-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23561-120">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="23561-120">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





