---
title: weeksType Complex Type
description: Definiert das untergeordnete Element und Sequenzierungsinformationen für das Week-Element.
ms.assetid: c9e8814c-b8f9-426d-943d-ca3efa5d914b
keywords:
- weeksType complex type Taskplaner
topic_type:
- apiref
api_name:
- weeksType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 876d798acdf1f8684fc4f2cecac8e77bceb73dddd0036f2117d4bb55a77a71ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757987"
---
# <a name="weekstype-complex-type"></a>weeksType Complex Type

Definiert das untergeordnete Element und [](taskschedulerschema-week-weekstype-element.md) Sequenzierungsinformationen für das Week-Element.

``` syntax
<xs:complexType name="weeksType">
    <xs:sequence>
        <xs:element name="Week"
            type="weekType"
            minOccurs="0"
            maxOccurs="5"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                    | type                                                        | Beschreibung                                             |
|------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------|
| [**Woche**](taskschedulerschema-week-weekstype-element.md) | [**weekType**](taskschedulerschema-weektype-simpletype.md) | Gibt die Woche an, in der der Task ausgeführt wird.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





