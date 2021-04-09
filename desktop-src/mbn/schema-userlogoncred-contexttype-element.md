---
description: Enthält Anmelde Informationen für eine Verbindung.
ms.assetid: 79c1d277-6284-4adb-a1bd-6c207b37e33e
title: Userlogonkred (ContextType)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserLogonCred
api_type:
- Schema
ms.openlocfilehash: d3dc0c22d6242ee894545bd61f839574afd06141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129564"
---
# <a name="userlogoncred-contexttype-element"></a>Userlogonkred (ContextType)-Element

Das **userlogonkred (ContextType)-** Element enthält Anmelde Informationen für eine Verbindung.

Dieses Element kann die folgenden untergeordneten Elemente aufweisen.

-   [**User**](schema-username-userlogoncred-element.md)
-   [**Kennwort**](schema-password-userlogoncred-element.md)
-   [**Ignorepassword**](schema-ignorepassword-userlogoncred-element.md)

Dieses Element kann maximal ein Vorkommen aufweisen.

Dieses Element ist optional.

``` syntax
<xs:element name="UserLogonCred">
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
```

Das **userlogonkred-** Element wird durch den komplexen [**ContextType**](schema-contexttype-complextype.md) -Typ definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                               | type                                           | BESCHREIBUNG                                                 |
|-----------------------------------------------------------------------|------------------------------------------------|-------------------------------------------------------------|
| [**Ignorepassword**](schema-ignorepassword-userlogoncred-element.md) | boolean                                        | Behandeln von Kenn Wörtern beim Aktualisieren von Profilen<br/> |
| [**Anmelden**](schema-password-userlogoncred-element.md)             | Zeichenfolge                                         | Benutzerkennwort.<br/>                                   |
| [**User**](schema-username-userlogoncred-element.md)             | [**nametype**](schema-nametype-simpletype.md) | Benutzername.<br/>                                       |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Kontext (mbnprofile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




