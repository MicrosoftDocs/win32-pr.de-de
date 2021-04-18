---
title: Komplexer keywordlisttype-Typ
description: Definiert eine Liste von Schlüsselwörtern zum Kategorisieren von Ereignissen. | Komplexer keywordlisttype-Typ
ms.assetid: 7aeb5ca1-b23f-40f5-a77b-894deaf9c6bb
keywords:
- Keywordlisttype, komplexer Typ EventLog
topic_type:
- apiref
api_name:
- KeywordListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7132e2e85015aaf9d38adbd6278ea4d3e1296446
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365262"
---
# <a name="keywordlisttype-complex-type"></a>Komplexer keywordlisttype-Typ

Definiert eine Liste von Schlüsselwörtern zum Kategorisieren von Ereignissen.

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
| [**Schlüsselwort**](eventmanifestschema-keyword-keywordlisttype-element.md) | [**Keywordtype**](eventmanifestschema-keywordtype-complextype.md) | Definiert ein Schlüsselwort, das eine Kategorie von Ereignissen bezeichnet. Sie können maximal 48 Schlüsselwörter angeben.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





