---
description: Enthält den Zeitstempel des Gerätetreibers.
ms.assetid: 8904d104-ebcc-474d-b6b5-b262b6f62ee9
title: MFSampleExtension_DeviceTimestamp -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3322f295908ae2bbdc095a21ab57ee2e0f2ed10dd2267eaea227b9248ddc226b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241125"
---
# <a name="mfsampleextension_devicetimestamp-attribute"></a>DeviceTimestamp-Attribut "MFSampleExtension" \_

Enthält den Zeitstempel des Gerätetreibers.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT64 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT64 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)

## <a name="applies-to"></a>Gilt für:

[**VERERBUNGSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird für Medienbeispiele festgelegt, die von einer Medienquelle für ein Erfassungsgerät erstellt wurden. Der Wert dieses Attributs befindet sich in der [**MFTIME-Domäne**](mftime.md) und teilt eine Epoche mit QPC-Zeit (Query Performance Counter) und wird immer in Einheiten von 100 ns ausgedrückt. Dieses Attribut ist für MFTs verfügbar, die in die Erfassungspipeline eingefügt werden.

Um den Zeitstempel relativ zum Beginn des Streamings zu erhalten, rufen Sie die [**METHODE VERSAMPLE::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) auf.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Audio-/Videoaufnahme in Media Foundation](audio-video-capture-in-media-foundation.md)
</dt> <dt>

[Beispielattribute](sample-attributes.md)
</dt> </dl>

 

 




