---
title: clockType (ChannelPublishingType) -Element
description: Die Uhrauflösung, die beim Protokollieren des Zeitstempels für jedes Ereignis verwendet werden soll.
ms.assetid: dc2ed9d0-782c-44c9-aa55-ca6ff340f413
keywords:
- clockType-Element EventLog
topic_type:
- apiref
api_name:
- clockType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fde3b263c2a190e91fdd2ddde8f05a40e9026486195ca9ae95b5f98cdcf7733d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590031"
---
# <a name="clocktype-channelpublishingtype-element"></a>clockType (ChannelPublishingType) -Element

Die Uhrauflösung, die beim Protokollieren des Zeitstempels für jedes Ereignis verwendet werden soll.

``` syntax
<xs:element name="clockType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="SystemTime"
             />
            <xs:enumeration
                value="QPC"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das **clockType-Element** wird durch den komplexen [**ChannelPublishingType-Typ**](eventmanifestschema-channelpublishingtype-complextype.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**publishing (ChannelType)**](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





