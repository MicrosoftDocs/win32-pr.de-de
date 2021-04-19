---
description: Gibt die Startzeit der Präsentation an.
ms.assetid: a2a64cac-0dc1-41b0-b59c-a477c7304ba1
title: MF_TOPONODE_MEDIASTART-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab00727cc328bfd6ba780050160fb21eecbb96f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361763"
---
# <a name="mf_toponode_mediastart-attribute"></a>MF \_ toponode \_ mediastart-Attribut

Gibt die Startzeit der Präsentation an.

## <a name="data-type"></a>Datentyp

**UINT64**

Als **Longlong** -Wert behandeln.

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Gilt für:

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gibt die Position in der Quelle an, an der die Wiedergabe in 100-Nanosecond-Einheiten relativ zum Start der Quelle beginnt. Wenn das-Attribut nicht festgelegt ist, wird die Wiedergabe bei NULL (dem Anfang der Datei) gestartet. Wenn Sie z. b. die Wiedergabe an der 5-Sekunden-Markierung starten möchten, legen Sie dieses Attribut auf 50 Millionen fest. Legen Sie das-Attribut auf den Quellknoten in der Topologie fest (Knoten, deren Typ gleich der **MF- \_ Topologie \_ sourcestream- \_ Knoten** ist). Legen Sie das-Attribut vor dem Aufrufen von [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)fest.

> [!Note]  
> Wenn Sie einen Decoder manuell in die Topologie einfügen, müssen Sie auch die hier aufgeführten Attribute " [MF \_ toponode \_ Markin \_ here](mf-toponode-markin-here-attribute.md) " und " [MF \_ toponode \_ markout \_ ](mf-toponode-markout-here-attribute.md) " auf dem Decoder-Knoten festlegen.

 

Dieses Attribut ist ein Wert mit Vorzeichen, obwohl er als **UINT64** gespeichert wird. Negative Werte sind jedoch nicht sinnvoll.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Sequenz Präsentations Zeiten](sequence-presentation-times.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> <dt>

[**MF- \_ toponode- \_ mediastop**](mf-toponode-mediastop-attribute.md)
</dt> </dl>

 

 




