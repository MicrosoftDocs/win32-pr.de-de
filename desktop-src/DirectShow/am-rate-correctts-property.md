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
# <a name="am_rate_correctts-property"></a>AM \_ RATE \_ CorrectTS-Eigenschaft

Der DVD-Navigator verwendet diese Eigenschaft, um den Decoder darüber zu informieren, dass der Navigator die richtigen Zeitstempel für die Samplings festlegt, die er an den Decoder übermittelt.



| Bezeichnung | Wert |
|-------------------|-------------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ TSRateChange |
| Eigenschafts-ID       | AM \_ RATE \_ CorrectTS           |
| Datentyp         | **LONG**                      |



 

## <a name="remarks"></a>Bemerkungen

Frühere Versionen des DVD-Navigators haben nicht die richtigen Zeitstempel festgelegt, wenn die Wiedergaberate etwas anderes als 1.0 war. Viele Decoder umgehen dieses Problem, indem sie die Zeitstempel beim Zurückspulen oder schnellen Vorwärtsgehen ignorieren und die richtigen Präsentationszeiten schätzen.

Diese Probleme wurden in der aktuellen Version des DVD-Navigators behoben. Aus Gründen der Abwärtskompatibilität mit vorhandenen Decodern gibt der DVD-Navigator an, dass die Zeitstempel korrekt sind, indem die AM \_ RATE \_ CorrectTS-Eigenschaft für den Decoder mit dem Wert **TRUE** festgelegt wird. Wenn diese Eigenschaft festgelegt ist, sollte der Decoder die tatsächlichen Zeitstempel verwenden, anstatt die Präsentationszeiten zu schätzen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ratenänderungseigenschaftensatz**](rate-change-property-set.md)
</dt> </dl>

 

 




