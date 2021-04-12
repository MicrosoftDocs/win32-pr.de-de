---
description: Neu in Windows 7. Bezeichnet eine Eigenschaft, die mit der in der Eigenschafts Beschreibungsdatei definierten Eigenschaft verknüpft ist.
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabde093a47a25834598659d3ad38e0847c1351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344799"
---
# <a name="relatedproperty"></a><span data-ttu-id="17a4b-104">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="17a4b-104">relatedProperty</span></span>

<span data-ttu-id="17a4b-105">Neu in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="17a4b-105">New for Windows 7.</span></span> <span data-ttu-id="17a4b-106">Bezeichnet eine Eigenschaft, die mit der in der Eigenschafts Beschreibungsdatei definierten Eigenschaft verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="17a4b-106">Identifies a property that is related to the property defined in the property description file.</span></span> <span data-ttu-id="17a4b-107">Es können beliebig viele [relatedproperty]() -Elemente innerhalb von [relatedpropertyinfo](./propdesc-schema-relatedpropertyinfo.md) vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="17a4b-107">There can be as many [relatedProperty]() elements within a [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="17a4b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="17a4b-108">Syntax</span></span>


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
        <xs:attribute name="propertyName" type="canonical-name" use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="17a4b-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="17a4b-109">Element Information</span></span>



| <span data-ttu-id="17a4b-110">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="17a4b-110">Parent Element</span></span>                                                   | <span data-ttu-id="17a4b-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17a4b-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="17a4b-112">relatedpropertyinfo</span><span class="sxs-lookup"><span data-stu-id="17a4b-112">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md) | <span data-ttu-id="17a4b-113">Keine</span><span class="sxs-lookup"><span data-stu-id="17a4b-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="17a4b-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="17a4b-114">Attributes</span></span>



| <span data-ttu-id="17a4b-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="17a4b-115">Attribute</span></span>        | <span data-ttu-id="17a4b-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17a4b-116">Description</span></span>                                                        |
|------------------|--------------------------------------------------------------------|
| <span data-ttu-id="17a4b-117">relationshipName</span><span class="sxs-lookup"><span data-stu-id="17a4b-117">relationshipName</span></span> | <span data-ttu-id="17a4b-118">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="17a4b-118">Public.</span></span> <span data-ttu-id="17a4b-119">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="17a4b-119">Required.</span></span> <span data-ttu-id="17a4b-120">Der kanonische Name der Eigenschafts Beziehung.</span><span class="sxs-lookup"><span data-stu-id="17a4b-120">The canonical name of the property relationship.</span></span> |
| <span data-ttu-id="17a4b-121">propertyName</span><span class="sxs-lookup"><span data-stu-id="17a4b-121">propertyName</span></span>     | <span data-ttu-id="17a4b-122">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="17a4b-122">Public.</span></span> <span data-ttu-id="17a4b-123">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="17a4b-123">Required.</span></span> <span data-ttu-id="17a4b-124">Der kanonische Name der verwandten Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="17a4b-124">The canonical name of the related property.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="17a4b-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17a4b-125">Remarks</span></span>

<span data-ttu-id="17a4b-126">Dieses Element ermöglicht es Ihnen, eine Eigenschaft einem anderen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="17a4b-126">This element enables you to map one property to another.</span></span> <span data-ttu-id="17a4b-127">Beispielsweise können Sie den Text der benutzerdefinierten Eigenschaft fabrikam. storagecapacity zu System. Capacity zuordnen:</span><span class="sxs-lookup"><span data-stu-id="17a4b-127">For example, you can map the text of your custom property, Fabrikam.StorageCapacity, to System.Capacity:</span></span>


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 
