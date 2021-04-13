---
title: Select (QueryType)-Element
description: Eine XPath-Abfrage, die die Ereignisse identifiziert, die im Resultset der Abfrage enthalten sein sollen.
ms.assetid: b6aa747b-3586-460b-b51c-52fb112739c3
keywords:
- Element "EventLog" auswählen
topic_type:
- apiref
api_name:
- Select
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b1735f5de49853357eed1ce00b8d181edf2279ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392156"
---
# <a name="select-querytype-element"></a>Select (QueryType)-Element

Eine XPath-Abfrage, die die Ereignisse identifiziert, die im Resultset der Abfrage enthalten sein sollen.

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

Das **Select** -Element wird durch den komplexen Typ [**QueryType**](queryschema-querytype-complextype.md) definiert.

## <a name="attributes"></a>Attributes



| Name | type   | BESCHREIBUNG                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| `Path` | anyURI | Der Name des Kanals oder der Pfad zu der Protokolldatei, in der die Ereignisse enthalten sind.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**Query (querylisttype)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





