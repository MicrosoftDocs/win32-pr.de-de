---
description: Ruft die Anzahl der Kanäle im Audiobitstream ab.
ms.assetid: e395ce9c-3f11-41e9-8c8c-48c17b217ebc
title: AVAudioChannelCount-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c698eb4d802dd3e41fcd53434ab2649f447fb1981a4aada0a977fd2ccab7039
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641380"
---
# <a name="avaudiochannelcount-property"></a>AVAudioChannelCount-Eigenschaft

Ruft die Anzahl der Kanäle im Audiobitstream ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVAudioChannelCount**

## <a name="remarks"></a>Hinweise

Die Anzahl von Kanälen umfasst den LFE-Kanal (Low Frequency Effect), sofern vorhanden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




