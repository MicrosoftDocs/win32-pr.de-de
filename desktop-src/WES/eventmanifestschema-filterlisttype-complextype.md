---
title: Komplexer filterlisttype-Typ
description: Definiert eine Liste von Filtern, die von einem etw-Controller an Ihren Anbieter übergeben werden können, um die zu schreibenden Ereignisse weiter einzuschränken.
ms.assetid: 27f7b150-1264-4a12-858e-b0b0dff5baa7
keywords:
- Filterlisttype Complex-Typ EventLog
topic_type:
- apiref
api_name:
- FilterListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d1071fbbb9eba6bf6ebf0d74d4caaac50e1ccce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341217"
---
# <a name="filterlisttype-complex-type"></a>Komplexer filterlisttype-Typ

Definiert eine Liste von Filtern, die von einem etw-Controller an Ihren Anbieter übergeben werden können, um die zu schreibenden Ereignisse weiter einzuschränken.

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



| Element    | type                                                             | BESCHREIBUNG                   |
|------------|------------------------------------------------------------------|-------------------------------|
| **filter** | [**Filter Type**](eventmanifestschema-filtertype-complextype.md) | Eine Liste mit Filtern.<br/> |



## <a name="remarks"></a>Bemerkungen

Ein etw-Controller ist eine Anwendung, die die [**Start Trace**](/windows/desktop/ETW/starttrace) -Funktion aufruft, um eine ETW-Sitzung zu erstellen. Weitere Informationen finden Sie unter [Steuern von Ereignis Ablauf Verfolgungs Sitzungen](/windows/desktop/ETW/controlling-event-tracing-sessions). Der Controller kann die [**tdhenumerateproviderfilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) -Funktion verwenden, um die von Ihnen definierten Filter aufzuzählen. Der Controller kann dann einen oder mehrere der Filter übergeben, wenn die [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) -Funktion aufgerufen wird, um den Anbieter zu aktivieren. Der Anbieter empfängt die Filter zusammen mit den restlichen enable-Parametern in Ihrer [*enablecallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) -Rückruffunktion.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



 

