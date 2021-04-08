---
description: Gibt an, wie der Decoder Dual Mono-Audiodaten wiederherstellt.
ms.assetid: 3ef1f52c-13b2-4d9f-99fe-3317846be8a0
title: Avdecaudiodualmonorepromode-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71ebe7e003b2dc4b6eebc30901525ffb918a9a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747081"
---
# <a name="avdecaudiodualmonorepromode-property"></a>Avdecaudiodualmonorepromode (Eigenschaft)

Gibt an, wie der Decoder Dual Mono-Audiodaten wiederherstellt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avdecaudiodualmonorepromode**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein Member der [**eavdecaudiodualmonorepromode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode) -Enumeration.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften sind nur anwendbar, wenn der Eingabe Bitstream des Decoders Dual Mono-Audiodaten enthält. Um diese Bedingung zu testen, müssen Sie den Wert der [avdecaudiodualmono](avdecaudiodualmono-property.md) -Eigenschaft erhalten.

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

 

 




