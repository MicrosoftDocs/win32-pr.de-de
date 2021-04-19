---
description: Enthält Flags, um den audiorenderer zu konfigurieren.
ms.assetid: 07433904-1bf6-4e8d-9571-8d663bf4fd13
title: MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c17d4b5a51384ebcd180643e0a07601d25e5fb5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350551"
---
# <a name="mf_audio_renderer_attribute_flags-attribute"></a><span data-ttu-id="b9013-103">Attribut \_ Flags-Attribut für MF- \_ audiorenderer \_ \_</span><span class="sxs-lookup"><span data-stu-id="b9013-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS attribute</span></span>

<span data-ttu-id="b9013-104">Enthält Flags, um den audiorenderer zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b9013-104">Contains flags to configure the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="b9013-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b9013-105">Data type</span></span>

<span data-ttu-id="b9013-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b9013-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b9013-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9013-107">Remarks</span></span>

<span data-ttu-id="b9013-108">Der Wert dieses Attributs ist ein bitweises **or** der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="b9013-108">The value of this attribute is a bitwise **OR** of the following flags.</span></span>



| <span data-ttu-id="b9013-109">Wert</span><span class="sxs-lookup"><span data-stu-id="b9013-109">Value</span></span>                                                   | <span data-ttu-id="b9013-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9013-110">Description</span></span>                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9013-111">**der MF \_ - \_ audiorendererattributflags \_ \_ \_ CrossProcess**</span><span class="sxs-lookup"><span data-stu-id="b9013-111">**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_CROSSPROCESS**</span></span> | <span data-ttu-id="b9013-112">Der audiorenderer verwendet eine prozessübergreifende Audiositzung.</span><span class="sxs-lookup"><span data-stu-id="b9013-112">The audio renderer is uses a cross-process audio session.</span></span> <span data-ttu-id="b9013-113">Mit diesem Flag können audiorenderer in mehreren Prozessen dieselbe Audiositzung gemeinsam mit den zugehörigen Volumes und Richtlinien Steuerelementen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9013-113">This flag enables audio renderers in multiple processes to share the same audio session, along with the associated volume and policy controls.</span></span><br/> <span data-ttu-id="b9013-114">Wenn dieses Flag nicht festgelegt ist, kann die Audiositzung nicht von audiorenderatoren in anderen Prozessen gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="b9013-114">If this flag is not set, the audio session cannot be shared by audio renderers in other processes.</span></span><br/> |
| <span data-ttu-id="b9013-115">**MF \_ - \_ \_ audiorendererattributflags \_ \_ nopersist**</span><span class="sxs-lookup"><span data-stu-id="b9013-115">**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_NOPERSIST**</span></span>    | <span data-ttu-id="b9013-116">Die Windows-audiositzungs-API (WASAPI) speichert die Eigenschaften dieser Audiositzung (z. b. das Sitzungs Volume) nicht.</span><span class="sxs-lookup"><span data-stu-id="b9013-116">The Windows audio session API (WASAPI) will not persist the properties for this audio session, such as the session volume.</span></span><br/> <span data-ttu-id="b9013-117">Wenn dieses Flag nicht festgelegt ist, werden die Eigenschaften der Audiositzung von WASAPI persistent gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b9013-117">If this flag is not set, WASAPI will persist the audio session properties.</span></span><br/>                                                                                                       |



 

<span data-ttu-id="b9013-118">Sie können dieses Attribut verwenden, um den audiorenderer zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b9013-118">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="b9013-119">Die Verwendung hängt von der Funktion ab, die Sie zum Erstellen des audiorenderers aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="b9013-119">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="b9013-120">[**MF | ateaudiorenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Legen Sie dieses Attribut mit dem im *paudioattribute* -Parameter angegebenen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstellen Zeiger fest.</span><span class="sxs-lookup"><span data-stu-id="b9013-120">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="b9013-121">[**Mfkreateaudiorendereraktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Legen Sie dieses Attribut mit dem [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstellen Zeiger fest, der im *ppaktivierungs* -Parameter abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b9013-121">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="b9013-122">Legen Sie das-Attribut vor dem Aufrufen von [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)fest.</span><span class="sxs-lookup"><span data-stu-id="b9013-122">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="b9013-123">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="b9013-123">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9013-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9013-124">Requirements</span></span>



| <span data-ttu-id="b9013-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9013-125">Requirement</span></span> | <span data-ttu-id="b9013-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b9013-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b9013-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9013-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b9013-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9013-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b9013-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9013-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b9013-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9013-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b9013-131">Header</span><span class="sxs-lookup"><span data-stu-id="b9013-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9013-132"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9013-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9013-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9013-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9013-134">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="b9013-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b9013-135">Audiorendererattribute</span><span class="sxs-lookup"><span data-stu-id="b9013-135">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="b9013-136">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b9013-136">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b9013-137">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b9013-137">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b9013-138">Streamingaudiorenderer</span><span class="sxs-lookup"><span data-stu-id="b9013-138">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 




