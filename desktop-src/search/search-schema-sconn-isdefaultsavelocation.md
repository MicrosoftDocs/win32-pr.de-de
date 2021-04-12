---
description: Das optionale boolesche <isDefaultSaveLocation> Element gibt an, ob der im Suchconnector beschriebene Speicherort als Standard Speicherort verwendet werden soll. Dieses Element hat keine untergeordneten Elemente und keine Attribute.
ms.assetid: 4a33f411-d71e-41d3-b5fd-018a92dceeac
title: isdefaultsaveloation-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b664e4cd6f7c88f1dfbeb44ba23faee5d24a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342909"
---
# <a name="isdefaultsavelocation-element-search-connector-schema"></a><span data-ttu-id="5ae37-104">isdefaultsaveloation-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="5ae37-104">isDefaultSaveLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="5ae37-105">Das optionale boolesche <isDefaultSaveLocation> Element gibt an, ob der im Suchconnector beschriebene Speicherort als Standard Speicherort verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ae37-105">The optional Boolean <isDefaultSaveLocation> element specifies whether the location described in the search connector should be used as the default save location.</span></span> <span data-ttu-id="5ae37-106">Dieses Element hat keine untergeordneten Elemente und keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="5ae37-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ae37-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ae37-107">Syntax</span></span>


```
<!-- isDefaultSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="5ae37-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5ae37-108">Element Information</span></span>



| <span data-ttu-id="5ae37-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="5ae37-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="5ae37-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5ae37-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="5ae37-111">searchconnectordescriptiontype-Element (suchconnectorschema)</span><span class="sxs-lookup"><span data-stu-id="5ae37-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="5ae37-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ae37-112">Remarks</span></span>

<span data-ttu-id="5ae37-113">Wenn ein Benutzer ein Element speichert, speichert Windows-Explorer das Element an der Position, die im- <simpleLocation> Element angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="5ae37-113">When a user chooses to save an item, Windows Explorer saves the item to the location specified in the <simpleLocation> element.</span></span> <span data-ttu-id="5ae37-114">Benutzer können diese Einstellung im Dialogfeld "Eigenschaften" für den Suchconnector ändern.</span><span class="sxs-lookup"><span data-stu-id="5ae37-114">Users can change this setting using the Properties dialog for the search connector.</span></span>

## <a name="example"></a><span data-ttu-id="5ae37-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5ae37-115">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultSaveLocation>true</isDefaultSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



