---
description: Gibt an, ob die Verbindung mit einem Drahtlos LAN automatisch oder vom Benutzer initiiert werden soll.
ms.assetid: 0fad8392-3053-494b-9b30-1db85408a437
title: ConnectionMode (wlanprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 3dafb9561bf8b5e3c5c66eb23bd5e286cbd38118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753753"
---
# <a name="connectionmode-wlanprofile-element"></a>ConnectionMode (wlanprofile)-Element

Das ConnectionMode (wlanprofile)-Element gibt an, ob die Verbindung mit einem Drahtlos LAN automatisch oder vom Benutzer initiiert werden soll.

Wenn [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) auf ESS festgelegt ist, kann dieser Wert entweder "Auto" oder "Manual" lauten. Der Standardwert ist Auto, wenn dieses Element nicht vorhanden ist.

Wenn [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) auf IBSS festgelegt ist, muss dieser Wert manuell lauten.

``` syntax
<xs:element name="connectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="manual"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das **ConnectionMode** -Element wird durch das [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

In der folgenden Tabelle werden die-Enumerationswerte beschrieben.



| Wert  | BESCHREIBUNG                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| auto   | Die Verbindung mit dem Drahtlos Netzwerk sollte automatisch initiiert werden, wenn das Netzwerk in Reichweite ist. |
| manual | Die Verbindung mit dem Drahtlos Netzwerk wird nur bei der expliziten Anforderung eines Benutzers hergestellt.               |



 

## <a name="examples"></a>Beispiele

Beispiel Profile, die das **ConnectionMode** -Element verwenden, finden Sie unter [Beispiele für Funk profile](wireless-profile-samples.md).

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

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




