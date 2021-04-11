---
description: Enthält Informationen über den Ersteller des Profils.
ms.assetid: a3adb323-d1de-4026-976e-a106007f4cc2
title: Profilekreationtype (mbnprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProfileCreationType
api_type:
- Schema
ms.openlocfilehash: 661306cf53b1ae4c7c9cd49a295afe5b84dabd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129569"
---
# <a name="profilecreationtype-mbnprofile-element"></a>Profilekreationtype (mbnprofile)-Element

Das **profilekreationtype (mbnprofile)** -Element enthält Informationen zum Ersteller des Profils.

Dieses Element kann einen der folgenden Werte aufweisen.



| Wert                 | Bedeutung                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| "Userprovisioned"     | Dieses Profil wird von Informationen erstellt, die vom Benutzer des Geräts bereitgestellt werden.                                                     |
| "Adminprovisioned"    | Dieses Profil wird von IT-Administratoren erstellt und an Benutzer verteilt.                                                     |
| "Operatorprovisioned" | Dieses Profil wird von einem Netzwerk Operator erstellt und an Benutzer verteilt.                                                    |
| "Deviceprovisioned"   | Dieses Profil wird vom mobilen Breitbanddienst erstellt, indem die Informationen verwendet werden, die im bereitgestellten Gerätekontext gespeichert wurden. |



 

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

Das **profilekreationtype** -Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Mbnprofile**](schema-mbnprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Mbnprofile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




