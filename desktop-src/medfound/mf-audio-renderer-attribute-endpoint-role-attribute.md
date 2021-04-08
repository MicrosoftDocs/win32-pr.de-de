---
description: Gibt die audioendpunktrolle für den audiorenderer an.
ms.assetid: f0456337-5351-457e-9830-920bf346bfc4
title: MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ROLE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1b6599ffc97cfa9c7fc2b6a75f4ed4ae7c2c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960094"
---
# <a name="mf_audio_renderer_attribute_endpoint_role-attribute"></a><span data-ttu-id="91058-103">Attribut für die \_ \_ \_ \_ Endpunkt Rolle " \_ MF-audiorenderer"</span><span class="sxs-lookup"><span data-stu-id="91058-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE attribute</span></span>

<span data-ttu-id="91058-104">Gibt die audioendpunktrolle für den audiorenderer an.</span><span class="sxs-lookup"><span data-stu-id="91058-104">Specifies the audio endpoint role for the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="91058-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="91058-105">Data type</span></span>

<span data-ttu-id="91058-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="91058-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="91058-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91058-107">Remarks</span></span>

<span data-ttu-id="91058-108">Sie können dieses Attribut verwenden, um den audiorenderer zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="91058-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="91058-109">Die Verwendung hängt von der Funktion ab, die Sie zum Erstellen des audiorenderers aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="91058-109">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="91058-110">[**MF | ateaudiorenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Legen Sie dieses Attribut mit dem im *paudioattribute* -Parameter angegebenen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstellen Zeiger fest.</span><span class="sxs-lookup"><span data-stu-id="91058-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="91058-111">[**Mfkreateaudiorendereraktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Legen Sie dieses Attribut mit dem [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstellen Zeiger fest, der im *ppaktivierungs* -Parameter abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="91058-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="91058-112">Legen Sie das-Attribut vor dem Aufrufen von [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)fest.</span><span class="sxs-lookup"><span data-stu-id="91058-112">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="91058-113">Bei einem audioendpunktgerät handelt es sich um ein Hardware Gerät, das sich an einem Ende eines audiodatenpfads befindet, z. b. ein Telefon oder ein Redner.</span><span class="sxs-lookup"><span data-stu-id="91058-113">An audio endpoint device is a hardware device that lies at one end of an audio data path, such as a headphone or a speaker.</span></span>

<span data-ttu-id="91058-114">Wenn dieses Attribut festgelegt ist, verwendet der audiorenderer das Standardaudiogerät für die angegebene Rolle.</span><span class="sxs-lookup"><span data-stu-id="91058-114">If this attribute is set, the audio renderer uses the default audio device for the specified role.</span></span> <span data-ttu-id="91058-115">Der Wert dieses Attributs ist ein Member der **erole** -Enumeration, der in der Header Datei mmdeviceapi. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="91058-115">The value of this attribute is a member of the **ERole** enumeration, which is defined in the header file mmdeviceapi.h.</span></span> <span data-ttu-id="91058-116">Weitere Informationen finden Sie in der Dokumentation zur kernton-API.</span><span class="sxs-lookup"><span data-stu-id="91058-116">For more information, see the Core Audio API documentation.</span></span> <span data-ttu-id="91058-117">Wenn dieses Attribut nicht festgelegt ist, verwendet der audiorenderer das standardend Punkt Gerät.</span><span class="sxs-lookup"><span data-stu-id="91058-117">If this attribute is not set, the audio renderer uses the default endpoint device.</span></span>

<span data-ttu-id="91058-118">Wenn dieses Attribut festgelegt ist, legen Sie das [**Attribut \_ Endpunkt-ID für das MF- \_ audiorenderer \_ Attribut \_ \_**](mf-audio-renderer-attribute-endpoint-id-attribute.md) nicht fest.</span><span class="sxs-lookup"><span data-stu-id="91058-118">If this attribute is set, do not set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID**](mf-audio-renderer-attribute-endpoint-id-attribute.md) attribute.</span></span> <span data-ttu-id="91058-119">Wenn beide Attribute festgelegt sind, tritt ein Fehler auf, wenn der audiorenderer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="91058-119">If both attributes are set, a failure will occur when the audio renderer is created.</span></span>

<span data-ttu-id="91058-120">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="91058-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="91058-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91058-121">Requirements</span></span>



| <span data-ttu-id="91058-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91058-122">Requirement</span></span> | <span data-ttu-id="91058-123">Wert</span><span class="sxs-lookup"><span data-stu-id="91058-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="91058-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91058-124">Minimum supported client</span></span><br/> | <span data-ttu-id="91058-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91058-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="91058-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91058-126">Minimum supported server</span></span><br/> | <span data-ttu-id="91058-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91058-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="91058-128">Header</span><span class="sxs-lookup"><span data-stu-id="91058-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="91058-129"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="91058-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91058-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91058-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91058-131">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="91058-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="91058-132">Audiorendererattribute</span><span class="sxs-lookup"><span data-stu-id="91058-132">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="91058-133">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="91058-133">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="91058-134">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="91058-134">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="91058-135">Streamingaudiorenderer</span><span class="sxs-lookup"><span data-stu-id="91058-135">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 




