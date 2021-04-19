---
description: 'Gibt an, wie ipropertydescription:: formatfordisplay den Wert der Eigenschaft als Zeichenfolge formatieren soll.'
ms.assetid: 49ba57b8-3e08-425f-98b2-52ed2c41a488
title: enumeratedlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d098b47463b65c483be68eb7750da929df43cee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373059"
---
# <a name="enumeratedlist"></a><span data-ttu-id="59652-103">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="59652-103">enumeratedList</span></span>

<span data-ttu-id="59652-104">Gibt an, wie [**ipropertydescription:: formatfordisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) den Wert der Eigenschaft als Zeichenfolge formatieren soll.</span><span class="sxs-lookup"><span data-stu-id="59652-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="59652-105">Außerdem wird beeinflusst, wie die-Eigenschaft gruppiert werden kann oder welche Werte in der Liste angezeigt werden sollen, wenn "editcontrol" ein listblox ist.</span><span class="sxs-lookup"><span data-stu-id="59652-105">It also influences how the property may be grouped, or what values to show in the list if the "editControl" is a listblox.</span></span> <span data-ttu-id="59652-106">Dies gilt nur, wenn <displayInfo displayType="Enumerated"> .</span><span class="sxs-lookup"><span data-stu-id="59652-106">This is applicable only if <displayInfo displayType="Enumerated">.</span></span> <span data-ttu-id="59652-107">Es darf nur ein [enumeratedlist]() -Element für jedes [DisplayInfo](./propdesc-schema-displayinfo.md) -Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="59652-107">There should be only one [enumeratedList]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="59652-108">Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet.</span><span class="sxs-lookup"><span data-stu-id="59652-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="59652-109">Wenn kein [enumeratedlist]() -Element bereitgestellt wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.</span><span class="sxs-lookup"><span data-stu-id="59652-109">If no [enumeratedList]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="59652-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="59652-110">Syntax</span></span>


```
<!-- enumeratedList -->
<xs:element name="enumeratedList"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="value" type="xs:string" use="required"/>
                    <xs:attribute name="text" type="xs:string" use="required"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="minValue" type="xs:integer" use="required"/>
                    <xs:attribute name="setValue" type="xs:integer"/>
                    <xs:attribute name="text" type="xs:string"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
        <xs:attribute name="defaultText" type="xs:string"/>
        <xs:attribute name="useValueForDefault" type="xs:boolean"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="59652-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="59652-111">Element Information</span></span>



| <span data-ttu-id="59652-112">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="59652-112">Parent Element</span></span>                                   | <span data-ttu-id="59652-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="59652-113">Child Elements</span></span>                               |
|--------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="59652-114">Display Info</span><span class="sxs-lookup"><span data-stu-id="59652-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | [<span data-ttu-id="59652-115">enum</span><span class="sxs-lookup"><span data-stu-id="59652-115">enum</span></span>](./propdesc-schema-enum.md)           |
|                                                  | [<span data-ttu-id="59652-116">enumbereich</span><span class="sxs-lookup"><span data-stu-id="59652-116">enumRange</span></span>](./propdesc-schema-enumrange.md) |



 

## <a name="attributes"></a><span data-ttu-id="59652-117">Attribute</span><span class="sxs-lookup"><span data-stu-id="59652-117">Attributes</span></span>



| <span data-ttu-id="59652-118">Attribut</span><span class="sxs-lookup"><span data-stu-id="59652-118">Attribute</span></span>          | <span data-ttu-id="59652-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59652-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59652-120">DefaultText</span><span class="sxs-lookup"><span data-stu-id="59652-120">defaultText</span></span>        | <span data-ttu-id="59652-121">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="59652-121">Public.</span></span> <span data-ttu-id="59652-122">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="59652-122">Optional.</span></span> <span data-ttu-id="59652-123">Geben Sie den Standardtext an, der verwendet werden soll, wenn [**ipropertydescription:: formatfordisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) ein Wert zugewiesen wird, der keinem der aufgelisteten Elemente in der Liste zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="59652-123">Specify default text to use if a value is given to [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) that does not map to one of the enumerated elements in the list.</span></span> <span data-ttu-id="59652-124">Die Syntax ermöglicht eine direkte Anzeige Zeichenfolge oder einen indirekten Verweis auf eine Anzeige Zeichenfolge. Verwenden Sie den Verweis, damit er lokalisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="59652-124">The syntax allows for a direct display string or an indirect display string reference; use the reference, so it can be localized.</span></span>                              |
| <span data-ttu-id="59652-125">usevaluefordefault</span><span class="sxs-lookup"><span data-stu-id="59652-125">useValueForDefault</span></span> | <span data-ttu-id="59652-126">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="59652-126">Public.</span></span> <span data-ttu-id="59652-127">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="59652-127">Optional.</span></span> <span data-ttu-id="59652-128">Wenn diese Eigenschaft auf "true" festgelegt wird, wird [**ipropertydescription:: formatfordisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) so informiert, dass der Wert unverändert verwendet wird, wenn der Wert keinem der aufgelisteten Elemente in der Liste zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="59652-128">Setting this to "true" will inform [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) to use the value as-is if the value does not map to one of the enumerated elements in the list.</span></span> <span data-ttu-id="59652-129">Für **ipropertydescription:: formatfordisplay** hat die Festlegung auf "true" Vorrang vor dem Festlegen von "DefaultText".</span><span class="sxs-lookup"><span data-stu-id="59652-129">For **IPropertyDescription::FormatForDisplay**, setting this to "true" takes precedence over setting the "defaultText".</span></span> <span data-ttu-id="59652-130">Der Standardwert lautet "false".</span><span class="sxs-lookup"><span data-stu-id="59652-130">The default is "false".</span></span> |



 

 

 
