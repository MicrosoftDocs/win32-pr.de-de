---
description: Gibt den Status eines Versuchs zum Auflösen einer Topologie an.
ms.assetid: 7c2410ce-e70b-4303-9dbc-caff4a355d6b
title: MF_TOPOLOGY_RESOLUTION_STATUS-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb98db0de67e228606d9f37216d1ea13cbc2f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863579"
---
# <a name="mf_topology_resolution_status-attribute"></a>Status Attribut der MF- \_ topologieauflösung \_ \_

Gibt den Status eines Versuchs zum Auflösen einer Topologie an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Das topologielader oder die Medien Sitzung kann dieses Attribut in einer Topologie festlegen. Der Wert dieses Attributs ist ein bitweises **or** von Flags aus der-Enumeration der [**MF- \_ topologiestatusflags \_ \_ \_**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) -Enumeration.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**Imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> </dl>

 

 




