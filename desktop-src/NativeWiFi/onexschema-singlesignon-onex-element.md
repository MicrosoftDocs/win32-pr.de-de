---
description: Gibt Netzwerkkonfigurationsinformationen für einmaliges Anmelden (Single Sign-On, SSO) an.
ms.assetid: c0a26f15-77fd-43e9-a6af-54e9b46f03fa
title: singleSignOn-Element (OneX)
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
ms.openlocfilehash: 5d0e002133366527624a0954df9054272cc08d894ba8dc3121b8a86b807caab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798031"
---
# <a name="singlesignon-onex-element"></a>singleSignOn-Element (OneX)

Das SingleSignOn-Element (OneX) gibt Netzwerkkonfigurationsinformationen für einmaliges Anmelden (Single Sign-On, SSO) an.

Dieses Element ist optional. Verwenden Sie das singleSignOn-Element nicht in einem Profil, wenn es für das Netzwerk nicht erforderlich ist.

**Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.

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

Das **singleSignOn-Element** wird durch das [**OneX-Element**](onexschema-onex-element.md) definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                            | type    | BESCHREIBUNG                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**maxDelay**](onexschema-maxdelay-singlesignon-element.md)                       |         | Gibt die maximale Verzögerung in Sekunden an, bevor der Verbindungsversuch für einmaliges Anmelden fehlschlägt.<br/>                                                                                                                      |
| [**Typ**](onexschema-type-singlesignon-element.md)                               |         | Gibt an, wann einmaliges Anmelden ausgeführt wird. Wenn auf festgelegt `preLogon` ist, wird einmaliges Anmelden ausgeführt, bevor sich der Benutzer anmeldet. Wenn dies auf festgelegt ist, erfolgt `postLogon` das einmalige Anmelden unmittelbar nach der Anmeldung des Benutzers.<br/> |
| [**userBasedVirtualLan**](onexschema-userbasedvirtuallan-singlesignon-element.md) | boolean | Gibt an, ob sich das vom Gerät verwendete virtuelle LAN (VLAN) basierend auf den Anmeldeinformationen des Benutzers ändert.<br/>                                                                                                                   |



## <a name="remarks"></a>Hinweise

Dieser Parameter kann über die Befehlszeile mit dem Befehl **netsh wlan set profileparameter festgelegt** werden. Weitere Informationen finden Sie unter [Netsh Commands for Wireless Local Area Network (WLAN).](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 
