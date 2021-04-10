---
description: Gibt den Offset (in Bytes) vom Anfang der Datei "Advanced Systems Format (ASF)" bis zum Anfang des ersten Datenpakets an.
ms.assetid: 5145d952-19d9-4bf8-9046-0b5d28f5e641
title: MF_PD_ASF_DATA_START_OFFSET-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 125ae1263467afe7e0aa9017e8049b13796538fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867540"
---
# <a name="mf_pd_asf_data_start_offset-attribute"></a><span data-ttu-id="515c8-103">MF \_ PD-Attribut für das \_ \_ \_ Start Offset-Daten \_ Satz</span><span class="sxs-lookup"><span data-stu-id="515c8-103">MF\_PD\_ASF\_DATA\_START\_OFFSET attribute</span></span>

<span data-ttu-id="515c8-104">Gibt den Offset (in Bytes) vom Anfang der Datei "Advanced Systems Format (ASF)" bis zum Anfang des ersten Datenpakets an.</span><span class="sxs-lookup"><span data-stu-id="515c8-104">Specifies the offset, in bytes, from the start of an Advanced Systems Format (ASF) file to the start of the first data packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="515c8-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="515c8-105">Data type</span></span>

<span data-ttu-id="515c8-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="515c8-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="515c8-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="515c8-107">Remarks</span></span>

<span data-ttu-id="515c8-108">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="515c8-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="515c8-109">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="515c8-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="515c8-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="515c8-110">Requirements</span></span>



| <span data-ttu-id="515c8-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="515c8-111">Requirement</span></span> | <span data-ttu-id="515c8-112">Wert</span><span class="sxs-lookup"><span data-stu-id="515c8-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="515c8-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="515c8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="515c8-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="515c8-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="515c8-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="515c8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="515c8-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="515c8-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="515c8-117">Header</span><span class="sxs-lookup"><span data-stu-id="515c8-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="515c8-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="515c8-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="515c8-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="515c8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="515c8-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="515c8-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="515c8-121">**Imfattributes:: GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="515c8-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="515c8-122">**Imfattributes:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="515c8-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="515c8-123">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="515c8-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="515c8-124">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="515c8-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="515c8-125">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="515c8-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




