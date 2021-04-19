---
description: Wird in Windows 7 und höher nicht unterstützt. Gibt an, welches Steuerelement im Abfrage-Generator verwendet werden soll.
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: querycontrol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448b47038f82afb9f860209bfe89eb9e6eecb890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356632"
---
# <a name="querycontrol"></a><span data-ttu-id="00d01-104">querycontrol</span><span class="sxs-lookup"><span data-stu-id="00d01-104">queryControl</span></span>

<span data-ttu-id="00d01-105">Wird in Windows 7 und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00d01-105">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="00d01-106">Gibt an, welches Steuerelement im Abfrage-Generator verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="00d01-106">Specifies what control to use in the query builder.</span></span> <span data-ttu-id="00d01-107">Es darf nur ein [querycontrol]() -Element für jedes [DisplayInfo](./propdesc-schema-displayinfo.md) -Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="00d01-107">There should be only one [queryControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="00d01-108">Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet.</span><span class="sxs-lookup"><span data-stu-id="00d01-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="00d01-109">Wenn kein [querycontrol]() -Element bereitgestellt wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.</span><span class="sxs-lookup"><span data-stu-id="00d01-109">If no [queryControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="00d01-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="00d01-110">Syntax</span></span>


```
<!-- queryControl -->
<xs:element name="queryControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="NumericText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="00d01-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="00d01-111">Element Information</span></span>



| <span data-ttu-id="00d01-112">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="00d01-112">Parent Element</span></span>                                   | <span data-ttu-id="00d01-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="00d01-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="00d01-114">Display Info</span><span class="sxs-lookup"><span data-stu-id="00d01-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="00d01-115">Keine</span><span class="sxs-lookup"><span data-stu-id="00d01-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="00d01-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="00d01-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00d01-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="00d01-117">Attribute</span></span></th>
<th><span data-ttu-id="00d01-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00d01-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="00d01-119">Steuerung</span><span class="sxs-lookup"><span data-stu-id="00d01-119">control</span></span></td>
<td><span data-ttu-id="00d01-120">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="00d01-120">Public.</span></span> <span data-ttu-id="00d01-121">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="00d01-121">Optional.</span></span> <span data-ttu-id="00d01-122">Der Standardwert ist Default &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="00d01-122">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="00d01-123">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="00d01-123">The following are valid values.</span></span> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00d01-124">Wert</span><span class="sxs-lookup"><span data-stu-id="00d01-124">Value</span></span></th>
<th><span data-ttu-id="00d01-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="00d01-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="00d01-126">Standard</span><span class="sxs-lookup"><span data-stu-id="00d01-126">Default</span></span></td>
<td><span data-ttu-id="00d01-127">Standard.</span><span class="sxs-lookup"><span data-stu-id="00d01-127">Default.</span></span> <span data-ttu-id="00d01-128">Verwendet das Standard Steuerelement auf Grundlage des- <typeInfo type=&quot;&quot;> Attributs.</span><span class="sxs-lookup"><span data-stu-id="00d01-128">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="00d01-129">Die Standardtypen sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="00d01-129">The default types are listed below.</span></span> <span data-ttu-id="00d01-130">Jeder andere Typ führt zur Verwendung des &quot; Text- &quot; Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="00d01-130">Any other type results in using the &quot;Text&quot; control.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="00d01-131">ConditionType</span><span class="sxs-lookup"><span data-stu-id="00d01-131">ConditionType</span></span></th>
<th><span data-ttu-id="00d01-132">Control</span><span class="sxs-lookup"><span data-stu-id="00d01-132">Control</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="00d01-133">String</span><span class="sxs-lookup"><span data-stu-id="00d01-133">String</span></span></td>
<td><span data-ttu-id="00d01-134">Text</span><span class="sxs-lookup"><span data-stu-id="00d01-134">Text</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00d01-135">Zeichenfolge (mehrere Werte)</span><span class="sxs-lookup"><span data-stu-id="00d01-135">String (multi-value)</span></span></td>
<td><span data-ttu-id="00d01-136">Multivaluetext</span><span class="sxs-lookup"><span data-stu-id="00d01-136">MultiValueText</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00d01-137">Anzahl oder Größe</span><span class="sxs-lookup"><span data-stu-id="00d01-137">Number or Size</span></span></td>
<td><span data-ttu-id="00d01-138">Numerictext</span><span class="sxs-lookup"><span data-stu-id="00d01-138">NumericText</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00d01-139">Number oder size (Enum)</span><span class="sxs-lookup"><span data-stu-id="00d01-139">Number or Size (enum)</span></span></td>
<td><span data-ttu-id="00d01-140">List</span><span class="sxs-lookup"><span data-stu-id="00d01-140">List</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00d01-141">Datetime</span><span class="sxs-lookup"><span data-stu-id="00d01-141">DateTime</span></span></td>
<td><span data-ttu-id="00d01-142">Kalender</span><span class="sxs-lookup"><span data-stu-id="00d01-142">Calendar</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00d01-143">Boolean</span><span class="sxs-lookup"><span data-stu-id="00d01-143">Boolean</span></span></td>
<td><span data-ttu-id="00d01-144">Boolean</span><span class="sxs-lookup"><span data-stu-id="00d01-144">Boolean</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00d01-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="00d01-145">Boolean</span></span></td>
<td><span data-ttu-id="00d01-146">Verwendet das boolesche Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="00d01-146">Uses the boolean control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00d01-147">Kalender</span><span class="sxs-lookup"><span data-stu-id="00d01-147">Calendar</span></span></td>
<td><span data-ttu-id="00d01-148">Verwendet das Dropdown-Kalender Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="00d01-148">Uses the dropdown calendar control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00d01-149">Checkboxdroplist</span><span class="sxs-lookup"><span data-stu-id="00d01-149">CheckboxDropList</span></span></td>
<td><span data-ttu-id="00d01-150">Verwendet das Listen Steuerelement mit Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="00d01-150">Uses the list control with checkboxes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00d01-151">Droplist</span><span class="sxs-lookup"><span data-stu-id="00d01-151">DropList</span></span></td>
<td><span data-ttu-id="00d01-152">Verwendet das Dropdown Listen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="00d01-152">Uses the dropdown list control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00d01-153">Multivaluetext</span><span class="sxs-lookup"><span data-stu-id="00d01-153">MultiValueText</span></span></td>
<td><span data-ttu-id="00d01-154">Verwendet das mehrwertige Text Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="00d01-154">Uses the multi-value text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00d01-155">Numerictext</span><span class="sxs-lookup"><span data-stu-id="00d01-155">NumericText</span></span></td>
<td><span data-ttu-id="00d01-156">Verwendet das numerische Textbearbeitungs-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="00d01-156">Uses the numeric text edit control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00d01-157">Rating</span><span class="sxs-lookup"><span data-stu-id="00d01-157">Rating</span></span></td>
<td><span data-ttu-id="00d01-158">Verwendet das 5-Sterne-Bewertungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="00d01-158">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00d01-159">Text</span><span class="sxs-lookup"><span data-stu-id="00d01-159">Text</span></span></td>
<td><span data-ttu-id="00d01-160">Verwendet das Steuerelement für die Textbearbeitung.</span><span class="sxs-lookup"><span data-stu-id="00d01-160">Uses the text edit control.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
