---
title: komplexer sendEmailType-Typ
description: Definiert den Aktionstyp, mit dem angegeben wird, dass beim Ausführen eines Tasks eine E-Mail gesendet wird. Dieser Typ definiert alle Elemente, die zum Modellieren der E-Mail-Nachricht verwendet werden.
ms.assetid: e384971f-e7e4-4206-9d15-9555dfcbac2f
keywords:
- komplexer sendEmailType-Typ Taskplaner
topic_type:
- apiref
api_name:
- sendEmailType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0242700b2f22050741d9de175b7dae532cc5ef4bb2097fadb23799ce3b2f82b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356342"
---
# <a name="sendemailtype-complex-type"></a>komplexer sendEmailType-Typ

Definiert den Aktionstyp, mit dem angegeben wird, dass beim Ausführen eines Tasks eine E-Mail gesendet wird. Dieser Typ definiert alle Elemente, die zum Modellieren der E-Mail-Nachricht verwendet werden.

``` syntax
<xs:complexType name="sendEmailType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Server"
                    type="nonEmptyString"
                 />
                <xs:element name="Subject"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="To"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Cc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Bcc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="ReplyTo"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="From"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="HeaderFields"
                    type="headerFieldsType"
                    minOccurs="0"
                 />
                <xs:element name="Body"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Attachments"
                    type="attachmentsType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                        | type                                                                         | BESCHREIBUNG                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Attachments**](taskschedulerschema-attachments-sendemailtype-element.md)   | [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md)   | Gibt eine Liste der Anlagen in der E-Mail-Nachricht an.<br/>                                 |
| [**Bcc**](taskschedulerschema-bcc-sendemailtype-element.md)                   | **string**                                                                   | Gibt die E-Mail-Adressen an, die in der Bcc-Zeile einer E-Mail-Nachricht verwendet werden.<br/>               |
| [**Text**](taskschedulerschema-body-sendemailtype-element.md)                 | **string**                                                                   | Gibt den Text im Text der E-Mail an.<br/>                                  |
| [**Cc**](taskschedulerschema-cc-sendemailtype-element.md)                     | **string**                                                                   | Gibt die E-Mail-Adressen an, die in der Cc-Zeile einer E-Mail-Nachricht verwendet werden.<br/>                |
| [**Von**](taskschedulerschema-from-sendemailtype-element.md)                 | **string**                                                                   | Gibt die E-Mail-Adresse des Absenders an.<br/>                                            |
| [**HeaderFields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) | Gibt die Headerfelder und deren Werte an, die im Header der E-Mail-Nachricht verwendet werden.<br/> |
| [**ReplyTo**](taskschedulerschema-replyto-sendemailtype-element.md)           | **string**                                                                   | Gibt die E-Mail-Adressen an, auf die in der E-Mail-Nachricht geantwortet wird.<br/>               |
| [**Server**](taskschedulerschema-server-sendemailtype-element.md)             | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)      | Gibt den E-Mail-Server an, der zum Senden der E-Mail-Nachricht verwendet wird. <br/>                           |
| [**Betreff**](taskschedulerschema-subject-sendemailtype-element.md)           | **string**                                                                   | Gibt den Betreff der E-Mail an.<br/>                                           |
| [**An**](taskschedulerschema-to-sendemailtype-element.md)                     | **string**                                                                   | Gibt die E-Mail-Adressen an, an die die E-Mail gesendet wird.<br/>                        |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





