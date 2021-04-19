---
description: Gibt Single Sign-on Netzwerk Konfigurationsinformationen (SSO) an.
ms.assetid: c0a26f15-77fd-43e9-a6af-54e9b46f03fa
title: SingleSignOn (Onex)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- singleSignOn
api_type:
- Schema
api_location: ''
ms.openlocfilehash: fd25767ed311e9a6f0e75f8dec090d4b80d3f0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349397"
---
# <a name="singlesignon-onex-element"></a>SingleSignOn (Onex)-Element

Das Element SingleSignOn (Onex) gibt Single Sign-on Netzwerk Konfigurationsinformationen (SSO) an.

Dieses Element ist optional. Verwenden Sie das SingleSignOn-Element nicht in einem Profil, wenn es vom Netzwerk nicht benötigt wird.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.

``` syntax
<xs:element name="singleSignOn">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="type"
                minOccurs="1"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="preLogon"
                         />
                        <xs:enumeration
                            value="postLogon"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxDelay"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="0"
                         />
                        <xs:enumeration
                            value="120"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="userBasedVirtualLan"
                type="boolean"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Das **SingleSignOn** -Element wird durch das [**Onex**](onexschema-onex-element.md) -Element definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                            | type    | BESCHREIBUNG                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MaxDelay**](onexschema-maxdelay-singlesignon-element.md)                       |         | Gibt die maximale Verzögerung in Sekunden an, bevor der Single Sign-on Verbindungsversuch fehlschlägt.<br/>                                                                                                                      |
| [**Sorte**](onexschema-type-singlesignon-element.md)                               |         | Gibt an, wann Single Sign-on ausgeführt wird. Wenn diese Einstellung auf festgelegt `preLogon` ist, wird Single Sign-on ausgeführt, bevor sich der Benutzer anmeldet. Wenn diese Einstellung auf festgelegt `postLogon` ist, wird Single Sign-on sofort nach der Anmeldung des Benutzers ausgeführt.<br/> |
| [**userbasedvirtuallan**](onexschema-userbasedvirtuallan-singlesignon-element.md) | boolean | Gibt an, ob das vom Gerät verwendete virtuelle LAN (VLAN) basierend auf den Anmelde Informationen des Benutzers geändert wird.<br/>                                                                                                                   |



## <a name="remarks"></a>Bemerkungen

Dieser Parameter kann über die Befehlszeile mit dem **Netsh WLAN Set ProfileParameter** -Befehl festgelegt werden. Weitere Informationen finden Sie unter [Netsh Commands for Wireless Local Area Network (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



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

 

 
