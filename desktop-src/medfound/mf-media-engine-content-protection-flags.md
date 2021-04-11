---
description: Gibt an, ob die Medien-Engine geschützte Inhalte wieder gibt.
ms.assetid: 2A593499-BF40-440E-AF1D-3B0E7732489A
title: MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS-Attribut (MF mediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33feb8d3e1d7c216cfd0392a1fcf9df0100f924
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351349"
---
# <a name="mf_media_engine_content_protection_flags-attribute"></a><span data-ttu-id="50362-103">MF \_ - \_ \_ Attribut für Content \_ Protection \_ Flags für die MF-Medien</span><span class="sxs-lookup"><span data-stu-id="50362-103">MF\_MEDIA\_ENGINE\_CONTENT\_PROTECTION\_FLAGS attribute</span></span>

<span data-ttu-id="50362-104">Gibt an, ob die Medien-Engine geschützte Inhalte wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="50362-104">Specifies whether the Media Engine will play protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="50362-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="50362-105">Data type</span></span>

<span data-ttu-id="50362-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="50362-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="50362-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50362-107">Remarks</span></span>

<span data-ttu-id="50362-108">Der Wert dieses Attributs ist ein bitweises **or** von-Flags aus der-Enumeration der [**MF-Medien-Engine- \_ \_ \_ \_ Schutzflags**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) .</span><span class="sxs-lookup"><span data-stu-id="50362-108">The value of this attribute is a bitwise **OR** of flags from the [**MF\_MEDIA\_ENGINE\_PROTECTION\_FLAGS**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) enumeration.</span></span> <span data-ttu-id="50362-109">Um die Wiedergabe geschützter Inhalte zu aktivieren, legen Sie das Flag zum **\_ \_ \_ aktivieren \_ geschützter \_ Inhalte** für das MF-Medium fest.</span><span class="sxs-lookup"><span data-stu-id="50362-109">To enable playback of protected content, set the **MF\_MEDIA\_ENGINE\_ENABLE\_PROTECTED\_CONTENT** flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="50362-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50362-110">Requirements</span></span>



| <span data-ttu-id="50362-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50362-111">Requirement</span></span> | <span data-ttu-id="50362-112">Wert</span><span class="sxs-lookup"><span data-stu-id="50362-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="50362-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50362-113">Minimum supported client</span></span><br/> | <span data-ttu-id="50362-114">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="50362-114">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="50362-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50362-115">Minimum supported server</span></span><br/> | <span data-ttu-id="50362-116">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="50362-116">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="50362-117">Header</span><span class="sxs-lookup"><span data-stu-id="50362-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="50362-118"><dt>MF mediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="50362-118"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50362-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50362-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50362-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="50362-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="50362-121">Medien-Engine-Attribute</span><span class="sxs-lookup"><span data-stu-id="50362-121">Media Engine Attributes</span></span>](media-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="50362-122">**IMF mediaengineclassfactory:: "forateinstance"**</span><span class="sxs-lookup"><span data-stu-id="50362-122">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




