---
description: Das- <searchConnectorDescriptionType> Element ist der Container der obersten Ebene für die Suchconnector-Definition.
ms.assetid: a6b45864-210d-4099-804d-7548fd8eb562
title: searchconnectordescriptiontype-Element (suchconnectorschema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7edb69647567b7e18e25e11dcd0fc773d0be7902
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345486"
---
# <a name="searchconnectordescriptiontype-element-search-connector-schema"></a>searchconnectordescriptiontype-Element (suchconnectorschema)

Das- <searchConnectorDescriptionType> Element ist der Container der obersten Ebene für die Suchconnector-Definition.

-   [Syntax](#syntax)
-   [Elementinformationen](#element-information)
-   [Attribute](#attributes)
-   [Anmerkungen](#remarks)
-   [Beispiel für eine Suchconnector-Beschreibungsdatei](#example-of-a-search-connector-description-file)
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
|                | [issearchonlyitem-Element (Suchconnector-Schema)](search-schema-sconn-issearchonlyitem.md)                           |
|                | [isdefaultsaveloation-Element (Suchconnector-Schema)](search-schema-sconn-isdefaultsavelocation.md)                 |
|                | [isdefaultnonbesitzsaveloationselement (Suchconnector-Schema)](search-schema-sconn-isdefaultnonownersavelocation.md) |
|                | [Description-Element (Suchconnector-Schema)](search-schema-sconn-description.md)                                     |
|                | [iconReference-Element (Suchconnector-Schema)](search-schema-sconn-iconreference.md)                                 |
|                | [IMAGELINK-Element (Suchconnector-Schema)](search-schema-sconn-imagelink.md)                                         |
|                | [Author-Element (Suchconnector-Schema)](search-schema-sconn-author.md)                                               |
|                | [DateCreated-Element (Suchconnector-Schema)](search-schema-sconn-datecreated.md)                                     |
|                | [templateingefo-Element (Suchconnector-Schema)](search-schema-sconn-templateinfo.md)                                   |
|                | [locationprovider-Element (Suchconnector-Schema)](search-schema-sconn-locationprovider.md)                           |
|                | [Scope-Element (Suchconnector-Schema)](search-schema-sconn-scope.md)                                                 |
|                | [PropertyStore-Element (Suchconnector-Schema)](search-schema-sconn-propertystore.md)                                 |
|                | [includeinstartmenus-Element (Suchconnector-Schema)](search-schema-sconn-includeinstartmenuscope.md)             |
|                | [Domain-Element (Suchconnector-Schema)](search-schema-sconn-domain.md)                                               |
|                | [supportsadvancedquerysyntax-Element (Suchconnector-Schema)](search-schema-sconn-supportsadvancedquerysyntax.md)     |
|                | [isinentxed-Element (Suchconnector-Schema)](search-schema-sconn-isindexed.md)                                         |



 

## <a name="attributes"></a>Attribute



| Attribut | BESCHREIBUNG                                                                      |
|-----------|----------------------------------------------------------------------------------|
| publisher | Dies ist optional. Der Anzeige Name des Verlegers, der den Suchconnector bereitstellt.      |
| product   | Dies ist optional. Der Anzeige Name des Produkts, auf das der Suchconnector angewendet wird. |



 

## <a name="remarks"></a>Bemerkungen

Suchconnectors für die Verbund Suche können nicht in Bibliotheken verwendet werden. Das Schema für Bibliotheks Suchconnectors ist eine Erweiterung des hier beschriebenen Schemas und enthält Informationen, die für Bibliotheken spezifisch sind.

## <a name="example-of-a-search-connector-description-file"></a>Beispiel für eine Suchconnector-Beschreibungsdatei

Im folgenden finden Sie ein Beispiel für eine Suchconnector-Beschreibungsdatei für einen Verbund Suchweb Dienst.


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



Im folgenden finden Sie ein Beispiel für eine Suchconnector-Beschreibungsdatei für einen MAPI-Protokollhandler.


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

[Übersicht über das Suchconnector-Beschreibungs Schema](search-sconn-desc-schema-entry.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Verbundsuche in Windows 10](-search-federated-search-overview.md)
</dt> </dl>

 

 



