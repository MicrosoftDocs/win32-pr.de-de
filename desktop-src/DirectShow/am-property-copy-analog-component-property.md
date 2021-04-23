---
description: Fragt ab, ob es sich bei der Videoausgabe um videobasierte Standarddefinitionen handelt, analoges Komponentenvideo.
ms.assetid: bd4fc5bc-c45d-4228-9759-6300fdfff6a0
title: AM_PROPERTY_COPY_ANALOG_COMPONENT-Eigenschaft (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6448bfbcc07be6ca37189c15c7c605887e6d22b3
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910308"
---
# <a name="am_property_copy_analog_component-property"></a>AM \_ PROPERTY COPY ANALOG \_ \_ \_ COMPONENT-Eigenschaft

Fragt ab, ob es sich bei der Videoausgabe um videobasierte Standarddefinitionen handelt, analoges Komponentenvideo.



| Bezeichnung | Wert |
|-------------------|---------------------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ CopyProt             |
| Eigenschafts-ID       | \_AM-EIGENSCHAFT \_ – \_ ANALOGE KOMPONENTE \_ KOPIEREN |
| Datentyp         | **ULONG**                             |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist schreibgeschützt.

Der Wert der -Eigenschaft ist **TRUE,** wenn die Videoausgabe analoges Komponentenvideo mit einer Auflösung von nicht größer als 480p für NTSC oder 540p für PAL ist. Andernfalls ist der Wert **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DVD Copy Protection-Eigenschaftensatz**](dvd-copy-protection-property-set.md)
</dt> </dl>

 

 




