---
description: Gibt das Element an, das diesen Quellknoten enthält.
ms.assetid: f5fa5c10-8f30-43bd-8054-a39996f807a3
title: MF_TOPONODE_SEQUENCE_ELEMENTID -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00af7212013d26c51ecdf7d2ea4a22855f9b52524c5188d3514d34b5d6976b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739935"
---
# <a name="mf_toponode_sequence_elementid-attribute"></a>MF \_ TOPONODE \_ SEQUENCE \_ ELEMENTID-Attribut

Gibt das Element an, das diesen Quellknoten enthält.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Quellknoten (**MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**).

Die Medienpipeline verwendet dieses Attribut, um zu entdecken, wann Medienquellen Teil desselben Elements sind. Die Pipeline behandelt alle Quellknoten, die Teil desselben Elements sind, mit der gleichen Uhr.

Wenn die Pipeline eine neue Topologie in die Warteschlange einreiht, die Quellknoten enthält, die Teil eines Elements sind, das in der vorherigen Topologie vorhanden ist, behandelt die Pipeline diese Quellknoten so, als ob sie dieselbe Uhr wie die Quellknoten aus diesem Element in der vorherigen Topologie haben.

> [!Note]  
> Die Medienpipeline korrigiert keine Zeitstempel für Quellknoten mit unterschiedlichen Taktraten.

 

Eine Medienquelle, die Topologien bereitstellen kann, sollte die [**BENUTZEROBERFLÄCHEMediaSourceTopologyProvider-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) oder [**dieTOPOLOGYSequencerSource-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) implementieren. Eine Medienquelle, die Topologien bietet, sollte das **MF \_ TOPONODE \_ SEQUENCE \_ ELEMENTID-Attribut** auf jedem Quellknoten festlegen, den sie erstellt.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**TOPOLOGYMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
</dt> <dt>

[**VERALTENQuencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)
</dt> <dt>

[**TOPOLOGIENode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> <dt>

[Sequencerquelle](sequencer-source.md)
</dt> </dl>

 

 




