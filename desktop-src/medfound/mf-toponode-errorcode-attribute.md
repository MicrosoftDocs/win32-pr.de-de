---
description: Enthält den Fehlercode des letzten Verbindungsfehlers für diesen topologietknoten.
ms.assetid: fae90e06-0ae0-43a1-aaf2-7a2d1dabc79b
title: MF_TOPONODE_ERRORCODE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4b28c8f630d06f3545ca44c5b064c0bb6dac32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130144"
---
# <a name="mf_toponode_errorcode-attribute"></a>MF- \_ toponode- \_ errorCode-Attribut

Enthält den Fehlercode des letzten Verbindungsfehlers für diesen topologietknoten.

## <a name="data-type"></a>Datentyp

**UINT32**

"Ttreat" als **HRESULT** -Wert.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für alle Knoten Typen.

Der Wert dieses Attributs ist ein **HRESULT** -Wert.

Das-Attribut kann von der Medien Sitzung oder dem topologielader festgelegt werden. Anwendungen lesen dieses Attribut in der Regel, ohne es festzulegen.

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

 

 




