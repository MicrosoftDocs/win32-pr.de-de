---
description: Das- <searchConnectorDescription> Element ist das Containerelement der obersten Ebene einer Suchconnector-Definition.
ms.assetid: 383CAA20-56CA-4bdc-AC79-E57A1D59785C
title: searchconnectordescription-Element (Bibliotheks Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa6c213d43a648ebea51b58b4c3103a0ee42f13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980472"
---
# <a name="searchconnectordescription-element-library-schema"></a><span data-ttu-id="28fb9-103">searchconnectordescription-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="28fb9-103">searchConnectorDescription Element (Library Schema)</span></span>

<span data-ttu-id="28fb9-104">Das- <searchConnectorDescription> Element ist das Containerelement der obersten Ebene einer Suchconnector-Definition.</span><span class="sxs-lookup"><span data-stu-id="28fb9-104">The <searchConnectorDescription> element is the top level container element of a search connector definition.</span></span> <span data-ttu-id="28fb9-105">Das- <searchConnectorDescription> Element ist eine Erweiterung des- <searchConnectorDescriptionType> Elementtyps, der mit Windows-Verbund Suchconnectors verknüpft ist. es ist jedoch nicht möglich, Suchconnectors für die Windows-Verbund Suche oder-Protokollhandler in einer Bibliothek einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="28fb9-105">The <searchConnectorDescription> element is an extension of the <searchConnectorDescriptionType> element type associated with Windows Federated Search connectors; however, you cannot include search connectors for Windows Federated Search or protocol handlers in a library.</span></span>

## <a name="syntax"></a><span data-ttu-id="28fb9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="28fb9-106">Syntax</span></span>

``` syntax
<!-- searchConnectorDescription -->
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

## <a name="element-information"></a><span data-ttu-id="28fb9-107">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="28fb9-107">Element Information</span></span>

<span data-ttu-id="28fb9-108">Weitere Informationen finden Sie in der Schema Dokumentation in [Windows Search](/previous-versions/bb268030(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="28fb9-108">Refer to the schema documentation in [Windows Search](/previous-versions/bb268030(v=msdn.10))</span></span>



| <span data-ttu-id="28fb9-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="28fb9-109">Parent Element</span></span>                                                                                               | <span data-ttu-id="28fb9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28fb9-110">Child Elements</span></span>                        |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [<span data-ttu-id="28fb9-111">searchconnectordescriptionlist-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="28fb9-111">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md) | <span data-ttu-id="28fb9-112"><issearchonlyi. tem></span><span class="sxs-lookup"><span data-stu-id="28fb9-112"><isSearchOnlyI.tem></span></span>             |
|                                                                                                              | <description>                   |
|                                                                                                              | <iconReference>                 |
|                                                                                                              | <imageLink>                     |
|                                                                                                              | <author>                        |
|                                                                                                              | <dateCreated>                   |
|                                                                                                              | <templateInfo>                  |
|                                                                                                              | <locationProvider>              |
|                                                                                                              | <scope>                         |
|                                                                                                              | <propertyStore>                 |
|                                                                                                              | <domain>                        |
|                                                                                                              | <supportsAdvancedQuerySyntax>   |
|                                                                                                              | <isDefaultSaveLocation>         |
|                                                                                                              | <isDefaultNonOwnerSaveLocation> |
|                                                                                                              | <isIndexed>                     |
|                                                                                                              | <simpleLocation>                |
|                                                                                                              | <includeInStartMenu>            |



 

## <a name="attributes"></a><span data-ttu-id="28fb9-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="28fb9-113">Attributes</span></span>



| <span data-ttu-id="28fb9-114">attribute</span><span class="sxs-lookup"><span data-stu-id="28fb9-114">Attribute</span></span> | <span data-ttu-id="28fb9-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28fb9-115">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="28fb9-116">publisher</span><span class="sxs-lookup"><span data-stu-id="28fb9-116">publisher</span></span> | <span data-ttu-id="28fb9-117">Optional.</span><span class="sxs-lookup"><span data-stu-id="28fb9-117">Optional.</span></span> <span data-ttu-id="28fb9-118">Der Anzeige Name des Verlegers, der den Suchconnector bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="28fb9-118">The display name of the publisher providing the search connector.</span></span>      |
| <span data-ttu-id="28fb9-119">product</span><span class="sxs-lookup"><span data-stu-id="28fb9-119">product</span></span>   | <span data-ttu-id="28fb9-120">Optional.</span><span class="sxs-lookup"><span data-stu-id="28fb9-120">Optional.</span></span> <span data-ttu-id="28fb9-121">Der Anzeige Name des Produkts, auf das der Suchconnector angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="28fb9-121">The display name of the product to which the search connector applies.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="28fb9-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28fb9-122">Remarks</span></span>

<span data-ttu-id="28fb9-123">Das- <searchConnectorDescription> Element einer Bibliothek verwendet die gleiche Schema Definition wie <searchConnectorDescription> für die Windows-Verbund Suche.</span><span class="sxs-lookup"><span data-stu-id="28fb9-123">The <searchConnectorDescription> element of a library uses the same schema definition as the <searchConnectorDescription> for Windows Federated Search.</span></span> <span data-ttu-id="28fb9-124">Obwohl die gleichen Schemas verwendet werden, können Suchconnectors für die Windows-Verbund Suche nicht in einer Bibliothek enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="28fb9-124">Although they use the same schemas, search connectors for Windows Federated search cannot be included in a library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28fb9-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="28fb9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28fb9-126">Bibliotheks Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="28fb9-126">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="28fb9-127">Suchdienst-Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="28fb9-127">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
