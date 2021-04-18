---
description: Gibt die EAPHost-Konfiguration an.
ms.assetid: 71ec3ed6-3670-46fc-a24b-580d15297437
title: Eapconfig-Element (Onex)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 955b3647aca787097495b6051407b718dfa91f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347562"
---
# <a name="eapconfig-onex-element"></a>Eapconfig-Element (Onex)

Das **eapconfig** (Onex)-Element gibt die EAPHost-Konfiguration an.

Im Gegensatz zu den meisten Elementen im 802.1 x-Profil Schema befindet sich dieses Element im- `https://www.microsoft.com/provisioning/EapHostConfig` Namespace. Die untergeordneten Elemente werden im [eaphostconfig-Schema](../eaphost/eaphostconfigschema-schema.md)definiert. Das [**eaphostconfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) -Element ist ein untergeordnetes Element des **eapconfig** -Elements.

``` syntax
<xs:element name="EAPConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                minOccurs="1"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Das **eapconfig** -Element wird durch das [**Onex**](onexschema-onex-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                |
| Verteilbare Komponente<br/>          | Drahtlose LAN-API für Windows XP mit SP2<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 
