---
description: Legt die Microsoft DirectX Graphics Infrastructure (DXGI)-Device Manager für die Medien-Engine fest.
ms.assetid: CB952492-0ACF-4501-BD8B-133E26FCE8F7
title: MF_MEDIA_ENGINE_DXGI_MANAGER-Attribut (MF mediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98e731b5aa2449ae772427c6743ec4f97b5d7601
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106351196"
---
# <a name="mf_media_engine_dxgi_manager-attribute"></a><span data-ttu-id="8dc4c-103">\_ \_ \_ DXGI \_ Manager-Attribut der MF-Medien-Engine</span><span class="sxs-lookup"><span data-stu-id="8dc4c-103">MF\_MEDIA\_ENGINE\_DXGI\_MANAGER attribute</span></span>

<span data-ttu-id="8dc4c-104">Legt die Microsoft DirectX Graphics Infrastructure (DXGI)-Device Manager für die Medien-Engine fest.</span><span class="sxs-lookup"><span data-stu-id="8dc4c-104">Sets the Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager on the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="8dc4c-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8dc4c-105">Data type</span></span>

<span data-ttu-id="8dc4c-106">**IMF dxgidebug Manager \* *_ gespeichert als _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="8dc4c-106">**IMFDXGIDeviceManager\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="8dc4c-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="8dc4c-107">Get/set</span></span>

<span data-ttu-id="8dc4c-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="8dc4c-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="8dc4c-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="8dc4c-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="8dc4c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8dc4c-110">Remarks</span></span>

<span data-ttu-id="8dc4c-111">Der Wert dieses Attributs ist ein Zeiger auf die [**imfdxgidebug Manager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8dc4c-111">The value of this attribute is a pointer to the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span>

<span data-ttu-id="8dc4c-112">Im Frame-Server-Modus ermöglicht dieses Attribut der Medien-Engine die Verwendung der Hardwarebeschleunigung für Video Decodierung und Videoverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="8dc4c-112">In frame-server mode, this attribute enables the Media Engine to use hardware acceleration for video decoding and video processing.</span></span> <span data-ttu-id="8dc4c-113">Wenn das-Attribut nicht festgelegt ist, verwendet die Medien-Engine Debuggen und Verarbeiten von Software.</span><span class="sxs-lookup"><span data-stu-id="8dc4c-113">If the attribute is not set, the Media Engine uses software decoding and processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dc4c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8dc4c-114">Requirements</span></span>



| <span data-ttu-id="8dc4c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8dc4c-115">Requirement</span></span> | <span data-ttu-id="8dc4c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8dc4c-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dc4c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8dc4c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8dc4c-118">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="8dc4c-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="8dc4c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8dc4c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8dc4c-120">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="8dc4c-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="8dc4c-121">Header</span><span class="sxs-lookup"><span data-stu-id="8dc4c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dc4c-122"><dt>MF mediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dc4c-122"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dc4c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8dc4c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dc4c-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="8dc4c-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8dc4c-125">**IMF mediaengineclassfactory:: "forateinstance"**</span><span class="sxs-lookup"><span data-stu-id="8dc4c-125">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




