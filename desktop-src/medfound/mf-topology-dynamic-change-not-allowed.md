---
description: Gibt an, ob die Medien Sitzung versucht, die Topologie zu ändern, wenn das Format eines Datenstroms geändert wird.
ms.assetid: 8272ded7-9d27-4652-877b-40fc76426ffc
title: MF_TOPOLOGY_DYNAMIC_CHANGE_NOT_ALLOWED-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ade7308c4fadef315fae0828a5c2cb29575b03a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484803"
---
# <a name="mf_topology_dynamic_change_not_allowed-attribute"></a>Die \_ dynamische Änderung der MF-Topologie ist \_ \_ \_ nicht \_ zulässig.

Gibt an, ob die Medien Sitzung versucht, die Topologie zu ändern, wenn das Format eines Datenstroms geändert wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**Imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut steuert, wie die Medien Sitzung antwortet, wenn sich das Format eines Streams beim Streaming ändert.

Wenn das Format geändert wird und das \_ Attribut "dynamische Änderung der MF-Topologie \_ \_ nicht zulässig" auf "false" gesetzt \_ \_ ist, kann die Medien Sitzung neue Knoten in die Topologie einfügen, damit Sie dem neuen Format entspricht.  Wenn sich beispielsweise die Videogröße ändert, kann die Medien Sitzung eine Media Foundation Transformation (MFT) hinzufügen, die die Größe des Videos ändert. Wenn das Attribut **true** ist, wird die Topologie in der Medien Sitzung nicht geändert.

Der Standardwert dieses Attributs ist **false**. Der empfohlene Wert ist **false**.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> </dl>

 

 




