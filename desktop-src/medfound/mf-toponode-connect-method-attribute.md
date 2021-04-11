---
description: Gibt an, wie der topologielader diesen topologieknoten verbindet und ob dieser Knoten optional ist.
ms.assetid: 8d70e1af-607b-47c3-9808-091c95fd05b7
title: MF_TOPONODE_CONNECT_METHOD-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3db5fef529ef451fa02ac4a29e62002b0a1996a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217843"
---
# <a name="mf_toponode_connect_method-attribute"></a>MF \_ toponode \_ Connect- \_ Methoden Attribut

Gibt an, wie der topologielader diesen topologieknoten verbindet und ob dieser Knoten optional ist.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für alle Knoten Typen.

Der Attribut Wert ist ein bitweises **or** von-Flags aus der [**MF \_ Connect- \_ Methoden**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) Enumeration. Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert **MF \_ Connect \_ Allow \_ Decoder**.

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

 

 




