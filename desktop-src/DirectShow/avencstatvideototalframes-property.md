---
description: Gibt die Anzahl der Video Frames zurück, die der Encoder empfangen hat.
ms.assetid: 3de49105-3c74-4a52-9cac-465b4abfcbf5
title: Avencstatus videototalframes-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76adda51e6d16676a2a957fd16a5aac2a15691e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345584"
---
# <a name="avencstatvideototalframes-property"></a>Avencstatus videototalframes (Eigenschaft)

Gibt die Anzahl der Video Frames zurück, die der Encoder empfangen hat.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencstatus Video Total Frames**

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist nach Abschluss der Codierung verfügbar.

Der Wert dieser Eigenschaft ist die Gesamtzahl der an den Encoder gesendeten Frames, einschließlich abgelöschter Frames. Um die Anzahl der codierten Frames zu erhalten, lesen Sie die Eigenschaft " [**avencstatus videocodedframes**](avencstatvideocodedframes-property.md) ".

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

 

 




