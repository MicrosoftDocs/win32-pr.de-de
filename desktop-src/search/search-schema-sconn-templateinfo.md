---
description: Dieses optionale <templateInfo> Element gibt einen Ordnertyp zum Anzeigen der Ergebnisse einer Abfrage über diesen Suchconnector an. Dieses Element weist keine Attribute und nur ein obligatorisches untergeordnetes Element auf.
ms.assetid: fe42f589-5c47-4629-94eb-78dbaffa4112
title: templateingefo-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fd28780689b4d544f251bbaf1542bc379ecdaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346494"
---
# <a name="templateinfo-element-search-connector-schema"></a><span data-ttu-id="cc53c-104">templateingefo-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="cc53c-104">templateInfo Element (Search Connector Schema)</span></span>

<span data-ttu-id="cc53c-105">Dieses optionale <templateInfo> Element gibt einen Ordnertyp zum Anzeigen der Ergebnisse einer Abfrage über diesen Suchconnector an.</span><span class="sxs-lookup"><span data-stu-id="cc53c-105">This optional <templateInfo> element specifies a folder type for displaying the results from a query over this search connector.</span></span> <span data-ttu-id="cc53c-106">Dieses Element weist keine Attribute und nur ein obligatorisches untergeordnetes Element auf.</span><span class="sxs-lookup"><span data-stu-id="cc53c-106">This element has no attributes and only one mandatory child.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc53c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc53c-107">Syntax</span></span>


```
<!-- templateInfo -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="templateInfo" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="folderType" minOccurs="0"/>
                    </xs:all>
                </xs:complexType>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="cc53c-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="cc53c-108">Element Information</span></span>



| <span data-ttu-id="cc53c-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="cc53c-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="cc53c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cc53c-110">Child Elements</span></span>                                                                     |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc53c-111">searchconnectordescriptiontype-Element (suchconnectorschema)</span><span class="sxs-lookup"><span data-stu-id="cc53c-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="cc53c-112">foldertype-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="cc53c-112">folderType Element (Search Connector Schema)</span></span>](search-schema-sconn-foldertype.md) |



 

## <a name="remarks"></a><span data-ttu-id="cc53c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc53c-113">Remarks</span></span>

<span data-ttu-id="cc53c-114">Wenn Sie keinen bestimmten Ordnertyp im- <templateInfo> Element angeben, verwendet Windows den Ordner "General Search Connector" {8faf9629-1980-46ff-8023-9dceab9c3ee3}.</span><span class="sxs-lookup"><span data-stu-id="cc53c-114">If you don't specify a particular folder type in the <templateInfo> element, Windows uses the general search connector folder type {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.</span></span>

## <a name="example-of-a-templateinfo-element"></a><span data-ttu-id="cc53c-115">Beispiel für ein templateingefo-Element</span><span class="sxs-lookup"><span data-stu-id="cc53c-115">Example of a templateInfo Element</span></span>


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



