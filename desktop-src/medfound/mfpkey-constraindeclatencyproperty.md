---
description: Gibt an, ob der Encoder durch eine maximale Anzahl von decoderlatenzanforderungen eingeschränkt wird.
ms.assetid: 054e445e-fc71-4d4f-9e9f-f5ff71f0b4ee
title: MFPKEY_CONSTRAINDECLATENCY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343bcc9bd365b9f1321b200baa203fc27784594c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345285"
---
# <a name="mfpkey_constraindeclatency-property"></a><span data-ttu-id="82da7-103">Mfpkey- \_ einschränkeyclatency (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="82da7-103">MFPKEY\_CONSTRAINDECLATENCY Property</span></span>

<span data-ttu-id="82da7-104">Gibt an, ob der Encoder durch eine maximale Anzahl von decoderlatenzanforderungen eingeschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="82da7-104">Specifies whether the encoder is constrained by a maximum decoder latency requirement.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="82da7-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="82da7-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="82da7-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="82da7-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="82da7-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="82da7-107">Data Type</span></span>

<span data-ttu-id="82da7-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="82da7-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="82da7-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="82da7-109">Default Value</span></span>

<span data-ttu-id="82da7-110">**Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="82da7-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="82da7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82da7-111">Remarks</span></span>

<span data-ttu-id="82da7-112">Wenn Sie für diese Eigenschaft den Standardwert **Variant \_ false** belassen, listet der Encoder einen Standardsatz von Modi auf, die ungefähr 1500 Millisekunden von Decoder-Latenzzeit haben.</span><span class="sxs-lookup"><span data-stu-id="82da7-112">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder enumerates a default set of modes that have about 1500 milliseconds of decoder latency.</span></span> <span data-ttu-id="82da7-113">Wenn Sie diese Eigenschaft auf **Variant \_ true** festlegen, müssen Sie auch eine maximale decoderwartezeit angeben, indem Sie die Eigenschaft " [**mfpkey \_ maxdeclatencyms**](mfpkey-maxdeclatencymsproperty.md) " festlegen.</span><span class="sxs-lookup"><span data-stu-id="82da7-113">If you set this property to **VARIANT\_TRUE**, you must also specify a maximum decoder latency by setting the [**MFPKEY\_MAXDECLATENCYMS**](mfpkey-maxdeclatencymsproperty.md) property.</span></span> <span data-ttu-id="82da7-114">In diesem Fall erstellt der Encoder Modi, die die Latenz Anforderung erfüllen, und listet nur diese Modi auf.</span><span class="sxs-lookup"><span data-stu-id="82da7-114">In that case, the encoder creates modes that satisfy the latency requirement and enumerates only those modes.</span></span> <span data-ttu-id="82da7-115">Der Encoder stellt sicher, dass die vorab Anforderungen (Decoder-Puffergröße) kleiner oder gleich **mfpkey \_ maxdeclatencyms** sind.</span><span class="sxs-lookup"><span data-stu-id="82da7-115">The encoder ensures that the preroll requirements (decoder buffer size) are less than or equal to **MFPKEY\_MAXDECLATENCYMS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="82da7-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82da7-116">Requirements</span></span>



| <span data-ttu-id="82da7-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82da7-117">Requirement</span></span> | <span data-ttu-id="82da7-118">Wert</span><span class="sxs-lookup"><span data-stu-id="82da7-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82da7-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82da7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="82da7-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82da7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="82da7-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82da7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="82da7-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82da7-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="82da7-123">Header</span><span class="sxs-lookup"><span data-stu-id="82da7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="82da7-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="82da7-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82da7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82da7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82da7-126">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="82da7-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
