---
description: Gibt an, ob der codierte videobit-Stream einen Puffer Füllwert mit jedem Keyframe enthält.
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: MFPKEY_BUFFERFULLNESSINFIRSTBYTE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fbcdb6306faeb7481f1cc7be20088ff0cedd5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350922"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a><span data-ttu-id="12ce9-103">Mfpkey \_ bufferfullnessinfirstbyte (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="12ce9-103">MFPKEY\_BUFFERFULLNESSINFIRSTBYTE Property</span></span>

<span data-ttu-id="12ce9-104">Gibt an, ob der codierte videobit-Stream einen Puffer Füllwert mit jedem Keyframe enthält.</span><span class="sxs-lookup"><span data-stu-id="12ce9-104">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="12ce9-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="12ce9-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="12ce9-106">g \_ wszwmvcbufferfullnessinfirstbyte</span><span class="sxs-lookup"><span data-stu-id="12ce9-106">g\_wszWMVCBufferFullnessInFirstByte</span></span>

## <a name="data-type"></a><span data-ttu-id="12ce9-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="12ce9-107">Data Type</span></span>

<span data-ttu-id="12ce9-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="12ce9-108">VT\_BOOL</span></span>

## <a name="remarks"></a><span data-ttu-id="12ce9-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12ce9-109">Remarks</span></span>

<span data-ttu-id="12ce9-110">Sie müssen einen Ausgabetyp festlegen, bevor Sie diesen Wert erhalten.</span><span class="sxs-lookup"><span data-stu-id="12ce9-110">You must set an output type before getting this value.</span></span>

<span data-ttu-id="12ce9-111">Sie können den Wert dieser Eigenschaft mithilfe von [iwmcodecprop:: getcodecprop](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop)erhalten.</span><span class="sxs-lookup"><span data-stu-id="12ce9-111">You can get the value of this property using [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span></span> <span data-ttu-id="12ce9-112">Wenn Sie **IPropertyBag** verwenden, müssen Sie zuerst den FourCC-Wert des gewünschten komprimierten Formats mit der Eigenschaft " [mfpkey \_ FourCC](mfpkey-fourccproperty.md) " festlegen.</span><span class="sxs-lookup"><span data-stu-id="12ce9-112">If you use **IPropertyBag**, you must first set the FOURCC value of the desired compressed format with the [MFPKEY\_FOURCC](mfpkey-fourccproperty.md) property.</span></span>

<span data-ttu-id="12ce9-113">Wenn Sie die Puffergröße im ersten Byte aller Keyframes haben, können Sie die erforderliche Puffergröße beim Verketten komprimierter Videostreams ermitteln.</span><span class="sxs-lookup"><span data-stu-id="12ce9-113">Having the buffer fullness in the first byte of all key frames enables you to determine the buffer size required when concatenating compressed video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="12ce9-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12ce9-114">Requirements</span></span>



| <span data-ttu-id="12ce9-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12ce9-115">Requirement</span></span> | <span data-ttu-id="12ce9-116">Wert</span><span class="sxs-lookup"><span data-stu-id="12ce9-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12ce9-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12ce9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="12ce9-118">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12ce9-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="12ce9-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12ce9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="12ce9-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12ce9-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="12ce9-121">Header</span><span class="sxs-lookup"><span data-stu-id="12ce9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="12ce9-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="12ce9-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12ce9-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12ce9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12ce9-124">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="12ce9-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




