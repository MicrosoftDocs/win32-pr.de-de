---
description: Gibt den Status eines Versuchten an, eine Topologie aufzulösen.
ms.assetid: 7c2410ce-e70b-4303-9dbc-caff4a355d6b
title: MF_TOPOLOGY_RESOLUTION_STATUS -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a62645b17efadb8216ba078b966bc2f7f47debae60103fa6665daaeaebc13306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691232"
---
# <a name="mf_topology_resolution_status-attribute"></a>STATUS-Attribut \_ der MF-TOPOLOGIEAUFLÖSUNG \_ \_

Gibt den Status eines Versuchten an, eine Topologie aufzulösen.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Das Topologielader oder die Mediensitzung kann dieses Attribut für eine Topologie festlegen. Der Wert dieses Attributs ist ein bitweises **OR** von Flags aus der [**MF \_ TOPOLOGY \_ RESOLUTION STATUS \_ \_ FLAGS-Enumeration.**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags)

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**TOPOLOGYTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> </dl>

 

 




