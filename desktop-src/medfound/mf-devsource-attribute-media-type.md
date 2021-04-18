---
description: Gibt das Ausgabeformat eines Geräts an.
ms.assetid: 33a1b546-ece2-44ef-a1c0-5579c32be0bc
title: MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a05283f33fa3b3bf4b9e339b830c2ae6a948ea82
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354909"
---
# <a name="mf_devsource_attribute_media_type-attribute"></a><span data-ttu-id="29b19-103">Attribut für \_ \_ \_ \_ Medientyp des MF-devsource-Attributs</span><span class="sxs-lookup"><span data-stu-id="29b19-103">MF\_DEVSOURCE\_ATTRIBUTE\_MEDIA\_TYPE attribute</span></span>

<span data-ttu-id="29b19-104">Gibt das Ausgabeformat eines Geräts an.</span><span class="sxs-lookup"><span data-stu-id="29b19-104">Specifies the output format of a device.</span></span>

## <a name="data-type"></a><span data-ttu-id="29b19-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="29b19-105">Data type</span></span>

<span data-ttu-id="29b19-106">**[**MFT \_ Registrieren \_ \_**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** von als **\[ Byte \]** gespeicherten Typinformationen</span><span class="sxs-lookup"><span data-stu-id="29b19-106">**[**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="29b19-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="29b19-107">Get/set</span></span>

<span data-ttu-id="29b19-108">Zum Abrufen dieses Attributs müssen Sie [**imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="29b19-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="29b19-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="29b19-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="29b19-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29b19-110">Remarks</span></span>

<span data-ttu-id="29b19-111">Dieses Attribut enthält ein paar von GUIDs: einen Haupttyp und einen Untertyp.</span><span class="sxs-lookup"><span data-stu-id="29b19-111">This attribute contains a pair of GUIDs: a major type and a subtype.</span></span> <span data-ttu-id="29b19-112">Diese GUIDs beschreiben das Standardausgabeformat des Geräts.</span><span class="sxs-lookup"><span data-stu-id="29b19-112">These GUIDs describe the default output format of the device.</span></span> <span data-ttu-id="29b19-113">Das Gerät unterstützt möglicherweise zusätzliche Ausgabeformate.</span><span class="sxs-lookup"><span data-stu-id="29b19-113">The device might support additional output formats.</span></span>

<span data-ttu-id="29b19-114">Wenn z. b. ein Video Erfassungsgerät das RGB-32-Video ausgibt, ist der Wert dieses Attributs `{ MFMediaType_Video, MFVideoFormat_RGB32 }` .</span><span class="sxs-lookup"><span data-stu-id="29b19-114">For example, if a video capture device outputs RGB-32 video, the value of this attribute is `{ MFMediaType_Video, MFVideoFormat_RGB32 }`.</span></span>

<span data-ttu-id="29b19-115">Dieses Attribut ist ein Hinweis für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="29b19-115">This attribute is a hint to the application.</span></span> <span data-ttu-id="29b19-116">Um das genaue Ausgabeformat zu erhalten, erstellen Sie die Medienquelle für das Gerät, und rufen Sie den Präsentations Deskriptor der Medienquelle ab.</span><span class="sxs-lookup"><span data-stu-id="29b19-116">To get the exact output format, create the media source for the device and get the media source's presentation descriptor.</span></span>

<span data-ttu-id="29b19-117">Dieses Attribut wird für die Aktivierungs Objekte festgelegt, die von den folgenden Funktionen zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="29b19-117">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="29b19-118">**MF | atedevicesourceaktivierungs**</span><span class="sxs-lookup"><span data-stu-id="29b19-118">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="29b19-119">**Mfenumschlag**</span><span class="sxs-lookup"><span data-stu-id="29b19-119">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="29b19-120">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="29b19-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="29b19-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29b19-121">Requirements</span></span>



| <span data-ttu-id="29b19-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29b19-122">Requirement</span></span> | <span data-ttu-id="29b19-123">Wert</span><span class="sxs-lookup"><span data-stu-id="29b19-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="29b19-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29b19-124">Minimum supported client</span></span><br/> | <span data-ttu-id="29b19-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29b19-125">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="29b19-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29b19-126">Minimum supported server</span></span><br/> | <span data-ttu-id="29b19-127">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29b19-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="29b19-128">Header</span><span class="sxs-lookup"><span data-stu-id="29b19-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="29b19-129"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="29b19-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29b19-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29b19-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29b19-131">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="29b19-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="29b19-132">Audio-/Videoaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="29b19-132">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="29b19-133">Geräte Attribute erfassen</span><span class="sxs-lookup"><span data-stu-id="29b19-133">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




