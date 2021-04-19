---
title: Dtcpipport-Attribut
description: Das dtcpipport-Attribut ist die TCP-Portnummer (Transmission Control Protocol) des Computers oder Geräts, die für das Medien Element über den DTCP-IP (Digital Transmission Content Protection over Internet Protocol) kontaktiert werden muss.
ms.assetid: 63767ec1-dd01-40c2-bf9a-6e9b8a7db7f8
keywords:
- Dtcpipport-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- DTCPIPPort Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c1c6117425211c0015d218412c8a9ac0971d7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369308"
---
# <a name="dtcpipport-attribute"></a><span data-ttu-id="f5b7f-104">Dtcpipport-Attribut</span><span class="sxs-lookup"><span data-stu-id="f5b7f-104">DTCPIPPort Attribute</span></span>

<span data-ttu-id="f5b7f-105">Das **dtcpipport** -Attribut ist die TCP-Portnummer (Transmission Control Protocol) des Computers oder Geräts, die für das Medien Element über den DTCP-IP (Digital Transmission Content Protection over Internet Protocol) kontaktiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="f5b7f-105">The **DTCPIPPort** attribute is the Transmission Control Protocol (TCP) port number of the computer or device that must be contacted for the Digital Transmission Content Protection over Internet Protocol (DTCP-IP) Authenticated Key Exchange (AKE) for the media item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f5b7f-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="f5b7f-106">Applies To</span></span>

-   [<span data-ttu-id="f5b7f-107">**Audioelemente**</span><span class="sxs-lookup"><span data-stu-id="f5b7f-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="f5b7f-108">**Foto Elemente**</span><span class="sxs-lookup"><span data-stu-id="f5b7f-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="f5b7f-109">**Wiedergabelisten Elemente**</span><span class="sxs-lookup"><span data-stu-id="f5b7f-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="f5b7f-110">**Video Elemente**</span><span class="sxs-lookup"><span data-stu-id="f5b7f-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="f5b7f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5b7f-111">Remarks</span></span>

<span data-ttu-id="f5b7f-112">Wenn dieses Attribut verfügbar ist, wird das Medien Element mithilfe von DTCP-IP geschützt.</span><span class="sxs-lookup"><span data-stu-id="f5b7f-112">If this attribute is available, the media item is protected using DTCP-IP.</span></span>

<span data-ttu-id="f5b7f-113">Dieses Attribut ist für Medienelemente in der lokalen Bibliothek des aktuellen Benutzers nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f5b7f-113">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="f5b7f-114">Sie ist nur für Medienelemente verfügbar, die zu einer Remote Bibliothek gehören. Das heißt, eine Bibliothek, die von einem anderen Benutzer im Heimnetzwerk verfügbar gemacht wurde.</span><span class="sxs-lookup"><span data-stu-id="f5b7f-114">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="f5b7f-115">Um zu ermitteln, ob eine Medienbibliothek Remote ist, nennen Sie den [**\_ Typ iwmplibrary:: Get**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="f5b7f-115">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5b7f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5b7f-116">Requirements</span></span>



| <span data-ttu-id="f5b7f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5b7f-117">Requirement</span></span> | <span data-ttu-id="f5b7f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f5b7f-118">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="f5b7f-119">Version</span><span class="sxs-lookup"><span data-stu-id="f5b7f-119">Version</span></span><br/> | <span data-ttu-id="f5b7f-120">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="f5b7f-120">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f5b7f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5b7f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5b7f-122">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="f5b7f-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





