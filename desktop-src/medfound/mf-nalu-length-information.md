---
description: Gibt die Länge von nalus in der Stichprobe an. Hierbei handelt es sich um ein MF-BLOB, das auf komprimierte Eingabe Beispiele für den H. 264-Decoder festgelegt ist.
ms.assetid: 09F54504-A6CF-4385-BDD7-8D23B1D0125C
title: MF_NALU_LENGTH_INFORMATION-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46d9a0b7cbec92c4cde40548b8d3baecf955b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347936"
---
# <a name="mf_nalu_length_information-attribute"></a><span data-ttu-id="73a7a-104">MF \_ Nalu- \_ Längen \_ Informations Attribut</span><span class="sxs-lookup"><span data-stu-id="73a7a-104">MF\_NALU\_LENGTH\_INFORMATION attribute</span></span>

<span data-ttu-id="73a7a-105">Gibt die Länge von nalus in der Stichprobe an.</span><span class="sxs-lookup"><span data-stu-id="73a7a-105">Indicates the lengths of NALUs in the sample.</span></span> <span data-ttu-id="73a7a-106">Hierbei handelt es sich um ein MF- **BLOB** , das auf komprimierte Eingabe Beispiele für den H. 264-Decoder festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="73a7a-106">This is a MF **BLOB** that is set on compressed input samples to the H.264 decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="73a7a-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="73a7a-107">Data type</span></span>

<span data-ttu-id="73a7a-108">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="73a7a-108">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="73a7a-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73a7a-109">Remarks</span></span>

<span data-ttu-id="73a7a-110">Damit dieses Attribut festgelegt werden kann, muss das Medium den Typ "mediasubtype H264" aufweisen, \_ und das Attribut " [MF \_ Nalu \_ length \_ Set](mf-nalu-length-set.md) " muss für den Eingabe Medientyp von mediasubtype H264 festgelegt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="73a7a-110">In order for this attribute to be set, the media must be of type MEDIASUBTYPE\_H264 and the [MF\_NALU\_LENGTH\_SET](mf-nalu-length-set.md) attribute must be set on the input media type of MEDIASUBTYPE\_H264.</span></span>

<span data-ttu-id="73a7a-111">Legen Sie \_ \_ \_ für das Eingabe Beispiel die Informationen der MF-Nalu-Länge als **BLOB** fest, mit einem DWORD für jede Nalu im Beispiel.</span><span class="sxs-lookup"><span data-stu-id="73a7a-111">Set MF\_NALU\_LENGTH\_INFORMATION as a **BLOB** on the input sample, with one DWORD for each NALU in the sample.</span></span> <span data-ttu-id="73a7a-112">Wenn z. b. AUD (9 Bytes), SPS (25 Bytes), PPS (10 Bytes), IDR slice1 (50 k), IDR Slice 2 (60 k) vorhanden sind, sollten 5 DWords mit den Werten 9, 25, 10, 50 k, 60 k im **BLOB** vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="73a7a-112">For example, if there are AUD (9 bytes), SPS (25 bytes), PPS (10 bytes), IDR slice1 (50 k), IDR slice 2 (60 k), then there should be 5 DWORDs with values 9, 25, 10, 50 k, 60 k in the **BLOB**.</span></span>

<span data-ttu-id="73a7a-113">Hier finden Sie Code, in dem das **BLOB** festgelegt wird. **rgdwnalulengthinfo** ist ein Array vom Typ DWORD und **uinalulengthidx** ist die gültige Nalu-Länge, die auf das **BLOB** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="73a7a-113">Here some code that sets the **BLOB**, where **rgdwNALULengthInfo** is an array of type DWORD and **uiNaluLengthIdx** is the valid NALU lengths set to the **BLOB**.</span></span>


```C++
m_spSample->SetBlob( MF_NALU_LENGTH_INFORMATION, 
                    (UINT8*) m_wpParent->m_pdwNALULengthInfo, 
                    sizeof(DWORD)*uiNaluLengthIdx ), 
                    done );
```



## <a name="requirements"></a><span data-ttu-id="73a7a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73a7a-114">Requirements</span></span>



| <span data-ttu-id="73a7a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73a7a-115">Requirement</span></span> | <span data-ttu-id="73a7a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="73a7a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73a7a-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73a7a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="73a7a-118">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="73a7a-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="73a7a-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73a7a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="73a7a-120">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="73a7a-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="73a7a-121">Header</span><span class="sxs-lookup"><span data-stu-id="73a7a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="73a7a-122"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="73a7a-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73a7a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73a7a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73a7a-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="73a7a-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="73a7a-125">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="73a7a-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




