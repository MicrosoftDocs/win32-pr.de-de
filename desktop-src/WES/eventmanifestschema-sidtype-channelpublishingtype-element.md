---
title: SIDType (channelpublishingtype)-Element
description: Bestimmt, ob eine Sicherheits-ID (SID) des Prinzipals mit jedem Ereignis eingeschlossen werden soll, das in den Kanal geschrieben wird.
ms.assetid: 3ce176a3-9e21-4646-8c99-7beb687e6847
keywords:
- SIDType-Element EventLog
topic_type:
- apiref
api_name:
- sidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d65e1ade4ded95b070b45de9462f6aee2c60ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342218"
---
# <a name="sidtype-channelpublishingtype-element"></a>SIDType (channelpublishingtype)-Element

Bestimmt, ob eine Sicherheits-ID (SID) des Prinzipals mit jedem Ereignis eingeschlossen werden soll, das in den Kanal geschrieben wird.

``` syntax
<xs:element name="sidType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="None"
             />
            <xs:enumeration
                value="Publishing"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das Element " **SIDType** " wird vom komplexen Typ " [**channelpublishingtype**](eventmanifestschema-channelpublishingtype-complextype.md) " definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**Veröffentlichung (channelType)**](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





