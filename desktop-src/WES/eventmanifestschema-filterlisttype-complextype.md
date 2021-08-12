---
title: Komplexer FilterListType-Typ
description: Definiert eine Liste von Filtern, die ein ETW-Controller an Ihren Anbieter übergeben kann, um die von ihm zu schreibenden Ereignisse weiter zu begrenzen.
ms.assetid: 27f7b150-1264-4a12-858e-b0b0dff5baa7
keywords:
- Komplexer FilterListType-Typ EventLog
topic_type:
- apiref
api_name:
- FilterListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b66ccc002372159540895dfbe95786921266320bb4d3a4e6827085ae7822c12c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589625"
---
# <a name="filterlisttype-complex-type"></a>Komplexer FilterListType-Typ

Definiert eine Liste von Filtern, die ein ETW-Controller an Ihren Anbieter übergeben kann, um die von ihm zu schreibenden Ereignisse weiter zu begrenzen.

``` syntax
<xs:complexType name="FilterListType">
    <xs:sequence>
        <xs:element name="filter"
            type="FilterType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element    | Typ                                                             | BESCHREIBUNG                   |
|------------|------------------------------------------------------------------|-------------------------------|
| **filter** | [**FilterType**](eventmanifestschema-filtertype-complextype.md) | Eine Liste von Filtern.<br/> |



## <a name="remarks"></a>Bemerkungen

Ein ETW-Controller ist eine Anwendung, die die [**StartTrace-Funktion**](/windows/desktop/ETW/starttrace) aufruft, um eine ETW-Sitzung zu erstellen. Weitere Informationen finden Sie unter [Steuern von Ereignisablaufverfolgungssitzungen.](/windows/desktop/ETW/controlling-event-tracing-sessions) Der Controller kann die [**TdhEnumerateProviderFilters-Funktion**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) verwenden, um die von Ihnen festgelegten Filter zu aufzählen. Der Controller kann dann einen oder mehrere Filter übergeben, wenn er die [**EnableTraceEx2-Funktion**](/windows/desktop/ETW/enabletraceex2) aufruft, um Ihren Anbieter zu aktivieren. Ihr Anbieter empfängt die Filter zusammen mit den restlichen Aktivierungsparametern in Ihrer [*EnableCallback-Rückruffunktion.*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



 

