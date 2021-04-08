---
description: Das optionale <dateCreated> -Element identifiziert das Datum und die Uhrzeit der Erstellung dieses Suchconnector mit dem ISO 8601-Standard. Sie verfügt über keine untergeordneten Elemente und keine Attribute.
ms.assetid: 96d8b067-b5ab-4d36-a8d7-1d084a9f661d
title: DateCreated-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6017c0555d464a49192c4fe8cb7e347bbab0e367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750344"
---
# <a name="datecreated-element-search-connector-schema"></a><span data-ttu-id="c141a-104">DateCreated-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="c141a-104">dateCreated Element (Search Connector Schema)</span></span>

<span data-ttu-id="c141a-105">Das optionale <dateCreated> -Element identifiziert das Datum und die Uhrzeit der Erstellung dieses Suchconnector mit dem ISO 8601-Standard.</span><span class="sxs-lookup"><span data-stu-id="c141a-105">The optional <dateCreated> element identifies the date and the time when this search connector was created, using the ISO 8601 standard.</span></span> <span data-ttu-id="c141a-106">Sie verfügt über keine untergeordneten Elemente und keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="c141a-106">It has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c141a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c141a-107">Syntax</span></span>


```
<!-- dateCreated -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="c141a-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c141a-108">Element Information</span></span>



| <span data-ttu-id="c141a-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="c141a-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="c141a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c141a-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="c141a-111">searchconnectordescriptiontype-Element (suchconnectorschema)</span><span class="sxs-lookup"><span data-stu-id="c141a-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="c141a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c141a-112">Remarks</span></span>

<span data-ttu-id="c141a-113">Das Format des Werts dieses Elements folgt dem ISO 8601-Standard.</span><span class="sxs-lookup"><span data-stu-id="c141a-113">The format of the value of this element follows the ISO 8601 standard.</span></span> <span data-ttu-id="c141a-114">Eine gängige Verwendung wäre eine der folgenden:</span><span class="sxs-lookup"><span data-stu-id="c141a-114">A common use would be either of the following:</span></span>

-   <span data-ttu-id="c141a-115">\[Yyyy \] - \[ mm \] - \[ DD \] T \[ HH \] : \[ mm \] : \[ SS \] ± \[ HH \] : \[ mm \] ("1981-04-05t14:30:30-05:00")</span><span class="sxs-lookup"><span data-stu-id="c141a-115">\[YYYY\]-\[MM\]-\[DD\]T\[hh\]:\[mm\]:\[ss\]±\[hh\]:\[mm\] ("1981-04-05T14:30:30-05:00")</span></span>
-   <span data-ttu-id="c141a-116">\[Yyyy \] \[ mm \] \[ DD \] T \[ HH \] \[ mm \] \[ SS \] Z ("19810405t193030Z")</span><span class="sxs-lookup"><span data-stu-id="c141a-116">\[YYYY\]\[MM\]\[DD\]T\[hh\]\[mm\]\[ss\]Z ("19810405T193030Z")</span></span>

## <a name="example"></a><span data-ttu-id="c141a-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c141a-117">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <dateCreated>2009-04-05T12:00:00-05:00</dateCreated>
    ...
</searchConnectionDescription>
```



 

 



