---
title: Komplexer KeywordListType-Typ
description: Definiert eine Liste von Schlüsselwörtern, die Ereignisse kategorisieren. | Komplexer KeywordListType-Typ
ms.assetid: 7aeb5ca1-b23f-40f5-a77b-894deaf9c6bb
keywords:
- Komplexer KeywordListType-Typ EventLog
topic_type:
- apiref
api_name:
- KeywordListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: da027136deed48a97b2ea9384bc37a1a45d00650d90b8fd855ea8226e58583aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343646"
---
# <a name="keywordlisttype-complex-type"></a>Komplexer KeywordListType-Typ

Definiert eine Liste von Schlüsselwörtern, die Ereignisse kategorisieren.

``` syntax
<xs:complexType name="KeywordListType">
    <xs:sequence>
        <xs:element name="keyword"
            type="KeywordType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                | type                                                               | BESCHREIBUNG                                                                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Schlüsselwort**](eventmanifestschema-keyword-keywordlisttype-element.md) | [**KeywordType**](eventmanifestschema-keywordtype-complextype.md) | Definiert ein Schlüsselwort, das eine Kategorie von Ereignissen identifiziert. Sie können maximal 48 Schlüsselwörter angeben.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





