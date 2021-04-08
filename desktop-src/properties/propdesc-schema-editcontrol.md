---
description: Gibt das Steuerelement an, das beim Bearbeiten der Eigenschaft verwendet werden soll.
ms.assetid: cef6d76f-664a-4808-a224-e82a5adb2d70
title: editcontrol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966f9742082fd6b5f939941a956eaae1ac4e427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959832"
---
# <a name="editcontrol"></a><span data-ttu-id="95420-103">editcontrol</span><span class="sxs-lookup"><span data-stu-id="95420-103">editControl</span></span>

<span data-ttu-id="95420-104">Gibt das Steuerelement an, das beim Bearbeiten der Eigenschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="95420-104">Specifies what control to use when editing the property.</span></span> <span data-ttu-id="95420-105">Es darf nur ein [editcontrol]() -Element für jedes [DisplayInfo](./propdesc-schema-displayinfo.md) -Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="95420-105">There should be only one [editControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="95420-106">Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet.</span><span class="sxs-lookup"><span data-stu-id="95420-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="95420-107">Wenn kein [editcontrol]() -Element bereitgestellt wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.</span><span class="sxs-lookup"><span data-stu-id="95420-107">If no [editControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

<span data-ttu-id="95420-108">Wenn <typeInfo isInnate="true"> , wird dieses Element ignoriert, da eine angeborene Eigenschaft nicht bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="95420-108">If <typeInfo isInnate="true">, this element is ignored because an innate property cannot be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="95420-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="95420-109">Syntax</span></span>


```
<!-- editControl -->
<xs:element name="editControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                    <xs:enumeration value="IconList"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="95420-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="95420-110">Element Information</span></span>



| <span data-ttu-id="95420-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="95420-111">Parent Element</span></span>                                   | <span data-ttu-id="95420-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="95420-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="95420-113">Display Info</span><span class="sxs-lookup"><span data-stu-id="95420-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="95420-114">Keine</span><span class="sxs-lookup"><span data-stu-id="95420-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="95420-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="95420-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="95420-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="95420-116">Attribute</span></span></th>
<th><span data-ttu-id="95420-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95420-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="95420-118">Steuerung</span><span class="sxs-lookup"><span data-stu-id="95420-118">control</span></span></td>
<td><span data-ttu-id="95420-119">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="95420-119">Public.</span></span> <span data-ttu-id="95420-120">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="95420-120">Optional.</span></span> <span data-ttu-id="95420-121">Der Standardwert ist Default &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="95420-121">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="95420-122">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="95420-122">The following are valid values.</span></span> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="95420-123">Wert</span><span class="sxs-lookup"><span data-stu-id="95420-123">Value</span></span></th>
<th><span data-ttu-id="95420-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="95420-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="95420-125">Standard</span><span class="sxs-lookup"><span data-stu-id="95420-125">Default</span></span></td>
<td><span data-ttu-id="95420-126">Standard.</span><span class="sxs-lookup"><span data-stu-id="95420-126">Default.</span></span> <span data-ttu-id="95420-127">Verwendet das Standard Steuerelement auf Grundlage des- <typeInfo type=&quot;&quot;> Attributs.</span><span class="sxs-lookup"><span data-stu-id="95420-127">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="95420-128">Die Standardtypen sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="95420-128">The default types are listed below.</span></span> <span data-ttu-id="95420-129">Jeder andere Typ führt zur Verwendung des &quot; Text- &quot; Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="95420-129">Any other type results in using the &quot;Text&quot; control.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="95420-130">type</span><span class="sxs-lookup"><span data-stu-id="95420-130">Type</span></span></th>
<th><span data-ttu-id="95420-131">Control</span><span class="sxs-lookup"><span data-stu-id="95420-131">Control</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="95420-132">String</span><span class="sxs-lookup"><span data-stu-id="95420-132">String</span></span></td>
<td><span data-ttu-id="95420-133">Text</span><span class="sxs-lookup"><span data-stu-id="95420-133">Text</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95420-134">Zeichenfolge (mehrere Werte)</span><span class="sxs-lookup"><span data-stu-id="95420-134">String (multi-value)</span></span></td>
<td><span data-ttu-id="95420-135">Multivaluetext</span><span class="sxs-lookup"><span data-stu-id="95420-135">MultiValueText</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95420-136">Datetime</span><span class="sxs-lookup"><span data-stu-id="95420-136">DateTime</span></span></td>
<td><span data-ttu-id="95420-137">Kalender</span><span class="sxs-lookup"><span data-stu-id="95420-137">Calendar</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95420-138">Kalender</span><span class="sxs-lookup"><span data-stu-id="95420-138">Calendar</span></span></td>
<td><span data-ttu-id="95420-139">Verwendet das Kalender Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="95420-139">Uses the calendar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95420-140">Checkboxdroplist</span><span class="sxs-lookup"><span data-stu-id="95420-140">CheckboxDropList</span></span></td>
<td><span data-ttu-id="95420-141">Verwendet das Listen Steuerelement mit Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="95420-141">Uses the list control with checkboxes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95420-142">Droplist</span><span class="sxs-lookup"><span data-stu-id="95420-142">DropList</span></span></td>
<td><span data-ttu-id="95420-143">Verwendet das Dropdown Listen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="95420-143">Uses the dropdown list control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95420-144">Multilinetext</span><span class="sxs-lookup"><span data-stu-id="95420-144">MultiLineText</span></span></td>
<td><span data-ttu-id="95420-145">Verwendet das mehrzeilige Textbearbeitungs-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="95420-145">Uses the multi-line text edit control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95420-146">Multivaluetext</span><span class="sxs-lookup"><span data-stu-id="95420-146">MultiValueText</span></span></td>
<td><span data-ttu-id="95420-147">Verwendet das mehrwertige Text Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="95420-147">Uses the multi-value text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95420-148">Rating</span><span class="sxs-lookup"><span data-stu-id="95420-148">Rating</span></span></td>
<td><span data-ttu-id="95420-149">Verwendet das 5-Sterne-Bewertungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="95420-149">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95420-150">Text</span><span class="sxs-lookup"><span data-stu-id="95420-150">Text</span></span></td>
<td><span data-ttu-id="95420-151">Verwendet das Steuerelement für die Textbearbeitung.</span><span class="sxs-lookup"><span data-stu-id="95420-151">Uses the text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95420-152">IconList</span><span class="sxs-lookup"><span data-stu-id="95420-152">IconList</span></span></td>
<td><span data-ttu-id="95420-153"><strong>Windows 7 und höher.</strong></span><span class="sxs-lookup"><span data-stu-id="95420-153"><strong>Windows 7 and later.</strong></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
