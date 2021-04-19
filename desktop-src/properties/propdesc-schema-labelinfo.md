---
description: Gibt an, wie die Bezeichnungen der Eigenschaft angezeigt werden.
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: Labelinfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cc0cfc417fae49527bcee50ac5043b1f07f309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349134"
---
# <a name="labelinfo"></a><span data-ttu-id="ae6df-103">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="ae6df-103">labelInfo</span></span>

<span data-ttu-id="ae6df-104">Gibt an, wie die Bezeichnungen der Eigenschaft angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ae6df-104">Specifies how the property's labels are displayed.</span></span> <span data-ttu-id="ae6df-105">Es darf nur ein [Labelinfo]() -Element für jedes [propertydescription](./propdesc-schema-propertydescription.md) -Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ae6df-105">There should be only one [labelInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span>

<span data-ttu-id="ae6df-106">Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet.</span><span class="sxs-lookup"><span data-stu-id="ae6df-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="ae6df-107">Wenn kein [Labelinfo]() -Element angegeben wird, wird die Bezeichnung der Eigenschaft nicht angezeigt. Dies wäre in der Regel jedoch ein Fehler.</span><span class="sxs-lookup"><span data-stu-id="ae6df-107">If no [labelInfo]() element is provided, then the property's label is not displayed; however, this would typically be a defect.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae6df-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae6df-108">Syntax</span></span>


```
<!-- labelInfo -->
<xs:element name="labelInfo">
    <xs:complexType>
        <xs:attribute name="label" type="xs:string"/>
        <xs:attribute name="sortDescription">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="AToZ"/>
                    <xs:enumeration value="LowestHighest"/>
                    <xs:enumeration value="OldestNewest"/>
                    <xs:enumeration value="SmallestLargest"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="invitationText" type="xs:string"/>
        <xs:attribute name="hideLabel" type="xs:boolean" default="false"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="ae6df-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ae6df-109">Element Information</span></span>



| <span data-ttu-id="ae6df-110">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="ae6df-110">Parent Element</span></span>                                                   | <span data-ttu-id="ae6df-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ae6df-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="ae6df-112">propertydescription</span><span class="sxs-lookup"><span data-stu-id="ae6df-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="ae6df-113">Keine</span><span class="sxs-lookup"><span data-stu-id="ae6df-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="ae6df-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="ae6df-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae6df-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="ae6df-115">Attribute</span></span></th>
<th><span data-ttu-id="ae6df-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae6df-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ae6df-117">label</span><span class="sxs-lookup"><span data-stu-id="ae6df-117">label</span></span></td>
<td><span data-ttu-id="ae6df-118">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="ae6df-118">Public.</span></span> <span data-ttu-id="ae6df-119">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ae6df-119">Optional.</span></span> <span data-ttu-id="ae6df-120">Die Bezeichnung, wie Sie in der Benutzeroberfläche angezeigt wird (z. b. die Bezeichnung "Details" oder "Vorschau").</span><span class="sxs-lookup"><span data-stu-id="ae6df-120">The label as it is displayed in the UI (for example, the details column label or preview pane).</span></span> <span data-ttu-id="ae6df-121">Die Syntax ermöglicht eine direkte Anzeige Zeichenfolge oder einen indirekten Verweis auf eine Anzeige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ae6df-121">The syntax allows for a direct display string or an indirect display string reference.</span></span> <span data-ttu-id="ae6df-122">Verwenden Sie die indirekte Anzeige Zeichenfolge, da Sie lokalisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae6df-122">Use the indirect display string because it can be localized.</span></span> <span data-ttu-id="ae6df-123"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>Ipropertydescription:: GetDisplayName</strong></a> gibt den aufgelösten anzeigen Amen zurück.</span><span class="sxs-lookup"><span data-stu-id="ae6df-123"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription::GetDisplayName</strong></a> returns the resolved display name.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae6df-124">SortDescription</span><span class="sxs-lookup"><span data-stu-id="ae6df-124">sortDescription</span></span></td>
<td><span data-ttu-id="ae6df-125">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ae6df-125">Optional.</span></span> <span data-ttu-id="ae6df-126">Gibt die als Sortieroptionen angebotenen Zeichen folgen an.</span><span class="sxs-lookup"><span data-stu-id="ae6df-126">Specifies the strings offered as sort options.</span></span> <span data-ttu-id="ae6df-127"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>Ipropertydescription:: getsortdescription</strong></a> gibt diese Sortier Beschreibung zurück.</span><span class="sxs-lookup"><span data-stu-id="ae6df-127"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription::GetSortDescription</strong></a> returns this sort description.</span></span> <span data-ttu-id="ae6df-128">Die folgenden Werte stellen die entsprechenden UI-Zeichen folgen bereit.</span><span class="sxs-lookup"><span data-stu-id="ae6df-128">The following values provide the corresponding UI strings.</span></span>
<ul>
<li><span data-ttu-id="ae6df-129">Allgemein: &quot; Sortieren nach oben &quot;  /  &quot; Sortieren&quot;</span><span class="sxs-lookup"><span data-stu-id="ae6df-129">General: &quot;Sort going up&quot; / &quot;Sort going down&quot;</span></span></li>
<li><span data-ttu-id="ae6df-130">Atoz: &quot; A in Top &quot;  /  &quot; Z on Top&quot;</span><span class="sxs-lookup"><span data-stu-id="ae6df-130">AToZ: &quot;A on top&quot; / &quot;Z on top&quot;</span></span></li>
<li><span data-ttu-id="ae6df-131">Lowesthighest: &quot; niedrigste am oberen &quot; oberen Rand  /  &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="ae6df-131">LowestHighest: &quot;Lowest on top&quot; / &quot;Highest on top&quot;</span></span></li>
<li><span data-ttu-id="ae6df-132">Oldestlatest: &quot; älteste oben nach oben &quot;  /  &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="ae6df-132">OldestNewest: &quot;Oldest on top&quot; / &quot;Newest on top&quot;</span></span></li>
<li><span data-ttu-id="ae6df-133">Smallestmost: &quot; kleinste am oberen &quot; oberen Rand  /  &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="ae6df-133">SmallestLargest: &quot;Smallest on top&quot; / &quot;Largest on top&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae6df-134">invitationtext</span><span class="sxs-lookup"><span data-stu-id="ae6df-134">invitationText</span></span></td>
<td><span data-ttu-id="ae6df-135">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ae6df-135">Optional.</span></span> <span data-ttu-id="ae6df-136">Der Text der Hilfe Zeichenfolge, der dem Benutzer als Anweisung für das Steuerelement oder die QuickInfo angezeigt wird (z.b. &quot; Name des Autors &quot; ).</span><span class="sxs-lookup"><span data-stu-id="ae6df-136">The Help string text that is displayed as an instruction to the user for the control or ToolTip (for instance, &quot;Enter author name.&quot;).</span></span> <span data-ttu-id="ae6df-137">Die Syntax ermöglicht eine direkte Anzeige Zeichenfolge oder einen indirekten Verweis auf eine Anzeige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ae6df-137">The syntax allows for a direct display string or an indirect display string reference.</span></span> <span data-ttu-id="ae6df-138">Verwenden Sie die indirekte Anzeige Zeichenfolge, da Sie lokalisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae6df-138">Use the indirect display string because it can be localized.</span></span> <span data-ttu-id="ae6df-139"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>Ipropertydescription:: geteditinvitation</strong></a> gibt den aufgelösten Einladungstext zurück.</span><span class="sxs-lookup"><span data-stu-id="ae6df-139"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription::GetEditInvitation</strong></a> returns the resolved invitation text.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae6df-140">hidelta Label</span><span class="sxs-lookup"><span data-stu-id="ae6df-140">hideLabel</span></span></td>
<td><span data-ttu-id="ae6df-141">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ae6df-141">Optional.</span></span> <span data-ttu-id="ae6df-142">Die Standardeinstellung ist &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="ae6df-142">The default is &quot;false&quot;.</span></span> <span data-ttu-id="ae6df-143">Gibt an, ob die Bezeichnung ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="ae6df-143">Indicates whether the label is hidden.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
