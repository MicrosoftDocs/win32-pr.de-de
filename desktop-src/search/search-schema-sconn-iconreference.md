---
description: Das optionale- <iconReference> Element gibt ein benutzerdefiniertes Symbol für diese Position an. Dieses Element hat keine Attribute und keine untergeordneten Elemente.
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: iconReference-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c181efe3bb8ac04f08d4fa16016d3468af6f10c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525463"
---
# <a name="iconreference-element-search-connector-schema"></a><span data-ttu-id="d97a0-104">iconReference-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="d97a0-104">iconReference Element (Search Connector Schema)</span></span>

<span data-ttu-id="d97a0-105">Das optionale- <iconReference> Element gibt ein benutzerdefiniertes Symbol für diese Position an.</span><span class="sxs-lookup"><span data-stu-id="d97a0-105">The optional <iconReference> element specifies a custom icon for this location.</span></span> <span data-ttu-id="d97a0-106">Dieses Element hat keine Attribute und keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="d97a0-106">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="d97a0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d97a0-107">Syntax</span></span>


```
<!-- iconReference -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="d97a0-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d97a0-108">Element Information</span></span>



| <span data-ttu-id="d97a0-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="d97a0-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="d97a0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d97a0-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="d97a0-111">searchconnectordescriptiontype-Element (suchconnectorschema)</span><span class="sxs-lookup"><span data-stu-id="d97a0-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="d97a0-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d97a0-112">Remarks</span></span>

<span data-ttu-id="d97a0-113">Das Format des Verweises muss in einer für die [pathparametenconlocation](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) -Funktion geeigneten Form angegeben werden: (z <dll file name> . b <icon index> .,).</span><span class="sxs-lookup"><span data-stu-id="d97a0-113">The format of the reference must be specified in a form suitable for the [PathParseIconLocation](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) function: (for example, <dll file name>,<icon index>).</span></span>

## <a name="example"></a><span data-ttu-id="d97a0-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d97a0-114">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <iconReference>example.dll,-1002</iconReference>
    ...
</searchConnectionDescription>
```



 

 
