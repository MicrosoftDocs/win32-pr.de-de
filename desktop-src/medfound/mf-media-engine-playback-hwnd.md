---
description: Legt ein Handle für ein Videowiedergabe Fenster für die Medien-Engine fest.
ms.assetid: 63889D81-12C5-47C1-B52A-6358E68830C3
title: MF_MEDIA_ENGINE_PLAYBACK_HWND-Attribut (MF mediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6a9d38d40b04b32244f48289d3334199a7e035
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961126"
---
# <a name="mf_media_engine_playback_hwnd-attribute"></a><span data-ttu-id="bb9f5-103">Der MF- \_ Medien- \_ Engine-Wiedergabe- \_ \_ HWND</span><span class="sxs-lookup"><span data-stu-id="bb9f5-103">MF\_MEDIA\_ENGINE\_PLAYBACK\_HWND attribute</span></span>

<span data-ttu-id="bb9f5-104">Legt ein Handle für ein Videowiedergabe Fenster für die Medien-Engine fest.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-104">Sets a handle to a video playback window for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="bb9f5-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bb9f5-105">Data type</span></span>

<span data-ttu-id="bb9f5-106">**HWND** als **UINT64** gespeichert</span><span class="sxs-lookup"><span data-stu-id="bb9f5-106">**HWND** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="bb9f5-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="bb9f5-107">Get/set</span></span>

<span data-ttu-id="bb9f5-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="bb9f5-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="bb9f5-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="bb9f5-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="remarks"></a><span data-ttu-id="bb9f5-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb9f5-110">Remarks</span></span>

<span data-ttu-id="bb9f5-111">Dieses Attribut wird mit der [**imfmediaengineclassfactory:: forateinstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) -Methode verwendet, um die Medien-Engine zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-111">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb9f5-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb9f5-112">Requirements</span></span>



| <span data-ttu-id="bb9f5-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb9f5-113">Requirement</span></span> | <span data-ttu-id="bb9f5-114">Wert</span><span class="sxs-lookup"><span data-stu-id="bb9f5-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb9f5-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb9f5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bb9f5-116">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bb9f5-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="bb9f5-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb9f5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bb9f5-118">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bb9f5-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="bb9f5-119">Header</span><span class="sxs-lookup"><span data-stu-id="bb9f5-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb9f5-120"><dt>MF mediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb9f5-120"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb9f5-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb9f5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb9f5-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="bb9f5-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




