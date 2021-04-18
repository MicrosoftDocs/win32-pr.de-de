---
title: komplexer sendemailtype-Typ
description: Definiert den Aktionstyp, der verwendet wird, um anzugeben, dass eine e-Mail gesendet wird, wenn eine Aufgabe ausgeführt wird. Dieser Typ definiert alle Elemente, die zum Modellieren der e-Mail-Nachricht verwendet werden.
ms.assetid: e384971f-e7e4-4206-9d15-9555dfcbac2f
keywords:
- komplexer sendemailtype-Typ Taskplaner
topic_type:
- apiref
api_name:
- sendEmailType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 959e0b8f03223eb23b7a7bec69ba9b2aeea66447
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341040"
---
# <a name="sendemailtype-complex-type"></a>komplexer sendemailtype-Typ

Definiert den Aktionstyp, der verwendet wird, um anzugeben, dass eine e-Mail gesendet wird, wenn eine Aufgabe ausgeführt wird. Dieser Typ definiert alle Elemente, die zum Modellieren der e-Mail-Nachricht verwendet werden.

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
| [**Attachments**](taskschedulerschema-attachments-sendemailtype-element.md)   | [**attachmentstype**](taskschedulerschema-attachmentstype-complextype.md)   | Gibt eine Liste der Anlagen in der e-Mail-Nachricht an.<br/>                                 |
| [**Bcc**](taskschedulerschema-bcc-sendemailtype-element.md)                   | **string**                                                                   | Gibt die e-Mail-Adressen an, die in der Bcc-Zeile einer e-Mail verwendet werden.<br/>               |
| [**Text**](taskschedulerschema-body-sendemailtype-element.md)                 | **string**                                                                   | Gibt den Text im Textkörper der e-Mail-Nachricht an.<br/>                                  |
| [**125**](taskschedulerschema-cc-sendemailtype-element.md)                     | **string**                                                                   | Gibt die e-Mail-Adressen an, die in der CC-Zeile einer e-Mail verwendet werden.<br/>                |
| [**From**](taskschedulerschema-from-sendemailtype-element.md)                 | **string**                                                                   | Gibt die e-Mail-Adresse des Absenders an.<br/>                                            |
| [**Headerfields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerfieldstype**](taskschedulerschema-headerfieldstype-complextype.md) | Gibt die Header Felder und deren Werte an, die im Header der e-Mail-Nachricht verwendet werden.<br/> |
| [**ReplyTo**](taskschedulerschema-replyto-sendemailtype-element.md)           | **string**                                                                   | Gibt die e-Mail-Adressen an, auf die in der e-Mail geantwortet wird.<br/>               |
| [**Servers**](taskschedulerschema-server-sendemailtype-element.md)             | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)      | Gibt den e-Mail-Server an, mit dem die e-Mail gesendet wird. <br/>                           |
| [**Subject**](taskschedulerschema-subject-sendemailtype-element.md)           | **string**                                                                   | Gibt den Betreff der e-Mail-Nachricht an.<br/>                                           |
| [**An**](taskschedulerschema-to-sendemailtype-element.md)                     | **string**                                                                   | Gibt die e-Mail-Adressen an, an die die e-Mail gesendet wird.<br/>                        |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





