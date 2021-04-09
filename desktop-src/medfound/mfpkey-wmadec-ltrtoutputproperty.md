---
description: Gibt an, ob der Decoder Lt-Rt-Fold ausführen soll.
ms.assetid: ce1dc4ea-4326-40ab-bb30-ff1a34f06d79
title: MFPKEY_WMADEC_LTRTOUTPUT-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f4a83d2529ce3b37282be35924b48288d4df45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130541"
---
# <a name="mfpkey_wmadec_ltrtoutput-property"></a><span data-ttu-id="90ef7-103">Mfpkey \_ wmadec \_ ltrtoutput (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="90ef7-103">MFPKEY\_WMADEC\_LTRTOUTPUT Property</span></span>

<span data-ttu-id="90ef7-104">Gibt an, ob der Decoder Lt-Rt-Fold ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="90ef7-104">Specifies whether the decoder should perform Lt-Rt fold down.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="90ef7-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="90ef7-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="90ef7-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="90ef7-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="90ef7-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="90ef7-107">Data Type</span></span>

<span data-ttu-id="90ef7-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="90ef7-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="90ef7-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="90ef7-109">Default Value</span></span>

<span data-ttu-id="90ef7-110">**Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="90ef7-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="90ef7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90ef7-111">Remarks</span></span>

<span data-ttu-id="90ef7-112">Wenn diese Eigenschaft den Wert Variant false aufweist \_ und die Ausgabe Stereo ist, verwendet der Audiodecoder die einfache kanaldown-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="90ef7-112">If this property has a value of VARIANT\_FALSE and the output is stereo, the audio decoder uses simple channel fold down.</span></span> <span data-ttu-id="90ef7-113">Wenn für diese Eigenschaft der Wert Variant \_ true festgelegt ist, führt der Audiodecoder Lt-Rt (matrixt) Fold (matrixt) in Stereo aus, und anschließend kann ein beliebiger Dolby Surround-Decoder zum Decodieren der matriten umschließenden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90ef7-113">If this property has a value of VARIANT\_TRUE, the audio decoder performs Lt-Rt (matrixed) fold down to stereo, and then any Dolby Surround decoder can be used to decode the matrixed surround .</span></span> <span data-ttu-id="90ef7-114">Der Audiodecoder könnte z. b. Lt-Rt für den Inhalt von 5,1 oder 7,1 ausführen.</span><span class="sxs-lookup"><span data-stu-id="90ef7-114">For example, the audio decoder could perform Lt-Rt fold down on 5.1 or 7.1 content.</span></span>

<span data-ttu-id="90ef7-115">Diese Eigenschaft wird nur unterstützt, wenn der Decoder als DirectX-Medienobjekt (DMO) fungiert.</span><span class="sxs-lookup"><span data-stu-id="90ef7-115">This property is supported only when the decoder is acting as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="90ef7-116">Wenn der Decoder als Media Foundation Transformation (MFT) fungiert, wird kein Fold unterstützt.</span><span class="sxs-lookup"><span data-stu-id="90ef7-116">No fold down of any kind is supported when the decoder is acting as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="90ef7-117">Wenn Sie unter Windows Vista eine **IPropertyStore** -Schnittstelle für einen Audiodecoder erhalten, fungiert der Decoder als MFT.</span><span class="sxs-lookup"><span data-stu-id="90ef7-117">On Windows Vista, if you obtain an **IPropertyStore** interface on an audio decoder, the decoder acts as an MFT.</span></span> <span data-ttu-id="90ef7-118">Folglich kann diese Eigenschaft nicht unter Windows Vista verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90ef7-118">Consequently, this property cannot be used on Windows Vista.</span></span> <span data-ttu-id="90ef7-119">Informationen darüber, wann ein Decoder als DMO oder MFT fungiert, finden Sie auf den einzelnen Codec-Referenzseiten unter [Codec-Objekte](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="90ef7-119">For information on when a decoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90ef7-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90ef7-120">Requirements</span></span>



| <span data-ttu-id="90ef7-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90ef7-121">Requirement</span></span> | <span data-ttu-id="90ef7-122">Wert</span><span class="sxs-lookup"><span data-stu-id="90ef7-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90ef7-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90ef7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="90ef7-124">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90ef7-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="90ef7-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90ef7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="90ef7-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90ef7-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="90ef7-127">Header</span><span class="sxs-lookup"><span data-stu-id="90ef7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="90ef7-128"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="90ef7-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90ef7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90ef7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90ef7-130">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="90ef7-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
