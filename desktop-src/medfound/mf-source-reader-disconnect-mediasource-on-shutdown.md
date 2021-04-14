---
description: Gibt an, ob der Quell Leser die Medienquelle herunterfährt.
ms.assetid: c85f5994-8005-48c9-8a05-0316f48f4142
title: MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a9474e7fb19bb6531baf31a97238bbe6b10e46
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351718"
---
# <a name="mf_source_reader_disconnect_mediasource_on_shutdown-attribute"></a>Der MF- \_ Quell \_ Leser \_ trennt \_ MediaSource \_ beim \_ Shutdown-Attribut.

Gibt an, ob der [Quell Leser](source-reader.md) die Medienquelle herunterfährt.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt nur, wenn die Anwendung den Quell Leser aus einem vorhandenen Medien Quell Objekt erstellt, indem Sie entweder [**mfcreatesourcereaderfrommediasource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) aufrufen oder [**imfreadschreiteclassfactory:: createinstancefromuject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)aufrufen.

Wenn die Anwendung den Quell Leser freigibt, fährt der Quell Leser standardmäßig die Medienquelle durch Aufrufen von [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) für die Medienquelle herunter. An diesem Punkt kann die Anwendung die Medienquelle nicht mehr verwenden.

Wenn der MF- \_ Quell \_ Leser \_ \_ MediaSource \_ beim Shutdown-Attribut jedoch auf \_ **true** trennt, wird die Medienquelle vom Quell Leser nicht heruntergefahren. Dies bedeutet, dass die Anwendung nach der Veröffentlichung des Quell Readers die Medienquelle weiterhin verwenden kann. Dies bedeutet auch, dass die Anwendung für das Aufrufen von [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) für die Medienquelle zuständig ist.

Wenn die Anwendung den Quell Leser aus einer URL oder einem Bytestream erstellt, fährt der Quell Leser die Medienquelle immer herunter. In diesem Fall wird die Verbindung des MF- \_ Quell \_ Lesers " \_ \_ MediaSource" \_ beim \_ Shutdown-Attribut ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>"Mfreadwrite. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Quell Leser](source-reader.md)
</dt> <dt>

[Attribute des Quell Readers](source-reader-attributes.md)
</dt> </dl>

 

 




