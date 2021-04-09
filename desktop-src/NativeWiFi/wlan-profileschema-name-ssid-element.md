---
description: Enthält die SSID eines drahtlosen LANs.
ms.assetid: ed23ccd0-9b44-4c97-a5ed-93e86632b819
title: Name (SSID)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: dbb1301de2a2d70edf8c61de002c28e48b00a5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867279"
---
# <a name="name-ssid-element"></a>Name (SSID)-Element

Das Name (SSID)-Element enthält die SSID eines drahtlosen LANs.

``` syntax
<xs:element name="name">
    <xs:simpleType>
        <xs:restriction
            base="string"
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

Bei Namen wird Groß-/Kleinschreibung beachtet.

Obwohl das [**Hex**](wlan-profileschema-hex-ssid-element.md) -Element und das **Name** -Element optional sind, muss mindestens ein **Hex** -oder **Name** -Element als untergeordnetes Element des [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) -Elements angezeigt werden.

Wenn Profilinformationen in eine SSID konvertiert werden, wird das [**Hex**](wlan-profileschema-hex-ssid-element.md) -Element in die SSID (sofern vorhanden) konvertiert, und das **Name** -Element wird ignoriert. Wenn das **Hex** -Element nicht vorhanden ist, wird das **Name** -Element mithilfe der Unicode-in-ASCII-Konvertierung in eine SSID konvertiert.

Wenn eine SSID in einem Profil gespeichert wird, wird das [**Hex**](wlan-profileschema-hex-ssid-element.md) -Element immer generiert. Das **Name** -Element wird nur generiert, wenn sowohl die ASCII-als auch die Unicode-Konvertierung der SSID und die Generierung des XML-Profils erfolgreich sind. Einige Informationen aus der ursprünglichen SSID können verloren gehen, wenn Sie in einen **Namen** konvertiert werden.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** XML-Escapezeichen, wie z. b. &, werden nicht angezeigt. Vermeiden Sie die Verwendung von XML-Escapezeichen in SSID-Namen für Profile, die unter Windows XP mit SP3 und Wireless LAN API für Windows XP SP2 bereitgestellt werden.

## <a name="examples"></a>Beispiele

Beispiel Profile, die das **Name** -Element verwenden, finden Sie unter [Beispiele für Funk profile](wireless-profile-samples.md).

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

 

 




