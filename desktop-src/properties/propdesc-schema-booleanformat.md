---
description: 'Gibt an, wie ipropertydescription:: formatfordisplay den Wert der Eigenschaft als Zeichenfolge formatieren soll. Dies gilt nur, wenn <displayInfo displayType=&\#0034;String&\#0034;> .'
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: BooleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91332f0cc062e7ee4a83e3584776ecf09c5c4b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959833"
---
# <a name="booleanformat"></a><span data-ttu-id="f9d1b-104">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="f9d1b-104">booleanFormat</span></span>

<span data-ttu-id="f9d1b-105">Gibt an, wie [**ipropertydescription:: formatfordisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) den Wert der Eigenschaft als Zeichenfolge formatieren soll.</span><span class="sxs-lookup"><span data-stu-id="f9d1b-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="f9d1b-106">Dies gilt nur, wenn <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="f9d1b-106">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="f9d1b-107">Es darf nur ein [BooleanFormat]() -Element für jedes [DisplayInfo](./propdesc-schema-displayinfo.md) -Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f9d1b-107">There should be only one [booleanFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="f9d1b-108">Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9d1b-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="f9d1b-109">Wenn kein [BooleanFormat]() -Element bereitgestellt wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.</span><span class="sxs-lookup"><span data-stu-id="f9d1b-109">If no [booleanFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9d1b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9d1b-110">Syntax</span></span>


```
      <!-- booleanFormat -->
      <xs:element name="booleanFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="YesNo"/>
                <xs:enumeration value="OnOff"/>
                <xs:enumeration value="TrueFalse"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="f9d1b-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f9d1b-111">Element Information</span></span>



| <span data-ttu-id="f9d1b-112">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="f9d1b-112">Parent Element</span></span>                                   | <span data-ttu-id="f9d1b-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9d1b-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="f9d1b-114">Display Info</span><span class="sxs-lookup"><span data-stu-id="f9d1b-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="f9d1b-115">Keine</span><span class="sxs-lookup"><span data-stu-id="f9d1b-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="f9d1b-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="f9d1b-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9d1b-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="f9d1b-117">Attribute</span></span></th>
<th><span data-ttu-id="f9d1b-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9d1b-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9d1b-119">formatas</span><span class="sxs-lookup"><span data-stu-id="f9d1b-119">formatAs</span></span></td>
<td><span data-ttu-id="f9d1b-120">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="f9d1b-120">Public.</span></span> <span data-ttu-id="f9d1b-121">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="f9d1b-121">Optional.</span></span> <span data-ttu-id="f9d1b-122">Der Standardwert ist &quot; YesNo &quot; .</span><span class="sxs-lookup"><span data-stu-id="f9d1b-122">Default is &quot;YesNo&quot;.</span></span> <span data-ttu-id="f9d1b-123">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="f9d1b-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f9d1b-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f9d1b-124">Value</span></span></th>
<th><span data-ttu-id="f9d1b-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f9d1b-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9d1b-126">YesNo</span><span class="sxs-lookup"><span data-stu-id="f9d1b-126">YesNo</span></span></td>
<td><span data-ttu-id="f9d1b-127">Standard.</span><span class="sxs-lookup"><span data-stu-id="f9d1b-127">Default.</span></span> <span data-ttu-id="f9d1b-128">Formatiert den Wert entweder als " &quot; yes" &quot; oder "No" &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="f9d1b-128">Formats the value as either &quot;Yes&quot; or &quot;No&quot;.</span></span> <span data-ttu-id="f9d1b-129">Erfordert, dass der Eigenschaftentyp ein boolescher Wert ist.</span><span class="sxs-lookup"><span data-stu-id="f9d1b-129">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9d1b-130">OnOff</span><span class="sxs-lookup"><span data-stu-id="f9d1b-130">OnOff</span></span></td>
<td><span data-ttu-id="f9d1b-131">Formatiert den Wert entweder als ein- &quot; &quot; oder &quot; ausschalten &quot; .</span><span class="sxs-lookup"><span data-stu-id="f9d1b-131">Formats the value as either &quot;On&quot; or &quot;Off&quot;.</span></span> <span data-ttu-id="f9d1b-132">Erfordert, dass der Eigenschaftentyp ein boolescher Wert ist.</span><span class="sxs-lookup"><span data-stu-id="f9d1b-132">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9d1b-133">TrueFalse</span><span class="sxs-lookup"><span data-stu-id="f9d1b-133">TrueFalse</span></span></td>
<td><span data-ttu-id="f9d1b-134">Formatiert den Wert entweder als " &quot; true" &quot; oder "false" &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="f9d1b-134">Formats the value as either &quot;True&quot; or &quot;False&quot;.</span></span> <span data-ttu-id="f9d1b-135">Erfordert, dass der Eigenschaftentyp ein boolescher Wert ist.</span><span class="sxs-lookup"><span data-stu-id="f9d1b-135">Requires the property type to be Boolean.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
