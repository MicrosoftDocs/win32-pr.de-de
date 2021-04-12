---
description: Enthält Verschlüsselungs Daten für eine ASF-Datei (Advanced Systems Format). Dieses Attribut entspricht dem Objekt für die erweiterte Inhalts Verschlüsselung im ASF-Header, das in der ASF-Spezifikation definiert ist.
ms.assetid: 8bf5e7a4-073f-4b2c-8e9c-49f6f11c9093
title: MF_PD_ASF_CONTENTENCRYPTIONEX_ENCRYPTION_DATA-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550e75f50a7f09556cd9dd89239b3f33fb74d289
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344559"
---
# <a name="mf_pd_asf_contentencryptionex_encryption_data-attribute"></a><span data-ttu-id="7d26e-104">MF \_ PD \_ ASF \_ contentverschlüsselungex- \_ Verschlüsselungs \_ Daten Attribut</span><span class="sxs-lookup"><span data-stu-id="7d26e-104">MF\_PD\_ASF\_CONTENTENCRYPTIONEX\_ENCRYPTION\_DATA attribute</span></span>

<span data-ttu-id="7d26e-105">Enthält Verschlüsselungs Daten für eine ASF-Datei (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="7d26e-105">Contains encryption data for an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="7d26e-106">Dieses Attribut entspricht dem Objekt für die erweiterte Inhalts Verschlüsselung im ASF-Header, das in der ASF-Spezifikation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7d26e-106">This attribute corresponds to the Extended Content Encryption Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="7d26e-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7d26e-107">Data type</span></span>

<span data-ttu-id="7d26e-108">Bytearray</span><span class="sxs-lookup"><span data-stu-id="7d26e-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="7d26e-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d26e-109">Remarks</span></span>

<span data-ttu-id="7d26e-110">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="7d26e-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="7d26e-111">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode erstellt den Präsentations Deskriptor und generiert dieses Attribut aus dem Header der erweiterten Inhalts Verschlüsselungs Objekte.</span><span class="sxs-lookup"><span data-stu-id="7d26e-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Extended Content Encryption Object header.</span></span> <span data-ttu-id="7d26e-112">Die Größe des BLOBs ist mit dem Datengrößen Feld zu groß.</span><span class="sxs-lookup"><span data-stu-id="7d26e-112">The size of the blob equals the Data Size field.</span></span> <span data-ttu-id="7d26e-113">Das im BLOB enthaltene Bytearray ist mit dem Datenfeld im erweiterten Inhalts Verschlüsselungs Objekt des ASF-Headers Gleichheits.</span><span class="sxs-lookup"><span data-stu-id="7d26e-113">The byte array contained in the blob equals the Data field in the Extended Content Encryption object of the ASF header.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d26e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d26e-114">Requirements</span></span>



| <span data-ttu-id="7d26e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d26e-115">Requirement</span></span> | <span data-ttu-id="7d26e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7d26e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d26e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d26e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7d26e-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d26e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7d26e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d26e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7d26e-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d26e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7d26e-121">Header</span><span class="sxs-lookup"><span data-stu-id="7d26e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d26e-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d26e-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d26e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d26e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d26e-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="7d26e-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7d26e-125">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="7d26e-125">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="7d26e-126">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="7d26e-126">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="7d26e-127">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="7d26e-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="7d26e-128">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="7d26e-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="7d26e-129">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="7d26e-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="7d26e-130">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="7d26e-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




