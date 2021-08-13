---
description: Gibt die Anzahl der Videoframes zurück, die der Encoder empfangen hat.
ms.assetid: 3de49105-3c74-4a52-9cac-465b4abfcbf5
title: AVEncStatVideoTotalFrames-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 461708e9006db183992cf550bf7f98eeaeacbfe16c100675ab4992b54f0768d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663441"
---
# <a name="avencstatvideototalframes-property"></a>AVEncStatVideoTotalFrames (Eigenschaft)

Gibt die Anzahl der Videoframes zurück, die der Encoder empfangen hat.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncStatVideoTotalFrames**

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist nach Abschluss der Codierung verfügbar.

Der Wert dieser Eigenschaft ist die Gesamtzahl der an den Encoder gesendeten Frames, einschließlich der gelöschten Frames. Um die Anzahl der codierten Frames zu erhalten, lesen Sie die [**AVEncStatVideoCodedFrames-Eigenschaft.**](avencstatvideocodedframes-property.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




