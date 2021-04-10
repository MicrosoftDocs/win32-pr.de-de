---
title: komplexer showmessagetype-Typ
description: Definiert die Elemente, die eine Aktion darstellen, die ein Meldungs Feld anzeigt.
ms.assetid: eb841d9f-0be2-433b-9002-5e41c6ee78f9
keywords:
- komplexer showmessagetype-Typ Taskplaner
topic_type:
- apiref
api_name:
- showMessageType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d65ed893bce63c95fffcf237d3a3a95ebb1550d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956760"
---
# <a name="showmessagetype-complex-type"></a>komplexer showmessagetype-Typ

Definiert die Elemente, die eine Aktion darstellen, die ein Meldungs Feld anzeigt.

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



| Element                                                            | type           | BESCHREIBUNG                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [**Text**](taskschedulerschema-body-showmessagetype-element.md)   | nonEmptyString | Gibt den Text an, der im Textkörper des Meldungs Felds angezeigt werden soll. <br/> |
| [**Titel**](taskschedulerschema-title-showmessagetype-element.md) | nonEmptyString | Gibt den Titel des Meldungs Felds an. <br/>                       |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





