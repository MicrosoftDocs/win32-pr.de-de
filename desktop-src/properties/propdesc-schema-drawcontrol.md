---
description: Gibt das Steuerelement an, das beim einfachen Anzeigen der Eigenschaft verwendet werden soll.
ms.assetid: 0fb8afc4-d16b-4c2e-80b3-da9935b11bb5
title: DrawControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5318fdebc995ff45932f75b4000ceda6e74068e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042032"
---
# <a name="drawcontrol"></a><span data-ttu-id="815f5-103">DrawControl</span><span class="sxs-lookup"><span data-stu-id="815f5-103">drawControl</span></span>

<span data-ttu-id="815f5-104">Gibt das Steuerelement an, das beim einfachen Anzeigen der Eigenschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="815f5-104">Specifies what control to use when simply displaying the property.</span></span> <span data-ttu-id="815f5-105">Es darf nur ein [DrawControl]() -Element für jedes [DisplayInfo](./propdesc-schema-displayinfo.md) -Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="815f5-105">There should be only one [drawControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="815f5-106">Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet.</span><span class="sxs-lookup"><span data-stu-id="815f5-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="815f5-107">Wenn kein [DrawControl]() -Element bereitgestellt wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.</span><span class="sxs-lookup"><span data-stu-id="815f5-107">If no [drawControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

<span data-ttu-id="815f5-108">Diese Form des Steuer Elements ermöglicht keine Eigenschaften Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="815f5-108">This form of the control does not allow for property editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="815f5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="815f5-109">Syntax</span></span>


```
<!-- drawControl -->
<xs:element name="drawControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="PercentBar"/>
                    <xs:enumeration value="ProgressBar"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="StaticText"/>
                    <xs:enumeration value="IconList"/>
                    <xs:enumeration value="BooleanCheckMark"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="815f5-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="815f5-110">Element Information</span></span>



| <span data-ttu-id="815f5-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="815f5-111">Parent Element</span></span>                                   | <span data-ttu-id="815f5-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="815f5-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="815f5-113">Display Info</span><span class="sxs-lookup"><span data-stu-id="815f5-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="815f5-114">Keine</span><span class="sxs-lookup"><span data-stu-id="815f5-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="815f5-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="815f5-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="815f5-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="815f5-116">Attribute</span></span></th>
<th><span data-ttu-id="815f5-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="815f5-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="815f5-118">Steuerung</span><span class="sxs-lookup"><span data-stu-id="815f5-118">control</span></span></td>
<td><span data-ttu-id="815f5-119">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="815f5-119">Public.</span></span> <span data-ttu-id="815f5-120">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="815f5-120">Optional.</span></span> <span data-ttu-id="815f5-121">Der Standardwert ist Default &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="815f5-121">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="815f5-122">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="815f5-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="815f5-123">Wert</span><span class="sxs-lookup"><span data-stu-id="815f5-123">Value</span></span></th>
<th><span data-ttu-id="815f5-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="815f5-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="815f5-125">Standard</span><span class="sxs-lookup"><span data-stu-id="815f5-125">Default</span></span></td>
<td><span data-ttu-id="815f5-126">Standard.</span><span class="sxs-lookup"><span data-stu-id="815f5-126">Default.</span></span> <span data-ttu-id="815f5-127">Verwendet das Standard Steuerelement auf Grundlage des- <typeInfo type=&quot;&quot;> Attributs.</span><span class="sxs-lookup"><span data-stu-id="815f5-127">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="815f5-128">Der Standardtyp ist &quot; String &quot; (MultiValue), und das Standard Steuerelement ist &quot; multivaluetext &quot; .</span><span class="sxs-lookup"><span data-stu-id="815f5-128">The default type is &quot;String&quot; (multi-value) and the default control is &quot;MultiValueText&quot;.</span></span> <span data-ttu-id="815f5-129">Jeder andere Typ führt zur Verwendung des &quot; StaticText- &quot; Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="815f5-129">Any other type results in using the &quot;StaticText&quot; control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="815f5-130">Multilinetext</span><span class="sxs-lookup"><span data-stu-id="815f5-130">MultiLineText</span></span></td>
<td><span data-ttu-id="815f5-131">Verwendet das mehrzeilige Text Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="815f5-131">Uses the multi-line text control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="815f5-132">Multivaluetext</span><span class="sxs-lookup"><span data-stu-id="815f5-132">MultiValueText</span></span></td>
<td><span data-ttu-id="815f5-133">Verwendet das mehrwertige Text Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="815f5-133">Uses the multi-value text control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="815f5-134">Prozentualbar</span><span class="sxs-lookup"><span data-stu-id="815f5-134">PercentBar</span></span></td>
<td><span data-ttu-id="815f5-135">Verwendet das Prozent leisten-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="815f5-135">Uses the percent bar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="815f5-136">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="815f5-136">ProgressBar</span></span></td>
<td><span data-ttu-id="815f5-137">Verwendet das Statusanzeige-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="815f5-137">Uses the progress bar control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="815f5-138">Rating</span><span class="sxs-lookup"><span data-stu-id="815f5-138">Rating</span></span></td>
<td><span data-ttu-id="815f5-139">Verwendet das 5-Sterne-Bewertungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="815f5-139">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="815f5-140">StaticText</span><span class="sxs-lookup"><span data-stu-id="815f5-140">StaticText</span></span></td>
<td><span data-ttu-id="815f5-141">Verwendet <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>ipropertydescription:: formatfordisplay</strong></a> , um den Eigenschafts Wert anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="815f5-141">Uses <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>IPropertyDescription::FormatForDisplay</strong></a> to display the property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="815f5-142">IconList</span><span class="sxs-lookup"><span data-stu-id="815f5-142">IconList</span></span></td>
<td><span data-ttu-id="815f5-143"><strong>Windows 7 und höher.</strong></span><span class="sxs-lookup"><span data-stu-id="815f5-143"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="815f5-144">Eine Enumeration von Symbolen.</span><span class="sxs-lookup"><span data-stu-id="815f5-144">An enumeration of icons.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="815f5-145">Booleancheckmark</span><span class="sxs-lookup"><span data-stu-id="815f5-145">BooleanCheckMark</span></span></td>
<td><span data-ttu-id="815f5-146"><strong>Windows 7 und höher.</strong></span><span class="sxs-lookup"><span data-stu-id="815f5-146"><strong>Windows 7 and later.</strong></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
