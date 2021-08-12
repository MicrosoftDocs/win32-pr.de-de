---
title: sidType(ChannelPublishingType)-Element
description: Bestimmt, ob eine Sicherheits-ID (SID) des Prinzipals mit jedem ereignis in den Kanal geschrieben werden soll.
ms.assetid: 3ce176a3-9e21-4646-8c99-7beb687e6847
keywords:
- sidType-Element EventLog
topic_type:
- apiref
api_name:
- sidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41653a1fbda3400b74ca5302deb8075ae891e69f22ca0f0e88b6ec4dbb58dfc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589151"
---
# <a name="sidtype-channelpublishingtype-element"></a>sidType(ChannelPublishingType)-Element

Bestimmt, ob eine Sicherheits-ID (SID) des Prinzipals mit jedem ereignis in den Kanal geschrieben werden soll.

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

Das **sidType-Element** wird vom komplexen [**ChannelPublishingType-Typ**](eventmanifestschema-channelpublishingtype-complextype.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**publishing (ChannelType)**](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





