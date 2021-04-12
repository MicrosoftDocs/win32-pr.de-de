---
title: Security-Element (systempropertiestype)
description: Identifiziert den Benutzer, der das Ereignis protokolliert hat.
ms.assetid: f421b0c3-96ea-440c-a3b2-0ddd8f327eec
keywords:
- Sicherheitselement-Ereignisprotokoll
topic_type:
- apiref
api_name:
- Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b793193d7afdfde5fd515252a024432ed45ff8b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105795"
---
# <a name="security-systempropertiestype-element"></a>Security-Element (systempropertiestype)

Identifiziert den Benutzer, der das Ereignis protokolliert hat.

``` syntax
<xs:element name="Security">
    <xs:complexType>
        <xs:attribute name="UserID"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

Das **Security** -Element wird durch den komplexen [**systempropertiestype**](eventschema-systempropertiestype-complextype.md) -Typ definiert.

## <a name="attributes"></a>Attributes



| Name   | type   | BESCHREIBUNG                                                          |
|--------|--------|----------------------------------------------------------------------|
| UserID | Zeichenfolge | Die Sicherheits-ID (SID) des Benutzers in Form einer Zeichenfolge.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**System (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





