---
description: Gibt die vom Autor bereitgestellten Fold-Koeffizienten für das Decodieren von Multichannel-Audiodaten für weniger Kanäle an, als der codierte Stream enthält.
ms.assetid: f6737c05-4b39-4209-9985-9402b28cf316
title: MFPKEY_WMADEC_FOLDDOWN_MATRIX-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92cb2495863d319c7f755d7d72f475ccf1eda75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356848"
---
# <a name="mfpkey_wmadec_folddown_matrix-property"></a><span data-ttu-id="57aab-103">Eigenschaft "mfpkey \_ wmadec- \_ FoldDown- \_ Matrix"</span><span class="sxs-lookup"><span data-stu-id="57aab-103">MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX Property</span></span>

<span data-ttu-id="57aab-104">Gibt die vom Autor bereitgestellten Fold-Koeffizienten für das Decodieren von Multichannel-Audiodaten für weniger Kanäle an, als der codierte Stream enthält.</span><span class="sxs-lookup"><span data-stu-id="57aab-104">Specifies the author-supplied fold-down coefficients for decoding multichannel audio for fewer channels than the encoded stream contains.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="57aab-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="57aab-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="57aab-106">g \_ wszwmacfolddownxychannels</span><span class="sxs-lookup"><span data-stu-id="57aab-106">g\_wszWMACFoldDownXToYChannels</span></span>

<span data-ttu-id="57aab-107">g \_ wszwmacfoldxychannelsz</span><span class="sxs-lookup"><span data-stu-id="57aab-107">g\_wszWMACFoldXToYChannelsZ</span></span>

## <a name="data-type"></a><span data-ttu-id="57aab-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="57aab-108">Data Type</span></span>

<span data-ttu-id="57aab-109">**VT \_ array \| VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="57aab-109">**VT\_ARRAY \| VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="57aab-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57aab-110">Remarks</span></span>

<span data-ttu-id="57aab-111">Ein Audiodecoder kann als DirectX-Medienobjekt (DMO) oder als Media Foundation Transformation (MFT) fungieren.</span><span class="sxs-lookup"><span data-stu-id="57aab-111">An audio decoder can act as a DirectX Media Object (DMO) or as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="57aab-112">Informationen darüber, wann ein Decoder als DMO oder MFT fungiert, finden Sie auf den einzelnen Codec-Referenzseiten unter [Codec-Objekte](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="57aab-112">For information on when a decoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="57aab-113">Wenn Sie einen Decoder als DMO verwenden, kann der Decoder den Kanal durchlaufen, und Sie können durch Aufrufen von [**imediaobject:: getoutputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)Ausgabemedien Typen aufklappen.</span><span class="sxs-lookup"><span data-stu-id="57aab-113">When you use a decoder as a DMO, the decoder can perform channel fold down, and you can enumerate folded down output media types by calling [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span></span>

<span data-ttu-id="57aab-114">Wenn Sie einen Decoder als MFT verwenden, führt der Decoder standardmäßig keine abklappvorgänge aus und bietet keine Ausgabemedien Typen mit einem Fold-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="57aab-114">When you use a decoder as an MFT, the decoder by default will not perform any fold down, and will not offer folded down output media types.</span></span> <span data-ttu-id="57aab-115">Ein Decoder, der als MFT fungiert, führt die Faltung nur dann durch, wenn benutzerdefinierte Fold-Koeffizienten mithilfe der Eigenschaft **mfpkey \_ wmadec- \_ FoldDown- \_ Matrix** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="57aab-115">A decoder acting as an MFT will perform fold down only if custom fold-down coefficients are set using the **MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX** property.</span></span>

<span data-ttu-id="57aab-116">Wenn die **mfpkey \_ wmadec- \_ \_ Matrix** Eigenschaft nicht auf dem Audiodecoder-MFT festgelegt ist und Sie ein Fold ausführen möchten, können Sie (als MFT) den audioresampler Digital Signal Processor verwenden.</span><span class="sxs-lookup"><span data-stu-id="57aab-116">If the **MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX** property is not set on the audio decoder MFT, and you want to perform a fold down, you can use (as an MFT) the Audio Resampler digital signal processor.</span></span>

<span data-ttu-id="57aab-117">Der Wert für diese Eigenschaft ist eine Zeichenfolge, die in einer durch Trennzeichen getrennten Liste von ganzzahligen Werten in einer durch Trennzeichen getrennten Liste mit separaten Werten.</span><span class="sxs-lookup"><span data-stu-id="57aab-117">The value for this property is a string containing fold-down coefficients in a comma-separated list of integer values.</span></span> <span data-ttu-id="57aab-118">Die Liste muss eine Reihe von ganzen Zahlen für jeden Kanal im codierten Inhalt enthalten, der der Anzahl der Kanäle im decodierten Inhalt entspricht.</span><span class="sxs-lookup"><span data-stu-id="57aab-118">The list must contain a number of integers for each channel in the encoded content equal to the number of channels in the decoded content.</span></span>

<span data-ttu-id="57aab-119">Wenn der Koeffizient NULL ist, muss der Wert, der in der Zeichenfolge verwendet werden soll, "-2147483648" lauten; andernfalls wird der Wert mit der Gleichung berechnet: 20 \* 65536 \* log10 (x).</span><span class="sxs-lookup"><span data-stu-id="57aab-119">If the coefficient is zero, the value to be used in the string must be "-2147483648";otherwise the value is computed using the equation: 20 \* 65536 \* log10(x).</span></span>

<span data-ttu-id="57aab-120">Koeffizienten werden in der Reihenfolge der Kanalmasken aufgeführt, wie von den channelmasken Konstanten definiert, die in der Header Datei "mmreg. h" enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="57aab-120">Coefficients are listed in channel mask order, as defined by the channel mask constants that are included in the mmreg.h header file.</span></span> <span data-ttu-id="57aab-121">Daher stellen die ersten beiden Werte in einer 6-zu-2-Kanal-Faltung die Teile des linken Ausgabe Kanals und den rechten Ausgabekanal dar, die aus dem linken Mitte-Kanal im 6-kanalstream bestehen.</span><span class="sxs-lookup"><span data-stu-id="57aab-121">Therefore, the first two values in a 6-to-2 channel fold-down represent the portions of the left output channel and the right output channel that are made up of the center left channel in the 6 channel stream.</span></span>

<span data-ttu-id="57aab-122">Diese Eigenschaft sollte nur festgelegt werden, wenn vom Autor angegebene Fold-Werte mit dem codierten Inhalt persistent gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="57aab-122">You should set this property only if author-supplied fold-down values are persisted with the encoded content.</span></span> <span data-ttu-id="57aab-123">Andernfalls kann der Decoder seine eigenen Berechnungen durchführen lassen.</span><span class="sxs-lookup"><span data-stu-id="57aab-123">Otherwise, let the decoder make its own calculations.</span></span>

<span data-ttu-id="57aab-124">Der Windows Media Audio 10 Professional-Codec unterstützt zurzeit nur die Aufteilung auf zwei Kanäle.</span><span class="sxs-lookup"><span data-stu-id="57aab-124">The Windows Media Audio 10 Professional codec currently only supports fold-down to two channels.</span></span>

<span data-ttu-id="57aab-125">Wenn die Eigenschaft [mfpkey \_ wmadec \_ spkrcfg](mfpkey-wmadec-spkrcfgproperty.md) auf **dsspeaker- \_ umschließen** festgelegt ist, ignoriert der Codec vom Autor bereitgestellte Fold-und-Zeichen, die vom Matrix Decoder des Empfängers verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="57aab-125">If the [MFPKEY\_WMADEC\_SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) property is set to **DSSPEAKER\_SURROUND**, the codec will ignore author-supplied fold-down coefficients and fold down to a 2-channel signal that can be processed by the matrix decoder of the receiver.</span></span> <span data-ttu-id="57aab-126">Dadurch können umschließende Geräte vier Kanäle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="57aab-126">This enables surround equipment to deliver four channels.</span></span> <span data-ttu-id="57aab-127">Dieser Modus wird nur unterstützt, wenn die Quelle 5,1 ist.</span><span class="sxs-lookup"><span data-stu-id="57aab-127">This mode is supported only if the source is 5.1.</span></span> <span data-ttu-id="57aab-128">Der Codec kann nur acht Kanäle in zwei Kanäle Falten.</span><span class="sxs-lookup"><span data-stu-id="57aab-128">The codec can only fold 8 channels to 2 channels.</span></span>

## <a name="requirements"></a><span data-ttu-id="57aab-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57aab-129">Requirements</span></span>



| <span data-ttu-id="57aab-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57aab-130">Requirement</span></span> | <span data-ttu-id="57aab-131">Wert</span><span class="sxs-lookup"><span data-stu-id="57aab-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57aab-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57aab-132">Minimum supported client</span></span><br/> | <span data-ttu-id="57aab-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57aab-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="57aab-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57aab-134">Minimum supported server</span></span><br/> | <span data-ttu-id="57aab-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57aab-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="57aab-136">Header</span><span class="sxs-lookup"><span data-stu-id="57aab-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="57aab-137"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="57aab-137"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57aab-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57aab-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57aab-139">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="57aab-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
