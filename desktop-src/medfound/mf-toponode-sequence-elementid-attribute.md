---
description: Gibt das Element an, das diesen Quellknoten enthält.
ms.assetid: f5fa5c10-8f30-43bd-8054-a39996f807a3
title: MF_TOPONODE_SEQUENCE_ELEMENTID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3cd2c66c40a0bc3776d2fd2b7d78535cf24b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345172"
---
# <a name="mf_toponode_sequence_elementid-attribute"></a>\_ \_ \_ ElementId-Attribut der MF-toponode-Sequenz

Gibt das Element an, das diesen Quellknoten enthält.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Quellknoten (**MF- \_ Topologie \_ sourcestream- \_ Knoten**).

Die Medien Pipeline verwendet dieses Attribut, um zu ermitteln, wann Medienquellen Teil desselben Elements sind. Die Pipeline behandelt alle Quellknoten, die Teil desselben Elements sind, mit derselben Uhr.

Wenn die Pipeline eine neue Topologie in die Warteschlange stellt, die Quellknoten enthält, die Teil eines in der vorherigen Topologie vorhandenen Elements sind, behandelt die Pipeline diese Quellknoten als dieselbe Uhr wie die Quellknoten von diesem Element in der vorherigen Topologie.

> [!Note]  
> Die Medien Pipeline korrigiert Zeitstempel für Quellknoten mit unterschiedlichen Takt Raten nicht.

 

Eine Medienquelle, die Topologien bereitstellen kann, sollte die [**imfmediasourcetopologyprovider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) -Schnittstelle oder die [**imfsequencersource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) -Schnittstelle implementieren. Eine Medienquelle, die Topologien bereitstellt, sollte das **Element "MF \_ toponode \_ Sequence \_ elementId** " für jeden Quellknoten festlegen, den Sie erstellt.

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

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**Imfmediasourcetopologyprovider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
</dt> <dt>

[**IMF sequencersource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)
</dt> <dt>

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> <dt>

[Sequencer-Quelle](sequencer-source.md)
</dt> </dl>

 

 




