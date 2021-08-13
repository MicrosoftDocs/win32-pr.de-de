---
title: Select(QueryType)-Element
description: Eine XPath-Abfrage, die die Ereignisse identifiziert, die in das Abfrageresultset aufgenommen werden sollen.
ms.assetid: b6aa747b-3586-460b-b51c-52fb112739c3
keywords:
- Select-Element EventLog
topic_type:
- apiref
api_name:
- Select
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b38a4f24746425bcdbea845b1c23ea5dadfdbcbefa41ebc5fa502147aba2ec67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587403"
---
# <a name="select-querytype-element"></a>Select(QueryType)-Element

Eine XPath-Abfrage, die die Ereignisse identifiziert, die in das Abfrageresultset aufgenommen werden sollen.

``` syntax
<xs:element name="Select">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

Das **Select-Element** wird durch den komplexen [**QueryType-Typ**](queryschema-querytype-complextype.md) definiert.

## <a name="attributes"></a>Attributes



| Name | Typ   | BESCHREIBUNG                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| `Path` | anyURI | Der Name des Kanals oder der Pfad zur Protokolldatei, die die Ereignisse enthält.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**Query (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





