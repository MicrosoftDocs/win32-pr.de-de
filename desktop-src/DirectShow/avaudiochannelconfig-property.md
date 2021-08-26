---
description: Ruft die Sprecherkonfiguration für die Audiokanäle im Audiobitstream ab.
ms.assetid: ec13bb55-47af-4d79-9560-d297bce8e236
title: AVAudioChannelConfig-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba9c497305292abeb34b86a7989fb05fbb872c898d10743ebd93b3982089e00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983790"
---
# <a name="avaudiochannelconfig-property"></a>AVAudioChannelConfig(Eigenschaft)

Ruft die Sprecherkonfiguration für die Audiokanäle im Audiobitstream ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVAudioChannelConfig**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein bitweises OR von Membern der [**eAVAudioChannelConfig-Enumeration.**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig)

## <a name="remarks"></a>Hinweise

Die Anzahl der Kanäle schließt den LFE-Kanal (Low Frequency Effect) ein, falls vorhanden.

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

 

 




