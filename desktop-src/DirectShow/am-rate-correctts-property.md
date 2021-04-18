---
description: Der DVD-Navigator verwendet diese Eigenschaft, um den Decoder darüber zu informieren, dass der Navigator die richtigen Zeitstempel für die Stichproben festlegt, die er an den Decoder übergibt.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: AM_RATE_CorrectTS-Eigenschaft (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa410b079d3de63de364662c7d5465c82814d24a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371428"
---
# <a name="am_rate_correctts-property"></a><span data-ttu-id="b69ba-103">\_Eigenschaft für Raten \_ Korrekturen</span><span class="sxs-lookup"><span data-stu-id="b69ba-103">AM\_RATE\_CorrectTS Property</span></span>

<span data-ttu-id="b69ba-104">Der DVD-Navigator verwendet diese Eigenschaft, um den Decoder darüber zu informieren, dass der Navigator die richtigen Zeitstempel für die Stichproben festlegt, die er an den Decoder übergibt.</span><span class="sxs-lookup"><span data-stu-id="b69ba-104">The DVD Navigator uses this property to inform the decoder that the Navigator is setting the correct time stamps on the samples it delivers to the decoder.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="b69ba-105">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="b69ba-105">Property Set GUID</span></span> | <span data-ttu-id="b69ba-106">AM \_ kspropltid \_</span><span class="sxs-lookup"><span data-stu-id="b69ba-106">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="b69ba-107">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="b69ba-107">Property ID</span></span>       | <span data-ttu-id="b69ba-108">Bei \_ Raten \_ Korrekturen</span><span class="sxs-lookup"><span data-stu-id="b69ba-108">AM\_RATE\_CorrectTS</span></span>           |
| <span data-ttu-id="b69ba-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b69ba-109">Data Type</span></span>         | <span data-ttu-id="b69ba-110">**LONG**</span><span class="sxs-lookup"><span data-stu-id="b69ba-110">**LONG**</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="b69ba-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b69ba-111">Remarks</span></span>

<span data-ttu-id="b69ba-112">Frühere Versionen des DVD-Navigators haben nicht die richtigen Zeitstempel festgelegt, als die Wiedergabe Rate etwas anderes als 1,0 war.</span><span class="sxs-lookup"><span data-stu-id="b69ba-112">Earlier versions of the DVD Navigator did not set the correct time stamps when the playback rate was something other than 1.0.</span></span> <span data-ttu-id="b69ba-113">Viele Decoder umgehen dieses Problem, indem Sie die Zeitstempel beim Zurückspulen oder schnell vorwärts ignorieren und die richtigen Präsentations Zeiten schätzen.</span><span class="sxs-lookup"><span data-stu-id="b69ba-113">Many decoders work around this problem by ignoring the time stamps during rewind or fast forward, and estimating the correct presentation times.</span></span>

<span data-ttu-id="b69ba-114">Diese Probleme wurden in der aktuellen Version des DVD-Navigators korrigiert.</span><span class="sxs-lookup"><span data-stu-id="b69ba-114">These problems have been corrected in the current version of the DVD Navigator.</span></span> <span data-ttu-id="b69ba-115">Aus Gründen der Abwärtskompatibilität mit vorhandenen Decodern zeigt der DVD-Navigator an, dass die Zeitstempel korrekt sind, indem die \_ \_ Eigenschaft für die Wert Korrektur für den Decoder mit dem Wert **true** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b69ba-115">For backward compatibility with existing decoders, the DVD Navigator indicates that the time stamps are correct by setting the AM\_RATE\_CorrectTS property on the decoder with the value **TRUE**.</span></span> <span data-ttu-id="b69ba-116">Wenn diese Eigenschaft festgelegt ist, sollte der Decoder die tatsächlichen Zeitstempel verwenden, anstatt die Präsentations Zeiten zu schätzen.</span><span class="sxs-lookup"><span data-stu-id="b69ba-116">When this property is set, the decoder should use the actual time stamps, instead of estimating the presentation times.</span></span>

## <a name="requirements"></a><span data-ttu-id="b69ba-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b69ba-117">Requirements</span></span>



| <span data-ttu-id="b69ba-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b69ba-118">Requirement</span></span> | <span data-ttu-id="b69ba-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b69ba-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b69ba-120">Header</span><span class="sxs-lookup"><span data-stu-id="b69ba-120">Header</span></span><br/> | <dl> <span data-ttu-id="b69ba-121"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="b69ba-121"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b69ba-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b69ba-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b69ba-123">**Eigenschaften Satz für Raten Änderung**</span><span class="sxs-lookup"><span data-stu-id="b69ba-123">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




