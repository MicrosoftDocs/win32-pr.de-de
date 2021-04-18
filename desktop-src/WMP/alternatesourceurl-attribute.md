---
title: "\"Alternative\"-Attribut"
description: Das Attribut "appliesourceurl" ist ein einheitlicher ressourcenlocator für das Medien Element, das als Alternative zu den Attributen "dlnasourceuri" und "SourceUrl" fungiert.
ms.assetid: 2be88d9b-4fd8-4e70-9a4d-114a2bf8b23c
keywords:
- Media Player des alternativen ceurdeurl-Attributs
topic_type:
- apiref
api_name:
- AlternateSourceURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574a355dfa862c4db004fa2df942e464934a38ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364967"
---
# <a name="alternatesourceurl-attribute"></a><span data-ttu-id="b8075-104">"Alternative"-Attribut</span><span class="sxs-lookup"><span data-stu-id="b8075-104">AlternateSourceURL Attribute</span></span>

<span data-ttu-id="b8075-105">Das Attribut " **appliesourceurl** " ist ein einheitlicher ressourcenlocator für das Medien Element, das als Alternative zu den Attributen " [**dlnasourceuri**](dlnasourceuri-attribute.md) " und " [**SourceUrl**](sourceurl-attribute.md) " fungiert.</span><span class="sxs-lookup"><span data-stu-id="b8075-105">The **AlternateSourceURL** attribute is a uniform resource locator for the media item that serves as an alternative to the [**DLNASourceURI**](dlnasourceuri-attribute.md) and [**SourceURL**](sourceurl-attribute.md) attributes.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b8075-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="b8075-106">Applies To</span></span>

-   [<span data-ttu-id="b8075-107">**Audioelemente**</span><span class="sxs-lookup"><span data-stu-id="b8075-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="b8075-108">**Foto Elemente**</span><span class="sxs-lookup"><span data-stu-id="b8075-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="b8075-109">**Wiedergabelisten Elemente**</span><span class="sxs-lookup"><span data-stu-id="b8075-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="b8075-110">**Video Elemente**</span><span class="sxs-lookup"><span data-stu-id="b8075-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="b8075-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8075-111">Remarks</span></span>

<span data-ttu-id="b8075-112">Dieses Attribut ist für Medienelemente in der lokalen Bibliothek des aktuellen Benutzers nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b8075-112">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="b8075-113">Sie ist nur für Medienelemente verfügbar, die zu einer Remote Bibliothek gehören. Das heißt, eine Bibliothek, die von einem anderen Benutzer im Heimnetzwerk verfügbar gemacht wurde.</span><span class="sxs-lookup"><span data-stu-id="b8075-113">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="b8075-114">Um zu ermitteln, ob eine Medienbibliothek Remote ist, nennen Sie den [**\_ Typ iwmplibrary:: Get**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="b8075-114">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8075-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8075-115">Requirements</span></span>



| <span data-ttu-id="b8075-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8075-116">Requirement</span></span> | <span data-ttu-id="b8075-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b8075-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="b8075-118">Version</span><span class="sxs-lookup"><span data-stu-id="b8075-118">Version</span></span><br/> | <span data-ttu-id="b8075-119">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="b8075-119">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b8075-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8075-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8075-121">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="b8075-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





