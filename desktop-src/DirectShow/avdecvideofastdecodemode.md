---
description: Ruft die videodecodierungs Geschwindigkeit ab oder legt Sie fest
ms.assetid: 76F7013D-C172-4D31-93BC-EA3D186EB14C
title: Avdecvideofastdecodemode-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355c085731befedbcb9245a67870d9d609a92c6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125264"
---
# <a name="avdecvideofastdecodemode-property"></a>Avdecvideofastdecodemode (Eigenschaft)

Ruft die videodecodierungs Geschwindigkeit ab oder legt Sie fest

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avdecvideofastdecodemode**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft kann zwischen 0 und 32 liegen. der Wert 0 gibt eine normale Decodierung an, und 32 ist der schnellste Decodierungs Modus. Das genaue Verhalten hängt von der Decoder-Implementierung ab. Nicht jedes Inkrement zwischen 1 und 32 definiert notwendigerweise einen eindeutigen Modus.

Die [**eavfastdecodemode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) -Enumeration enthält einige vordefinierte Modi für diese Eigenschaft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[ Desktop Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften der Codec-API](codec-api-properties.md)
</dt> <dt>

[**Icodecapi-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




