---
description: Enthält geheime Daten für eine verschlüsselte ASF-Datei (Advanced Systems Format). Dieses Attribut entspricht dem Geheimnis Daten Feld des Content Encryption Headers, das in der ASF-Spezifikation definiert ist.
ms.assetid: e6ce71d6-59cd-42da-906a-ab71f2bef16f
title: MF_PD_ASF_CONTENTENCRYPTION_SECRET_DATA-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28c960131e61e539fa417e1068b45974a24c42a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526000"
---
# <a name="mf_pd_asf_contentencryption_secret_data-attribute"></a><span data-ttu-id="28925-104">MF \_ PD \_ - \_ Attribut für \_ Geheimnis Daten (Secret contentencryption \_ )</span><span class="sxs-lookup"><span data-stu-id="28925-104">MF\_PD\_ASF\_CONTENTENCRYPTION\_SECRET\_DATA attribute</span></span>

<span data-ttu-id="28925-105">Enthält geheime Daten für eine verschlüsselte ASF-Datei (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="28925-105">Contains secret data for an encrypted Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="28925-106">Dieses Attribut entspricht dem Geheimnis Daten Feld des Content Encryption Headers, das in der ASF-Spezifikation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="28925-106">This attribute corresponds to the Secret Data field of the Content Encryption Header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="28925-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="28925-107">Data type</span></span>

<span data-ttu-id="28925-108">Bytearray</span><span class="sxs-lookup"><span data-stu-id="28925-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="28925-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28925-109">Remarks</span></span>

<span data-ttu-id="28925-110">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="28925-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="28925-111">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode füllt ein Bytearray mit dem geheimen Datenfeld auf.</span><span class="sxs-lookup"><span data-stu-id="28925-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method populates a byte array with the Secret Data field.</span></span> <span data-ttu-id="28925-112">Die Größe des Arrays ist mit dem Feld für die geheime Daten Länge des Content Encryption-Headers Gleichheits.</span><span class="sxs-lookup"><span data-stu-id="28925-112">The size of the array equals the Secret Data Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="28925-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28925-113">Requirements</span></span>



| <span data-ttu-id="28925-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28925-114">Requirement</span></span> | <span data-ttu-id="28925-115">Wert</span><span class="sxs-lookup"><span data-stu-id="28925-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="28925-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28925-116">Minimum supported client</span></span><br/> | <span data-ttu-id="28925-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28925-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="28925-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28925-118">Minimum supported server</span></span><br/> | <span data-ttu-id="28925-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28925-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="28925-120">Header</span><span class="sxs-lookup"><span data-stu-id="28925-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="28925-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="28925-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28925-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28925-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28925-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="28925-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="28925-124">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="28925-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="28925-125">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="28925-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="28925-126">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="28925-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="28925-127">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="28925-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="28925-128">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="28925-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="28925-129">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="28925-129">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




