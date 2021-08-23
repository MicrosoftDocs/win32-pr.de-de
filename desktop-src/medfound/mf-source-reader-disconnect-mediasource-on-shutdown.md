---
description: Gibt an, ob der Quellleser die Medienquelle heruntergefahren hat.
ms.assetid: c85f5994-8005-48c9-8a05-0316f48f4142
title: MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN -Attribut (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 323340a0b95fd6f52d4ac7e8db2e9ff53bf70edb30442369f1ffd8f2f2c55fa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663890"
---
# <a name="mf_source_reader_disconnect_mediasource_on_shutdown-attribute"></a>\_MF-QUELLLESER \_ \_ DISCONNECT \_ MEDIASOURCE ON \_ \_ SHUTDOWN-Attribut

Gibt an, ob [der Quellleser](source-reader.md) die Medienquelle heruntergefahren hat.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt nur, wenn die Anwendung den Quellreader aus einem vorhandenen Medienquellenobjekt erstellt, entweder durch Aufrufen von [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) oder durch Aufrufen [**vonWRITEReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).

Wenn die Anwendung den Quellleser frei gibt, fährt der Quellleser die Medienquelle standardmäßig herunter, indem [**er FÜR DIE MEDIENQUELLE::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) für die Medienquelle aufruft. An diesem Punkt kann die Anwendung die Medienquelle nicht mehr verwenden.

Wenn das MF SOURCE READER DISCONNECT MEDIASOURCE ON SHUTDOWN-Attribut jedoch TRUE ist, fährt der Quellleser \_ \_ die \_ \_ \_ \_ Medienquelle nicht herunter.  Das bedeutet, dass die Anwendung die Medienquelle weiterhin verwenden kann, nachdem die Anwendung den Quellleser veröffentlicht hat. Dies bedeutet auch, dass die Anwendung für den Aufruf von 1000222222222111111111111111111177111111111111771 [](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)

Wenn die Anwendung den Quellreader aus einer URL oder einem Bytestream erstellt, fährt der Quellleser immer die Medienquelle herunter. Das MF \_ SOURCE \_ READER DISCONNECT \_ \_ MEDIASOURCE ON \_ \_ SHUTDOWN-Attribut wird in diesem Fall ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server 2008 \[ \| R2-Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Quellleser](source-reader.md)
</dt> <dt>

[Quellleseattribute](source-reader-attributes.md)
</dt> </dl>

 

 




