---
description: Gibt die Anzahl der Videorahmen an, die übersprungen werden, da Sie Duplikate vorheriger Frames waren.
ms.assetid: ef4aa5a0-3788-493e-b541-c3a24509d939
title: MFPKEY_ZEROBYTEFRAMES-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffcf29d099b3a3fb27a307e970af7af1a5c3d58b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863432"
---
# <a name="mfpkey_zerobyteframes-property"></a><span data-ttu-id="25cf9-103">Mfpkey \_ zerobyteframes (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="25cf9-103">MFPKEY\_ZEROBYTEFRAMES Property</span></span>

<span data-ttu-id="25cf9-104">Gibt die Anzahl der Videorahmen an, die übersprungen werden, da Sie Duplikate vorheriger Frames waren.</span><span class="sxs-lookup"><span data-stu-id="25cf9-104">Specifies the number of video frames that are skipped because they were duplicates of previous frames.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="25cf9-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="25cf9-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="25cf9-106">g \_ wszwmvczerobyteframes</span><span class="sxs-lookup"><span data-stu-id="25cf9-106">g\_wszWMVCZeroByteFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="25cf9-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="25cf9-107">Data Type</span></span>

<span data-ttu-id="25cf9-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="25cf9-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="25cf9-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25cf9-109">Remarks</span></span>

<span data-ttu-id="25cf9-110">Der Wert wird nicht von der Gesamtzahl der übergebenen Frames ([mfpkey \_ totalFrames](mfpkey-totalframesproperty.md)) abgezogen, wenn die Anzahl der codierten Frames ([mfpkey \_ codedframes](mfpkey-codedframesproperty.md)) berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="25cf9-110">This value is not subtracted from the total number of frames passed ([MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md)) when calculating the number of encoded frames ([MFPKEY\_CODEDFRAMES](mfpkey-codedframesproperty.md)).</span></span>

<span data-ttu-id="25cf9-111">Sie können den Codec daran hindern, doppelte Frames zu überspringen, indem Sie [mfpkey \_ producedummyframes](mfpkey-producedummyframesproperty.md) auf Variant \_ true festlegen.</span><span class="sxs-lookup"><span data-stu-id="25cf9-111">You can stop the codec from skipping duplicate frames by setting [MFPKEY\_PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) to VARIANT\_TRUE.</span></span>

<span data-ttu-id="25cf9-112">Sie können diesen Wert erhalten, nachdem Sie die Übergabe von Beispielen abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="25cf9-112">You can get this value after you are finished passing samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="25cf9-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25cf9-113">Requirements</span></span>



| <span data-ttu-id="25cf9-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25cf9-114">Requirement</span></span> | <span data-ttu-id="25cf9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="25cf9-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25cf9-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25cf9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="25cf9-117">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25cf9-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="25cf9-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25cf9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="25cf9-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25cf9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="25cf9-120">Header</span><span class="sxs-lookup"><span data-stu-id="25cf9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="25cf9-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="25cf9-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25cf9-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25cf9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25cf9-123">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="25cf9-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




