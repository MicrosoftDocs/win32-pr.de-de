---
description: Gibt die Konformitäts Vorlage für Geräte für einen Datenstrom in einer ASF-Datei (Advanced Systems Format) an.
ms.assetid: e0bfb393-c8de-47cf-b80a-b0d88722e815
title: MF_SD_ASF_METADATA_DEVICE_CONFORMANCE_TEMPLATE-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e0ae20ae02617fab6f9669a50c7b8383b90a9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347404"
---
# <a name="mf_sd_asf_metadata_device_conformance_template-attribute"></a><span data-ttu-id="25b20-103">Vorlagen Attribut für das SD-Datei- \_ \_ ASF- \_ \_ metadatengerät \_ \_</span><span class="sxs-lookup"><span data-stu-id="25b20-103">MF\_SD\_ASF\_METADATA\_DEVICE\_CONFORMANCE\_TEMPLATE attribute</span></span>

<span data-ttu-id="25b20-104">Gibt die Konformitäts Vorlage für Geräte für einen Datenstrom in einer ASF-Datei (Advanced Systems Format) an.</span><span class="sxs-lookup"><span data-stu-id="25b20-104">Specifies the device conformance template for a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="25b20-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="25b20-105">Data type</span></span>

<span data-ttu-id="25b20-106">Breitzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="25b20-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="25b20-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25b20-107">Remarks</span></span>

<span data-ttu-id="25b20-108">Dieses Attribut gilt für streamdeskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="25b20-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="25b20-109">Weitere Informationen zu den Vorlagen für die Geräte Konformität finden Sie im Thema "Geräte Übereinstimmungs-Vorlagen Parameter" im SDK für den Windows Media-Format.</span><span class="sxs-lookup"><span data-stu-id="25b20-109">For more information about device conformance templates, see the topic "Device Conformance Template Parameters" in the Windows Media Format SDK.</span></span>

<span data-ttu-id="25b20-110">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="25b20-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="25b20-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25b20-111">Requirements</span></span>



| <span data-ttu-id="25b20-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25b20-112">Requirement</span></span> | <span data-ttu-id="25b20-113">Wert</span><span class="sxs-lookup"><span data-stu-id="25b20-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="25b20-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25b20-114">Minimum supported client</span></span><br/> | <span data-ttu-id="25b20-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25b20-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="25b20-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25b20-116">Minimum supported server</span></span><br/> | <span data-ttu-id="25b20-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25b20-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="25b20-118">Header</span><span class="sxs-lookup"><span data-stu-id="25b20-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="25b20-119"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="25b20-119"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25b20-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25b20-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25b20-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="25b20-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="25b20-122">**Imfattributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="25b20-122">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="25b20-123">**Imfattributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="25b20-123">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="25b20-124">**IMF-Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="25b20-124">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="25b20-125">Streamdeskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="25b20-125">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="25b20-126">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="25b20-126">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




