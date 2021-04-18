---
description: Diese Eigenschaft fragt den Decoder nach der maximalen voll Bild Rate ab, die der Decoder unterstützt. Der Datentyp für diese Eigenschaft ist eine "am \_ queryrate"-Struktur.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: AM_RATE_QueryFullFrameRate-Eigenschaft (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2c99564caa09253198b101a3e2467ec88c7e34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371427"
---
# <a name="am_rate_queryfullframerate-property"></a><span data-ttu-id="2ad86-104">Der \_ Rate der \_ queryfullframerate-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2ad86-104">AM\_RATE\_QueryFullFrameRate Property</span></span>

<span data-ttu-id="2ad86-105">Diese Eigenschaft fragt den Decoder nach der maximalen voll Bild Rate ab, die der Decoder unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2ad86-105">This property queries the decoder for the maximum full-frame rate that the decoder supports.</span></span> <span data-ttu-id="2ad86-106">Der Datentyp für diese Eigenschaft ist eine " **am \_ queryrate** "-Struktur.</span><span class="sxs-lookup"><span data-stu-id="2ad86-106">The data type for this property is an **AM\_QueryRate** structure.</span></span>

<span data-ttu-id="2ad86-107">Diese Eigenschaft ist für die Version 1,1 dieser Eigenschaften Gruppe definiert. Weitere Informationen finden Sie unter [**\_ Rate \_ userateversion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="2ad86-107">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



|                   |                                       |
|-------------------|---------------------------------------|
| <span data-ttu-id="2ad86-108">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="2ad86-108">Property Set GUID</span></span> | <span data-ttu-id="2ad86-109">AM \_ kspropltid \_</span><span class="sxs-lookup"><span data-stu-id="2ad86-109">AM\_KSPROPSETID\_TSRateChange</span></span>         |
| <span data-ttu-id="2ad86-110">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="2ad86-110">Property ID</span></span>       | <span data-ttu-id="2ad86-111">Der \_ Rate der \_ queryfullframerate-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2ad86-111">AM\_RATE\_QueryFullFrameRate Property</span></span> |
| <span data-ttu-id="2ad86-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2ad86-112">Data Type</span></span>         | [<span data-ttu-id="2ad86-113">**AM- \_ querytrate**</span><span class="sxs-lookup"><span data-stu-id="2ad86-113">**AM\_QueryRate**</span></span>](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a><span data-ttu-id="2ad86-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ad86-114">Remarks</span></span>

<span data-ttu-id="2ad86-115">Wenn die Wiedergabe Rate die maximale Rate des Decoders überschreitet, sendet der Quell Filter Gruppen von kontinuierlichen Samplings, die durch Diskontinuitäten getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="2ad86-115">If the playback rate exceeds the decoder's maximum rate, the source filter sends groups of continuous samples separated by discontinuities.</span></span> <span data-ttu-id="2ad86-116">Die Zeitstempel überspringen die Diskontinuitäten.</span><span class="sxs-lookup"><span data-stu-id="2ad86-116">The time stamps jump across the discontinuities.</span></span> <span data-ttu-id="2ad86-117">Der Quell Filter kann dies auch dann tun, wenn die Wiedergabe Rate innerhalb der maximalen Rate des Decoders liegt, da es möglicherweise andere Faktoren gibt, wie z. b. Datenträger-e/a, die die vollständige Wiedergabe Rate einschränken.</span><span class="sxs-lookup"><span data-stu-id="2ad86-117">The source filter might do this even if the playback rate is within the decoder's maximum rate, because there may be other factors, such as disk IO, that limit the full playback rate.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ad86-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ad86-118">Requirements</span></span>



| <span data-ttu-id="2ad86-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ad86-119">Requirement</span></span> | <span data-ttu-id="2ad86-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2ad86-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ad86-121">Header</span><span class="sxs-lookup"><span data-stu-id="2ad86-121">Header</span></span><br/> | <dl> <span data-ttu-id="2ad86-122"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ad86-122"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ad86-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ad86-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ad86-124">**Eigenschaften Satz für Raten Änderung**</span><span class="sxs-lookup"><span data-stu-id="2ad86-124">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




