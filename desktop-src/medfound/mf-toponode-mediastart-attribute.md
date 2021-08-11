---
description: Gibt die Startzeit der Präsentation an.
ms.assetid: a2a64cac-0dc1-41b0-b59c-a477c7304ba1
title: MF_TOPONODE_MEDIASTART -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7efeed2bd34745ffda4e756c8b43894bd51fc287ded5cba0ecf0ffb323713754
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244421"
---
# <a name="mf_toponode_mediastart-attribute"></a>MF \_ TOPONODE \_ MEDIASTART-Attribut

Gibt die Startzeit der Präsentation an.

## <a name="data-type"></a>Datentyp

**UINT64**

Als **LONGLONG-Wert** behandeln.

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT64 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT64 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)

## <a name="applies-to"></a>Gilt für:

[**TOPOLOGIENode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a>Hinweise

Dieses Attribut gibt die Position in der Quelle an, an der die Wiedergabe in Einheiten von 100 Nanosekunden relativ zum Start der Quelle beginnt. Wenn das Attribut nicht festgelegt ist, beginnt die Wiedergabe bei 0 (dem Anfang der Datei). Um die Wiedergabe beispielsweise bei der 5-Sekunden-Marke zu starten, legen Sie dieses Attribut auf 50000000 fest. Legen Sie das -Attribut auf den Quellknoten in der Topologie fest (Knoten mit dem Typ **MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**). Legen Sie das -Attribut fest, bevor [**SIE DIEMEDIASession::SetTopology aufrufen.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)

> [!Note]  
> Wenn Sie manuell einen Decoder in die Topologie einfügen, müssen Sie auch die [Attribute MF \_ TOPONODE \_ MARKIN \_ HERE](mf-toponode-markin-here-attribute.md) und [MF \_ TOPONODE \_ MARKOUT \_ HERE](mf-toponode-markout-here-attribute.md) auf dem Decoderknoten festlegen.

 

Dieses Attribut ist ein signierter Wert, obwohl es als **UINT64 gespeichert wird.** Negative Werte sind jedoch nicht sinnvoll.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Sequenzpräsentationszeiten](sequence-presentation-times.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> <dt>

[**MF \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md)
</dt> </dl>

 

 




