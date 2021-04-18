---
description: Gibt den Modus des voicecodec an.
ms.assetid: 8425cdab-e43c-41ca-9c20-09ab6a5f06f4
title: MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9776c76f2a8863afe73626f5a2940de2c0ccb7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345204"
---
# <a name="mfpkey_wmavoice_enc_musicspeechclassmode-property"></a><span data-ttu-id="05de2-103">Mfpkey \_ wmavoice \_ ENC \_ musicvoiceclassmode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="05de2-103">MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode Property</span></span>

<span data-ttu-id="05de2-104">Gibt den Modus des voicecodec an.</span><span class="sxs-lookup"><span data-stu-id="05de2-104">Specifies the mode of the voice codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="05de2-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="05de2-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="05de2-106">g \_ wszwmacmusicredner classmode</span><span class="sxs-lookup"><span data-stu-id="05de2-106">g\_wszWMACMusicSpeechClassMode</span></span>

## <a name="data-type"></a><span data-ttu-id="05de2-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="05de2-107">Data Type</span></span>

<span data-ttu-id="05de2-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="05de2-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="05de2-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="05de2-109">Default Value</span></span>

<span data-ttu-id="05de2-110">1</span><span class="sxs-lookup"><span data-stu-id="05de2-110">1</span></span>

## <a name="remarks"></a><span data-ttu-id="05de2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05de2-111">Remarks</span></span>

<span data-ttu-id="05de2-112">Mit dem Wert 1 wird dem Codec mitgeteilt, dass der Inhalt sprach geschützt ist, bei einem Wert von 2 der Codec den Modus automatisch bestimmt, und jeder andere Wert informiert den Codec über die Verwendung des Musik Modus.</span><span class="sxs-lookup"><span data-stu-id="05de2-112">A value of 1 informs the codec that the content is voice-only, a value of 2 has the codec determine the mode automatically, and any other value informs the codec to use music mode.</span></span>

<span data-ttu-id="05de2-113">Wenn der automatische Modus gemischte Sprache und Musik nicht ordnungsgemäß codiert, können Sie mithilfe der Eigenschaft [mfpkey \_ wmavoice \_ ENC \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) die Codierung für einzelne Abschnitte der Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="05de2-113">If automatic mode is not encoding mixed voice and music properly, you can specify encoding for individual sections of the file by using the [MFPKEY\_WMAVOICE\_ENC\_EDL](mfpkey-wmavoice-enc-edlproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="05de2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05de2-114">Requirements</span></span>



| <span data-ttu-id="05de2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05de2-115">Requirement</span></span> | <span data-ttu-id="05de2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="05de2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05de2-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05de2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="05de2-118">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05de2-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="05de2-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05de2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="05de2-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05de2-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="05de2-121">Header</span><span class="sxs-lookup"><span data-stu-id="05de2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="05de2-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="05de2-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05de2-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05de2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05de2-124">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05de2-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




