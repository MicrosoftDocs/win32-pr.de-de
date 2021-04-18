---
description: Enthält einen Zeiger auf die Rückruf Schnittstelle für die Medien-Engine.
ms.assetid: 5FAEF29A-B978-410A-8F5B-EB6F7E35EE6D
title: MF_MEDIA_ENGINE_CALLBACK-Attribut (MF mediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1173e22f9d87f4a77f9ed4a1d1b405fc040bd32b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106364991"
---
# <a name="mf_media_engine_callback-attribute"></a><span data-ttu-id="d4e9f-103">\_ \_ \_ Rückruf Attribut der MF-Medien-Engine</span><span class="sxs-lookup"><span data-stu-id="d4e9f-103">MF\_MEDIA\_ENGINE\_CALLBACK attribute</span></span>

<span data-ttu-id="d4e9f-104">Enthält einen Zeiger auf die Rückruf Schnittstelle für die Medien-Engine.</span><span class="sxs-lookup"><span data-stu-id="d4e9f-104">Contains a pointer to the callback interface for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="d4e9f-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d4e9f-105">Data type</span></span>

<span data-ttu-id="d4e9f-106">**IMF mediaenginenotify \* *_ gespeichert als _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="d4e9f-106">**IMFMediaEngineNotify\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="d4e9f-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="d4e9f-107">Get/set</span></span>

<span data-ttu-id="d4e9f-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="d4e9f-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="d4e9f-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="d4e9f-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="d4e9f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4e9f-110">Remarks</span></span>

<span data-ttu-id="d4e9f-111">Der Wert dieses Attributs ist ein Zeiger auf die [**imfmediaenginenotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify) -Schnittstelle, die von der Anwendung implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="d4e9f-111">The value of this attribute is a pointer to the [**IMFMediaEngineNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify) interface, implemented by the application.</span></span>

<span data-ttu-id="d4e9f-112">Dieses Attribut wird mit der [**imfmediaengineclassfactory:: forateinstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) -Methode verwendet, um die Medien-Engine zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="d4e9f-112">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span> <span data-ttu-id="d4e9f-113">Das-Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d4e9f-113">The attribute is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4e9f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4e9f-114">Requirements</span></span>



| <span data-ttu-id="d4e9f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4e9f-115">Requirement</span></span> | <span data-ttu-id="d4e9f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d4e9f-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4e9f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4e9f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d4e9f-118">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d4e9f-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="d4e9f-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4e9f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d4e9f-120">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d4e9f-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="d4e9f-121">Header</span><span class="sxs-lookup"><span data-stu-id="d4e9f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4e9f-122"><dt>MF mediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4e9f-122"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4e9f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4e9f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4e9f-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="d4e9f-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d4e9f-125">**IMF mediaengineclassfactory:: "forateinstance"**</span><span class="sxs-lookup"><span data-stu-id="d4e9f-125">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> <dt>

[<span data-ttu-id="d4e9f-126">**IMF Media enginenotify**</span><span class="sxs-lookup"><span data-stu-id="d4e9f-126">**IMFMediaEngineNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify)
</dt> </dl>

 

 




