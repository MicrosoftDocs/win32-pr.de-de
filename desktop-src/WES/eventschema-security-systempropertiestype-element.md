---
title: Security (SystemPropertiesType)-Element
description: Identifiziert den Benutzer, der das Ereignis protokolliert hat.
ms.assetid: f421b0c3-96ea-440c-a3b2-0ddd8f327eec
keywords:
- Security-Element EventLog
topic_type:
- apiref
api_name:
- Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 20aef5465b8790bdba92c50181c0550ca5989c29d66fd53b9ec7ed0f760a2129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118588286"
---
# <a name="security-systempropertiestype-element"></a>Security (SystemPropertiesType)-Element

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

Das **Security-Element** wird vom komplexen [**SystemPropertiesType-Typ**](eventschema-systempropertiestype-complextype.md) definiert.

## <a name="attributes"></a>Attributes



| Name   | Typ   | BESCHREIBUNG                                                          |
|--------|--------|----------------------------------------------------------------------|
| UserID | Zeichenfolge | Die Sicherheits-ID (SID) des Benutzers in Zeichenfolgenform.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**System (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





