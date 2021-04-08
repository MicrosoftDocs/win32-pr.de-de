---
description: Das optionale <propertyStore> -Element gibt den Speicherort eines XML-basierten IPropertyStore an, um geöffnete Metadaten für diesen Suchconnector zu speichern. Dieses Element weist keine Attribute und nur ein untergeordnetes Element auf.
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: PropertyStore-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11f8cda6457de764b00519a81a1134e7eecc8638
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750329"
---
# <a name="propertystore-element-search-connector-schema"></a><span data-ttu-id="cfb43-104">PropertyStore-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="cfb43-104">propertyStore Element (Search Connector Schema)</span></span>

<span data-ttu-id="cfb43-105">Das optionale <propertyStore> -Element gibt den Speicherort eines XML-basierten IPropertyStore an, um geöffnete Metadaten für diesen Suchconnector zu speichern.</span><span class="sxs-lookup"><span data-stu-id="cfb43-105">The optional <propertyStore> element specifies the location of an XML-based IPropertyStore to store open metadata for this search connector.</span></span> <span data-ttu-id="cfb43-106">Dieses Element weist keine Attribute und nur ein untergeordnetes Element auf.</span><span class="sxs-lookup"><span data-stu-id="cfb43-106">This element has no attributes and only one child element.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfb43-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfb43-107">Syntax</span></span>


```
<!-- propertyStore -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0">
            <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="cfb43-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="cfb43-108">Element Information</span></span>



| <span data-ttu-id="cfb43-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="cfb43-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="cfb43-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cfb43-110">Child Elements</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cfb43-111">searchconnectordescriptiontype-Element (suchconnectorschema)</span><span class="sxs-lookup"><span data-stu-id="cfb43-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="cfb43-112">Property-Element von PropertyStore (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="cfb43-112">property Element of propertyStore (Search Connector Schema)</span></span>](search-schema-sconn-propstore-property.md) |



 

## <a name="example"></a><span data-ttu-id="cfb43-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cfb43-113">Example</span></span>

<span data-ttu-id="cfb43-114">Das folgende Beispiel zeigt ein- <propertyStore> Element mit zwei- <property> Elementen.</span><span class="sxs-lookup"><span data-stu-id="cfb43-114">The following example shows a <propertyStore> element with two <property> elements.</span></span>


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



