---
title: showMessageType Complex Type
description: Definiert die Elemente, die eine Aktion darstellen, die ein Meldungsfeld anzeigt.
ms.assetid: eb841d9f-0be2-433b-9002-5e41c6ee78f9
keywords:
- komplexer showMessageType-Typ Taskplaner
topic_type:
- apiref
api_name:
- showMessageType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aeb2c0e1b3ac3e29502e7d998305674aaa283371be6a22324dde6d84c4330326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611242"
---
# <a name="showmessagetype-complex-type"></a>showMessageType Complex Type

Definiert die Elemente, die eine Aktion darstellen, die ein Meldungsfeld anzeigt.

``` syntax
<xs:complexType name="showMessageType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Title"
                    type="nonEmptyString"
                 />
                <xs:element name="Body"
                    type="nonEmptyString"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                            | type           | Beschreibung                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [**Körper**](taskschedulerschema-body-showmessagetype-element.md)   | nonEmptyString | Gibt den Text an, der im Text des Meldungsfelds angezeigt werden soll. <br/> |
| [**Titel**](taskschedulerschema-title-showmessagetype-element.md) | nonEmptyString | Gibt den Titel des Meldungsfelds an. <br/>                       |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





