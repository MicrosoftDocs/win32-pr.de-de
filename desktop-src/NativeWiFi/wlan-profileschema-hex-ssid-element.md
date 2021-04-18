---
description: Enthält die SSID eines Drahtlos-LANs im Hexadezimal Format.
ms.assetid: 6c49a3e6-f167-408b-a96f-5b6032108f34
title: Hex (SSID)-Element
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
ms.openlocfilehash: 6bc214f50788fdc6965a1ce429c5c2919846cf72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368120"
---
# <a name="hex-ssid-element"></a>Hex (SSID)-Element

Das Hex (SSID)-Element enthält die SSID eines drahtlosen LANs im Hexadezimal Format.

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

Das-Element wird durch das [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Obwohl das **Hex** -Element und das [**Name**](wlan-profileschema-name-ssid-element.md) -Element optional sind, muss mindestens ein **Hex** -oder [**Name**](wlan-profileschema-name-ssid-element.md) -Element als untergeordnetes Element des [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) -Elements angezeigt werden.

Wenn Profilinformationen in eine SSID konvertiert werden, wird das **Hex** -Element in die SSID (sofern vorhanden) konvertiert, und das [**Name**](wlan-profileschema-name-ssid-element.md) -Element wird ignoriert. Wenn das **Hex** -Element nicht vorhanden ist, wird das [**Name**](wlan-profileschema-name-ssid-element.md) -Element mithilfe der Unicode-in-ASCII-Konvertierung in eine SSID konvertiert.

Wenn eine SSID in einem Profil gespeichert wird, wird das **Hex** -Element immer generiert. Das [**Name**](wlan-profileschema-name-ssid-element.md) -Element wird nur generiert, wenn sowohl die ASCII-als auch die Unicode-Konvertierung der SSID und die Generierung des XML-Profils erfolgreich sind. Einige Informationen aus der ursprünglichen SSID können verloren gehen, wenn Sie in einen [**Namen**](wlan-profileschema-name-ssid-element.md)konvertiert werden.

## <a name="examples"></a>Beispiele

Ein Beispiel Profil, das das **Hex** -Element verwendet, finden Sie unter Beispiel für ein Beispiel für den [PPS-Profil](fips-profile-sample.md)

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

[**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**SSID (ssidconfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




