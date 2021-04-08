---
description: Gibt die Zeit an, die für die Wiedergabe einer ASF-Datei (Advanced Systems Format) in 100-Nanosecond-Einheiten erforderlich ist.
ms.assetid: 3d36808b-aa13-4205-ad92-97e951ee827e
title: MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac62dfbd86dfcbd001555343309568033787186b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960193"
---
# <a name="mf_pd_asf_fileproperties_play_duration-attribute"></a><span data-ttu-id="4ba23-103">MF \_ PD \_ ASF \_ File Properties \_ Play \_ Duration-Attribut</span><span class="sxs-lookup"><span data-stu-id="4ba23-103">MF\_PD\_ASF\_FILEPROPERTIES\_PLAY\_DURATION attribute</span></span>

<span data-ttu-id="4ba23-104">Gibt die Zeit an, die für die Wiedergabe einer ASF-Datei (Advanced Systems Format) in 100-Nanosecond-Einheiten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4ba23-104">Specifies the time needed to play an Advanced Systems Format (ASF) file, in 100-nanosecond units.</span></span>

<span data-ttu-id="4ba23-105">Dieser Wert enthält die Vorabversion.</span><span class="sxs-lookup"><span data-stu-id="4ba23-105">This value includes the preroll time.</span></span> <span data-ttu-id="4ba23-106">Um die tatsächliche Wiedergabedauer abzurufen, rufen Sie den Wert des " [**MF \_ PD \_ Duration**](mf-pd-duration-attribute.md) "-Attributs ab.</span><span class="sxs-lookup"><span data-stu-id="4ba23-106">To retrieve the actual playback duration, get the value of the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute.</span></span> <span data-ttu-id="4ba23-107">Wenn der ein Vorlauf ausgeführt-Wert jedoch größer als die Wiedergabedauer ist, ist der Wert von **MF \_ PD \_ Duration** gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="4ba23-107">However, if the preroll value is greater than the play duration, the value of **MF\_PD\_DURATION** is zero.</span></span>

## <a name="data-type"></a><span data-ttu-id="4ba23-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4ba23-108">Data type</span></span>

<span data-ttu-id="4ba23-109">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="4ba23-109">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="4ba23-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ba23-110">Remarks</span></span>

<span data-ttu-id="4ba23-111">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="4ba23-111">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="4ba23-112">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="4ba23-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="examples"></a><span data-ttu-id="4ba23-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ba23-113">Examples</span></span>


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



## <a name="requirements"></a><span data-ttu-id="4ba23-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ba23-114">Requirements</span></span>



| <span data-ttu-id="4ba23-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ba23-115">Requirement</span></span> | <span data-ttu-id="4ba23-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4ba23-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ba23-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4ba23-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4ba23-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ba23-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4ba23-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4ba23-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4ba23-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ba23-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4ba23-121">Header</span><span class="sxs-lookup"><span data-stu-id="4ba23-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ba23-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ba23-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ba23-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ba23-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ba23-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4ba23-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4ba23-125">**Imfattributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="4ba23-125">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="4ba23-126">**Imfattributes:: SetGuid**</span><span class="sxs-lookup"><span data-stu-id="4ba23-126">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="4ba23-127">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="4ba23-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="4ba23-128">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="4ba23-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="4ba23-129">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="4ba23-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="4ba23-130">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="4ba23-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




