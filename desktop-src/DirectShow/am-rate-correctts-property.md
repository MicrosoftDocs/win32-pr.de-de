---
description: Der DVD-Navigator verwendet diese Eigenschaft, um den Decoder darüber zu informieren, dass der Navigator die richtigen Zeitstempel für die Samplings festlegt, die er an den Decoder übermittelt.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: AM_RATE_CorrectTS-Eigenschaft (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c65b613f892708dc210af2ca2a05efb74785fb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910298"
---
# <a name="am_rate_correctts-property"></a><span data-ttu-id="71bbd-103">AM \_ RATE \_ CorrectTS-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="71bbd-103">AM\_RATE\_CorrectTS Property</span></span>

<span data-ttu-id="71bbd-104">Der DVD-Navigator verwendet diese Eigenschaft, um den Decoder darüber zu informieren, dass der Navigator die richtigen Zeitstempel für die Samplings festlegt, die er an den Decoder übermittelt.</span><span class="sxs-lookup"><span data-stu-id="71bbd-104">The DVD Navigator uses this property to inform the decoder that the Navigator is setting the correct time stamps on the samples it delivers to the decoder.</span></span>



| <span data-ttu-id="71bbd-105">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="71bbd-105">Label</span></span> | <span data-ttu-id="71bbd-106">Wert</span><span class="sxs-lookup"><span data-stu-id="71bbd-106">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="71bbd-107">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="71bbd-107">Property Set GUID</span></span> | <span data-ttu-id="71bbd-108">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="71bbd-108">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="71bbd-109">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="71bbd-109">Property ID</span></span>       | <span data-ttu-id="71bbd-110">AM \_ RATE \_ CorrectTS</span><span class="sxs-lookup"><span data-stu-id="71bbd-110">AM\_RATE\_CorrectTS</span></span>           |
| <span data-ttu-id="71bbd-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="71bbd-111">Data Type</span></span>         | <span data-ttu-id="71bbd-112">**LONG**</span><span class="sxs-lookup"><span data-stu-id="71bbd-112">**LONG**</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="71bbd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71bbd-113">Remarks</span></span>

<span data-ttu-id="71bbd-114">Frühere Versionen des DVD-Navigators haben nicht die richtigen Zeitstempel festgelegt, wenn die Wiedergaberate etwas anderes als 1.0 war.</span><span class="sxs-lookup"><span data-stu-id="71bbd-114">Earlier versions of the DVD Navigator did not set the correct time stamps when the playback rate was something other than 1.0.</span></span> <span data-ttu-id="71bbd-115">Viele Decoder umgehen dieses Problem, indem sie die Zeitstempel beim Zurückspulen oder schnellen Vorwärtsgehen ignorieren und die richtigen Präsentationszeiten schätzen.</span><span class="sxs-lookup"><span data-stu-id="71bbd-115">Many decoders work around this problem by ignoring the time stamps during rewind or fast forward, and estimating the correct presentation times.</span></span>

<span data-ttu-id="71bbd-116">Diese Probleme wurden in der aktuellen Version des DVD-Navigators behoben.</span><span class="sxs-lookup"><span data-stu-id="71bbd-116">These problems have been corrected in the current version of the DVD Navigator.</span></span> <span data-ttu-id="71bbd-117">Aus Gründen der Abwärtskompatibilität mit vorhandenen Decodern gibt der DVD-Navigator an, dass die Zeitstempel korrekt sind, indem die AM \_ RATE \_ CorrectTS-Eigenschaft für den Decoder mit dem Wert **TRUE** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="71bbd-117">For backward compatibility with existing decoders, the DVD Navigator indicates that the time stamps are correct by setting the AM\_RATE\_CorrectTS property on the decoder with the value **TRUE**.</span></span> <span data-ttu-id="71bbd-118">Wenn diese Eigenschaft festgelegt ist, sollte der Decoder die tatsächlichen Zeitstempel verwenden, anstatt die Präsentationszeiten zu schätzen.</span><span class="sxs-lookup"><span data-stu-id="71bbd-118">When this property is set, the decoder should use the actual time stamps, instead of estimating the presentation times.</span></span>

## <a name="requirements"></a><span data-ttu-id="71bbd-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71bbd-119">Requirements</span></span>



| <span data-ttu-id="71bbd-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71bbd-120">Requirement</span></span> | <span data-ttu-id="71bbd-121">Wert</span><span class="sxs-lookup"><span data-stu-id="71bbd-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71bbd-122">Header</span><span class="sxs-lookup"><span data-stu-id="71bbd-122">Header</span></span><br/> | <dl> <span data-ttu-id="71bbd-123"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="71bbd-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71bbd-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71bbd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71bbd-125">**Ratenänderungseigenschaftensatz**</span><span class="sxs-lookup"><span data-stu-id="71bbd-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




