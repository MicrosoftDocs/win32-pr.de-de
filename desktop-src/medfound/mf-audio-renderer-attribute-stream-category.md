---
description: Gibt die audiostreamkategorie für den streamingaudiorenderer (SAR) an.
ms.assetid: 88E79DE6-2062-4471-A939-D1D4DD2EC42D
title: MF_AUDIO_RENDERER_ATTRIBUTE_STREAM_CATEGORY-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd96c219e43f85c516a5f862e2a978724328a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359973"
---
# <a name="mf_audio_renderer_attribute_stream_category-attribute"></a><span data-ttu-id="f6ebd-103">\_Kategorie-Attribut für das MF- \_ audiorenderattribut \_ \_ Stream \_</span><span class="sxs-lookup"><span data-stu-id="f6ebd-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_STREAM\_CATEGORY attribute</span></span>

<span data-ttu-id="f6ebd-104">Gibt die audiostreamkategorie für den [streamingaudiorenderer](streaming-audio-renderer.md) (SAR) an.</span><span class="sxs-lookup"><span data-stu-id="f6ebd-104">Specifies the audio stream category for the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR).</span></span>

## <a name="data-type"></a><span data-ttu-id="f6ebd-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f6ebd-105">Data type</span></span>

<span data-ttu-id="f6ebd-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f6ebd-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f6ebd-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6ebd-107">Remarks</span></span>

<span data-ttu-id="f6ebd-108">Sie können dieses Attribut verwenden, um den audiorenderer zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f6ebd-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="f6ebd-109">Die Verwendung hängt von der Funktion ab, die Sie zum Erstellen des audiorenderers aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="f6ebd-109">The usage depends on which function you call to create the audio renderer.</span></span>



| <span data-ttu-id="f6ebd-110">Funktion</span><span class="sxs-lookup"><span data-stu-id="f6ebd-110">Function</span></span>                                                               | <span data-ttu-id="f6ebd-111">Festlegen des Attributs</span><span class="sxs-lookup"><span data-stu-id="f6ebd-111">How to Set the attribute</span></span>                                                                                                                                                                       |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6ebd-112">**Mskreateaudiorenderer**</span><span class="sxs-lookup"><span data-stu-id="f6ebd-112">**MFCreateAudioRenderer**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)                 | <span data-ttu-id="f6ebd-113">Verwenden Sie den [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger, der im *paudioattribute* -Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f6ebd-113">Use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer specified in the *pAudioAttributes* parameter.</span></span>                                                                                          |
| [<span data-ttu-id="f6ebd-114">**MF | ateaudiorendereraktivierungs**</span><span class="sxs-lookup"><span data-stu-id="f6ebd-114">**MFCreateAudioRendererActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) | <span data-ttu-id="f6ebd-115">Verwenden Sie den [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger, der im *ppaktivierungs* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f6ebd-115">Use the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer returned in the *ppActivate* parameter.</span></span> <span data-ttu-id="f6ebd-116">Legen Sie das-Attribut vor dem Aufrufen von [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)fest.</span><span class="sxs-lookup"><span data-stu-id="f6ebd-116">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> |



 

<span data-ttu-id="f6ebd-117">Der Wert des-Attributs ist ein Member der [**\_ \_ Kategorie-**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) Enumeration des Audiostreams.</span><span class="sxs-lookup"><span data-stu-id="f6ebd-117">The value of the attribute is a member of the [**AUDIO\_STREAM\_CATEGORY**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) enumeration.</span></span> <span data-ttu-id="f6ebd-118">Der Audiodienst verwendet die Kategorie Stream, um Audiorichtlinien zu ermitteln, wenn mehrere Anwendungen gleichzeitig Audiodaten abspielen.</span><span class="sxs-lookup"><span data-stu-id="f6ebd-118">The audio service uses the stream category to determine audio policies when multiple applications play audio at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6ebd-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6ebd-119">Requirements</span></span>



| <span data-ttu-id="f6ebd-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6ebd-120">Requirement</span></span> | <span data-ttu-id="f6ebd-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f6ebd-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f6ebd-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6ebd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f6ebd-123">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6ebd-123">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f6ebd-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6ebd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f6ebd-125">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6ebd-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f6ebd-126">Header</span><span class="sxs-lookup"><span data-stu-id="f6ebd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6ebd-127"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6ebd-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6ebd-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6ebd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6ebd-129">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="f6ebd-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
