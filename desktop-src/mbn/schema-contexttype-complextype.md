---
description: Gibt den Konnenktionskontext eines mobilen Breitbandgeräts an.
ms.assetid: 513e744d-bd62-43e9-a636-6690867d8b9b
title: contextType Complex Type
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- contextType
api_type:
- Schema
ms.openlocfilehash: 58189cf27f667b3d7e5e6c387a52143b8c757724106e8d9941d31d2582002b0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118744447"
---
# <a name="contexttype-complex-type"></a>contextType Complex Type

Der **komplexe contextType-Typ** gibt den Konnenktionskontext eines mobilen Breitbandgeräts an.

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



| Element                                                               | type                                           | Beschreibung                                                                                    |
|-----------------------------------------------------------------------|------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**AccessString**](schema-accessstring-contexttype-element.md)       |                                                | APN oder Wählzeichenfolge zum Herstellen einer Datenverbindung<br/>                        |
| [**AuthProtocol**](schema-authprotocol-contexttype-element.md)       |                                                | Authentifizierungsprotokoll, das zum Aktivieren eines PDP-Kontexts verwendet werden soll.<br/>                    |
| [**Komprimierung**](schema-compression-contexttype-element.md)         |                                                | Gibt an, ob die Komprimierung an der Datenverknüpfung für Header und Datenübertragung verwendet wird.<br/> |
| [**IgnorePassword**](schema-ignorepassword-userlogoncred-element.md) | boolean                                        | Behandeln von Kennwörtern beim Aktualisieren von Profilen.<br/>                                    |
| [**Passwort**](schema-password-userlogoncred-element.md)             | Zeichenfolge                                         | Kennwort zum Authentifizieren eines Benutzers<br/>                                                |
| [**UserLogonCred**](schema-userlogoncred-contexttype-element.md)     |                                                | Melden Sie sich anmeldeinformationen für eine Verbindung an.<br/>                                                |
| [**Nutzername**](schema-username-userlogoncred-element.md)             | [**nameType**](schema-nametype-simpletype.md) | Benutzername für die Anmeldung<br/>                                                                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



 

 




