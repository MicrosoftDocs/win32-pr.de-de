---
description: Gibt die Inhalts Teile an, die vom Voice-Codec als Musik codiert werden sollen.
ms.assetid: c63034ce-33d7-4f2f-9498-fc16e25b6d4d
title: MFPKEY_WMAVOICE_ENC_EDL-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f3ac85ebd3a0542fbcf6554205d0b2f2623957c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755305"
---
# <a name="mfpkey_wmavoice_enc_edl-property"></a><span data-ttu-id="89c13-103">Mfpkey \_ wmavoice \_ ENC \_ EDL (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="89c13-103">MFPKEY\_WMAVOICE\_ENC\_EDL Property</span></span>

<span data-ttu-id="89c13-104">Gibt die Inhalts Teile an, die vom Voice-Codec als Musik codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="89c13-104">Specifies the portions of content to be encoded as music by the voice codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="89c13-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="89c13-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="89c13-106">g \_ wszwmacvoicebuffer</span><span class="sxs-lookup"><span data-stu-id="89c13-106">g\_wszWMACVoiceBuffer</span></span>

## <a name="data-type"></a><span data-ttu-id="89c13-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="89c13-107">Data Type</span></span>

<span data-ttu-id="89c13-108">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="89c13-108">VT\_BSTR</span></span>

## <a name="default-value"></a><span data-ttu-id="89c13-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="89c13-109">Default Value</span></span>

<span data-ttu-id="89c13-110">Für dieses Feld gibt es keinen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="89c13-110">No default value.</span></span> <span data-ttu-id="89c13-111">Wenn diese Eigenschaft nicht festgelegt ist, verwendet der Codec den Wert der Eigenschaft [mfpkey \_ wmavoice \_ ENC \_ musicvoiceclassmode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) , um zu bestimmen, wie der Inhalt codiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="89c13-111">If this property is not set, the codec will use the value of the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property to determine how to encode the content.</span></span>

## <a name="remarks"></a><span data-ttu-id="89c13-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89c13-112">Remarks</span></span>

<span data-ttu-id="89c13-113">Sie können diese Eigenschaft verwenden, wenn der automatische Modus des Codecs keine zufriedenstellenden Ergebnisse liefert.</span><span class="sxs-lookup"><span data-stu-id="89c13-113">You can use this property if the automatic mode of the codec is not giving satisfactory results.</span></span>

<span data-ttu-id="89c13-114">Dieser Wert ist eine durch Trennzeichen getrennte Zeichenfolge, die mindestens vier ganze Zahlen enthält.</span><span class="sxs-lookup"><span data-stu-id="89c13-114">This value is a comma-delimited string containing at least four integers.</span></span> <span data-ttu-id="89c13-115">Die erste ganze Zahl ist die Versionsnummer. Verwenden Sie für diesen Wert immer 1.</span><span class="sxs-lookup"><span data-stu-id="89c13-115">The first integer is the version number; always use 1 for this value.</span></span> <span data-ttu-id="89c13-116">Die zweite Ganzzahl ist die Anzahl der Abschnitte, die als Musik codiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="89c13-116">The second integer is the number of sections that need to be encoded as music.</span></span> <span data-ttu-id="89c13-117">Die zweite Ganzzahl ist eine Reihe von Werten, die Bereiche in Millisekunden darstellen, ein paar für jeden Inhalts Abschnitt, der als Musik codiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="89c13-117">Following the second integer are a number of pairs of values representing ranges in milliseconds, one pair for each section of content that needs to be encoded as music.</span></span>

<span data-ttu-id="89c13-118">"1, 2100200500600" informiert den Encoder beispielsweise über die Verwendung von Version 1 mit 2 Teilen der Musik.</span><span class="sxs-lookup"><span data-stu-id="89c13-118">For example, "1,2,100,200,500,600" informs the encoder to use version 1 with 2 sections of music.</span></span> <span data-ttu-id="89c13-119">Der erste Musik Abschnitt beginnt bei 100 MS und endet um 200 ms.</span><span class="sxs-lookup"><span data-stu-id="89c13-119">The first music section starts at 100 ms and ends at 200 ms.</span></span> <span data-ttu-id="89c13-120">Der zweite Musik Abschnitt beginnt bei 500 ms und endet um 600 ms.</span><span class="sxs-lookup"><span data-stu-id="89c13-120">The second music section starts at 500 ms and ends at 600 ms.</span></span>

## <a name="requirements"></a><span data-ttu-id="89c13-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89c13-121">Requirements</span></span>



| <span data-ttu-id="89c13-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89c13-122">Requirement</span></span> | <span data-ttu-id="89c13-123">Wert</span><span class="sxs-lookup"><span data-stu-id="89c13-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89c13-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89c13-124">Minimum supported client</span></span><br/> | <span data-ttu-id="89c13-125">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89c13-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="89c13-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89c13-126">Minimum supported server</span></span><br/> | <span data-ttu-id="89c13-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89c13-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="89c13-128">Header</span><span class="sxs-lookup"><span data-stu-id="89c13-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="89c13-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="89c13-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89c13-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89c13-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89c13-131">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="89c13-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




