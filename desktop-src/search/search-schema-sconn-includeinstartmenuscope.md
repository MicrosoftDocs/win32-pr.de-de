---
description: Das optionale boolesche <includeInStartMenuScope> Element gibt an, ob dieser Suchconnector im Startmenü-Suchbereich enthalten sein soll.
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: includeinstartmenus-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 126d10a2b69dcec5057e732679c8531fd6e82bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343652"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a><span data-ttu-id="1b088-103">includeinstartmenus-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="1b088-103">includeInStartMenuScope Element (Search Connector Schema)</span></span>

<span data-ttu-id="1b088-104">Das optionale boolesche <includeInStartMenuScope> Element gibt an, ob dieser Suchconnector im Startmenü-Suchbereich enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="1b088-104">The optional Boolean <includeInStartMenuScope> element specifies whether this search connector should be included in the Start menu search scope.</span></span> <span data-ttu-id="1b088-105">Der Standardwert ist true für Suchconnectors, die das Dateisystem als Datenquelle verwenden, und false für Suchconnectors, die von Eigenschaften Handlern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b088-105">The default value is true for search connectors using the file system as a data source, and false for search connectors used by property handlers.</span></span> <span data-ttu-id="1b088-106">Dieses Element hat keine untergeordneten Elemente und keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="1b088-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b088-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b088-107">Syntax</span></span>


```
<!-- includeInStartMenuScope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="1b088-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1b088-108">Element Information</span></span>



| <span data-ttu-id="1b088-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1b088-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="1b088-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1b088-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="1b088-111">searchconnectordescriptiontype-Element (suchconnectorschema)</span><span class="sxs-lookup"><span data-stu-id="1b088-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="1b088-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b088-112">Remarks</span></span>

<span data-ttu-id="1b088-113">Wenn Sie den Suchconnector in den Startmenü Bereich einschließen, können Benutzer ihren Speicherort über das Suchfeld im Startmenü durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="1b088-113">If you include the search connector in the Start menu scope, users can search your location from the search box in the Start menu.</span></span>

## <a name="example"></a><span data-ttu-id="1b088-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1b088-114">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <includeinStartMenuScope>true</includeinStartMenuScope>
    ...
</searchConnectionDescription>
```



 

 



