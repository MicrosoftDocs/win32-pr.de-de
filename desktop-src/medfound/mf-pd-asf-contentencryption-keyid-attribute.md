---
description: Gibt den Schlüssel Bezeichner für eine verschlüsselte ASF-Datei (Advanced Systems Format) an. Dieses Attribut entspricht dem Schlüssel-ID-Feld des Content Encryption Headers, das in der ASF-Spezifikation definiert ist.
ms.assetid: ebadd156-28f4-499c-a182-f48a35ecbefb
title: MF_PD_ASF_CONTENTENCRYPTION_KEYID-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd49c7a006345cceba01edde7caf76e499323b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129004"
---
# <a name="mf_pd_asf_contentencryption_keyid-attribute"></a><span data-ttu-id="7dc56-104">Schlüssel-ID-Attribut für MF \_ PD \_ ASF \_ contentencryption \_</span><span class="sxs-lookup"><span data-stu-id="7dc56-104">MF\_PD\_ASF\_CONTENTENCRYPTION\_KEYID attribute</span></span>

<span data-ttu-id="7dc56-105">Gibt den Schlüssel Bezeichner für eine verschlüsselte ASF-Datei (Advanced Systems Format) an.</span><span class="sxs-lookup"><span data-stu-id="7dc56-105">Specifies the key identifier for an encrypted Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="7dc56-106">Dieses Attribut entspricht dem Schlüssel-ID-Feld des Content Encryption Headers, das in der ASF-Spezifikation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7dc56-106">This attribute corresponds to the Key ID field of the Content Encryption Header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="7dc56-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7dc56-107">Data type</span></span>

<span data-ttu-id="7dc56-108">Breitzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7dc56-108">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="7dc56-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7dc56-109">Remarks</span></span>

<span data-ttu-id="7dc56-110">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="7dc56-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="7dc56-111">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode ruft das Schlüssel-ID-Feld ab, konvertiert es in eine Zeichenfolge mit breit Zeichen und füllt dann ein mit Null endendes Array von **WCHAR** s auf.</span><span class="sxs-lookup"><span data-stu-id="7dc56-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method retrieves the Key ID field, converts it into a wide-character string, and then populates a null-terminated array of **WCHAR** s.</span></span> <span data-ttu-id="7dc56-112">Die Größe des Arrays ist mit dem Feld für die Länge der Schlüssel-ID des Content Encryption Headers.</span><span class="sxs-lookup"><span data-stu-id="7dc56-112">The size of the array equals the Key ID Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dc56-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7dc56-113">Requirements</span></span>



| <span data-ttu-id="7dc56-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7dc56-114">Requirement</span></span> | <span data-ttu-id="7dc56-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7dc56-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc56-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7dc56-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7dc56-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7dc56-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7dc56-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7dc56-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7dc56-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7dc56-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7dc56-120">Header</span><span class="sxs-lookup"><span data-stu-id="7dc56-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dc56-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dc56-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dc56-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7dc56-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dc56-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="7dc56-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7dc56-124">**Imfattributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="7dc56-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="7dc56-125">**Imfattributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="7dc56-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="7dc56-126">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="7dc56-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="7dc56-127">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="7dc56-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="7dc56-128">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="7dc56-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="7dc56-129">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="7dc56-129">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




