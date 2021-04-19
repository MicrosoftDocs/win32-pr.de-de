---
description: Ist das Stamm Element, das ein mobiles Breitband Profil identifiziert.
ms.assetid: 08302e7f-3024-439b-a2ad-a4ae9487b82b
title: Mbnprofile-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MBNProfile
api_type:
- Schema
ms.openlocfilehash: 7016d492a70192a7d6accdcb3aaa57a9c564960e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359858"
---
# <a name="mbnprofile-element"></a>Mbnprofile-Element

Das **mbnprofile** -Element ist das Stamm Element, das ein mobiles Breitband Profil identifiziert.

Es kann nur ein Element dieses Typs pro Dokument vorhanden sein.

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
| [**Autoconnectoninternet**](schema-autoconnectoninternet-mbnprofile-element.md) | boolean                                                        | Gibt an, ob das Gerät automatisch eine Verbindung herstellt.<br/> |
| [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md)               |                                                                | Die automatischen Geräte Verbindungseinstellungen.<br/>           |
| [**Kontext**](schema-context-mbnprofile-element.md)                             | [**contextType**](schema-contexttype-complextype.md)          | Setup Parameter für die Datenverbindung.<br/>              |
| [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md)     |                                                                | Bevorzugte Netzwerkanbieter für Roaming.<br/>       |
| [**Beschreibung**](schema-description-mbnprofile-element.md)                     | [**nametype**](schema-nametype-simpletype.md)                 | Beschreibung des Profils.<br/>                    |
| [**HomeProviderName**](schema-homeprovidername-mbnprofile-element.md)           | [**providernametype**](schema-providernametype-simpletype.md) | Der Name des Home-Anbieters.<br/>                     |
| [**Iconfilepath**](schema-iconfilepath-mbnprofile-element.md)                   | [**iconfiletype**](schema-iconfiletype-simpletype.md)         | Der Pfad zur Symbol Datei.<br/>                         |
| [**IsDefault**](schema-isdefault-mbnprofile-element.md)                         | boolean                                                        | Gibt an, ob das Profil das Standardprofil ist.<br/>            |
| [**Name**](schema-name-mbnprofile-element.md)                                   | [**nametype**](schema-nametype-simpletype.md)                 | Name des Profils.<br/>                           |
| [**Profilekreationtype**](schema-profilecreationtype-mbnprofile-element.md)     |                                                                | Informationen zum Ersteller des Profils.<br/>         |
| [**Simiccid**](schema-simiccid-mbnprofile-element.md)                           | [**simiccidtype**](schema-simiccidtype-simpletype.md)         | SIM-Identifikationsnummer für GSM-Geräte.<br/>     |
| [**Abonnement-ID**](schema-subscriberid-mbnprofile-element.md)                   | [**Index Type**](schema-subscriberidtype-simpletype.md) | Eindeutiger Bezeichner des Profils.<br/>              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



 

 




