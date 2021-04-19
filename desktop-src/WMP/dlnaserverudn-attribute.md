---
title: Dlnaserverudn-Attribut
description: Das dlnaserverudn-Attribut ist der eindeutige Gerätename des Servers, der das Medien Element hostet.
ms.assetid: 1965731d-1b6e-4d76-a983-fd57c851fcfb
keywords:
- Dlnaserverudn-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- DLNAServerUDN Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caa121df7a4f312e3cb00519d2ac4f519f844d41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359650"
---
# <a name="dlnaserverudn-attribute"></a><span data-ttu-id="28272-104">Dlnaserverudn-Attribut</span><span class="sxs-lookup"><span data-stu-id="28272-104">DLNAServerUDN Attribute</span></span>

<span data-ttu-id="28272-105">Das **dlnaserverudn** -Attribut ist der eindeutige Gerätename des Servers, der das Medien Element hostet.</span><span class="sxs-lookup"><span data-stu-id="28272-105">The **DLNAServerUDN** attribute is the unique device name of the server that hosts the media item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="28272-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="28272-106">Applies To</span></span>

-   [<span data-ttu-id="28272-107">**Audioelemente**</span><span class="sxs-lookup"><span data-stu-id="28272-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="28272-108">**Foto Elemente**</span><span class="sxs-lookup"><span data-stu-id="28272-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="28272-109">**Wiedergabelisten Elemente**</span><span class="sxs-lookup"><span data-stu-id="28272-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="28272-110">**Video Elemente**</span><span class="sxs-lookup"><span data-stu-id="28272-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="28272-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28272-111">Remarks</span></span>

<span data-ttu-id="28272-112">Dieses Attribut ist für Medienelemente in der lokalen Bibliothek des aktuellen Benutzers nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="28272-112">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="28272-113">Sie ist nur für Medienelemente verfügbar, die zu einer Remote Bibliothek gehören. Das heißt, eine Bibliothek, die von einem anderen Benutzer im Heimnetzwerk verfügbar gemacht wurde.</span><span class="sxs-lookup"><span data-stu-id="28272-113">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="28272-114">Um zu ermitteln, ob eine Medienbibliothek Remote ist, nennen Sie den [**\_ Typ iwmplibrary:: Get**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="28272-114">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="28272-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28272-115">Requirements</span></span>



| <span data-ttu-id="28272-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28272-116">Requirement</span></span> | <span data-ttu-id="28272-117">Wert</span><span class="sxs-lookup"><span data-stu-id="28272-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="28272-118">Version</span><span class="sxs-lookup"><span data-stu-id="28272-118">Version</span></span><br/> | <span data-ttu-id="28272-119">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="28272-119">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="28272-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28272-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28272-121">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="28272-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





