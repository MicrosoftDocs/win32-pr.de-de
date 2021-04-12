---
description: Gibt die endgültige Ausgabeauflösung des decodierten Bilds nach der Videoverarbeitung an.
ms.assetid: 067867D8-155C-4406-BE07-720016B2AEBC
title: MFT_DECODER_FINAL_VIDEO_RESOLUTION_HINT-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bbc0f01ef2a1d7062c6ab58c528b015383fc68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215036"
---
# <a name="mft_decoder_final_video_resolution_hint-attribute"></a><span data-ttu-id="828c0-103">\_ \_ Letztes \_ Video \_ Auflösungs \_ Hinweis Attribut des MFT-Decoders</span><span class="sxs-lookup"><span data-stu-id="828c0-103">MFT\_DECODER\_FINAL\_VIDEO\_RESOLUTION\_HINT attribute</span></span>

<span data-ttu-id="828c0-104">Gibt die endgültige Ausgabeauflösung des decodierten Bilds nach der Videoverarbeitung an.</span><span class="sxs-lookup"><span data-stu-id="828c0-104">Specifies the final output resolution of the decoded image, after video processing.</span></span>

## <a name="data-type"></a><span data-ttu-id="828c0-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="828c0-105">Data type</span></span>

<span data-ttu-id="828c0-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="828c0-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="828c0-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="828c0-107">Remarks</span></span>

<span data-ttu-id="828c0-108">Dieses Attribut wird von einigen Video-Decodern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="828c0-108">This attribute is supported by some video decoders.</span></span> <span data-ttu-id="828c0-109">Eine Anwendung kann dieses Attribut festlegen, um die Breite und Höhe des Bilds nach der Videoverarbeitung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="828c0-109">An application can set this attribute to indicate the width and height of the image after video processing.</span></span> <span data-ttu-id="828c0-110">Der Decoder kann diese Informationen verwenden, um den Decodierungs Prozess zu optimieren, insbesondere dann, wenn die endgültige Bildgröße wesentlich kleiner ist als die Größe des systemeigenen Bilds.</span><span class="sxs-lookup"><span data-stu-id="828c0-110">The decoder can use this information to optimize the decoding process, especially if the final image size is much smaller than the native image size.</span></span> <span data-ttu-id="828c0-111">Der Decoder könnte z. b. einen Out-of-Loop-Filter überspringen.</span><span class="sxs-lookup"><span data-stu-id="828c0-111">For example, the decoder might skip an out-of-loop filter.</span></span>

<span data-ttu-id="828c0-112">Die oberen 32 Bits enthalten die Breite, und die unteren 32 Bits enthalten die Höhe.</span><span class="sxs-lookup"><span data-stu-id="828c0-112">The upper 32 bits contain the width and the lower 32 bits contain the height.</span></span>

<span data-ttu-id="828c0-113">So legen Sie dieses Attribut fest:</span><span class="sxs-lookup"><span data-stu-id="828c0-113">To set this attribute:</span></span>

1.  <span data-ttu-id="828c0-114">Aufrufen von [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) für den Decoder zum Abrufen eines [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeigers.</span><span class="sxs-lookup"><span data-stu-id="828c0-114">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="828c0-115">Zum Hinzufügen des Attributs muss [**mftstributesize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="828c0-115">Call [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="828c0-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="828c0-116">Requirements</span></span>



| <span data-ttu-id="828c0-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="828c0-117">Requirement</span></span> | <span data-ttu-id="828c0-118">Wert</span><span class="sxs-lookup"><span data-stu-id="828c0-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="828c0-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="828c0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="828c0-120">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="828c0-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="828c0-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="828c0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="828c0-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="828c0-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="828c0-123">Header</span><span class="sxs-lookup"><span data-stu-id="828c0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="828c0-124"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="828c0-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="828c0-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="828c0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="828c0-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="828c0-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="828c0-127">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="828c0-127">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




