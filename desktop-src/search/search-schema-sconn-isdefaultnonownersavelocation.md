---
description: Das optionale boolesche <isDefaultNonOwnerSaveLocation> Element gibt an, ob der im Suchconnector beschriebene Speicherort als Standard Speicherort verwendet werden soll, wenn ein Benutzer von einem anderen Computer in einer Heim Netzgruppe ein Element speichern möchte.
ms.assetid: 4286b122-2454-4dc3-9c06-9967b7a763dd
title: isdefaultnonbesitzsaveloationselement (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edd39ab76ae1b99d6518ca40407d328f5da9778c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344261"
---
# <a name="isdefaultnonownersavelocation-element-search-connector-schema"></a><span data-ttu-id="62068-103">isdefaultnonbesitzsaveloationselement (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="62068-103">isDefaultNonOwnerSaveLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="62068-104">Das optionale boolesche <isDefaultNonOwnerSaveLocation> Element gibt an, ob der im Suchconnector beschriebene Speicherort als Standard Speicherort verwendet werden soll, wenn ein Benutzer von einem anderen Computer in einer Heim Netzgruppe ein Element speichern möchte.</span><span class="sxs-lookup"><span data-stu-id="62068-104">The optional Boolean <isDefaultNonOwnerSaveLocation> element specifies whether the location described in the search connector should be used as the default save location when a user from another computer in a Homegroup chooses to save an item.</span></span> <span data-ttu-id="62068-105">Dieses Element hat keine untergeordneten Elemente und keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="62068-105">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="62068-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="62068-106">Syntax</span></span>


```
<!-- isDefaultNonOwnerSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="62068-107">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="62068-107">Element Information</span></span>



| <span data-ttu-id="62068-108">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="62068-108">Parent Element</span></span>                                                                                                   | <span data-ttu-id="62068-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="62068-109">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="62068-110">searchconnectordescriptiontype-Element (suchconnectorschema)</span><span class="sxs-lookup"><span data-stu-id="62068-110">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="62068-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62068-111">Remarks</span></span>

<span data-ttu-id="62068-112">Wenn "true", wenn ein Benutzer eines anderen Computers in einer Heim Netzgruppe ein Element speichert, speichert Windows-Explorer das Element an dem im-Element angegebenen Speicherort <simpleLocation> .</span><span class="sxs-lookup"><span data-stu-id="62068-112">If true, when a user from another computer in a Homegroup chooses to save an item, Windows Explorer saves the item to the location specified in the <simpleLocation> element.</span></span>

## <a name="example"></a><span data-ttu-id="62068-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="62068-113">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



