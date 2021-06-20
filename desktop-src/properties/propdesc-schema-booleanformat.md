---
description: Gibt an, wie IPropertyDescription::FormatForDisplay den Wert der booleanFormat-Eigenschaft als Zeichenfolge formatieren soll.
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 528458d9c31d54ef43eca8325b1daeef4eee1195
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405963"
---
# <a name="booleanformat"></a><span data-ttu-id="3b068-103">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="3b068-103">booleanFormat</span></span>

<span data-ttu-id="3b068-104">Gibt an, wie [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) den Wert der Eigenschaft als Zeichenfolge formatieren soll.</span><span class="sxs-lookup"><span data-stu-id="3b068-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="3b068-105">Dies gilt nur, wenn <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="3b068-105">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="3b068-106">Es sollte nur ein [booleanFormat-Element]() für jedes [displayInfo-Element](./propdesc-schema-displayinfo.md) vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="3b068-106">There should be only one [booleanFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="3b068-107">Wenn mehrere Elemente vorhanden sind, wird das letzte Element verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b068-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="3b068-108">Wenn kein [booleanFormat-Element]() angegeben wird, werden die Standardattributeinstellungen auf die Eigenschaftenbeschreibung angewendet.</span><span class="sxs-lookup"><span data-stu-id="3b068-108">If no [booleanFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b068-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b068-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="3b068-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3b068-110">Element Information</span></span>



| <span data-ttu-id="3b068-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="3b068-111">Parent Element</span></span>                                   | <span data-ttu-id="3b068-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b068-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="3b068-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="3b068-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="3b068-114">Keine</span><span class="sxs-lookup"><span data-stu-id="3b068-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="3b068-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="3b068-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b068-116">attribute</span><span class="sxs-lookup"><span data-stu-id="3b068-116">Attribute</span></span></th>
<th><span data-ttu-id="3b068-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b068-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3b068-118">formatAs</span><span class="sxs-lookup"><span data-stu-id="3b068-118">formatAs</span></span></td>
<td><span data-ttu-id="3b068-119">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="3b068-119">Public.</span></span> <span data-ttu-id="3b068-120">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="3b068-120">Optional.</span></span> <span data-ttu-id="3b068-121">Der Standardwert ist &quot; &quot; YesNo.</span><span class="sxs-lookup"><span data-stu-id="3b068-121">Default is &quot;YesNo&quot;.</span></span> <span data-ttu-id="3b068-122">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="3b068-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3b068-123">Wert</span><span class="sxs-lookup"><span data-stu-id="3b068-123">Value</span></span></th>
<th><span data-ttu-id="3b068-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3b068-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3b068-125">YesNo</span><span class="sxs-lookup"><span data-stu-id="3b068-125">YesNo</span></span></td>
<td><span data-ttu-id="3b068-126">Standard.</span><span class="sxs-lookup"><span data-stu-id="3b068-126">Default.</span></span> <span data-ttu-id="3b068-127">Formatiert den Wert entweder als &quot; Ja &quot; oder &quot; &quot; Nein.</span><span class="sxs-lookup"><span data-stu-id="3b068-127">Formats the value as either &quot;Yes&quot; or &quot;No&quot;.</span></span> <span data-ttu-id="3b068-128">Erfordert, dass der Eigenschaftstyp boolesch ist.</span><span class="sxs-lookup"><span data-stu-id="3b068-128">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b068-129">OnOff</span><span class="sxs-lookup"><span data-stu-id="3b068-129">OnOff</span></span></td>
<td><span data-ttu-id="3b068-130">Formatiert den Wert entweder als &quot; Ein &quot; oder &quot; &quot; Aus.</span><span class="sxs-lookup"><span data-stu-id="3b068-130">Formats the value as either &quot;On&quot; or &quot;Off&quot;.</span></span> <span data-ttu-id="3b068-131">Erfordert, dass der Eigenschaftstyp boolesch ist.</span><span class="sxs-lookup"><span data-stu-id="3b068-131">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b068-132">TrueFalse</span><span class="sxs-lookup"><span data-stu-id="3b068-132">TrueFalse</span></span></td>
<td><span data-ttu-id="3b068-133">Formatiert den Wert entweder als &quot; True &quot; oder &quot; &quot; False.</span><span class="sxs-lookup"><span data-stu-id="3b068-133">Formats the value as either &quot;True&quot; or &quot;False&quot;.</span></span> <span data-ttu-id="3b068-134">Erfordert, dass der Eigenschaftstyp boolesch ist.</span><span class="sxs-lookup"><span data-stu-id="3b068-134">Requires the property type to be Boolean.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
