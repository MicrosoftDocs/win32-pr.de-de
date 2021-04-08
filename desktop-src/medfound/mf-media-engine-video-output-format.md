---
description: Legt das Renderziel-Format für die Medien-Engine fest.
ms.assetid: 70FFDD44-9FDE-4D86-AD65-60019AC4A2BC
title: MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT-Attribut (MF mediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004025da1ad5258e5b04a3afba4a359f50f7444c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761385"
---
# <a name="mf_media_engine_video_output_format-attribute"></a><span data-ttu-id="eb2d2-103">Format Attribut der MF- \_ Medien-Engine- \_ \_ Video \_ Ausgabe \_</span><span class="sxs-lookup"><span data-stu-id="eb2d2-103">MF\_MEDIA\_ENGINE\_VIDEO\_OUTPUT\_FORMAT attribute</span></span>

<span data-ttu-id="eb2d2-104">Legt das Renderziel-Format für die Medien-Engine fest.</span><span class="sxs-lookup"><span data-stu-id="eb2d2-104">Sets the render-target format for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="eb2d2-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="eb2d2-105">Data type</span></span>

<span data-ttu-id="eb2d2-106">**DXGI \_** Als **UInt32** gespeicherter Format</span><span class="sxs-lookup"><span data-stu-id="eb2d2-106">**DXGI\_FORMAT** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="eb2d2-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb2d2-107">Remarks</span></span>

<span data-ttu-id="eb2d2-108">Legen Sie dieses Attribut fest, wenn Sie die Medien-Engine im Frame Server Modus erstellen.</span><span class="sxs-lookup"><span data-stu-id="eb2d2-108">Set this attribute if you create the Media Engine in frame-server mode.</span></span> <span data-ttu-id="eb2d2-109">Weitere Informationen finden Sie unter [**IMF mediaengineclassfactory:: forateinstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span><span class="sxs-lookup"><span data-stu-id="eb2d2-109">For more information, see [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span></span> <span data-ttu-id="eb2d2-110">Der Wert des-Attributs ist ein [DXGI- \_ Format](../direct3d9/d3dformat.md) Wert.</span><span class="sxs-lookup"><span data-stu-id="eb2d2-110">The value of the attribute is a [DXGI\_FORMAT](../direct3d9/d3dformat.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb2d2-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb2d2-111">Requirements</span></span>



| <span data-ttu-id="eb2d2-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb2d2-112">Requirement</span></span> | <span data-ttu-id="eb2d2-113">Wert</span><span class="sxs-lookup"><span data-stu-id="eb2d2-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb2d2-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb2d2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="eb2d2-115">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="eb2d2-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="eb2d2-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb2d2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="eb2d2-117">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="eb2d2-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="eb2d2-118">Header</span><span class="sxs-lookup"><span data-stu-id="eb2d2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb2d2-119"><dt>MF mediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb2d2-119"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb2d2-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb2d2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb2d2-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="eb2d2-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
