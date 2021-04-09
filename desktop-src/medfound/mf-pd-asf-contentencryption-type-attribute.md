---
description: Gibt den Typ des Schutzmechanismus an, der in einer ASF-Datei (Advanced Systems Format) verwendet wird.
ms.assetid: 91ceb610-6ff4-4133-beab-6debb94eec2c
title: MF_PD_ASF_CONTENTENCRYPTION_TYPE-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9131b24138edf6e85fc0e264bdcdd028f2eb0538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862500"
---
# <a name="mf_pd_asf_contentencryption_type-attribute"></a><span data-ttu-id="446b3-103">MF \_ - \_ \_ \_ Attribut vom Typ "MF-Attribut"</span><span class="sxs-lookup"><span data-stu-id="446b3-103">MF\_PD\_ASF\_CONTENTENCRYPTION\_TYPE attribute</span></span>

<span data-ttu-id="446b3-104">Gibt den Typ des Schutzmechanismus an, der in einer ASF-Datei (Advanced Systems Format) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="446b3-104">Specifies the type of protection mechanism used in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="446b3-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="446b3-105">Data type</span></span>

<span data-ttu-id="446b3-106">Breitzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="446b3-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="446b3-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="446b3-107">Remarks</span></span>

<span data-ttu-id="446b3-108">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="446b3-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="446b3-109">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode ruft das Schutztyp Feld ab, konvertiert es in eine Zeichenfolge mit breit Zeichen und füllt dann ein mit Null endendes Array von **WCHAR** s auf.</span><span class="sxs-lookup"><span data-stu-id="446b3-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method retrieves the Protection Type field, converts it into a wide-character string, and then populates a null-terminated array of **WCHAR** s.</span></span> <span data-ttu-id="446b3-110">Falls vorhanden, muss der Wert "DRM" lauten.</span><span class="sxs-lookup"><span data-stu-id="446b3-110">If present, the value must be "DRM".</span></span> <span data-ttu-id="446b3-111">Die Größe des Arrays ist mit dem Feldlängen Feld der Schutzart des Inhalts Verschlüsselungs Headers Gleichheits.</span><span class="sxs-lookup"><span data-stu-id="446b3-111">The size of the array equals the Protection Type Field Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="446b3-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="446b3-112">Requirements</span></span>



| <span data-ttu-id="446b3-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="446b3-113">Requirement</span></span> | <span data-ttu-id="446b3-114">Wert</span><span class="sxs-lookup"><span data-stu-id="446b3-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="446b3-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="446b3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="446b3-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="446b3-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="446b3-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="446b3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="446b3-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="446b3-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="446b3-119">Header</span><span class="sxs-lookup"><span data-stu-id="446b3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="446b3-120"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="446b3-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="446b3-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="446b3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="446b3-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="446b3-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="446b3-123">**Imfattributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="446b3-123">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="446b3-124">**Imfattributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="446b3-124">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="446b3-125">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="446b3-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="446b3-126">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="446b3-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="446b3-127">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="446b3-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="446b3-128">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="446b3-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




