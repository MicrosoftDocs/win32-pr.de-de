---
description: Gibt an, ob ein Decoder für die Transcodierung und nicht für die Wiedergabe optimiert ist.
ms.assetid: 0e05cb05-87a8-4174-a3c6-a0a0c7765024
title: MFT_ENUM_TRANSCODE_ONLY_ATTRIBUTE-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fa3349da254534605178995d493f63525a81489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393582"
---
# <a name="mft_enum_transcode_only_attribute-attribute"></a><span data-ttu-id="fc956-103">Attribut Attribut für MFT-Aufzählung von \_ \_ transcode \_ \_</span><span class="sxs-lookup"><span data-stu-id="fc956-103">MFT\_ENUM\_TRANSCODE\_ONLY\_ATTRIBUTE attribute</span></span>

<span data-ttu-id="fc956-104">Gibt an, ob ein Decoder für die Transcodierung und nicht für die Wiedergabe optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="fc956-104">Specifies whether a decoder is optimized for transcoding rather than for playback.</span></span>

<span data-ttu-id="fc956-105">Derzeit gilt dieses Attribut nur für hardwarebasierte decoderer, die den AVStream-Mini Treiber verwenden.</span><span class="sxs-lookup"><span data-stu-id="fc956-105">Currently, this attribute applies only to hardware-based decoders that use the AVStream mini-driver.</span></span> <span data-ttu-id="fc956-106">Das-Attribut wird in der Registrierung unter den Funktions Informationen des Decoders gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fc956-106">The attribute is stored in the registry under the decoder's capabilities information.</span></span> <span data-ttu-id="fc956-107">Weitere Informationen finden Sie in der Dokumentation zu [**igetcapabilitieskey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).</span><span class="sxs-lookup"><span data-stu-id="fc956-107">For more information, see the documentation for [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).</span></span>

<span data-ttu-id="fc956-108">Anwendungen verwenden dieses Attribut in der Regel nicht.</span><span class="sxs-lookup"><span data-stu-id="fc956-108">Applications typically do not use this attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="fc956-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="fc956-109">Data type</span></span>

<span data-ttu-id="fc956-110">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fc956-110">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="fc956-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc956-111">Remarks</span></span>

<span data-ttu-id="fc956-112">Wenn dieser Registrierungs Eintrag vorhanden und gleich 1 ist, überspringt die [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion den Decoder, es sei denn, der Aufrufer hat das Flag " **\_ \_ \_ \_ nur transcode" der MFT** -Enumeration in " **mftenumex**" angegeben.</span><span class="sxs-lookup"><span data-stu-id="fc956-112">If this registry entry is present and equal to 1, the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function skips the decoder unless the caller specified the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag in **MFTEnumEx**.</span></span>

<span data-ttu-id="fc956-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="fc956-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc956-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc956-114">Requirements</span></span>



| <span data-ttu-id="fc956-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc956-115">Requirement</span></span> | <span data-ttu-id="fc956-116">Wert</span><span class="sxs-lookup"><span data-stu-id="fc956-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc956-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc956-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fc956-118">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="fc956-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="fc956-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc956-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fc956-120">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="fc956-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fc956-121">Header</span><span class="sxs-lookup"><span data-stu-id="fc956-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc956-122"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="fc956-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc956-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc956-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc956-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="fc956-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fc956-125">**MF-Datei**</span><span class="sxs-lookup"><span data-stu-id="fc956-125">**MFTEnumEx**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> </dl>

 

 
