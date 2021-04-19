---
description: Gibt den Datei Bezeichner einer ASF-Datei (Advanced Systems Format) an.
ms.assetid: 096c2e1a-7fd7-49ab-aa24-7d7c779d9e79
title: MF_PD_ASF_FILEPROPERTIES_FILE_ID-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a92d20351c11df4feebd732c670cbacabf3bd67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356600"
---
# <a name="mf_pd_asf_fileproperties_file_id-attribute"></a><span data-ttu-id="cb3f9-103">Datei-ID-Attribut für MF \_ PD- \_ \_ \_ Dateieigenschaften \_</span><span class="sxs-lookup"><span data-stu-id="cb3f9-103">MF\_PD\_ASF\_FILEPROPERTIES\_FILE\_ID attribute</span></span>

<span data-ttu-id="cb3f9-104">Gibt den Datei Bezeichner einer ASF-Datei (Advanced Systems Format) an.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-104">Specifies the file identifier of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="cb3f9-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="cb3f9-105">Data type</span></span>

<span data-ttu-id="cb3f9-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="cb3f9-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="cb3f9-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb3f9-107">Remarks</span></span>

<span data-ttu-id="cb3f9-108">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="cb3f9-109">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb3f9-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb3f9-110">Requirements</span></span>



| <span data-ttu-id="cb3f9-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb3f9-111">Requirement</span></span> | <span data-ttu-id="cb3f9-112">Wert</span><span class="sxs-lookup"><span data-stu-id="cb3f9-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb3f9-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb3f9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="cb3f9-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb3f9-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cb3f9-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb3f9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="cb3f9-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb3f9-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cb3f9-117">Header</span><span class="sxs-lookup"><span data-stu-id="cb3f9-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb3f9-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb3f9-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb3f9-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb3f9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb3f9-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="cb3f9-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cb3f9-121">**Imfattributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="cb3f9-121">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="cb3f9-122">**Imfattributes:: SetGuid**</span><span class="sxs-lookup"><span data-stu-id="cb3f9-122">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="cb3f9-123">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="cb3f9-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="cb3f9-124">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="cb3f9-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="cb3f9-125">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="cb3f9-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="cb3f9-126">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="cb3f9-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




