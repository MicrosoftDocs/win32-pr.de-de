---
description: Das optionale- <locationProvider> Element gibt den Suchanbieter an, der vom Webdienstanbieter-Suchconnector verwendet werden soll. Dieses Element enthält ein obligatorisches Attribut und ein optionales untergeordnetes Element.
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: locationprovider-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c68732300c190b44b984bbe64ca031a81ced84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346907"
---
# <a name="locationprovider-element-search-connector-schema"></a><span data-ttu-id="17eec-104">locationprovider-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="17eec-104">locationProvider Element (Search Connector Schema)</span></span>

<span data-ttu-id="17eec-105">Das optionale- <locationProvider> Element gibt den Suchanbieter an, der vom Webdienstanbieter-Suchconnector verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="17eec-105">The optional <locationProvider> element specifies the search provider to be used by the web service provider search connector.</span></span> <span data-ttu-id="17eec-106">Dieses Element enthält ein obligatorisches Attribut und ein optionales untergeordnetes Element.</span><span class="sxs-lookup"><span data-stu-id="17eec-106">This element contains one mandatory attribute and an optional child element.</span></span>

## <a name="syntax"></a><span data-ttu-id="17eec-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="17eec-107">Syntax</span></span>


```
<!-- locationProvider -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
                    </xs:all>
                <xs:attribute name="clsid" use="required"/>
                <xs:attribute name="codebase" type="xs:string"/>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="17eec-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="17eec-108">Element Information</span></span>



| <span data-ttu-id="17eec-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="17eec-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="17eec-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17eec-110">Child Elements</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="17eec-111">searchconnectordescriptiontype-Element (suchconnectorschema)</span><span class="sxs-lookup"><span data-stu-id="17eec-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="17eec-112">PropertyBag-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="17eec-112">propertyBag Element (Search Connector Schema)</span></span>](search-schema-sconn-propertybag.md) |



 

## <a name="attributes"></a><span data-ttu-id="17eec-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="17eec-113">Attributes</span></span>



| <span data-ttu-id="17eec-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="17eec-114">Attribute</span></span> | <span data-ttu-id="17eec-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17eec-115">Description</span></span>                                                    |
|-----------|----------------------------------------------------------------|
| @clsid    | <span data-ttu-id="17eec-116">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="17eec-116">Required.</span></span> <span data-ttu-id="17eec-117">Der Klassen Bezeichner (CLSID) des Such Anbieters.</span><span class="sxs-lookup"><span data-stu-id="17eec-117">The class identifier (CLSID) of the search provider.</span></span> |
| <span data-ttu-id="17eec-118">codebase</span><span class="sxs-lookup"><span data-stu-id="17eec-118">codebase</span></span>  | <span data-ttu-id="17eec-119">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="17eec-119">Optional.</span></span>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="17eec-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17eec-120">Remarks</span></span>

<span data-ttu-id="17eec-121">Der @clsid Attribut Wert für den OpenSearch-Anbieter ist {48e277f 6-4e74-4cd6-ba6s-fa4s42898223}.</span><span class="sxs-lookup"><span data-stu-id="17eec-121">The @clsid attribute value for the OpenSearch provider is {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.</span></span>

<span data-ttu-id="17eec-122">Auf Dateisystem-und protokollhandlerbasierten Suchconnectors kann stattdessen das-Element verwendet werden [<simpleLocation>](search-schema-sconn-simplelocation.md) .</span><span class="sxs-lookup"><span data-stu-id="17eec-122">File system and protocol handler based search connectors can use the [<simpleLocation>](search-schema-sconn-simplelocation.md) element instead.</span></span> <span data-ttu-id="17eec-123">Wenn <locationProvider> vorhanden ist, darf <simpleLocation> in der Suchconnector-Beschreibung kein-Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="17eec-123">If <locationProvider> is present, there MUST NOT be a <simpleLocation> element in the Search Connector description.</span></span>

## <a name="example-of-a-locationprovider-element"></a><span data-ttu-id="17eec-124">Beispiel für ein locationprovider-Element</span><span class="sxs-lookup"><span data-stu-id="17eec-124">Example of a locationProvider Element</span></span>


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



