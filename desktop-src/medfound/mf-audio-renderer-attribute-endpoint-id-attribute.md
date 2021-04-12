---
description: Gibt den Bezeichner für das audioendpunkt-Gerät an.
ms.assetid: f145fb80-c136-421c-9a65-e69c52109348
title: MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e042f59baf4812c177358acca6badb2422914afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344598"
---
# <a name="mf_audio_renderer_attribute_endpoint_id-attribute"></a><span data-ttu-id="ef2e9-103">\_ \_ \_ \_ Attribut Endpunkt- \_ ID für MF-audiorenderer</span><span class="sxs-lookup"><span data-stu-id="ef2e9-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID attribute</span></span>

<span data-ttu-id="ef2e9-104">Gibt den Bezeichner für das audioendpunkt-Gerät an.</span><span class="sxs-lookup"><span data-stu-id="ef2e9-104">Specifies the identifier for the audio endpoint device.</span></span>

## <a name="data-type"></a><span data-ttu-id="ef2e9-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ef2e9-105">Data type</span></span>

<span data-ttu-id="ef2e9-106">Breitzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ef2e9-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="ef2e9-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef2e9-107">Remarks</span></span>

<span data-ttu-id="ef2e9-108">Sie können dieses Attribut verwenden, um den audiorenderer zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ef2e9-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="ef2e9-109">Die Verwendung hängt von der Funktion ab, die Sie zum Erstellen des audiorenderers aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="ef2e9-109">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="ef2e9-110">[**MF | ateaudiorenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Legen Sie dieses Attribut mit dem im *paudioattribute* -Parameter angegebenen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstellen Zeiger fest.</span><span class="sxs-lookup"><span data-stu-id="ef2e9-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="ef2e9-111">[**Mfkreateaudiorendereraktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Legen Sie dieses Attribut mit dem [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstellen Zeiger fest, der im *ppaktivierungs* -Parameter abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ef2e9-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="ef2e9-112">Legen Sie das-Attribut vor dem Aufrufen von [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)fest.</span><span class="sxs-lookup"><span data-stu-id="ef2e9-112">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="ef2e9-113">Bei einem audioendpunktgerät handelt es sich um ein Hardware Gerät, das sich an einem Ende eines audiodatenpfads befindet, z. b. ein Telefon oder ein Redner.</span><span class="sxs-lookup"><span data-stu-id="ef2e9-113">An audio endpoint device is a hardware device that lies at one end of an audio data path, such as a headphone or a speaker.</span></span> <span data-ttu-id="ef2e9-114">Verwenden Sie zum Abrufen des audioendpunktbezeichners die folgenden kernaudioapis:</span><span class="sxs-lookup"><span data-stu-id="ef2e9-114">To obtain the audio endpoint identifier, use the following core audio APIs:</span></span>

-   <span data-ttu-id="ef2e9-115">Verwenden Sie die [**immdeviceenumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle, um die Geräte auf dem System aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="ef2e9-115">Use the [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface to enumerate the devices on the system.</span></span>
-   <span data-ttu-id="ef2e9-116">Bitten Sie [**immdevice:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) , um den Bezeichner für das Gerät abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ef2e9-116">Call [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to get the identifier for the device.</span></span>

<span data-ttu-id="ef2e9-117">Weitere Informationen finden Sie in der Dokumentation zur [kernton-](../coreaudio/core-audio-apis-in-windows-vista.md) API.</span><span class="sxs-lookup"><span data-stu-id="ef2e9-117">For more information, see the [Core Audio](../coreaudio/core-audio-apis-in-windows-vista.md) API documentation.</span></span> <span data-ttu-id="ef2e9-118">Wenn dieses Attribut nicht festgelegt ist, verwendet der audiorenderer das standardend Punkt Gerät.</span><span class="sxs-lookup"><span data-stu-id="ef2e9-118">If this attribute is not set, the audio renderer uses the default endpoint device.</span></span>

<span data-ttu-id="ef2e9-119">Wenn dieses Attribut festgelegt ist, legen Sie das Attribut für die [**\_ \_ \_ \_ Endpunkt \_ Rolle für das MF-audiorenderer-Attribut**](mf-audio-renderer-attribute-endpoint-role-attribute.md) nicht fest.</span><span class="sxs-lookup"><span data-stu-id="ef2e9-119">If this attribute is set, do not set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE**](mf-audio-renderer-attribute-endpoint-role-attribute.md) attribute.</span></span> <span data-ttu-id="ef2e9-120">Wenn beide Attribute festgelegt sind, tritt ein Fehler auf, wenn der audiorenderer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ef2e9-120">If both attributes are set, a failure will occur when the audio renderer is created.</span></span>

<span data-ttu-id="ef2e9-121">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="ef2e9-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef2e9-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef2e9-122">Requirements</span></span>



| <span data-ttu-id="ef2e9-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef2e9-123">Requirement</span></span> | <span data-ttu-id="ef2e9-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ef2e9-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ef2e9-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef2e9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ef2e9-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef2e9-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ef2e9-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef2e9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ef2e9-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef2e9-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ef2e9-129">Header</span><span class="sxs-lookup"><span data-stu-id="ef2e9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef2e9-130"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef2e9-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef2e9-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef2e9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef2e9-132">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="ef2e9-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ef2e9-133">Audiorendererattribute</span><span class="sxs-lookup"><span data-stu-id="ef2e9-133">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="ef2e9-134">**Imfattributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="ef2e9-134">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="ef2e9-135">**Imfattributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="ef2e9-135">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="ef2e9-136">Streamingaudiorenderer</span><span class="sxs-lookup"><span data-stu-id="ef2e9-136">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
