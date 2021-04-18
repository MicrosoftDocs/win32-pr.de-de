---
description: Das- <libraryDescription> Element ist der Container der obersten Ebene für die Bibliotheksdefinition. Dieses Element ist erforderlich.
ms.assetid: 62098944-E1B2-46e8-AC87-314C55F96B62
title: librarydescription-Element (Bibliotheks Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125cb01ce1bd38418c10f5b14ff7b28f64efba87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977841"
---
# <a name="librarydescription-element-library-schema"></a>librarydescription-Element (Bibliotheks Schema)

Das- <libraryDescription> Element ist der Container der obersten Ebene für die Bibliotheksdefinition. Dieses Element ist erforderlich.

## <a name="syntax"></a>Syntax


```
<!-- libraryDescription -->
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema" elementFormDefault="qualified" attributeFormDefault="unqualified">
    <xs:include schemaLocation="commonTypes-ms.xsd"/>
    <xs:element name="libraryDescription">
        <xs:complexType>
            <xs:all>
                <xs:element name="name" type="xs:string"/>
                <xs:element name="ownerSID" minOccurs="0"/>
                <xs:element name="version" type="xs:int" minOccurs="0"/>
                <xs:element name="isLibraryPinned" type="xs:boolean" default="false" minOccurs="0"/>
                <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
                <xs:element name="propertyStore" minOccurs="0">
                    <xs:complexType>
                        <xs:complexContent>
                            <xs:extension base="propertyStoreType"/>
                        </xs:complexContent>
                    </xs:complexType>
                </xs:element>
                <xs:element name="templateInfo" minOccurs="0">
                    <xs:complexType>
                        <xs:all>
                            <xs:element name="folderType" minOccurs="0"/>
                        </xs:all>
                    </xs:complexType>
                </xs:element>
                <xs:element name="searchConnectorDescriptionList" minOccurs="0">
                    <xs:complexType>
                        <xs:sequence minOccurs="0">
                            <xs:element name="searchConnectorDescription" 
                             type="searchConnectorDescriptionType" minOccurs="0" 
                             maxOccurs="unbounded"/>
                        </xs:sequence>
                    </xs:complexType>
                </xs:element>
            </xs:all>
        </xs:complexType>
    </xs:element>
</xs:schema>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element | Untergeordnete Elemente                                                                                                          |
|----------------|-------------------------------------------------------------------------------------------------------------------------|
|                | [Name-Element (Bibliotheks Schema)](schema-library-name.md). Erforderlich.                                                     |
|                | Besitzer- [sid-Element (Bibliotheks Schema)](schema-library-ownersid.md). Optional.                                             |
|                | [Version-Element (Bibliotheks Schema)](schema-library-version.md). Optional.                                               |
|                | [islibrarypinned-Element (Bibliotheks Schema)](schema-library-islibrarypinned.md). Optional.                               |
|                | [iconReference-Element (Bibliotheks Schema)](schema-library-iconreference.md). Optional.                                   |
|                | [PropertyStore-Element (Bibliotheks Schema)](schema-library-propertystore.md). Optional.                                   |
|                | [templateingefo-Element (Bibliotheks Schema)](schema-library-templateinfo.md). Optional.                                     |
|                | [searchconnectordescriptionlist-Element (Bibliotheks Schema)](schema-library-searchconnectordescriptionlist.md). Erforderlich. |



 

## <a name="remarks"></a>Bemerkungen

Jede Bibliothek kann einen oder mehrere Speicherorte enthalten, die von einem Benutzer mithilfe von Windows-Explorer durchsucht oder durchsucht werden können. Die Speicherorte werden von Suchconnectors mithilfe von [<searchConnectorDescription>](schema-library-searchconnectordescription.md) Elementen in einem [<searchConnectorDescriptionList>](schema-library-searchconnectordescriptionlist.md) Containerelement definiert.

Eine Bibliothek kann über einen eindeutigen Satz von Eigenschaften verfügen, und Positionen in der Bibliothek können auch eindeutige Eigenschaften Sätze aufweisen. Diese Eigenschaften werden in [<property>](schema-library-property.md) Elementen innerhalb eines [<propertyStore>](schema-library-propertystore.md) Container Elements definiert.

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
    <name>@shell32.dll,-34575</name>
    <ownerSID>S-1-5-21-379071477-2495173225-776587366-1000</ownerSID>
    <version>1</version>
    <isLibraryPinned>true</isLibraryPinned>
    <iconReference>imageres.dll,-1002</iconReference>
    <templateInfo>
        <folderType>{7d49d726-3c21-4f05-99aa-fdc2c9474656}</folderType>
    </templateInfo>
    <searchConnectorDescriptionList>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34577</description>
            <isDefaultSaveLocation>true</isDefaultSaveLocation>
            <simpleLocation>
                <url>knownfolder:{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</url>
                <serialized>MBAAAEAFCAAA...MFNVAAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34579</description>
            <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
            <simpleLocation>
                <url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
                <serialized>MBAAAEAFCAAA...HJIfK9AAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
    </searchConnectorDescriptionList>
</libraryDescription>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bibliotheks Beschreibungs Schema](library-schema-entry.md)
</dt> <dt>

[Suchdienst-Beschreibungs Schema](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
