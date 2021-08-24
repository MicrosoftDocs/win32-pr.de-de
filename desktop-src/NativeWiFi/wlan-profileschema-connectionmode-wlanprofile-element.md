---
description: Gibt an, ob die Verbindung mit einem WLAN automatisch oder vom Benutzer initiiert werden soll.
ms.assetid: 0fad8392-3053-494b-9b30-1db85408a437
title: connectionMode-Element (WLANProfile)
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
ms.openlocfilehash: a6ef18eff8ba27a3169399f1f10e0707c4e0b3c010d54830ad8f8f997c5e1b50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684440"
---
# <a name="connectionmode-wlanprofile-element"></a>connectionMode-Element (WLANProfile)

Das connectionMode-Element (WLANProfile) gibt an, ob die Verbindung mit einem WLAN automatisch oder vom Benutzer initiiert werden soll.

Wenn [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) auf ESS festgelegt ist, kann dieser Wert entweder automatisch oder manuell sein. Der Standardwert ist auto, wenn dieses Element nicht vorhanden ist.

Wenn [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) auf IBSS festgelegt ist, muss dieser Wert manuell sein.

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

Das **connectionMode-Element** wird durch das [**WLANProfile-Element**](wlan-profileschema-wlanprofile-element.md) definiert.

## <a name="remarks"></a>Hinweise

In der folgenden Tabelle werden die Enumerationswerte beschrieben.



| Wert  | Beschreibung                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| auto   | Die Verbindung mit dem Drahtlosnetzwerk sollte automatisch initiiert werden, wenn sich das Netzwerk in Reichweite befindet. |
| manual | Die Verbindung mit dem Drahtlosnetzwerk wird nur auf explizite Anforderung eines Benutzers hergestellt.               |



 

## <a name="examples"></a>Beispiele

Beispielprofile, die das **connectionMode-Element** verwenden, finden Sie unter [Beispiele für Funkprofile.](wireless-profile-samples.md)

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

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




