---
description: Enthält einen Zeiger auf die imfmediaengineextension-Schnittstelle.
ms.assetid: D2F3F41D-086A-4DEB-99D0-07574BC8F0D7
title: MF_MEDIA_ENGINE_EXTENSION-Attribut (MF mediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4496b40e9b69091b588ad38ad47d943dce5e1966
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104393862"
---
# <a name="mf_media_engine_extension-attribute"></a><span data-ttu-id="4aaf6-103">\_ \_ \_ Erweiterungs Attribut der MF-Medien-Engine</span><span class="sxs-lookup"><span data-stu-id="4aaf6-103">MF\_MEDIA\_ENGINE\_EXTENSION attribute</span></span>

<span data-ttu-id="4aaf6-104">Enthält einen Zeiger auf die [**imfmediaengineextension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-104">Contains a pointer to the [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="4aaf6-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4aaf6-105">Data type</span></span>

<span data-ttu-id="4aaf6-106">**IMF mediaengineextension \* *_ gespeichert als _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="4aaf6-106">**IMFMediaEngineExtension\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="4aaf6-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="4aaf6-107">Get/set</span></span>

<span data-ttu-id="4aaf6-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="4aaf6-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="4aaf6-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="4aaf6-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="4aaf6-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4aaf6-110">Remarks</span></span>

<span data-ttu-id="4aaf6-111">Dieses Attribut wird mit der [**imfmediaengineclassfactory:: forateinstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) -Methode verwendet, um die Medien-Engine zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-111">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

<span data-ttu-id="4aaf6-112">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-112">This attribute is optional.</span></span> <span data-ttu-id="4aaf6-113">Verwenden Sie es, um ein Objekt bereitzustellen, das die [**imfmediaengineextension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-113">Use it to provide an object that implements the [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) interface.</span></span> <span data-ttu-id="4aaf6-114">Diese Schnittstelle ermöglicht es der Anwendung, benutzerdefinierte Medienressourcen zu laden.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-114">This interface enables the application to load custom media resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aaf6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4aaf6-115">Requirements</span></span>



| <span data-ttu-id="4aaf6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4aaf6-116">Requirement</span></span> | <span data-ttu-id="4aaf6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4aaf6-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aaf6-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4aaf6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4aaf6-119">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4aaf6-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="4aaf6-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4aaf6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4aaf6-121">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4aaf6-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="4aaf6-122">Header</span><span class="sxs-lookup"><span data-stu-id="4aaf6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4aaf6-123"><dt>MF mediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="4aaf6-123"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aaf6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4aaf6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aaf6-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4aaf6-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




