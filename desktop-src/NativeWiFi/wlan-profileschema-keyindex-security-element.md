---
description: Gibt an, welcher Schlüssel Index verwendet werden soll, um drahtlosen Datenverkehr zu verschlüsseln. Dies wird nur verwendet, wenn KeyType auf &\# 0034; networkkey&0034; festgelegt ist \# .
ms.assetid: 5629605d-4c23-4318-8f09-939e13302552
title: KeyIndex (Security)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyIndex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 43bb802d46abb3c4684b63206377d3464078e2c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131937"
---
# <a name="keyindex-security-element"></a>KeyIndex (Security)-Element

Das KeyIndex (Security)-Element gibt an, welcher Schlüssel Index verwendet werden soll, um drahtlosen Datenverkehr zu verschlüsseln. Dies wird nur verwendet, wenn [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) auf "networkkey" festgelegt ist.

``` syntax
<xs:element name="keyIndex"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="0"
             />
            <xs:maxInclusive
                value="3"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das-Element wird durch das [**Security**](wlan-profileschema-security-msm-element.md) -Element definiert.

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

[**Sicherung**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Sicherheit (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




