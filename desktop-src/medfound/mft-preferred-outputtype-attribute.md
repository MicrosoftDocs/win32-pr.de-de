---
description: Gibt das bevorzugte Ausgabeformat für einen Encoder an.
ms.assetid: 36a09696-3fe7-41a0-93f1-712220f88b04
title: MFT_PREFERRED_OUTPUTTYPE_Attribute-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13cd079bee65f5324987d9b38dca845ec5b85f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863956"
---
# <a name="mft_preferred_outputtype_attribute-attribute"></a><span data-ttu-id="0e72a-103">MFT- \_ bevorzugtes \_ OutputType- \_ Attribut Attribut</span><span class="sxs-lookup"><span data-stu-id="0e72a-103">MFT\_PREFERRED\_OUTPUTTYPE\_Attribute attribute</span></span>

<span data-ttu-id="0e72a-104">Gibt das bevorzugte Ausgabeformat für einen Encoder an.</span><span class="sxs-lookup"><span data-stu-id="0e72a-104">Specifies the preferred output format for an encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="0e72a-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0e72a-105">Data type</span></span>

<span data-ttu-id="0e72a-106">**[**Imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) \** _ als " _*IUnknown \*\* " gespeichert_</span><span class="sxs-lookup"><span data-stu-id="0e72a-106">**[**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="0e72a-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="0e72a-107">Get/set</span></span>

<span data-ttu-id="0e72a-108">Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="0e72a-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="0e72a-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="0e72a-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="0e72a-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="0e72a-110">Applies to</span></span>

[<span data-ttu-id="0e72a-111">**Imfaktivate**</span><span class="sxs-lookup"><span data-stu-id="0e72a-111">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a><span data-ttu-id="0e72a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e72a-112">Remarks</span></span>

<span data-ttu-id="0e72a-113">Dieses Attribut kann für das Aktivierungs Objekt festgelegt werden, das von der [**msmekreatetransformaktivierungs**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e72a-113">This attribute can be set on the activation object returned by the [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) function.</span></span> <span data-ttu-id="0e72a-114">Das-Attribut wird nur angewendet, wenn das Aktivierungs Objekt zum Erstellen eines Encoders konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="0e72a-114">The attribute applies only when the activation object is configured to create an encoder.</span></span> <span data-ttu-id="0e72a-115">Der Wert des-Attributs ist ein Medientyp.</span><span class="sxs-lookup"><span data-stu-id="0e72a-115">The value of the attribute is a media type.</span></span> <span data-ttu-id="0e72a-116">Das Aktivierungs Objekt legt diesen Ausgabetyp für den Encoder fest.</span><span class="sxs-lookup"><span data-stu-id="0e72a-116">The activation object sets this output type on the encoder.</span></span>

<span data-ttu-id="0e72a-117">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="0e72a-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e72a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e72a-118">Requirements</span></span>



| <span data-ttu-id="0e72a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e72a-119">Requirement</span></span> | <span data-ttu-id="0e72a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0e72a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e72a-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0e72a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0e72a-122">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0e72a-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="0e72a-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0e72a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0e72a-124">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0e72a-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0e72a-125">Header</span><span class="sxs-lookup"><span data-stu-id="0e72a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e72a-126"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="0e72a-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e72a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e72a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e72a-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="0e72a-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0e72a-129">**MF | atetransformaktivierungs**</span><span class="sxs-lookup"><span data-stu-id="0e72a-129">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[<span data-ttu-id="0e72a-130">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="0e72a-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




