---
description: Das Überprüfungs Profil Schema definiert ein XML-Format, das verwendet werden kann, um die Eigenschaften von Elementen der Windows-Abbild Erfassung (WIA), wie z. b. Scanner und Kameras, zu speichern.
ms.assetid: e0848db3-652a-45be-a18b-99b82420c586
title: Profil Schema überprüfen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331c52e933e1e6b771c477bdc8a38f1c5f749448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349011"
---
# <a name="scan-profile-schema"></a>Profil Schema überprüfen

Das Überprüfungs Profil Schema definiert ein XML-Format, das verwendet werden kann, um die Eigenschaften von Elementen der Windows-Abbild Erfassung (WIA), wie z. b. Scanner und Kameras, zu speichern. Mit diesen permanenten Dateien können Anwendungen automatische Scans bereitstellen, ohne dass sich die Benutzer an die Eigenschafts Einstellungen der Elemente erinnern müssen.

Jedes [**IWiaItem2**](-wia-iwiaitem2.md) -Gerät kann über ein Überprüfungs Profil verfügen. Allerdings können **IWiaItem2** Items von Typen, \_ die mit einer Kategorie \_ fertiggestellt \_ wurden, die Datei fertiggestellt \_ \_ haben

Scan Profile werden über die Schnittstellen [**iscanprofile**](-wia-iscanprofile.md), [**iscanprofilemgr**](-wia-iscanprofilemgr.md)und [**iscanprofileui**](-wia-iscanprofileui.md) erstellt und verwaltet. Benutzer Ihrer Anwendung können Profile in eingeschränkter Weise mithilfe der [**iscanprofileui:: scanprofiledialog**](-wia-iscanprofileui-scanprofiledialog.md) -Methode ändern.

Alle Scan Profile verfügen über die folgenden Elemente: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` , und `<Properties>` . Das Standardprofil eines Geräts weist auch ein- `<Default>` Element auf.

Das `<ProfileGUID>` -Element und das- `<DeviceID>` Element können nicht geändert werden, nachdem das Scan Profil erstellt wurde. Die Werte des `<ProfileName>` -Elements und des- `<WiaItem>` Elements können geändert werden. Das- `<Default>` Element kann hinzugefügt oder gelöscht werden. Dies kann Programm gesteuert mithilfe der Methoden [**iscanprofile:: SetName**](-wia-iscanprofile-setname.md), [**iscanprofile:: SetItem**](-wia-iscanprofile-setitem.md)und [**iscanprofilemgr:: SetDefault**](-wia-iscanprofilemgr-setdefault.md) erfolgen. Diese Eigenschaften können auch von Benutzern über die [**iscanprofileui:: scanprofiledialog**](-wia-iscanprofileui-scanprofiledialog.md) -Methode geändert werden.

Das- `<Properties>` Element enthält untergeordnete Elemente `<Property>` . Verwenden Sie diese, um dem Profil eine beliebige WIA-Element-oder Geräte Eigenschaft hinzuzufügen. Sie können auch Ihre eigenen Image-Erstell-untergeordneten Elemente entwickeln `<Property>` . Dadurch ist das Scan Profil Schema erweiterbar. (Weitere Informationen zum Erweitern des Schemas finden Sie unter [Definieren von benutzerdefinierten Eigenschaften](-wia-defining-custom-properties.md), [**iscanprofile:: GetProperty**](-wia-iscanprofile-getproperty.md)und [**iscanprofile:: SetProperty**](-wia-iscanprofile-setproperty.md).)

Hier ist das komplette Überprüfungs Profil Schema. Ein Beispiel Profil folgt.


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



Klicken Sie auf **Beispiel anzeigen** , um ein Beispiel Profil anzuzeigen.


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

[**Iscanprofile:: GetProperty**](-wia-iscanprofile-getproperty.md)
</dt> <dt>

[**Iscanprofile:: SetProperty**](-wia-iscanprofile-setproperty.md)
</dt> <dt>

**Licher**
</dt> <dt>

[WIA-Eigenschafts Konstanten](-wia-wia-property-constants.md)
</dt> <dt>

[Definieren von benutzerdefinierten Eigenschaften](-wia-defining-custom-properties.md)
</dt> </dl>

 

 



