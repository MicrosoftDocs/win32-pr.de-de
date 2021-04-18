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
# <a name="am_rate_correctts-property"></a>\_Eigenschaft für Raten \_ Korrekturen

Der DVD-Navigator verwendet diese Eigenschaft, um den Decoder darüber zu informieren, dass der Navigator die richtigen Zeitstempel für die Stichproben festlegt, die er an den Decoder übergibt.



|                   |                               |
|-------------------|-------------------------------|
| Eigenschaftensatz-GUID | AM \_ kspropltid \_ |
| Eigenschafts-ID       | Bei \_ Raten \_ Korrekturen           |
| Datentyp         | **LONG**                      |



 

## <a name="remarks"></a>Bemerkungen

Frühere Versionen des DVD-Navigators haben nicht die richtigen Zeitstempel festgelegt, als die Wiedergabe Rate etwas anderes als 1,0 war. Viele Decoder umgehen dieses Problem, indem Sie die Zeitstempel beim Zurückspulen oder schnell vorwärts ignorieren und die richtigen Präsentations Zeiten schätzen.

Diese Probleme wurden in der aktuellen Version des DVD-Navigators korrigiert. Aus Gründen der Abwärtskompatibilität mit vorhandenen Decodern zeigt der DVD-Navigator an, dass die Zeitstempel korrekt sind, indem die \_ \_ Eigenschaft für die Wert Korrektur für den Decoder mit dem Wert **true** festgelegt wird. Wenn diese Eigenschaft festgelegt ist, sollte der Decoder die tatsächlichen Zeitstempel verwenden, anstatt die Präsentations Zeiten zu schätzen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften Satz für Raten Änderung**](rate-change-property-set.md)
</dt> </dl>

 

 




