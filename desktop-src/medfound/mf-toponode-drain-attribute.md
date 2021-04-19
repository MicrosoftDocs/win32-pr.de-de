---
description: Gibt an, wann eine Transformation entladen wird.
ms.assetid: 68332106-d1fe-467b-8baa-1e592b9cc243
title: MF_TOPONODE_DRAIN-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b87d626738b82f4504673392bd0fe159e2722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350500"
---
# <a name="mf_toponode_drain-attribute"></a>MF- \_ toponode-Attribut zum Entfernen \_

Gibt an, wann eine Transformation entladen wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Transformations Knoten (**MF- \_ topologietransformations- \_ \_ Knoten**).

Der Wert des-Attributs ist ein Member der [**MF- \_ toponode-Ausgleichs \_ \_ Modus**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_drain_mode) -Enumeration. Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert **MF \_ toponode- \_ \_ Standard** Wert.

Die Ableitung erfolgt durch Aufrufen von [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) für die Transformation mit der [**MFT- \_ Nachrichten \_ Befehls \_**](mft-message-command-drain.md) Ausgleichs Nachricht. Weitere Informationen finden Sie unter [**MFT \_ Message \_ Type**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) Enumeration.

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

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 




