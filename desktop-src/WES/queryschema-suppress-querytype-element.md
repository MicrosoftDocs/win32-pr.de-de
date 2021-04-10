---
title: Unterdrücken (QueryType)-Element
description: Eine XPath-Abfrage, die die aus dem Abfrageresultset auszuschließenden Ereignisse identifiziert.
ms.assetid: 41304a3c-bde1-49c3-8cb3-e95fc428bd96
keywords:
- Element EventLog unterdrücken
topic_type:
- apiref
api_name:
- Suppress
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a1d7fcec98d32167155ebcafc4f13d2a727d59a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106329"
---
# <a name="suppress-querytype-element"></a>Unterdrücken (QueryType)-Element

Eine XPath-Abfrage, die die aus dem Abfrageresultset auszuschließenden Ereignisse identifiziert.

``` syntax
<xs:element name="Suppress">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

Das unter **drücken** -Element wird durch den komplexen [**QueryType**](queryschema-querytype-complextype.md) -Typ definiert.

## <a name="attributes"></a>Attributes



| Name | type   | BESCHREIBUNG                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| `Path` | anyURI | Der Name des Kanals oder der Pfad zu der Protokolldatei, in der die Ereignisse enthalten sind.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**Query (querylisttype)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





