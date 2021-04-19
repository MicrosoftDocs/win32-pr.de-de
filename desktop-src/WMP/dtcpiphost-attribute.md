---
title: Dtcpiphost-Attribut
description: Das dtcpiphost-Attribut ist der Name oder die IP-Adresse des Computers oder Geräts, der für das Medien Element über den DTCP-IP (Digital Transmission Content Protection over Internet Protocol) kontaktiert werden muss.
ms.assetid: 61b7d6fb-c216-49ae-811a-8ce42fdb71e4
keywords:
- Dtcpiphost-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- DTCPIPHost Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9983cac920f2d11b9040e03af30e10b9c0c3fbcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362049"
---
# <a name="dtcpiphost-attribute"></a><span data-ttu-id="60a3c-104">Dtcpiphost-Attribut</span><span class="sxs-lookup"><span data-stu-id="60a3c-104">DTCPIPHost Attribute</span></span>

<span data-ttu-id="60a3c-105">Das **dtcpiphost** -Attribut ist der Name oder die IP-Adresse des Computers oder Geräts, der für das Medien Element über den DTCP-IP (Digital Transmission Content Protection over Internet Protocol) kontaktiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="60a3c-105">The **DTCPIPHost** attribute is the name or IP address of the computer or device that must be contacted for the Digital Transmission Content Protection over Internet Protocol (DTCP-IP) Authenticated Key Exchange (AKE) for the media item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="60a3c-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="60a3c-106">Applies To</span></span>

-   [<span data-ttu-id="60a3c-107">**Audioelemente**</span><span class="sxs-lookup"><span data-stu-id="60a3c-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="60a3c-108">**Foto Elemente**</span><span class="sxs-lookup"><span data-stu-id="60a3c-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="60a3c-109">**Wiedergabelisten Elemente**</span><span class="sxs-lookup"><span data-stu-id="60a3c-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="60a3c-110">**Video Elemente**</span><span class="sxs-lookup"><span data-stu-id="60a3c-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="60a3c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60a3c-111">Remarks</span></span>

<span data-ttu-id="60a3c-112">Wenn dieses Attribut verfügbar ist, wird das Medien Element mithilfe von DTCP-IP geschützt.</span><span class="sxs-lookup"><span data-stu-id="60a3c-112">If this attribute is available, the media item is protected using DTCP-IP.</span></span>

<span data-ttu-id="60a3c-113">Dieses Attribut ist für Medienelemente in der lokalen Bibliothek des aktuellen Benutzers nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="60a3c-113">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="60a3c-114">Sie ist nur für Medienelemente verfügbar, die zu einer Remote Bibliothek gehören. Das heißt, eine Bibliothek, die von einem anderen Benutzer im Heimnetzwerk verfügbar gemacht wurde.</span><span class="sxs-lookup"><span data-stu-id="60a3c-114">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="60a3c-115">Um zu ermitteln, ob eine Medienbibliothek Remote ist, nennen Sie den [**\_ Typ iwmplibrary:: Get**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="60a3c-115">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="60a3c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60a3c-116">Requirements</span></span>



| <span data-ttu-id="60a3c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60a3c-117">Requirement</span></span> | <span data-ttu-id="60a3c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="60a3c-118">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="60a3c-119">Version</span><span class="sxs-lookup"><span data-stu-id="60a3c-119">Version</span></span><br/> | <span data-ttu-id="60a3c-120">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="60a3c-120">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="60a3c-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60a3c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60a3c-122">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="60a3c-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





