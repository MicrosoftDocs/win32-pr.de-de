---
description: 'Gibt an, wie ipropertydescription:: formatfordisplay den Wert der Eigenschaft als Zeichenfolge formatieren soll. Dies gilt nur, wenn <displayInfo displayType=&\#0034;String&\#0034;> .'
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec05a6eedf1734c1d62c0503027810ad05916160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356888"
---
# <a name="stringformat"></a><span data-ttu-id="552cb-104">stringFormat</span><span class="sxs-lookup"><span data-stu-id="552cb-104">stringFormat</span></span>

<span data-ttu-id="552cb-105">Gibt an, wie [**ipropertydescription:: formatfordisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) den Wert der Eigenschaft als Zeichenfolge formatieren soll.</span><span class="sxs-lookup"><span data-stu-id="552cb-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="552cb-106">Dies gilt nur, wenn <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="552cb-106">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="552cb-107">Es darf nur ein [StringFormat]() -Element für jedes [DisplayInfo](./propdesc-schema-displayinfo.md) -Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="552cb-107">There should be only one [stringFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="552cb-108">Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet.</span><span class="sxs-lookup"><span data-stu-id="552cb-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="552cb-109">Wenn kein [StringFormat]() -Element bereitgestellt wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.</span><span class="sxs-lookup"><span data-stu-id="552cb-109">If no [stringFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="552cb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="552cb-110">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="552cb-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="552cb-111">Element Information</span></span>



| <span data-ttu-id="552cb-112">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="552cb-112">Parent Element</span></span>                                   | <span data-ttu-id="552cb-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="552cb-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="552cb-114">Display Info</span><span class="sxs-lookup"><span data-stu-id="552cb-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="552cb-115">Keine</span><span class="sxs-lookup"><span data-stu-id="552cb-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="552cb-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="552cb-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="552cb-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="552cb-117">Attribute</span></span></th>
<th><span data-ttu-id="552cb-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="552cb-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="552cb-119">formatas</span><span class="sxs-lookup"><span data-stu-id="552cb-119">formatAs</span></span></td>
<td><span data-ttu-id="552cb-120">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="552cb-120">Public.</span></span> <span data-ttu-id="552cb-121">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="552cb-121">Optional.</span></span> <span data-ttu-id="552cb-122">Der Standardwert ist &quot; Allgemein &quot; .</span><span class="sxs-lookup"><span data-stu-id="552cb-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="552cb-123">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="552cb-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="552cb-124">Wert</span><span class="sxs-lookup"><span data-stu-id="552cb-124">Value</span></span></th>
<th><span data-ttu-id="552cb-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="552cb-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="552cb-126">Allgemein</span><span class="sxs-lookup"><span data-stu-id="552cb-126">General</span></span></td>
<td><span data-ttu-id="552cb-127">Standard.</span><span class="sxs-lookup"><span data-stu-id="552cb-127">Default.</span></span> <span data-ttu-id="552cb-128">Gibt den Wert als unformatierte Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="552cb-128">Returns the value as an unformatted string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="552cb-129">FileName</span><span class="sxs-lookup"><span data-stu-id="552cb-129">FileName</span></span></td>
<td><span data-ttu-id="552cb-130">Formatiert den Wert als Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="552cb-130">Formats the value as a file name.</span></span> <span data-ttu-id="552cb-131">Blendet die Erweiterung entsprechend den Benutzereinstellungen aus.</span><span class="sxs-lookup"><span data-stu-id="552cb-131">Hides the extension according to user settings.</span></span> <span data-ttu-id="552cb-132">Erfordert, dass der Eigenschaftentyp Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="552cb-132">Requires the property type to be String.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="552cb-133">FilePath</span><span class="sxs-lookup"><span data-stu-id="552cb-133">FilePath</span></span></td>
<td><span data-ttu-id="552cb-134">Formatiert den Wert als Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="552cb-134">Formats the value as a file path.</span></span> <span data-ttu-id="552cb-135">Blendet die Erweiterung entsprechend den Benutzereinstellungen aus.</span><span class="sxs-lookup"><span data-stu-id="552cb-135">Hides the extension according to user settings.</span></span> <span data-ttu-id="552cb-136">Erfordert, dass der Eigenschaftentyp Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="552cb-136">Requires the property type to be String.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="552cb-137">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="552cb-137">Hyperlink</span></span></td>
<td><span data-ttu-id="552cb-138">Formatiert den Wert als Link.</span><span class="sxs-lookup"><span data-stu-id="552cb-138">Formats the value as a hyperlink.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
