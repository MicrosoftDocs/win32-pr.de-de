---
description: Gibt an, ob die zwei-Kanal-Audiodaten als Stereo oder Dual Mono codiert werden.
ms.assetid: 37f25590-69c2-43bd-a5d4-2262457cb39d
title: Avencaudiodualmono-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0a5b684638133a1449fc849348cdfd8627533fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341111"
---
# <a name="avencaudiodualmono-property"></a>Avencaudiodualmono (Eigenschaft)

Gibt an, ob die zwei-Kanal-Audiodaten als Stereo oder Dual Mono codiert werden.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencaudiodualmono**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein Member der [**eavencaudiodualmono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) -Enumeration.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gilt nicht für MPEG-Audioencoder. Verwenden Sie für MPEG-Audiodaten die Eigenschaft " [**avencmpacodingmode**](avencmpacodingmode-property.md) ".

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

 

