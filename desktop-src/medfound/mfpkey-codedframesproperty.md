---
description: Gibt die Anzahl der vom Codec codierten Videorahmen an.
ms.assetid: 4a812609-137f-4f7f-aa55-89e26d7f1972
title: MFPKEY_CODEDFRAMES-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708bb6c200701cdf48fa8407108be2161fdb4f61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373127"
---
# <a name="mfpkey_codedframes-property"></a><span data-ttu-id="ed291-103">Mfpkey- \_ codedframes (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ed291-103">MFPKEY\_CODEDFRAMES Property</span></span>

<span data-ttu-id="ed291-104">Gibt die Anzahl der vom Codec codierten Videorahmen an.</span><span class="sxs-lookup"><span data-stu-id="ed291-104">Specifies the number of video frames encoded by the codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ed291-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ed291-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ed291-106">g \_ wszwmvccodedframes</span><span class="sxs-lookup"><span data-stu-id="ed291-106">g\_wszWMVCCodedFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="ed291-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ed291-107">Data Type</span></span>

<span data-ttu-id="ed291-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ed291-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="ed291-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed291-109">Remarks</span></span>

<span data-ttu-id="ed291-110">Dieser Wert ist gleich [mfpkey \_ totalFrames](mfpkey-totalframesproperty.md) abzüglich aller Frames, die aufgrund von Bitraten Einschränkungen gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="ed291-110">This value is equal to [MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) minus any frames that were dropped due to bit-rate constraints.</span></span> <span data-ttu-id="ed291-111">Sie können diesen Wert erhalten, nachdem Sie die Übergabe von Beispielen abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="ed291-111">You can get this value after you are finished passing samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed291-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed291-112">Requirements</span></span>



| <span data-ttu-id="ed291-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed291-113">Requirement</span></span> | <span data-ttu-id="ed291-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ed291-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed291-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed291-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ed291-116">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed291-116">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ed291-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed291-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ed291-118">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed291-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ed291-119">Header</span><span class="sxs-lookup"><span data-stu-id="ed291-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed291-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed291-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed291-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed291-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed291-122">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ed291-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




