---
description: Neu in Windows 7. Container-Element für relatedproperty-Elemente.
ms.assetid: F8BAAE5C-A7EA-487a-B829-91A27E24B58D
title: relatedpropertyinfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 442de657bed7e97f74064c39cc0934c65a6f520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354616"
---
# <a name="relatedpropertyinfo"></a><span data-ttu-id="de4e9-104">relatedpropertyinfo</span><span class="sxs-lookup"><span data-stu-id="de4e9-104">relatedPropertyInfo</span></span>

<span data-ttu-id="de4e9-105">Neu in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="de4e9-105">New for Windows 7.</span></span> <span data-ttu-id="de4e9-106">Container-Element für [relatedproperty](./propdesc-schema-relatedproperty.md) -Elemente.</span><span class="sxs-lookup"><span data-stu-id="de4e9-106">Container element for [relatedProperty](./propdesc-schema-relatedproperty.md) elements.</span></span> <span data-ttu-id="de4e9-107">Es darf nur ein [relatedpropertyinfo]() -Element für jedes [propertydescription](./propdesc-schema-propertydescription.md) -Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="de4e9-107">There should be only one [relatedPropertyInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span>

## <a name="syntax"></a><span data-ttu-id="de4e9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="de4e9-108">Syntax</span></span>


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedPropertyInfo">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
                    <xs:attribute name="propertyName" type="canonical-name" use="required"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:unique name="No_two_relatedProperties_can_have_the_same_relationship_name">
        <xs:selector xpath="s:relatedProperty"/>
        <xs:field    xpath="@relationshipName"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="de4e9-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="de4e9-109">Element Information</span></span>



| <span data-ttu-id="de4e9-110">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="de4e9-110">Parent Element</span></span>                                                   | <span data-ttu-id="de4e9-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="de4e9-111">Child Elements</span></span>                                           |
|------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="de4e9-112">propertydescription</span><span class="sxs-lookup"><span data-stu-id="de4e9-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | [<span data-ttu-id="de4e9-113">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="de4e9-113">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md) |



 

## <a name="attributes"></a><span data-ttu-id="de4e9-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="de4e9-114">Attributes</span></span>

<span data-ttu-id="de4e9-115">Dieses Element weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="de4e9-115">This element has no attributes.</span></span>

 

 
