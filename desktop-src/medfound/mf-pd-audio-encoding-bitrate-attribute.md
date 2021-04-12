---
description: Gibt die audiocodierungs-Bitrate für die Präsentation in Bits pro Sekunde an. Dieses Attribut gilt für Präsentations Deskriptoren.
ms.assetid: 700f61f4-a0d7-4b69-ace5-356e4e29b93d
title: MF_PD_AUDIO_ENCODING_BITRATE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49566ecb225482ef6513e056de8ba11763de603e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216881"
---
# <a name="mf_pd_audio_encoding_bitrate-attribute"></a><span data-ttu-id="5f138-104">MF \_ PD \_ - \_ Attribut für die Audiocodierung- \_ Bitrate</span><span class="sxs-lookup"><span data-stu-id="5f138-104">MF\_PD\_AUDIO\_ENCODING\_BITRATE attribute</span></span>

<span data-ttu-id="5f138-105">Gibt die audiocodierungs-Bitrate für die Präsentation in Bits pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="5f138-105">Specifies the audio encoding bit rate for the presentation, in bits per second.</span></span> <span data-ttu-id="5f138-106">Dieses Attribut gilt für Präsentations Deskriptoren.</span><span class="sxs-lookup"><span data-stu-id="5f138-106">This attribute applies to presentation descriptors.</span></span>

## <a name="data-type"></a><span data-ttu-id="5f138-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5f138-107">Data type</span></span>

<span data-ttu-id="5f138-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5f138-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5f138-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f138-109">Remarks</span></span>

<span data-ttu-id="5f138-110">Das-Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="5f138-110">The attribute is optional.</span></span> <span data-ttu-id="5f138-111">Einige Formate verfügen über komplexere Codierungs Schemas, die nicht mithilfe dieses Attributs zusammengefasst werden können.</span><span class="sxs-lookup"><span data-stu-id="5f138-111">Some formats have more complex encoding schemes that cannot be summarized by using this attribute.</span></span> <span data-ttu-id="5f138-112">Bei ASF-Dateien (Advanced Systems Format) beschreiben die folgenden Attribute kollektiv die Codierungs Bitrate:</span><span class="sxs-lookup"><span data-stu-id="5f138-112">For Advanced Systems Format (ASF) files, the following attributes collectively describe the encoding bit rate:</span></span>

-   [<span data-ttu-id="5f138-113">**MF \_ PD \_ ASF \_ File Properties \_ Max. \_ Bitrate**</span><span class="sxs-lookup"><span data-stu-id="5f138-113">**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_BITRATE**</span></span>](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [<span data-ttu-id="5f138-114">**MF SD-Datei (in Bytes) \_ \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f138-114">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [<span data-ttu-id="5f138-115">**MF \_ SD \_ , \_ \_ maximal zulässige \_ Daten \_ Bitrate**</span><span class="sxs-lookup"><span data-stu-id="5f138-115">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [<span data-ttu-id="5f138-116">**MF \_ SD, \_ ASF \_ streambitraten \_ Bitrate**</span><span class="sxs-lookup"><span data-stu-id="5f138-116">**MF\_SD\_ASF\_STREAMBITRATES\_BITRATE**</span></span>](mf-sd-asf-streambitrates-bitrate-attribute.md)

<span data-ttu-id="5f138-117">Formate von Drittanbietern können andere benutzerdefinierte Attribute verwenden.</span><span class="sxs-lookup"><span data-stu-id="5f138-117">Third-party formats might use other custom attributes.</span></span>

<span data-ttu-id="5f138-118">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="5f138-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f138-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f138-119">Requirements</span></span>



| <span data-ttu-id="5f138-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f138-120">Requirement</span></span> | <span data-ttu-id="5f138-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5f138-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5f138-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f138-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5f138-123">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="5f138-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="5f138-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f138-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5f138-125">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="5f138-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5f138-126">Header</span><span class="sxs-lookup"><span data-stu-id="5f138-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f138-127"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f138-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f138-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f138-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f138-129">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="5f138-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5f138-130">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5f138-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5f138-131">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5f138-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5f138-132">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="5f138-132">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="5f138-133">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="5f138-133">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




