---
description: Gibt an, ob die Mediensitzung versucht, die Topologie zu ändern, wenn sich das Format eines Streams ändert.
ms.assetid: 8272ded7-9d27-4652-877b-40fc76426ffc
title: MF_TOPOLOGY_DYNAMIC_CHANGE_NOT_ALLOWED -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2e984b45abc55246c9b1ae291c535c7fbb00f01f9405d827b7fe833b57a368
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875731"
---
# <a name="mf_topology_dynamic_change_not_allowed-attribute"></a>DYNAMIC CHANGE NOT ALLOWED-Attribut der \_ MF-TOPOLOGIE \_ \_ \_ \_

Gibt an, ob die Mediensitzung versucht, die Topologie zu ändern, wenn sich das Format eines Streams ändert.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**TOPOLOGYTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Hinweise

Dieses Attribut steuert, wie die Mediensitzung reagiert, wenn sich das Format eines Streams während des Streamings ändert.

Wenn sich das Format ändert und das DYNAMIC CHANGE NOT ALLOWED-Attribut der MF-TOPOLOGIE FALSE ist, fügt die Mediensitzung möglicherweise neue Knoten in die Topologie ein, um dem \_ \_ neuen Format zu \_ \_ \_ passen.  Wenn sich beispielsweise die Videogröße ändert, kann die Mediensitzung eine MFT (Media Foundation Transformieren) hinzufügen, die die Größe des Videos ändert. Andernfalls ändert die Mediensitzung die Topologie nicht, wenn das Attribut **TRUE** ist.

Der Standardwert dieses Attributs ist **FALSE.** Der empfohlene Wert ist **FALSE.**

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

[Topologieattribute](topology-attributes.md)
</dt> </dl>

 

 




