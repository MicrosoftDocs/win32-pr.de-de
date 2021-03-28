---
description: Das- <propertyStore> Element gibt einen Satz von einer oder mehreren Eigenschaften an, die von dieser Bibliothek verwendet werden. Dieses Element ist optional und besitzt keine Attribute.
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: PropertyStore-Element (Bibliotheks Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ad3b2c15180d6859ea54dea63ec7fc46b7e636c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980320"
---
# <a name="propertystore-element-library-schema"></a><span data-ttu-id="3890a-104">PropertyStore-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="3890a-104">propertyStore Element (Library Schema)</span></span>

<span data-ttu-id="3890a-105">Das- <propertyStore> Element gibt einen Satz von einer oder mehreren Eigenschaften an, die von dieser Bibliothek verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3890a-105">The <propertyStore> element specifies a set of one or more properties used by this library.</span></span> <span data-ttu-id="3890a-106">Dieses Element ist optional und besitzt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="3890a-106">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="3890a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3890a-107">Syntax</span></span>

``` syntax
<!-- propertyStore -->
<xs:element name="propertyStore" minOccurs="0">
    <xs:complexType>
        <xs:complexContent>
            <!-- properties are extensions of propertyStoreType -->
            <xs:extension base="propertyStoreType"/>        
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="3890a-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3890a-108">Element Information</span></span>



| <span data-ttu-id="3890a-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="3890a-109">Parent Element</span></span>                                                               | <span data-ttu-id="3890a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3890a-110">Child Elements</span></span>                                                   |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="3890a-111">librarydescription-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="3890a-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="3890a-112">Property-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="3890a-112">property Element (Library Schema)</span></span>](schema-library-property.md) |



 

## <a name="remarks"></a><span data-ttu-id="3890a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3890a-113">Remarks</span></span>

<span data-ttu-id="3890a-114">Das- <propertyStore> Element kann ein oder mehrere untergeordnete- <property> Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3890a-114">The <propertyStore> element can have one or more <property> child elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3890a-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3890a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3890a-116">Bibliotheks Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="3890a-116">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="3890a-117">Suchdienst-Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="3890a-117">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
