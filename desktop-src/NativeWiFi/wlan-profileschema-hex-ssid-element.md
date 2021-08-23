---
description: Enthält die SSID eines WLAN im Hexadezimalformat.
ms.assetid: 6c49a3e6-f167-408b-a96f-5b6032108f34
title: hex-Element (SSID)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- hex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 666562f7a476505dbb0ff23d5354e0f073505d9dd5195bcae17543294cc5f176
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799890"
---
# <a name="hex-ssid-element"></a>hex-Element (SSID)

Das hexadezimale Element (SSID) enthält die SSID eines WLAN im Hexadezimalformat.

``` syntax
<xs:element name="hex"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="32"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das -Element wird durch das [**SSID-Element**](wlan-profileschema-ssid-ssidconfig-element.md) definiert.

## <a name="remarks"></a>Hinweise

Obwohl die **Hexadezimal-** und Namenselemente [](wlan-profileschema-name-ssid-element.md) optional sind, muss mindestens ein [](wlan-profileschema-name-ssid-element.md) Hexadezimal- oder Namenselement als untergeordnetes Element des [**SSID-Elements angezeigt**](wlan-profileschema-ssid-ssidconfig-element.md) werden. 

Wenn Profilinformationen in eine SSID  konvertiert werden, wird das hexadezimale Element in die SSID konvertiert (sofern vorhanden), und das [**Name-Element**](wlan-profileschema-name-ssid-element.md) wird ignoriert. Wenn das **hexadezimale** Element nicht vorhanden ist, wird das [**Name-Element**](wlan-profileschema-name-ssid-element.md) mithilfe der Unicode-Konvertierung in ASCII in eine SSID konvertiert.

Wenn eine SSID in einem Profil gespeichert wird, wird immer **das hexadezimale** Element generiert. Das [**Name-Element**](wlan-profileschema-name-ssid-element.md) wird nur generiert, wenn sowohl die ASCII- in Unicode-Konvertierung der SSID als auch die XML-Profilgenerierung erfolgreich sind. Einige Informationen aus der ursprünglichen SSID gehen möglicherweise verloren, wenn sie in einen Namen konvertiert [**wird.**](wlan-profileschema-name-ssid-element.md)

## <a name="examples"></a>Beispiele

Ein Beispielprofil, das das **hexadezimale Element** verwendet, finden Sie unter [FIPS-Profilbeispiel.](fips-profile-sample.md)

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

[**Ssid**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




