---
description: Gibt den konnenction-Kontext eines mobilen Breitband Geräts an.
ms.assetid: 513e744d-bd62-43e9-a636-6690867d8b9b
title: komplexer ContextType-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- contextType
api_type:
- Schema
ms.openlocfilehash: 63d221c6bd388196abfb73a8ac38a26de516d0df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345709"
---
# <a name="contexttype-complex-type"></a>komplexer ContextType-Typ

Der komplexe Typ " **ContextType** " gibt den konnenction-Kontext eines mobilen Breitband Geräts an.

``` syntax
<xs:complexType name="contextType">
    <xs:sequence>
        <xs:element name="AccessString"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:minLength
                        value="1"
                     />
                    <xs:maxLength
                        value="100"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="UserLogonCred"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="UserName"
                        type="nameType"
                     />
                    <xs:element name="IgnorePassword"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:element name="Compression"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="DISABLE"
                     />
                    <xs:enumeration
                        value="ENABLE"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="AuthProtocol"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="NONE"
                     />
                    <xs:enumeration
                        value="PAP"
                     />
                    <xs:enumeration
                        value="CHAP"
                     />
                    <xs:enumeration
                        value="MsCHAPv2"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                               | type                                           | BESCHREIBUNG                                                                                    |
|-----------------------------------------------------------------------|------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**AccessString**](schema-accessstring-contexttype-element.md)       |                                                | Zum Herstellen einer Datenverbindung zu verwendende APN-oder Wähl Zeichenfolge<br/>                        |
| [**AuthProtocol**](schema-authprotocol-contexttype-element.md)       |                                                | Das Authentifizierungsprotokoll, das zum Aktivieren eines PDP-Kontexts verwendet werden soll.<br/>                    |
| [**Komprimi**](schema-compression-contexttype-element.md)         |                                                | Gibt an, ob die Komprimierung beim Daten Link für Header und Datenübertragung verwendet wird.<br/> |
| [**Ignorepassword**](schema-ignorepassword-userlogoncred-element.md) | boolean                                        | Behandeln von Kenn Wörtern beim Aktualisieren von Profilen<br/>                                    |
| [**Anmelden**](schema-password-userlogoncred-element.md)             | Zeichenfolge                                         | Zum Authentifizieren eines Benutzers verwendetes Kennwort<br/>                                                |
| [**UserLogonCred**](schema-userlogoncred-contexttype-element.md)     |                                                | Anmelde Informationen für eine Verbindung anmelden.<br/>                                                |
| [**User**](schema-username-userlogoncred-element.md)             | [**nametype**](schema-nametype-simpletype.md) | Benutzername für die Anmeldung<br/>                                                                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



 

 




