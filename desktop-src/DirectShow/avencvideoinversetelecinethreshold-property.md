---
description: Legt den Schwellenwert fest, bei dem der Encoder ein Video Feld als redundant ansieht.
ms.assetid: db6c2f0e-f451-4d2d-984f-b507083e8358
title: Avencvideoinverabtelecinethreshold-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3427a8ff1491277c2e36640560acf728c0ef7208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745657"
---
# <a name="avencvideoinversetelecinethreshold-property"></a>Avencvideoinverabtelecinethreshold (Eigenschaft)

Legt den Schwellenwert fest, bei dem der Encoder ein Video Feld als redundant ansieht.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencvideoinverabtelecinethreshold**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft hat den folgenden Bereich.



| Wert | BESCHREIBUNG                                                    |
|-------|----------------------------------------------------------------|
| 0     | Der Encoder ist weniger wahrscheinlich, dass die Videofelder redundant sind. |
| 100   | Der Encoder ist eher in der Regel redundant, dass die Videofelder redundant sind. |



 

## <a name="remarks"></a>Bemerkungen

Legen Sie diese Eigenschaft fest, wenn der Encoder Inverse Telecine mit einer analogen Videoquelle ausführt.

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

 

 




