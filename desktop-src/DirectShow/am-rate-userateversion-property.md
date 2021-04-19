---
description: Diese Eigenschaft wird verwendet, um zu signalisieren, welche Version der Eigenschaften Satzänderung vom Decoder verwendet werden soll.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: AM_RATE_UseRateVersion-Eigenschaft (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab609d2d38dc28257d13994e6cd464094b714be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371425"
---
# <a name="am_rate_userateversion-property"></a>\_Ate \_ userateversion (Eigenschaft)

Diese Eigenschaft wird verwendet, um zu signalisieren, welche Version der Eigenschaften Satzänderung vom Decoder verwendet werden soll. Der Wert ist ein **Worttyp** . Das hochwertige Byte enthält die neben Versionsnummer, und das nieder wertige Byte enthält das nieder wertige Byte. Daher wird Version 1,1 mit dem Wert 0x0101 signalisiert.

Wenn der Decoder die angegebene Version nicht unterstützt, sollte er den [**callspropertyset:: Set**](ikspropertyset-set.md) -Befehl nicht ausführen und E \_ nointerface zurückgeben. Wenn der Quell Filter die Version nicht festgelegt hat, sollte der Decoder standardmäßig auf Version 1,0 festgelegt werden.



|                   |                               |
|-------------------|-------------------------------|
| Eigenschaftensatz-GUID | AM \_ kspropltid \_ |
| Eigenschafts-ID       | \_ \_ Userateversion für ATE      |
| Datentyp         | **WORD**                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften Satz für Raten Änderung**](rate-change-property-set.md)
</dt> </dl>

 

 




