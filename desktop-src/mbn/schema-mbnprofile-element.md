---
description: Das Stammelement, das ein mobiles Breitbandprofil identifiziert.
ms.assetid: 08302e7f-3024-439b-a2ad-a4ae9487b82b
title: MBNProfile-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MBNProfile
api_type:
- Schema
ms.openlocfilehash: 049ec22c170afda3a46620e2e94e2a16ae2708b4d6a69fcd0262baa69352a0a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943360"
---
# <a name="mbnprofile-element"></a>MBNProfile-Element

Das **MBNProfile-Element** ist das Stammelement, das ein mobiles Breitbandprofil identifiziert.

Pro Dokument kann nur ein Element dieses Typs vorhanden sein.

``` syntax
<xs:element name="MBNProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="nameType"
             />
            <xs:element name="Description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="ICONFilePath"
                type="iconFileType"
                minOccurs="0"
             />
            <xs:element name="IsDefault"
                type="boolean"
             />
            <xs:element name="ProfileCreationType"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="token"
                    >
                        <xs:enumeration
                            value="UserProvisioned"
                         />
                        <xs:enumeration
                            value="AdminProvisioned"
                         />
                        <xs:enumeration
                            value="OperatorProvisioned"
                         />
                        <xs:enumeration
                            value="DeviceProvisioned"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="SubscriberID"
                type="subscriberIdType"
             />
            <xs:element name="SimIccID"
                type="simIccIDType"
                minOccurs="0"
             />
            <xs:element name="HomeProviderName"
                type="providerNameType"
                minOccurs="0"
             />
            <xs:element name="AutoConnectOnInternet"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="ConnectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="manual"
                         />
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="auto-home"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="Context"
                type="contextType"
                minOccurs="0"
             />
            <xs:element name="DataRoamingPartners"
                minOccurs="0"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                          | type                                                           | BESCHREIBUNG                                               |
|----------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------|
| [**AutoConnectOnInternet**](schema-autoconnectoninternet-mbnprofile-element.md) | boolean                                                        | Gibt an, ob das Gerät automatisch eine Verbindung herstellt.<br/> |
| [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md)               |                                                                | Die Einstellungen für die automatische Geräteverbindung.<br/>           |
| [**Kontext**](schema-context-mbnprofile-element.md)                             | [**contextType**](schema-contexttype-complextype.md)          | Parameter für die Einrichtung der Datenverbindung.<br/>              |
| [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md)     |                                                                | Bevorzugte Netzwerkanbieter für Roaming.<br/>       |
| [**Beschreibung**](schema-description-mbnprofile-element.md)                     | [**nameType**](schema-nametype-simpletype.md)                 | Beschreibung des Profils.<br/>                    |
| [**HomeProviderName**](schema-homeprovidername-mbnprofile-element.md)           | [**providerNameType**](schema-providernametype-simpletype.md) | Name des Startanbieters.<br/>                     |
| [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md)                   | [**iconFileType**](schema-iconfiletype-simpletype.md)         | Pfad zur Symboldatei.<br/>                         |
| [**IsDefault**](schema-isdefault-mbnprofile-element.md)                         | boolean                                                        | Gibt an, ob das Profil die Standardeinstellung ist.<br/>            |
| [**Name**](schema-name-mbnprofile-element.md)                                   | [**nameType**](schema-nametype-simpletype.md)                 | Name des Profils.<br/>                           |
| [**ProfileCreationType**](schema-profilecreationtype-mbnprofile-element.md)     |                                                                | Informationen zum Ersteller des Profils.<br/>         |
| [**SimIccID**](schema-simiccid-mbnprofile-element.md)                           | [**simIccIDType**](schema-simiccidtype-simpletype.md)         | SIM-ID für GSM-Geräte.<br/>     |
| [**Subscriberid**](schema-subscriberid-mbnprofile-element.md)                   | [**subscriberIdType**](schema-subscriberidtype-simpletype.md) | Eindeutiger Bezeichner des Profils.<br/>              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



 

 




