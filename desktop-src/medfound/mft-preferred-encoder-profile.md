---
description: Enthält Konfigurations Eigenschaften für einen Encoder.
ms.assetid: f9bd8a50-e43e-4668-86a0-c9d5f517f4cf
title: MFT_PREFERRED_ENCODER_PROFILE-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfdc85ead0fe813215b3edaea14833400df5445d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959238"
---
# <a name="mft_preferred_encoder_profile-attribute"></a><span data-ttu-id="0c71c-103">"MFT \_ Preferred \_ Encoder profile"- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="0c71c-103">MFT\_PREFERRED\_ENCODER\_PROFILE attribute</span></span>

<span data-ttu-id="0c71c-104">Enthält Konfigurations Eigenschaften für einen Encoder.</span><span class="sxs-lookup"><span data-stu-id="0c71c-104">Contains configuration properties for an encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="0c71c-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0c71c-105">Data type</span></span>

<span data-ttu-id="0c71c-106">**[**Imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) \** _ als " _*IUnknown \*\* " gespeichert_</span><span class="sxs-lookup"><span data-stu-id="0c71c-106">**[**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="0c71c-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="0c71c-107">Get/set</span></span>

<span data-ttu-id="0c71c-108">Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="0c71c-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="0c71c-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="0c71c-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="0c71c-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="0c71c-110">Applies to</span></span>

[<span data-ttu-id="0c71c-111">**Imfaktivate**</span><span class="sxs-lookup"><span data-stu-id="0c71c-111">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a><span data-ttu-id="0c71c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c71c-112">Remarks</span></span>

<span data-ttu-id="0c71c-113">Dieses Attribut kann für das Aktivierungs Objekt festgelegt werden, das von der [**msmekreatetransformaktivierungs**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0c71c-113">This attribute can be set on the activation object returned by the [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) function.</span></span> <span data-ttu-id="0c71c-114">Das-Attribut wird nur angewendet, wenn das Aktivierungs Objekt zum Erstellen eines Encoders konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="0c71c-114">The attribute applies only when the activation object is configured to create an encoder.</span></span> <span data-ttu-id="0c71c-115">Der Wert des-Attributs ist ein Zeiger auf einen Attribut Speicher, der wiederum Eigenschaften enthält, die für den Encoder festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0c71c-115">The value of the attribute is a pointer to an attribute store, which itself contains properties to set on the encoder.</span></span>

<span data-ttu-id="0c71c-116">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="0c71c-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c71c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c71c-117">Requirements</span></span>



| <span data-ttu-id="0c71c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c71c-118">Requirement</span></span> | <span data-ttu-id="0c71c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0c71c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c71c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c71c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0c71c-121">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0c71c-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="0c71c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c71c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0c71c-123">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0c71c-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0c71c-124">Header</span><span class="sxs-lookup"><span data-stu-id="0c71c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c71c-125"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="0c71c-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c71c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c71c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c71c-127">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="0c71c-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0c71c-128">**MF | atetransformaktivierungs**</span><span class="sxs-lookup"><span data-stu-id="0c71c-128">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[<span data-ttu-id="0c71c-129">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="0c71c-129">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




