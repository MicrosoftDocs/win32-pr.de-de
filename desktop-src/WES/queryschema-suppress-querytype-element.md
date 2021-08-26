---
title: Suppress(QueryType)-Element
description: Eine XPath-Abfrage, die die Ereignisse identifiziert, die aus dem Abfrageresultset ausgeschlossen werden sollen.
ms.assetid: 41304a3c-bde1-49c3-8cb3-e95fc428bd96
keywords:
- Suppress-Element EventLog
topic_type:
- apiref
api_name:
- Suppress
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2612a98c282627154a9107f2f9f77a3ddb52c191e00dbcb394c8db4d7c796b79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032010"
---
# <a name="suppress-querytype-element"></a>Suppress(QueryType)-Element

Eine XPath-Abfrage, die die Ereignisse identifiziert, die aus dem Abfrageresultset ausgeschlossen werden sollen.

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

Das **Suppress-Element** wird vom komplexen [**QueryType-Typ**](queryschema-querytype-complextype.md) definiert.

## <a name="attributes"></a>Attributes



| Name | type   | BESCHREIBUNG                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| `Path` | anyURI | Der Name des Kanals oder der Pfad zur Protokolldatei, die die Ereignisse enthält.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**Query (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





