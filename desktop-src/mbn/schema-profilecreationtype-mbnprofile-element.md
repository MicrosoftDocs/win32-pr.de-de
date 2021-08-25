---
description: Enthält Informationen zum Ersteller des Profils.
ms.assetid: a3adb323-d1de-4026-976e-a106007f4cc2
title: ProfileCreationType (MBNProfile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProfileCreationType
api_type:
- Schema
ms.openlocfilehash: ddf3e70607cedbaed45da19651ec73736a54bfafab197e95d2cd634d8e3833f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959840"
---
# <a name="profilecreationtype-mbnprofile-element"></a>ProfileCreationType (MBNProfile)-Element

Das **Element ProfileCreationType (MBNProfile)** enthält Informationen zum Ersteller des Profils.

Dieses Element kann einen der folgenden Werte haben.



| Wert                 | Bedeutung                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| "UserProvisioned"     | Dieses Profil wird durch Informationen erstellt, die vom Benutzer des Geräts bereitgestellt werden.                                                     |
| "AdminProvisioned"    | Dieses Profil wird von IT-Administratoren erstellt und an Benutzer verteilt.                                                     |
| "OperatorProvisioned" | Dieses Profil wird von einem Netzbetreiber erstellt und an Benutzer verteilt.                                                    |
| "DeviceProvisioned"   | Dieses Profil wird vom Mobile Broadband-Dienst mithilfe der im gerätebereitstellungskontext gespeicherten Informationen erstellt. |



 

Dies ist ein optionales Element.

``` syntax
<xs:element name="ProfileCreationType">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="UserProvisioned"
             />
            <xs:enumeration
                value="AdminProvisioned"
             />
            <xs:enumeration
                value="OperatorProvisioned"
             />
            <xs:enumeration
                value="DeviceProvisioned"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das **ProfileCreationType-Element** wird durch das [**MBNProfile-Element**](schema-mbnprofile-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




