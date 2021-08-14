---
description: Das Scanprofilschema definiert ein XML-Format, das verwendet werden kann, um die Eigenschaften Windows WIA-Elemente (Image Acquisition) wie Scanner und Kameras zu speichern.
ms.assetid: e0848db3-652a-45be-a18b-99b82420c586
title: Scanprofilschema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81091e75269206b6b3b5a89f86c6f92da5c1d2080d90382ac6af48c6d1cc32ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208016"
---
# <a name="scan-profile-schema"></a>Scanprofilschema

Das Scanprofilschema definiert ein XML-Format, das verwendet werden kann, um die Eigenschaften Windows WIA-Elemente (Image Acquisition) wie Scanner und Kameras zu speichern. Diese persistenten Dateien ermöglichen Anwendungen die automatische Überprüfung, ohne dass benutzer sich die Eigenschafteneinstellungen der Elemente merken müssen.

Jedes [**IWiaItem2-Gerät**](-wia-iwiaitem2.md) kann über ein Überprüfungsprofil verfügen. **IWiaItem2-Elemente** der Typen WIA \_ CATEGORY \_ FINISHED FILE und WIA CATEGORY ROOT können jedoch \_ keine Profile \_ \_ aufweisen.

Scanprofile werden über die Schnittstellen [**IScanProfile,**](-wia-iscanprofile.md) [**IScanProfileMgr**](-wia-iscanprofilemgr.md)und [**IScanProfileUI**](-wia-iscanprofileui.md) erstellt und verwaltet. Benutzer Ihrer Anwendung können Profile auf eingeschränkte Weise mithilfe der [**IScanProfileUI::ScanProfileDialog-Methode**](-wia-iscanprofileui-scanprofiledialog.md) ändern.

Alle Scanprofile verfügen über die folgenden Elemente: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` und `<Properties>` . Das Standardprofil eines Geräts verfügt auch über ein `<Default>` -Element.

Das `<ProfileGUID>` -Element und das `<DeviceID>` -Element können nach dem Erstellen des Scanprofils nicht mehr geändert werden. Die Werte des `<ProfileName>` -Elements und des `<WiaItem>` -Elements können geändert werden. Das `<Default>` Element kann hinzugefügt oder gelöscht werden. Dies kann programmgesteuert mithilfe der Methoden [**IScanProfile::SetName,**](-wia-iscanprofile-setname.md) [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md)und [**IScanProfileMgr::SetDefault**](-wia-iscanprofilemgr-setdefault.md) erfolgen. Diese Eigenschaften können auch von Benutzern über die [**IScanProfileUI::ScanProfileDialog-Methode**](-wia-iscanprofileui-scanprofiledialog.md) geändert werden.

Das `<Properties>` -Element enthält `<Property>` untergeordnete Elemente. Verwenden Sie diese, um dem Profil alle WIA-Elemente oder Geräteeigenschaften hinzuzufügen. Sie können auch eigene untergeordnete Bilder `<Property>` entwickeln. Dadurch wird das Scanprofilschema erweiterbar. (Weitere Informationen zum Erweitern des Schemas finden Sie unter [Definieren von benutzerdefinierten Eigenschaften,](-wia-defining-custom-properties.md) [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md)und [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).)

Hier ist das vollständige Scanprofilschema angegeben. Es folgt ein Beispielprofil.


```
<?xml version="1.0"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema"
            targetNamespace="https://www.microsoft.com"
            xmlns="https://www.microsoft.com"
            elementFormDefault="qualified">

<xs:element name="ScanProfile">
            <xs:complexType>
            <xs:sequence>
                        <xs:element name="ProfileGUID" type="xs:string"/>
                        <xs:element name="DeviceID" type="xs:string"/>
<xs:element name="ProfileName" type="xs:string"/>
                        <xs:element name="Default" minOccurs="0">
                                    <xs:complexType>
                                    </xs:complexType>
                        </xs:element>
                        <xs:element name="WiaItem" type="xs:string"/>
                        <xs:element name="Properties" type="Properties"/>
            </xs:sequence>
            </xs:complexType>
</xs:element>
 
<xs:complexType name="Properties">
<xs:sequence>
            <xs:element name="Property" maxOccurs="unbounded" minOccurs="0">
            <xs:complexType>
            <xs:simpleContent>
                        <xs:extension base="xs:string">
                                    <xs:attribute name="id" type="xs:integer" use="required"/>
                                    <xs:attribute name="type" type="xs:integer" use="required"/>
                        </xs:extension>
            </xs:simpleContent>
            </xs:complexType>
            </xs:element>
</xs:sequence>
</xs:complexType>
 
</xs:schema>
```



Klicken Sie auf **Beispiel anzeigen,** um ein Beispielprofil anzuzeigen.


```
<ScanProfile>
    <ProfileGUID>
        {F862E217-32B0-4396-987A-2191224925CD}
    </ProfileGUID>
    <DeviceID>
        {6BDD1FC6-810F-11D0-BEC7-08002BE2092F}\0001
    </DeviceID>
    <ProfileName>
        Last used settings
    </ProfileName>
    <WiaItem>
        {FB607B1F-43F3-488B-855B-FB703EC342A6}
    </WiaItem>
    <Properties>
        <Property id="4103" type="3">
            3
        </Property>
        <Property id="4106" type="72">
            {B96B3CAB-0728-11D3-9D7B-0000F81EF32E}
        </Property>
        <Property id="6147" type="3">
            300
        </Property>
        <Property id="6154" type="3">
            0
        </Property>
        <Property id="6155" type="3">
            0
        </Property>
    </Properties>
</ScanProfile>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md)
</dt> <dt>

[**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[WIA-Eigenschaftenkonstanten](-wia-wia-property-constants.md)
</dt> <dt>

[Definieren von benutzerdefinierten Eigenschaften](-wia-defining-custom-properties.md)
</dt> </dl>

 

 



