---
description: Gibt an, wie IPropertyDescription::FormatForDisplay den Wert der stringFormat-Eigenschaft als Zeichenfolge formatieren soll.
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730355507b78d99eba02e82666427dd29425c942
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408353"
---
# <a name="stringformat"></a><span data-ttu-id="50a9b-103">stringFormat</span><span class="sxs-lookup"><span data-stu-id="50a9b-103">stringFormat</span></span>

<span data-ttu-id="50a9b-104">Gibt an, wie [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) den Wert der Eigenschaft als Zeichenfolge formatieren soll.</span><span class="sxs-lookup"><span data-stu-id="50a9b-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="50a9b-105">Dies gilt nur, wenn <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="50a9b-105">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="50a9b-106">Es sollte nur ein [stringFormat-Element]() für jedes [displayInfo-Element](./propdesc-schema-displayinfo.md) vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="50a9b-106">There should be only one [stringFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="50a9b-107">Wenn mehrere Elemente vorhanden sind, wird das letzte Element verwendet.</span><span class="sxs-lookup"><span data-stu-id="50a9b-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="50a9b-108">Wenn kein [stringFormat-Element]() bereitgestellt wird, werden die Standardattributeinstellungen auf die Eigenschaftenbeschreibung angewendet.</span><span class="sxs-lookup"><span data-stu-id="50a9b-108">If no [stringFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="50a9b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="50a9b-109">Syntax</span></span>


```
<!-- stringFormat -->
<xs:element name="stringFormat"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="formatAs">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="FileName"/>
                    <xs:enumeration value="FilePath"/>
                    <xs:enumeration value="Hyperlink"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="50a9b-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="50a9b-110">Element Information</span></span>



| <span data-ttu-id="50a9b-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="50a9b-111">Parent Element</span></span>                                   | <span data-ttu-id="50a9b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="50a9b-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="50a9b-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="50a9b-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="50a9b-114">Keine</span><span class="sxs-lookup"><span data-stu-id="50a9b-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="50a9b-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="50a9b-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="50a9b-116">attribute</span><span class="sxs-lookup"><span data-stu-id="50a9b-116">Attribute</span></span></th>
<th><span data-ttu-id="50a9b-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50a9b-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="50a9b-118">formatAs</span><span class="sxs-lookup"><span data-stu-id="50a9b-118">formatAs</span></span></td>
<td><span data-ttu-id="50a9b-119">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="50a9b-119">Public.</span></span> <span data-ttu-id="50a9b-120">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="50a9b-120">Optional.</span></span> <span data-ttu-id="50a9b-121">Der Standardwert ist &quot; &quot; Allgemein.</span><span class="sxs-lookup"><span data-stu-id="50a9b-121">Default is &quot;General&quot;.</span></span> <span data-ttu-id="50a9b-122">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="50a9b-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="50a9b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="50a9b-123">Value</span></span></th>
<th><span data-ttu-id="50a9b-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="50a9b-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="50a9b-125">Allgemein</span><span class="sxs-lookup"><span data-stu-id="50a9b-125">General</span></span></td>
<td><span data-ttu-id="50a9b-126">Standard.</span><span class="sxs-lookup"><span data-stu-id="50a9b-126">Default.</span></span> <span data-ttu-id="50a9b-127">Gibt den Wert als unformatierte Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="50a9b-127">Returns the value as an unformatted string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50a9b-128">FileName</span><span class="sxs-lookup"><span data-stu-id="50a9b-128">FileName</span></span></td>
<td><span data-ttu-id="50a9b-129">Formatiert den Wert als Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="50a9b-129">Formats the value as a file name.</span></span> <span data-ttu-id="50a9b-130">Blendet die Erweiterung entsprechend den Benutzereinstellungen aus.</span><span class="sxs-lookup"><span data-stu-id="50a9b-130">Hides the extension according to user settings.</span></span> <span data-ttu-id="50a9b-131">Erfordert, dass der Eigenschaftstyp String ist.</span><span class="sxs-lookup"><span data-stu-id="50a9b-131">Requires the property type to be String.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50a9b-132">FilePath</span><span class="sxs-lookup"><span data-stu-id="50a9b-132">FilePath</span></span></td>
<td><span data-ttu-id="50a9b-133">Formatiert den Wert als Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="50a9b-133">Formats the value as a file path.</span></span> <span data-ttu-id="50a9b-134">Blendet die Erweiterung entsprechend den Benutzereinstellungen aus.</span><span class="sxs-lookup"><span data-stu-id="50a9b-134">Hides the extension according to user settings.</span></span> <span data-ttu-id="50a9b-135">Erfordert, dass der Eigenschaftstyp String ist.</span><span class="sxs-lookup"><span data-stu-id="50a9b-135">Requires the property type to be String.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50a9b-136">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="50a9b-136">Hyperlink</span></span></td>
<td><span data-ttu-id="50a9b-137">Formatiert den Wert als Link.</span><span class="sxs-lookup"><span data-stu-id="50a9b-137">Formats the value as a hyperlink.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
