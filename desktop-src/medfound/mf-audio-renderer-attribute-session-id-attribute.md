---
description: Gibt die audiorichtlinienklasse für den audiorenderer an.
ms.assetid: 80b028f5-7756-4bb8-b5e3-ebc8343e168c
title: MF_AUDIO_RENDERER_ATTRIBUTE_SESSION_ID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4952a60d4438e610677b494290e9738e469770d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866807"
---
# <a name="mf_audio_renderer_attribute_session_id-attribute"></a><span data-ttu-id="9468e-103">\_Sitzungs-ID-Attribut für MF- \_ audiorenderer \_ Attribut \_ \_</span><span class="sxs-lookup"><span data-stu-id="9468e-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_SESSION\_ID attribute</span></span>

<span data-ttu-id="9468e-104">Gibt die audiorichtlinienklasse für den audiorenderer an.</span><span class="sxs-lookup"><span data-stu-id="9468e-104">Specifies the audio policy class for the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="9468e-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9468e-105">Data type</span></span>

<span data-ttu-id="9468e-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="9468e-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="9468e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9468e-107">Remarks</span></span>

<span data-ttu-id="9468e-108">Dieses Attribut ordnet den audiorenderer einer audiorichtlinienklasse zu.</span><span class="sxs-lookup"><span data-stu-id="9468e-108">This attribute associates the audio renderer with an audio policy class.</span></span> <span data-ttu-id="9468e-109">Jede Richtlinien Klasse verfügt über ein eigenes Volume und eine eigene Richtlinien Steuerung.</span><span class="sxs-lookup"><span data-stu-id="9468e-109">Each policy class has its own volume and policy control.</span></span> <span data-ttu-id="9468e-110">Wenn dieses Attribut nicht festgelegt ist, wird das neue SAR der standardmäßigen Audiositzung der Anwendung beitreten.</span><span class="sxs-lookup"><span data-stu-id="9468e-110">If this attribute is not set, the new SAR joins the application's default audio session.</span></span> <span data-ttu-id="9468e-111">Weitere Informationen finden Sie unter [**iaudioclient:: Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) in der Dokumentation zur kernaudio-API.</span><span class="sxs-lookup"><span data-stu-id="9468e-111">For more information, see [**IAudioClient::Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) in the core audio API documentation.</span></span>

<span data-ttu-id="9468e-112">Sie können dieses Attribut verwenden, um den audiorenderer zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="9468e-112">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="9468e-113">Die Verwendung hängt von der Funktion ab, die Sie zum Erstellen des audiorenderers aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="9468e-113">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="9468e-114">[**MF | ateaudiorenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Legen Sie dieses Attribut mit dem im *paudioattribute* -Parameter angegebenen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstellen Zeiger fest.</span><span class="sxs-lookup"><span data-stu-id="9468e-114">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="9468e-115">[**Mfkreateaudiorendereraktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Legen Sie dieses Attribut mit dem [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstellen Zeiger fest, der im *ppaktivierungs* -Parameter abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="9468e-115">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="9468e-116">Legen Sie das-Attribut vor dem Aufrufen von [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)fest.</span><span class="sxs-lookup"><span data-stu-id="9468e-116">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="9468e-117">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="9468e-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9468e-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9468e-118">Requirements</span></span>



| <span data-ttu-id="9468e-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9468e-119">Requirement</span></span> | <span data-ttu-id="9468e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9468e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9468e-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9468e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9468e-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9468e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9468e-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9468e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9468e-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9468e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9468e-125">Header</span><span class="sxs-lookup"><span data-stu-id="9468e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9468e-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9468e-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9468e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9468e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9468e-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="9468e-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9468e-129">Audiorendererattribute</span><span class="sxs-lookup"><span data-stu-id="9468e-129">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="9468e-130">**Imfattributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="9468e-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="9468e-131">**Imfattributes:: SetGuid**</span><span class="sxs-lookup"><span data-stu-id="9468e-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="9468e-132">Streamingaudiorenderer</span><span class="sxs-lookup"><span data-stu-id="9468e-132">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
