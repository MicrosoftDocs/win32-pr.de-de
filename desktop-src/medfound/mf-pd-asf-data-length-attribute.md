---
description: Gibt die Größe des Daten Abschnitts in einer ASF-Datei (Advanced Systems Format) in Bytes an.
ms.assetid: 93a0bf27-23db-4e8a-b471-a42122e8f9aa
title: MF_PD_ASF_DATA_LENGTH-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e62bccc594a12010cc477c241deac565d7ea62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343341"
---
# <a name="mf_pd_asf_data_length-attribute"></a><span data-ttu-id="1b455-103">MF \_ PD, \_ ASF- \_ Daten \_ Längen Attribut</span><span class="sxs-lookup"><span data-stu-id="1b455-103">MF\_PD\_ASF\_DATA\_LENGTH attribute</span></span>

<span data-ttu-id="1b455-104">Gibt die Größe des Daten Abschnitts in einer ASF-Datei (Advanced Systems Format) in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="1b455-104">Specifies the size, in bytes, of the data section of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="1b455-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1b455-105">Data type</span></span>

<span data-ttu-id="1b455-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="1b455-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="1b455-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b455-107">Remarks</span></span>

<span data-ttu-id="1b455-108">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="1b455-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="1b455-109">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="1b455-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b455-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b455-110">Requirements</span></span>



| <span data-ttu-id="1b455-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b455-111">Requirement</span></span> | <span data-ttu-id="1b455-112">Wert</span><span class="sxs-lookup"><span data-stu-id="1b455-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b455-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b455-113">Minimum supported client</span></span><br/> | <span data-ttu-id="1b455-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b455-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1b455-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b455-115">Minimum supported server</span></span><br/> | <span data-ttu-id="1b455-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b455-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1b455-117">Header</span><span class="sxs-lookup"><span data-stu-id="1b455-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b455-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b455-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b455-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b455-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b455-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="1b455-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1b455-121">**Imfattributes:: GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="1b455-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="1b455-122">**Imfattributes:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="1b455-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="1b455-123">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="1b455-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="1b455-124">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="1b455-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="1b455-125">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="1b455-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




