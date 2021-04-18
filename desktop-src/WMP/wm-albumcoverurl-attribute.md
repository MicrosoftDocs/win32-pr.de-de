---
title: WM/albumcoverurl-Attribut
description: Das WM/albumcoverurl-Attribut ist die URL (Uniform Resource Serverlocatorpunkt) für Albumkunst oder ein Miniaturbild.
ms.assetid: 0134867a-7c11-4d50-9ab5-b48c1ca6c473
keywords:
- WM/albumcoverurl-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- WM/AlbumCoverURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939c5451f3ae8f41214a817293e3c7f3cb3b66c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357637"
---
# <a name="wmalbumcoverurl-attribute"></a><span data-ttu-id="3217e-104">WM/albumcoverurl-Attribut</span><span class="sxs-lookup"><span data-stu-id="3217e-104">WM/AlbumCoverURL Attribute</span></span>

<span data-ttu-id="3217e-105">Das **WM/albumcoverurl-** Attribut ist die URL (Uniform Resource Serverlocatorpunkt) für Albumkunst oder ein Miniaturbild.</span><span class="sxs-lookup"><span data-stu-id="3217e-105">The **WM/AlbumCoverURL** attribute is the uniform resource locator (URL) for album art or a thumbnail image.</span></span>

## <a name="applies-to"></a><span data-ttu-id="3217e-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="3217e-106">Applies To</span></span>

-   [<span data-ttu-id="3217e-107">**Audioelemente**</span><span class="sxs-lookup"><span data-stu-id="3217e-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="3217e-108">**Foto Elemente**</span><span class="sxs-lookup"><span data-stu-id="3217e-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="3217e-109">**Video Elemente**</span><span class="sxs-lookup"><span data-stu-id="3217e-109">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="3217e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3217e-110">Remarks</span></span>

<span data-ttu-id="3217e-111">Bei einem Audioelement ist dieses Attribut die URL der Albumgrafik.</span><span class="sxs-lookup"><span data-stu-id="3217e-111">For an audio item, this attribute is the URL of the album art.</span></span> <span data-ttu-id="3217e-112">Bei einem Foto-oder Video Element ist dieses Attribut die URL eines Miniatur Bilds.</span><span class="sxs-lookup"><span data-stu-id="3217e-112">For a photo or video item, this attribute is the URL of a thumbnail image.</span></span>

<span data-ttu-id="3217e-113">Dieses Attribut ist für Medienelemente in der lokalen Bibliothek des aktuellen Benutzers nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3217e-113">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="3217e-114">Sie ist nur für Medienelemente verfügbar, die zu einer Remote Bibliothek gehören. Das heißt, eine Bibliothek, die von einem anderen Benutzer im Heimnetzwerk verfügbar gemacht wurde.</span><span class="sxs-lookup"><span data-stu-id="3217e-114">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="3217e-115">Um zu ermitteln, ob eine Medienbibliothek Remote ist, nennen Sie den [**\_ Typ iwmplibrary:: Get**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="3217e-115">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="3217e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3217e-116">Requirements</span></span>



| <span data-ttu-id="3217e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3217e-117">Requirement</span></span> | <span data-ttu-id="3217e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3217e-118">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="3217e-119">Version</span><span class="sxs-lookup"><span data-stu-id="3217e-119">Version</span></span><br/> | <span data-ttu-id="3217e-120">Windows Media Player 12 oder höher.</span><span class="sxs-lookup"><span data-stu-id="3217e-120">Windows Media Player 12 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3217e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3217e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3217e-122">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="3217e-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





