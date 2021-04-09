---
description: Gibt das Datum und die Uhrzeit an, zu denen eine ASF-Datei (Advanced Systems Format) erstellt wurde.
ms.assetid: 97f80584-9d74-4ba5-80f4-ddb6f2bc4625
title: MF_PD_ASF_FILEPROPERTIES_CREATION_TIME-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0f48f251f5ff9c7332de0e355c58782ed98fad0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958902"
---
# <a name="mf_pd_asf_fileproperties_creation_time-attribute"></a><span data-ttu-id="3af48-103">Buildzeit-Attribut für MF \_ PD \_ ASF \_ File Properties \_ \_</span><span class="sxs-lookup"><span data-stu-id="3af48-103">MF\_PD\_ASF\_FILEPROPERTIES\_CREATION\_TIME attribute</span></span>

<span data-ttu-id="3af48-104">Gibt das Datum und die Uhrzeit an, zu denen eine ASF-Datei (Advanced Systems Format) erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3af48-104">Specifies the date and time when an Advanced Systems Format (ASF) file was created.</span></span>

## <a name="data-type"></a><span data-ttu-id="3af48-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3af48-105">Data type</span></span>

<span data-ttu-id="3af48-106">Bytearray</span><span class="sxs-lookup"><span data-stu-id="3af48-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="3af48-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3af48-107">Remarks</span></span>

<span data-ttu-id="3af48-108">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="3af48-108">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="3af48-109">Der Wert des-Attributs ist eine **FILETIME** -Struktur, die in der Windows SDK dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="3af48-109">The value of the attribute is a **FILETIME** structure, which is documented in the Windows SDK.</span></span>

<span data-ttu-id="3af48-110">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="3af48-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="3af48-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3af48-111">Requirements</span></span>



| <span data-ttu-id="3af48-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3af48-112">Requirement</span></span> | <span data-ttu-id="3af48-113">Wert</span><span class="sxs-lookup"><span data-stu-id="3af48-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3af48-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3af48-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3af48-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3af48-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3af48-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3af48-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3af48-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3af48-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3af48-118">Header</span><span class="sxs-lookup"><span data-stu-id="3af48-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3af48-119"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="3af48-119"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3af48-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3af48-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3af48-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="3af48-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3af48-122">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="3af48-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="3af48-123">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="3af48-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="3af48-124">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="3af48-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="3af48-125">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="3af48-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="3af48-126">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="3af48-126">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="3af48-127">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="3af48-127">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




