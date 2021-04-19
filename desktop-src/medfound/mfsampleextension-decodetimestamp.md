---
description: Enthält den decodierungszeit Stempel (DTS) für das Beispiel.
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: MFSampleExtension_DecodeTimestamp-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9676b295eb16e7cb2bb607ef4a5074d24b276d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360134"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a><span data-ttu-id="6856d-103">MF Sample Extension- \_ decodetimestamp-Attribut</span><span class="sxs-lookup"><span data-stu-id="6856d-103">MFSampleExtension\_DecodeTimestamp attribute</span></span>

<span data-ttu-id="6856d-104">Enthält den decodierungszeit Stempel (DTS) für das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="6856d-104">Contains the decode time stamp (DTS) for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="6856d-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6856d-105">Data type</span></span>

<span data-ttu-id="6856d-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="6856d-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="6856d-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6856d-107">Remarks</span></span>

<span data-ttu-id="6856d-108">Der Wert des-Attributs ist der DTS in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="6856d-108">The value of the attribute is the DTS in 100-nanosecond units.</span></span> <span data-ttu-id="6856d-109">DTS ist in einigen Codierungsstandards definiert, einschließlich MPEG.</span><span class="sxs-lookup"><span data-stu-id="6856d-109">The DTS is defined in some encoding standards, including MPEG.</span></span> <span data-ttu-id="6856d-110">Der DTS gibt an, wann das codierte Bild decodiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6856d-110">The DTS specifies when the encoded picture should be decoded.</span></span> <span data-ttu-id="6856d-111">Wenn das codierte Video b-Frames enthält, kann sich der DTS von der Präsentationszeit unterscheiden, da B-Bilder im Bitstream außerhalb der temporalen Reihenfolge erscheinen.</span><span class="sxs-lookup"><span data-stu-id="6856d-111">If the encoded video contains B frames, the DTS can differ from the presentation time, because B pictures appear out of temporal order in the bitstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="6856d-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6856d-112">Requirements</span></span>



| <span data-ttu-id="6856d-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6856d-113">Requirement</span></span> | <span data-ttu-id="6856d-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6856d-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6856d-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6856d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6856d-116">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6856d-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="6856d-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6856d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6856d-118">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6856d-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6856d-119">Header</span><span class="sxs-lookup"><span data-stu-id="6856d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6856d-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6856d-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6856d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6856d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6856d-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="6856d-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6856d-123">Beispiel Attribute</span><span class="sxs-lookup"><span data-stu-id="6856d-123">Sample Attributes</span></span>](sample-attributes.md)
</dt> </dl>

 

 




