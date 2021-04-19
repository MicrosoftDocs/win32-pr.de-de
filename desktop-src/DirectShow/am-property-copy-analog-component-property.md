---
description: Fragt ab, ob es sich bei der Videoausgabe um ein Video mit der standardmäßigen Definition, Analog
ms.assetid: bd4fc5bc-c45d-4228-9759-6300fdfff6a0
title: AM_PROPERTY_COPY_ANALOG_COMPONENT-Eigenschaft (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f3998156bf372c39018aa73ba30a661117519c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373867"
---
# <a name="am_property_copy_analog_component-property"></a>Eigenschaften \_ \_ Kopie der \_ Analog \_ Component-Eigenschaft

Fragt ab, ob es sich bei der Videoausgabe um ein Video mit der standardmäßigen Definition, Analog



|                   |                                       |
|-------------------|---------------------------------------|
| Eigenschaftensatz-GUID | AM \_ kspropsetid \_ copyprot             |
| Eigenschafts-ID       | AM \_ - \_ Eigenschaften \_ Kopier \_ Komponente (analog) |
| Datentyp         | **ULONG**                             |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist schreibgeschützt.

Der Wert der-Eigenschaft ist **true** , wenn die Videoausgabe ein analoges Komponenten Video mit einer Auflösung ist, die nicht größer als 480p für NTSC oder 540p für PAL ist. Andernfalls ist der Wert **false**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften Satz für den DVD-Kopierschutz**](dvd-copy-protection-property-set.md)
</dt> </dl>

 

 




