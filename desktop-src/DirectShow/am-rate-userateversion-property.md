---
description: Diese Eigenschaft wird verwendet, um zu signalisieren, welche Version der Rate Change-Eigenschaft den Decoder verwenden soll.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: AM_RATE_UseRateVersion-Eigenschaft (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd33ef96c50ecc3da0711f08f0c7ffbf0a20825
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910218"
---
# <a name="am_rate_userateversion-property"></a>AM \_ RATE \_ UseRateVersion-Eigenschaft

Diese Eigenschaft wird verwendet, um zu signalisieren, welche Version der Rate Change-Eigenschaft den Decoder verwenden soll. Der Wert ist ein **WORD-Typ.** Das obere Byte enthält die Nebenversionsnummer, und das niedrige Byte enthält das niedrige Byte. Daher wird Version 1.1 mit dem Wert 0x0101.

Wenn der Decoder die angegebene Version nicht unterstützt, sollte der Aufruf von [**IKsPropertySet::Set**](ikspropertyset-set.md) fehlschlagen und E \_ NOINTERFACE zurückgeben. Wenn der Quellfilter die Version nicht festgelegt, sollte der Decoder standardmäßig auf Version 1.0 festgelegt werden.



| Bezeichnung | Wert |
|-------------------|-------------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ TSRateChange |
| Eigenschafts-ID       | AM \_ RATE \_ UseRateVersion      |
| Datentyp         | **WORD**                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rate Change Property Set**](rate-change-property-set.md)
</dt> </dl>

 

 




