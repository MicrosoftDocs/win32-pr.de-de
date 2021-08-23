---
description: gibt die EAPHost-Konfiguration an.
ms.assetid: 71ec3ed6-3670-46fc-a24b-580d15297437
title: EAPConfig-Element (OneX)
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
ms.openlocfilehash: 539f30d6730ec0735006f9dd3812322468ce71c7b0fbd90610b6cd589e0d60bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684880"
---
# <a name="eapconfig-onex-element"></a>EAPConfig-Element (OneX)

Das **Element EAPConfig** (OneX) gibt die EAPHost-Konfiguration an.

Im Gegensatz zu den meisten Elementen im 802.1X-Profilschema befindet sich dieses Element im `https://www.microsoft.com/provisioning/EapHostConfig` -Namespace. Die untergeordneten Elemente werden im [eaphostconfig-Schema definiert.](../eaphost/eaphostconfigschema-schema.md) Das [**EapHostConfig-Element**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) ist ein untergeordnetes Element des **EAPConfig-Elements.**

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

Das **EAPConfig-Element** wird durch das [**OneX-Element**](onexschema-onex-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP nur mit \[ SP3-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                |
| Verteilbare Komponente<br/>          | WLAN-API für Windows XP mit SP2<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 
