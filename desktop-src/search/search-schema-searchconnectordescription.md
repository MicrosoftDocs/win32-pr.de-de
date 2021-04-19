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
# <a name="searchconnectordescriptiontype-element-search-connector-schema"></a><span data-ttu-id="ab802-103">searchconnectordescriptiontype-Element (suchconnectorschema)</span><span class="sxs-lookup"><span data-stu-id="ab802-103">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>

<span data-ttu-id="ab802-104">Das- <searchConnectorDescriptionType> Element ist der Container der obersten Ebene für die Suchconnector-Definition.</span><span class="sxs-lookup"><span data-stu-id="ab802-104">The <searchConnectorDescriptionType> element is the top level container for the search connector definition.</span></span>

-   [<span data-ttu-id="ab802-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab802-105">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="ab802-106">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ab802-106">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ab802-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="ab802-107">Attributes</span></span>](#attributes)
-   [<span data-ttu-id="ab802-108">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="ab802-108">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="ab802-109">Beispiel für eine Suchconnector-Beschreibungsdatei</span><span class="sxs-lookup"><span data-stu-id="ab802-109">Example of a Search Connector Description File</span></span>](#example-of-a-search-connector-description-file)
-   [<span data-ttu-id="ab802-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ab802-110">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="ab802-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab802-111">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="ab802-112">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ab802-112">Element Information</span></span>



| <span data-ttu-id="ab802-113">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="ab802-113">Parent Element</span></span> | <span data-ttu-id="ab802-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ab802-114">Child Elements</span></span>                                                                                                           |
|----------------|--------------------------------------------------------------------------------------------------------------------------|
|                | [<span data-ttu-id="ab802-115">issearchonlyitem-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="ab802-115">isSearchOnlyItem Element (Search Connector Schema)</span></span>](search-schema-sconn-issearchonlyitem.md)                           |
|                | [<span data-ttu-id="ab802-116">isdefaultsaveloation-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="ab802-116">isDefaultSaveLocation Element (Search Connector Schema)</span></span>](search-schema-sconn-isdefaultsavelocation.md)                 |
|                | [<span data-ttu-id="ab802-117">isdefaultnonbesitzsaveloationselement (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="ab802-117">isDefaultNonOwnerSaveLocation Element (Search Connector Schema)</span></span>](search-schema-sconn-isdefaultnonownersavelocation.md) |
|                | [<span data-ttu-id="ab802-118">Description-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="ab802-118">description Element (Search Connector Schema)</span></span>](search-schema-sconn-description.md)                                     |
|                | [<span data-ttu-id="ab802-119">iconReference-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="ab802-119">iconReference Element (Search Connector Schema)</span></span>](search-schema-sconn-iconreference.md)                                 |
|                | [<span data-ttu-id="ab802-120">IMAGELINK-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="ab802-120">imageLink Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink.md)                                         |
|                | [<span data-ttu-id="ab802-121">Author-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="ab802-121">author Element (Search Connector Schema)</span></span>](search-schema-sconn-author.md)                                               |
|                | [<span data-ttu-id="ab802-122">DateCreated-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="ab802-122">dateCreated Element (Search Connector Schema)</span></span>](search-schema-sconn-datecreated.md)                                     |
|                | [<span data-ttu-id="ab802-123">templateingefo-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="ab802-123">templateInfo Element (Search Connector Schema)</span></span>](search-schema-sconn-templateinfo.md)                                   |
|                | [<span data-ttu-id="ab802-124">locationprovider-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="ab802-124">locationProvider Element (Search Connector Schema)</span></span>](search-schema-sconn-locationprovider.md)                           |
|                | [<span data-ttu-id="ab802-125">Scope-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="ab802-125">scope Element (Search Connector Schema)</span></span>](search-schema-sconn-scope.md)                                                 |
|                | [<span data-ttu-id="ab802-126">PropertyStore-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="ab802-126">propertyStore Element (Search Connector Schema)</span></span>](search-schema-sconn-propertystore.md)                                 |
|                | [<span data-ttu-id="ab802-127">includeinstartmenus-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="ab802-127">includeInStartMenuScope Element (Search Connector Schema)</span></span>](search-schema-sconn-includeinstartmenuscope.md)             |
|                | [<span data-ttu-id="ab802-128">Domain-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="ab802-128">domain Element (Search Connector Schema)</span></span>](search-schema-sconn-domain.md)                                               |
|                | [<span data-ttu-id="ab802-129">supportsadvancedquerysyntax-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="ab802-129">supportsAdvancedQuerySyntax Element (Search Connector Schema)</span></span>](search-schema-sconn-supportsadvancedquerysyntax.md)     |
|                | [<span data-ttu-id="ab802-130">isinentxed-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="ab802-130">isIndexed Element (Search Connector Schema)</span></span>](search-schema-sconn-isindexed.md)                                         |



 

## <a name="attributes"></a><span data-ttu-id="ab802-131">Attribute</span><span class="sxs-lookup"><span data-stu-id="ab802-131">Attributes</span></span>



| <span data-ttu-id="ab802-132">Attribut</span><span class="sxs-lookup"><span data-stu-id="ab802-132">Attribute</span></span> | <span data-ttu-id="ab802-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab802-133">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ab802-134">publisher</span><span class="sxs-lookup"><span data-stu-id="ab802-134">publisher</span></span> | <span data-ttu-id="ab802-135">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ab802-135">Optional.</span></span> <span data-ttu-id="ab802-136">Der Anzeige Name des Verlegers, der den Suchconnector bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ab802-136">The display name of the publisher providing the search connector.</span></span>      |
| <span data-ttu-id="ab802-137">product</span><span class="sxs-lookup"><span data-stu-id="ab802-137">product</span></span>   | <span data-ttu-id="ab802-138">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ab802-138">Optional.</span></span> <span data-ttu-id="ab802-139">Der Anzeige Name des Produkts, auf das der Suchconnector angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ab802-139">The display name of the product to which the search connector applies.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ab802-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab802-140">Remarks</span></span>

<span data-ttu-id="ab802-141">Suchconnectors für die Verbund Suche können nicht in Bibliotheken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab802-141">Search connectors for federated search cannot be used in libraries.</span></span> <span data-ttu-id="ab802-142">Das Schema für Bibliotheks Suchconnectors ist eine Erweiterung des hier beschriebenen Schemas und enthält Informationen, die für Bibliotheken spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="ab802-142">The schema for library search connectors is an extension of the schema described here and includes information specific to libraries.</span></span>

## <a name="example-of-a-search-connector-description-file"></a><span data-ttu-id="ab802-143">Beispiel für eine Suchconnector-Beschreibungsdatei</span><span class="sxs-lookup"><span data-stu-id="ab802-143">Example of a Search Connector Description File</span></span>

<span data-ttu-id="ab802-144">Im folgenden finden Sie ein Beispiel für eine Suchconnector-Beschreibungsdatei für einen Verbund Suchweb Dienst.</span><span class="sxs-lookup"><span data-stu-id="ab802-144">The following is an example of a Search Connector Description file for a federated search web service.</span></span>


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



<span data-ttu-id="ab802-145">Im folgenden finden Sie ein Beispiel für eine Suchconnector-Beschreibungsdatei für einen MAPI-Protokollhandler.</span><span class="sxs-lookup"><span data-stu-id="ab802-145">The following is an example of a Search Connector Description file for a MAPI protocol handler.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ab802-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ab802-146">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ab802-147">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="ab802-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ab802-148">Übersicht über das Suchconnector-Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="ab802-148">Overview of the Search Connector Description Schema</span></span>](search-sconn-desc-schema-entry.md)
</dt> <dt>

<span data-ttu-id="ab802-149">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ab802-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ab802-150">Verbundsuche in Windows 10</span><span class="sxs-lookup"><span data-stu-id="ab802-150">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> </dl>

 

 



