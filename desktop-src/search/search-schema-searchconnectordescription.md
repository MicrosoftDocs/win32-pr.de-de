---
description: Das &lt; searchConnectorDescriptionType-Element ist der Container der obersten Ebene &gt; für die Definition des Suchconnectors.
ms.assetid: a6b45864-210d-4099-804d-7548fd8eb562
title: searchConnectorDescriptionType-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f89621ab34f65fb3c3b1f8e88bbdc8dca246b8d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885080"
---
# <a name="searchconnectordescriptiontype-element-search-connector-schema"></a>searchConnectorDescriptionType-Element (Search Connector Schema)

Das &lt; searchConnectorDescriptionType-Element ist der Container der obersten Ebene &gt; für die Definition des Suchconnectors.

-   [Syntax](#syntax)
-   [Elementinformationen](#element-information)
-   [Attribute](#attributes)
-   [Anmerkungen](#remarks)
-   [Beispiel für eine Suchconnectorbeschreibungsdatei](#example-of-a-search-connector-description-file)
-   [Zugehörige Themen](#related-topics)

## <a name="syntax"></a>Syntax


```
<!-- searchConnectorDescriptionType -->
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema" elementFormDefault="qualified" attributeFormDefault="unqualified">
   <xs:complexType name="searchConnectorDescriptionType">
      <xs:all>
         <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
         <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/
         <xs:element name="description" type="xs:string" minOccurs="0"/>
         <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
         <xs:element name="imageLink" minOccurs="0">
            <xs:complexType>
               <xs:sequence>
                  <xs:element name="url" type="xs:anyURI"/>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
         <xs:element name="author" type="xs:string" minOccurs="0"/>
         <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
         <xs:element name="templateInfo" minOccurs="0">
            <xs:complexType>
               <xs:all>
                  <xs:element name="folderType" minOccurs="0"/>
               </xs:all>
            </xs:complexType>
         </xs:element>
         <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0"/>
         <xs:element name="locationProvider" minOccurs="0">
            <xs:complexType>
               <xs:all>
                  <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
               </xs:all>
               <xs:attribute name="clsid" use="required"/>
               <xs:attribute name="codebase" type="xs:string"/>
            </xs:complexType>
         </xs:element>
         <xs:element name="scope" minOccurs="0">
            <xs:complexType>
               <xs:sequence minOccurs="0">
                  <xs:element name="scopeItem" maxOccurs="unbounded">
                     <xs:complexType>
                        <xs:all>
                           <xs:element name="mode" default="Include">
                              <xs:simpleType>
                                 <xs:restriction base="xs:string">
                                    <xs:enumeration value="Include"/>
                                    <xs:enumeration value="Exclude"/>
                                 </xs:restriction>
                              </xs:simpleType>
                           </xs:element>
                           <xs:element name="depth" default="Shallow" minOccurs="0">
                              <xs:simpleType>
                                 <xs:restriction base="xs:string">
                                    <xs:enumeration value="Shallow"/>
                                    <xs:enumeration value="Deep"/>
                                 </xs:restriction>
                              </xs:simpleType>
                           </xs:element>
                           <xs:element name="url" type="xs:anyURI"/>
                        </xs:all>
                     </xs:complexType>
                  </xs:element>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
         <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0"/>
         <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="domain" type="xs:string" minOccurs="0"/>
         <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="isIndexed" type="xs:boolean" minOccurs="0"/>
      </xs:all>
      <xs:attribute name="publisher" type="xs:string"/>
      <xs:attribute name="product" type="xs:string"/>
   </xs:complexType>
</xs:schema>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element | Untergeordnete Elemente                                                                                                           |
|----------------|--------------------------------------------------------------------------------------------------------------------------|
|                | [isSearchOnlyItem-Element (Search Connector Schema)](search-schema-sconn-issearchonlyitem.md)                           |
|                | [isDefaultSaveLocation-Element (Connectorschema suchen)](search-schema-sconn-isdefaultsavelocation.md)                 |
|                | [isDefaultNonOwnerSaveLocation-Element (Connectorschema durchsuchen)](search-schema-sconn-isdefaultnonownersavelocation.md) |
|                | [description-Element (Search Connector Schema)](search-schema-sconn-description.md)                                     |
|                | [iconReference-Element (Suchconnectorschema)](search-schema-sconn-iconreference.md)                                 |
|                | [imageLink-Element (Connectorschema suchen)](search-schema-sconn-imagelink.md)                                         |
|                | [author-Element (Search Connector Schema)](search-schema-sconn-author.md)                                               |
|                | [dateCreated-Element (Suchconnectorschema)](search-schema-sconn-datecreated.md)                                     |
|                | [templateInfo-Element (Search Connector Schema)](search-schema-sconn-templateinfo.md)                                   |
|                | [locationProvider-Element (Connectorschema suchen)](search-schema-sconn-locationprovider.md)                           |
|                | [scope-Element (Search Connector Schema)](search-schema-sconn-scope.md)                                                 |
|                | [propertyStore-Element (Connectorschema suchen)](search-schema-sconn-propertystore.md)                                 |
|                | [includeInStartMenuScope-Element (Search Connector Schema)](search-schema-sconn-includeinstartmenuscope.md)             |
|                | [domain-Element (Search Connector Schema)](search-schema-sconn-domain.md)                                               |
|                | [supportsAdvancedQuerySyntax-Element (Search Connector Schema)](search-schema-sconn-supportsadvancedquerysyntax.md)     |
|                | [isIndexed-Element (Search Connector Schema)](search-schema-sconn-isindexed.md)                                         |



 

## <a name="attributes"></a>Attribute



| attribute | Beschreibung                                                                      |
|-----------|----------------------------------------------------------------------------------|
| publisher | Optional. Der Anzeigename des Herausgebers, der den Suchconnector an stellt.      |
| product   | Optional. Der Anzeigename des Produkts, für das der Suchconnector gilt. |



 

## <a name="remarks"></a>Hinweise

Suchconnectors für die Verbundsuche können nicht in Bibliotheken verwendet werden. Das Schema für Bibliothekssuchconnectors ist eine Erweiterung des hier beschriebenen Schemas und enthält spezifische Informationen für Bibliotheken.

## <a name="example-of-a-search-connector-description-file"></a>Beispiel für eine Suchconnectorbeschreibungsdatei

Im Folgenden finden Sie ein Beispiel für eine Search Connector Description-Datei für einen Verbundsuchwebdienst.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



Im Folgenden finden Sie ein Beispiel für eine Search Connector Description-Datei für einen MAPI-Protokollhandler.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Übersicht über das Suchconnector-Beschreibungsschema](search-sconn-desc-schema-entry.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Verbundsuche in Windows 10](-search-federated-search-overview.md)
</dt> </dl>

 

 



