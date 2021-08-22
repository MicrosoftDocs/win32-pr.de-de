---
description: Gibt die Standardanzahl aufeinanderfolgender B-Frames zwischen I- und P-Frames an.
ms.assetid: d41ed713-0159-4325-bc44-f4a3eea10aa2
title: AVEncMPVDefaultBPictureCount-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95604d8b3849175e579d276fa006f5a8c4d2833a167228316c4cf830b01618b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276260"
---
# <a name="avencmpvdefaultbpicturecount-property"></a>AVEncMPVDefaultBPictureCount (Eigenschaft)

Gibt die Standardanzahl aufeinanderfolgender B-Frames zwischen I- und P-Frames an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncMPVDefaultBPictureCount**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft verfügt über einen linearen Wertebereich. Um den unterstützten Bereich zu erhalten, rufen [**Sie ICodecAPI::GetParameterRange auf.**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)

## <a name="remarks"></a>Hinweise

Vor der Windows 8 gilt diese Eigenschaft für MPEG-Videoencoder. Ab Windows 8 wird diese Eigenschaft von MPEG-, WMV- und H.264-Videoencodern verwendet.

Wenn der Encoder diese Eigenschaft unterstützt, kann sie verwendet werden, um die GoP-Struktur (Group of Pictures) zu steuern.

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

 

 




