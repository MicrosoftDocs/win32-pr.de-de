---
description: Gibt die Drehung eines Video Frames in der Richtung gegen den Uhrzeigersinn an.
ms.assetid: 7C0911A6-6D7C-4510-891F-A6F56CE1EC2B
title: MF_MT_VIDEO_ROTATION-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f46a67c9861b8094e909e5c6fd7bc82e46166dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868936"
---
# <a name="mf_mt_video_rotation-attribute"></a><span data-ttu-id="e73b4-103">MF- \_ MT- \_ Video- \_ Rotations Attribut</span><span class="sxs-lookup"><span data-stu-id="e73b4-103">MF\_MT\_VIDEO\_ROTATION attribute</span></span>

<span data-ttu-id="e73b4-104">Gibt die Drehung eines Video Frames in der Richtung gegen den Uhrzeigersinn an.</span><span class="sxs-lookup"><span data-stu-id="e73b4-104">Specifies the rotation of a video frame in the counter-clockwise direction.</span></span>

## <a name="data-type"></a><span data-ttu-id="e73b4-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e73b4-105">Data type</span></span>

<span data-ttu-id="e73b4-106">**MF videorotationformat** , gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e73b4-106">**MFVideoRotationFormat** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e73b4-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e73b4-107">Remarks</span></span>

<span data-ttu-id="e73b4-108">Video von einem Hand Held Gerät, z. b. ein Mobiltelefon, wird häufig um 90, 180 oder 270 Grad gedreht.</span><span class="sxs-lookup"><span data-stu-id="e73b4-108">Video from a handheld device, such as a mobile phone, is often rotated by 90, 180, or 270 degrees.</span></span> <span data-ttu-id="e73b4-109">Wenn die Kamera die Ausrichtung als Metadaten in der Videodatei speichert, kann das Bild zum Zeitpunkt der Wiedergabe angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="e73b4-109">If the camera stores the orientation as metadata in the video file, the image can be adjusted at the time of playback.</span></span>

<span data-ttu-id="e73b4-110">Wenn dieses Attribut auf **mfvideorotationformat \_ 90** festgelegt ist, bedeutet dies, dass der Inhalt um 90 Grad in der Richtung gegen den Uhrzeigersinn gedreht wurde.</span><span class="sxs-lookup"><span data-stu-id="e73b4-110">If this attribute set to **MFVideoRotationFormat\_90**, it means that the content has been rotated 90 degrees in the counter-clockwise direction.</span></span> <span data-ttu-id="e73b4-111">Wenn der Inhalt 90 Grad in der Richtung im Uhrzeigersinn gedreht wurde, wäre der Attribut Wert **MF videorotationformat \_ 270**.</span><span class="sxs-lookup"><span data-stu-id="e73b4-111">If the content was rotated 90 degrees in the clockwise direction, the attribute value would be **MFVideoRotationFormat\_270**.</span></span>

<span data-ttu-id="e73b4-112">Die unterstützten Werte für dieses Attribut werden in [**MF videorotationformat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat)aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e73b4-112">The supported values for this attribute are enumerated in [**MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat).</span></span>

<span data-ttu-id="e73b4-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="e73b4-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e73b4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e73b4-114">Requirements</span></span>



| <span data-ttu-id="e73b4-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e73b4-115">Requirement</span></span> | <span data-ttu-id="e73b4-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e73b4-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e73b4-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e73b4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e73b4-118">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e73b4-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="e73b4-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e73b4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e73b4-120">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e73b4-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e73b4-121">Header</span><span class="sxs-lookup"><span data-stu-id="e73b4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e73b4-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e73b4-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e73b4-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e73b4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e73b4-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="e73b4-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e73b4-125">Medientypen</span><span class="sxs-lookup"><span data-stu-id="e73b4-125">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




