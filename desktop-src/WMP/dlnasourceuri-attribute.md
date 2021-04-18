---
title: Dlnasourceuri-Attribut
description: Das dlnasourceuri-Attribut ist der universelle Ressourcen Bezeichner (URI) des Elements.
ms.assetid: 323c897b-9b76-44f7-9313-c51595589583
keywords:
- Dlnasourceuri-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- DLNASourceURI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ebe21a39a67dec9356c5dd5360efb48f4ef029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366033"
---
# <a name="dlnasourceuri-attribute"></a><span data-ttu-id="488ac-104">Dlnasourceuri-Attribut</span><span class="sxs-lookup"><span data-stu-id="488ac-104">DLNASourceURI Attribute</span></span>

<span data-ttu-id="488ac-105">Das **dlnasourceuri** -Attribut ist der universelle Ressourcen Bezeichner (URI) des Elements.</span><span class="sxs-lookup"><span data-stu-id="488ac-105">The **DLNASourceURI** attribute is the universal resource identifier (URI) of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="488ac-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="488ac-106">Applies To</span></span>

-   [<span data-ttu-id="488ac-107">**Audioelemente**</span><span class="sxs-lookup"><span data-stu-id="488ac-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="488ac-108">**Andere Elemente**</span><span class="sxs-lookup"><span data-stu-id="488ac-108">**Other Items**</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="488ac-109">**Foto Elemente**</span><span class="sxs-lookup"><span data-stu-id="488ac-109">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="488ac-110">**Wiedergabelisten Elemente**</span><span class="sxs-lookup"><span data-stu-id="488ac-110">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="488ac-111">**Video Elemente**</span><span class="sxs-lookup"><span data-stu-id="488ac-111">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="488ac-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="488ac-112">Remarks</span></span>

<span data-ttu-id="488ac-113">Wenn sich das Element in der lokalen Bibliothek des aktuellen Benutzers befindet, sind dieses Attribut, das [**SourceUrl**](sourceurl-attribute.md) -Attribut und der von [**iwmpmedia:: get \_ SourceUrl**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) zurückgegebene Wert identisch.</span><span class="sxs-lookup"><span data-stu-id="488ac-113">If the item is in the current user's local library, this attribute, the [**SourceURL**](sourceurl-attribute.md) attribute, and the value returned by [**IWMPMedia::get\_sourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) are all the same.</span></span>

<span data-ttu-id="488ac-114">Wenn sich das Element nicht in der lokalen Bibliothek des aktuellen Benutzers befindet, aber zu einer Remote Bibliothek gehört, ist dieses Attribut ein Bezeichner der Form DLNA-playsingle://*xxx*.</span><span class="sxs-lookup"><span data-stu-id="488ac-114">If the item is not in the current user's local library, but belongs to a remote library, this attribute is an identifier of the form dlna-playsingle://*xxx*.</span></span>

<span data-ttu-id="488ac-115">Sie können einen DLNA-playsingle-URI an die [**IWMPCore3:: newmedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) -Methode übergeben, um eine [**iwmpmedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) -Schnittstelle zu erhalten, die es Ihnen ermöglicht, die Metadaten des Medien Elements anzuzeigen und ggf. die Stern Bewertung des Medien Elements zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="488ac-115">You can pass a dlna-playsingle URI to the [**IWMPCore3::newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) method to obtain an [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) interface that enables you to view the media item's metadata and potentially edit the media item's star rating.</span></span> <span data-ttu-id="488ac-116">Beachten Sie jedoch, dass der DLNA-playsingle-URI für einen Inhaltsverzeichnis Dienst (CDs) gelten muss, den Windows Media Player bereits ermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="488ac-116">Note, however, that the dlna-playsingle URI must be for a content directory service (CDS) that Windows Media Player has already discovered.</span></span> <span data-ttu-id="488ac-117">Die **newmedia** -Methode initiiert keine UPnP-Ermittlung und sucht nach den CDs.</span><span class="sxs-lookup"><span data-stu-id="488ac-117">The **newMedia** method will not initiate UPnP discovery and search for the CDS.</span></span>

<span data-ttu-id="488ac-118">Sie können die Stern Bewertung eines Medien Elements nur in einer Remote Bibliothek bearbeiten, wenn die Remote Bibliothek den Bearbeitungsvorgang unterstützt.</span><span class="sxs-lookup"><span data-stu-id="488ac-118">You can edit the star rating of a media item in a remote library only if the remote library supports the edit operation.</span></span> <span data-ttu-id="488ac-119">Remote Bibliotheken, die auf einem Computer unter Windows 7 gehostet werden, unterstützen den Bearbeitungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="488ac-119">Remote libraries hosted on a computer running Windows 7 support the edit operation.</span></span> <span data-ttu-id="488ac-120">Bei Remote Bibliotheken, die auf einem Computer mit einem älteren Windows-Betriebssystem als Windows 7 gehostet werden, wird der Bearbeitungsvorgang nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="488ac-120">Remote libraries hosted on a computer running a Windows operating system earlier than Windows 7 do not support the edit operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="488ac-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="488ac-121">Requirements</span></span>



| <span data-ttu-id="488ac-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="488ac-122">Requirement</span></span> | <span data-ttu-id="488ac-123">Wert</span><span class="sxs-lookup"><span data-stu-id="488ac-123">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="488ac-124">Version</span><span class="sxs-lookup"><span data-stu-id="488ac-124">Version</span></span><br/> | <span data-ttu-id="488ac-125">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="488ac-125">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="488ac-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="488ac-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="488ac-127">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="488ac-127">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





