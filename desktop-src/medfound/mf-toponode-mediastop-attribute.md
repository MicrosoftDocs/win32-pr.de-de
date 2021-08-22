---
description: Gibt die Beendigungszeit der Präsentation an.
ms.assetid: c1022538-ea9f-41e9-9075-c106e8b16b7b
title: MF_TOPONODE_MEDIASTOP-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea2abc172151afe404f3acc6cf8c75d03bd0ac495564cb0f322283998677f83b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663870"
---
# <a name="mf_toponode_mediastop-attribute"></a>MF \_ TOPONODE \_ MEDIASTOP-Attribut

Gibt die Beendigungszeit der Präsentation an.

## <a name="data-type"></a>Datentyp

**UINT64**

Als **LONGLONG-Wert** behandeln.

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT64 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT64 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)

## <a name="applies-to"></a>Gilt für:

[**TOPOLOGYNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a>Hinweise

Dieses Attribut gibt die Position in der Quelle an, an der die Wiedergabe in Einheiten von 100 Nanosekunden relativ zum Start der Quelle beendet wird. Wenn das Attribut nicht festgelegt ist, wird die Wiedergabe am Ende der Quelle beendet. Um beispielsweise die Wiedergabe bei der 5-Sekunden-Marke zu beenden, legen Sie dieses Attribut auf 50000000 fest. Legen Sie das Attribut auf den Quellknoten in der Topologie fest (Knoten mit dem Typ **MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**). Legen Sie das -Attribut fest, bevor [**Sie DIE ATTRIBUTEMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)aufrufen.

> [!Note]  
> Wenn Sie einen Decoder manuell in die Topologie einfügen, müssen Sie auch die Attribute [MF \_ TOPONODE \_ MARKIN \_ HERE](mf-toponode-markin-here-attribute.md) und [MF \_ TOPONODE \_ MARKOUT \_ HERE](mf-toponode-markout-here-attribute.md) auf dem Decoderknoten festlegen.

 

Nachdem die Topologie festgelegt wurde, hat das Festlegen dieses Attributs keine Auswirkungen.

Dieses Attribut ist ein Wert mit Vorzeichen, obwohl es als **UINT64** gespeichert ist. Negative Werte sind jedoch nicht sinnvoll.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Sequenzpräsentationszeiten](sequence-presentation-times.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> <dt>

[**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md)
</dt> </dl>

 

 




