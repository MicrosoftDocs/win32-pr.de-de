---
description: Gibt eine Liste von Bitraten und entsprechenden Puffer Fenstern für eine ASF-Datei (VBR) mit variabler Bitrate (Advanced Systems Format) an.
ms.assetid: e45d055f-d404-47e9-b3c8-ac743b290138
title: MF_PD_ASF_METADATA_LEAKY_BUCKET_PAIRS-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7426d15a806a8c61c9a2ea1fdfb0565372c5f48f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373150"
---
# <a name="mf_pd_asf_metadata_leaky_bucket_pairs-attribute"></a><span data-ttu-id="fdde0-103">MF \_ PD- \_ ASF-Metadaten- \_ \_ Attribut "Leaky \_ Bucket \_ Paars"</span><span class="sxs-lookup"><span data-stu-id="fdde0-103">MF\_PD\_ASF\_METADATA\_LEAKY\_BUCKET\_PAIRS attribute</span></span>

<span data-ttu-id="fdde0-104">Gibt eine Liste von Bitraten und entsprechenden Puffer Fenstern für eine ASF-Datei (VBR) mit variabler Bitrate (Advanced Systems Format) an.</span><span class="sxs-lookup"><span data-stu-id="fdde0-104">Specifies a list of bit rates and corresponding buffer windows for a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="fdde0-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="fdde0-105">Data type</span></span>

<span data-ttu-id="fdde0-106">Bytearray</span><span class="sxs-lookup"><span data-stu-id="fdde0-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="fdde0-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fdde0-107">Remarks</span></span>

<span data-ttu-id="fdde0-108">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="fdde0-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="fdde0-109">Die [**imfasfcontentinfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut, das für den Präsentations Deskriptor für den ASF-Inhalt gilt.</span><span class="sxs-lookup"><span data-stu-id="fdde0-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute that applies to the presentation descriptor for ASF content.</span></span>

<span data-ttu-id="fdde0-110">Der Wert des-Attributs weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="fdde0-110">The value of the attribute has the following format:</span></span>

``` syntax
struct {
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

<span data-ttu-id="fdde0-111">Die " **WM \_ Leaky \_ Bucket \_ Pair** "-Struktur ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="fdde0-111">The **WM\_LEAKY\_BUCKET\_PAIR** structure is defined as follows:</span></span>

``` syntax
typedef struct _WMLeakyBucketPair {
  DWORD  dwBitrate;
  DWORD  msBufferWindow;
} WM_LEAKY_BUCKET_PAIR;
```

<span data-ttu-id="fdde0-112">Der **msbufferwindow** -Member gibt für jede Bitrate an, wie viel Inhalt vor Beginn der Wiedergabe gepuffert wird (in Millisekunden).</span><span class="sxs-lookup"><span data-stu-id="fdde0-112">For each bit rate, the **msBufferWindow** member indicates how much content is buffered before playback begins, in milliseconds.</span></span> <span data-ttu-id="fdde0-113">Die Größe des Puffers in Bytes ist mit **msbufferwinow** x **dwbitrate** /8000.</span><span class="sxs-lookup"><span data-stu-id="fdde0-113">The size of the buffer in bytes equals **msBufferWinow** x **dwBitrate** / 8000.</span></span>

> [!Note]  
> <span data-ttu-id="fdde0-114">Dieses Attribut entspricht dem **asfleakybucketpair** -Attribut im Windows Media-Format-SDK.</span><span class="sxs-lookup"><span data-stu-id="fdde0-114">This attribute corresponds to the **ASFLeakyBucketPairs** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fdde0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fdde0-115">Requirements</span></span>



| <span data-ttu-id="fdde0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fdde0-116">Requirement</span></span> | <span data-ttu-id="fdde0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="fdde0-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdde0-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fdde0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fdde0-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fdde0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fdde0-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fdde0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fdde0-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fdde0-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fdde0-122">Header</span><span class="sxs-lookup"><span data-stu-id="fdde0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdde0-123"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdde0-123"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdde0-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fdde0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdde0-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="fdde0-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fdde0-126">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="fdde0-126">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="fdde0-127">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="fdde0-127">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="fdde0-128">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="fdde0-128">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="fdde0-129">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="fdde0-129">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="fdde0-130">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="fdde0-130">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="fdde0-131">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="fdde0-131">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




