---
description: Container für ein oder mehrere einzelne propertydescription-Elemente.
ms.assetid: b54aaa85-6928-470e-9630-44b094205106
title: propertydescriptionlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd0beaf4dbbd8b71c7f4b3335c169754c704d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343807"
---
# <a name="propertydescriptionlist"></a><span data-ttu-id="c42e0-103">propertydescriptionlist</span><span class="sxs-lookup"><span data-stu-id="c42e0-103">propertyDescriptionList</span></span>

<span data-ttu-id="c42e0-104">Container für ein oder mehrere einzelne [propertydescription](./propdesc-schema-propertydescription.md) -Elemente.</span><span class="sxs-lookup"><span data-stu-id="c42e0-104">Container for one or many individual [propertyDescription](./propdesc-schema-propertydescription.md) elements.</span></span> <span data-ttu-id="c42e0-105">Eine. PropDesc-Eigenschafts Beschreibungs-Schema Datei sollte mindestens ein [propertydescriptionlist]() -Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="c42e0-105">A .propdesc property description schema file should contain at least one [propertyDescriptionList]() element.</span></span>

## <a name="syntax"></a><span data-ttu-id="c42e0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c42e0-106">Syntax</span></span>


```
<!-- propertyDescriptionList -->
<xs:element name="propertyDescriptionList">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="s:propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string" use="required"/>
        <xs:attribute name="product"   type="xs:string" use="required"/>
    </xs:complexType>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_formatid_and_propid">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@formatID"/>
        <xs:field    xpath="@propID"/>
    </xs:unique>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_canonical_name">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@name"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="c42e0-107">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c42e0-107">Element Information</span></span>



| <span data-ttu-id="c42e0-108">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="c42e0-108">Parent Element</span></span>                        | <span data-ttu-id="c42e0-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c42e0-109">Child Elements</span></span>                                                   |
|---------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="c42e0-110">schema</span><span class="sxs-lookup"><span data-stu-id="c42e0-110">schema</span></span>](./propdesc-schema-entry.md) | [<span data-ttu-id="c42e0-111">propertydescription</span><span class="sxs-lookup"><span data-stu-id="c42e0-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) |



 

## <a name="attributes"></a><span data-ttu-id="c42e0-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="c42e0-112">Attributes</span></span>



| <span data-ttu-id="c42e0-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="c42e0-113">Attribute</span></span> | <span data-ttu-id="c42e0-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c42e0-114">Description</span></span>                                                               |
|-----------|---------------------------------------------------------------------------|
| <span data-ttu-id="c42e0-115">publisher</span><span class="sxs-lookup"><span data-stu-id="c42e0-115">publisher</span></span> | <span data-ttu-id="c42e0-116">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="c42e0-116">Public.</span></span> <span data-ttu-id="c42e0-117">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c42e0-117">Required.</span></span> <span data-ttu-id="c42e0-118">Der Anzeige Name des Verlegers, der das Schema bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c42e0-118">The display name of the publisher providing the schema.</span></span> |
| <span data-ttu-id="c42e0-119">product</span><span class="sxs-lookup"><span data-stu-id="c42e0-119">product</span></span>   | <span data-ttu-id="c42e0-120">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="c42e0-120">Public.</span></span> <span data-ttu-id="c42e0-121">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c42e0-121">Required.</span></span> <span data-ttu-id="c42e0-122">Der Anzeige Name des Produkts, das das Schema bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c42e0-122">The display name of the product providing the schema.</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="c42e0-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c42e0-123">Remarks</span></span>

<span data-ttu-id="c42e0-124">Die [propertydescriptionlist]() sollte nicht mit "Eigenschafts Listen" und " [**ipropertydescriptionlist**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)" verwechselt werden, die vollständig voneinander getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="c42e0-124">The [propertyDescriptionList]() should not be confused with "property lists" and [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), which are completely separate.</span></span>

 

 
