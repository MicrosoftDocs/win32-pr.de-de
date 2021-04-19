---
description: Enthält den Wert eines Hardware Codecs.
ms.assetid: 1df40a42-4c02-473f-a87f-2ae2d42e4f4e
title: MFT_CODEC_MERIT_Attribute-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74745244824bc766d0f7c1e691cb5f176d1da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353175"
---
# <a name="mft_codec_merit_attribute-attribute"></a><span data-ttu-id="1004e-103">Attribut Attribut Attribut für MFT- \_ Codec \_ \_</span><span class="sxs-lookup"><span data-stu-id="1004e-103">MFT\_CODEC\_MERIT\_Attribute attribute</span></span>

<span data-ttu-id="1004e-104">Enthält den Wert eines Hardware Codecs.</span><span class="sxs-lookup"><span data-stu-id="1004e-104">Contains the merit value of a hardware codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="1004e-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1004e-105">Data type</span></span>

<span data-ttu-id="1004e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1004e-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="1004e-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="1004e-107">Get/set</span></span>

<span data-ttu-id="1004e-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="1004e-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="1004e-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="1004e-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="1004e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1004e-110">Remarks</span></span>

<span data-ttu-id="1004e-111">Dieses Attribut wird für das Aktivierungs Objekt für eine Media Foundation Transformation (MFT) festgelegt, die einen Hardwarecodec darstellt.</span><span class="sxs-lookup"><span data-stu-id="1004e-111">This attribute is set on the activation object for a Media Foundation transform (MFT) that represents a hardware codec.</span></span> <span data-ttu-id="1004e-112">Der Wert des-Attributs ist der Verdienst Wert des Codecs.</span><span class="sxs-lookup"><span data-stu-id="1004e-112">The value of the attribute is the codec's merit value.</span></span>

<span data-ttu-id="1004e-113">Dieses Attribut steuert die Reihenfolge, in der die [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion Codecs auflistet, wenn das Flag **\_ \_ \_ sortandfilter für das MFT-Enum-Flag** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1004e-113">This attribute controls the order in which the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function enumerates codecs, if the **MFT\_ENUM\_FLAG\_SORTANDFILTER** flag is set.</span></span> <span data-ttu-id="1004e-114">MFTs mit einem Wert Wert werden in der Liste höher als andere MFTs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1004e-114">MFTs with a merit value appear higher in the list than other MFTs.</span></span>

<span data-ttu-id="1004e-115">Dieses Attribut enthält keinen vertrauenswürdigen Wert.</span><span class="sxs-lookup"><span data-stu-id="1004e-115">This attribute does not contain a trusted value.</span></span> <span data-ttu-id="1004e-116">Um den tatsächlichen Wert des Codecs zu überprüfen, müssen Sie die [**mfgetmftmerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1004e-116">To verify the codec's actual merit value, call the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function.</span></span>

<span data-ttu-id="1004e-117">Wenn der Wert des Attributs für den MFT- \_ Codec- \_ Attribut Wert \_ nicht mit dem von [**mfgetmftmerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit)abgerufenen Verdienst Wert identisch ist, schlägt die [**imfactivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) -Methode fehl und gibt den von **MF \_ E \_ ungültigen \_ Codec- \_ Verdienst** zurück.</span><span class="sxs-lookup"><span data-stu-id="1004e-117">If the value of the MFT\_CODEC\_MERIT\_Attribute attribute does not match the merit value retrieved by [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit), the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails and returns **MF\_E\_INVALID\_CODEC\_MERIT**.</span></span>

<span data-ttu-id="1004e-118">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="1004e-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1004e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1004e-119">Requirements</span></span>



| <span data-ttu-id="1004e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1004e-120">Requirement</span></span> | <span data-ttu-id="1004e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1004e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1004e-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1004e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1004e-123">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1004e-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="1004e-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1004e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1004e-125">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1004e-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="1004e-126">Header</span><span class="sxs-lookup"><span data-stu-id="1004e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1004e-127"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="1004e-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1004e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1004e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1004e-129">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="1004e-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1004e-130">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="1004e-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




