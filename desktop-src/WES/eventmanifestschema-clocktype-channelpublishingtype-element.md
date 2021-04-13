---
title: clocktype (channelpublishingtype)-Element
description: Die zu verwendende Takt Auflösung, wenn der Zeitstempel für jedes Ereignis protokolliert wird.
ms.assetid: dc2ed9d0-782c-44c9-aa55-ca6ff340f413
keywords:
- clocktype-Element EventLog
topic_type:
- apiref
api_name:
- clockType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6b85537ec209f39da87e74db6881abdf60e488b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391597"
---
# <a name="clocktype-channelpublishingtype-element"></a>clocktype (channelpublishingtype)-Element

Die zu verwendende Takt Auflösung, wenn der Zeitstempel für jedes Ereignis protokolliert wird.

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

Das Element " **clocktype** " wird vom komplexen Typ " [**channelpublishingtype**](eventmanifestschema-channelpublishingtype-complextype.md) " definiert.

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

 

 





