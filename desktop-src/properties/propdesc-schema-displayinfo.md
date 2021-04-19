---
description: Gibt die Anzeigeinformationen einer Eigenschaft an.
ms.assetid: 27c03ced-a5fa-4ab4-b88e-5b78701da878
title: Display Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fff0bb441b4535c0b6c6f3183671fbe8ade09183
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360558"
---
# <a name="displayinfo"></a><span data-ttu-id="4bc4a-103">Display Info</span><span class="sxs-lookup"><span data-stu-id="4bc4a-103">displayInfo</span></span>

<span data-ttu-id="4bc4a-104">Gibt die Anzeigeinformationen einer Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-104">Specifies a property's display information.</span></span> <span data-ttu-id="4bc4a-105">Es darf nur ein [DisplayInfo]() -Element für jede [propertydescription](./propdesc-schema-propertydescription.md)vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-105">There should be only one [displayInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md).</span></span>

<span data-ttu-id="4bc4a-106">Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="4bc4a-107">Wenn kein [DisplayInfo]() -Element bereitgestellt wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-107">If no [displayInfo]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bc4a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bc4a-108">Syntax</span></span>


```
<!-- displayInfo -->
<xs:element name="displayInfo">
    <xs:complexType>
        <xs:all>
            <xs:element name="stringFormat" minOccurs="0" maxOccurs="1">
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
            <xs:element name="booleanFormat" minOccurs="0" maxOccurs="1">
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
            <xs:element name="numberFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="General"/>
                                <xs:enumeration value="Percentage"/>
                                <xs:enumeration value="ByteSize"/>
                                <xs:enumeration value="KBSize"/>
                                <xs:enumeration value="SampleSize"/>
                                <xs:enumeration value="Bitrate"/>
                                <xs:enumeration value="SampleRate"/>
                                <xs:enumeration value="FrameRate"/>
                                <xs:enumeration value="Pixels"/>
                                <xs:enumeration value="DPI"/>
                                <xs:enumeration value="Duration"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                    <xs:attribute name="formatDurationAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="hh:mm"/>
                                <xs:enumeration value="hh:mm:ss"/>
                                <xs:enumeration value="hh:mm:ss.fff"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="dateTimeFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="General"/>
                                <xs:enumeration value="Month"/>
                                <xs:enumeration value="YearMonth"/>
                                <xs:enumeration value="Year"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                    <xs:attribute name="formatTimeAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="ShortTime"/>
                                <xs:enumeration value="LongTime"/>
                                <xs:enumeration value="HideTime"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                    <xs:attribute name="formatDateAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="ShortDate"/>
                                <xs:enumeration value="LongDate"/>
                                <xs:enumeration value="HideDate"/>
                                <xs:enumeration value="RelativeShortDate"/>
                                <xs:enumeration value="RelativeLongDate"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="enumeratedList" minOccurs="0" maxOccurs="1">
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
                                <xs:attribute name="minValue" type="xs:string" use="required"/>
                                <xs:attribute name="setValue" type="xs:string"/>
                                <xs:attribute name="text" type="xs:string"/>
                            </xs:complexType>
                        </xs:element>
                    </xs:sequence>

                    <xs:attribute name="defaultText" type="xs:string"/>
                    <xs:attribute name="useValueForDefault" type="xs:boolean"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="drawControl" minOccurs="0" maxOccurs="1">
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
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="editControl" minOccurs="0" maxOccurs="1">
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
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="filterControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="Rating"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="queryControl" minOccurs="0" maxOccurs="1">
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
        </xs:all>

        <xs:attribute name="defaultColumnWidth" type="xs:nonNegativeInteger" default="20"/>
        <xs:attribute name="displayType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        
        <xs:attribute name="alignment" default="Left">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Left"/>
                    <xs:enumeration value="Center"/>
                    <xs:enumeration value="Right"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="relativeDescriptionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Count"/>
                    <xs:enumeration value="Revision"/>
                    <xs:enumeration value="Length"/>
                    <xs:enumeration value="Duration"/>
                    <xs:enumeration value="Speed"/>
                    <xs:enumeration value="Rate"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Priority"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultSortDirection" default="Ascending">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                  <xs:enumeration value="Ascending"/>
                  <xs:enumeration value="Descending"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="4bc4a-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4bc4a-109">Element Information</span></span>



| <span data-ttu-id="4bc4a-110">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="4bc4a-110">Parent Element</span></span>                                                   | <span data-ttu-id="4bc4a-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4bc4a-111">Child Elements</span></span>                                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4bc4a-112">propertydescription</span><span class="sxs-lookup"><span data-stu-id="4bc4a-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | [<span data-ttu-id="4bc4a-113">StringFormat</span><span class="sxs-lookup"><span data-stu-id="4bc4a-113">stringFormat</span></span>](./propdesc-schema-stringformat.md)                                                             |
|                                                                  | [<span data-ttu-id="4bc4a-114">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="4bc4a-114">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)                                                           |
|                                                                  | [<span data-ttu-id="4bc4a-115">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="4bc4a-115">numberFormat</span></span>](./propdesc-schema-numberformat.md)                                                             |
|                                                                  | [<span data-ttu-id="4bc4a-116">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="4bc4a-116">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)                                                         |
|                                                                  | [<span data-ttu-id="4bc4a-117">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="4bc4a-117">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)                                                         |
|                                                                  | [<span data-ttu-id="4bc4a-118">DrawControl</span><span class="sxs-lookup"><span data-stu-id="4bc4a-118">drawControl</span></span>](./propdesc-schema-drawcontrol.md)                                                               |
|                                                                  | [<span data-ttu-id="4bc4a-119">editcontrol</span><span class="sxs-lookup"><span data-stu-id="4bc4a-119">editControl</span></span>](./propdesc-schema-editcontrol.md)                                                               |
|                                                                  | [<span data-ttu-id="4bc4a-120">FilterControl</span><span class="sxs-lookup"><span data-stu-id="4bc4a-120">filterControl</span></span>](./propdesc-schema-filtercontrol.md)                                                           |
|                                                                  | <span data-ttu-id="4bc4a-121">[querycontrol](./propdesc-schema-querycontrol.md) (nur Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="4bc4a-121">[queryControl](./propdesc-schema-querycontrol.md) (Windows Vista only.</span></span> <span data-ttu-id="4bc4a-122">Wird in Windows 7 und höher nicht unterstützt.)</span><span class="sxs-lookup"><span data-stu-id="4bc4a-122">Not supported in Windows 7 and later.)</span></span> |



 

## <a name="attributes"></a><span data-ttu-id="4bc4a-123">Attribute</span><span class="sxs-lookup"><span data-stu-id="4bc4a-123">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4bc4a-124">Attribut</span><span class="sxs-lookup"><span data-stu-id="4bc4a-124">Attribute</span></span></th>
<th><span data-ttu-id="4bc4a-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4bc4a-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4bc4a-126">defaultcolumnwidth</span><span class="sxs-lookup"><span data-stu-id="4bc4a-126">defaultColumnWidth</span></span></td>
<td><span data-ttu-id="4bc4a-127">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-127">Public.</span></span> <span data-ttu-id="4bc4a-128">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-128">Optional.</span></span> <span data-ttu-id="4bc4a-129">Der Standardwert ist &quot; 20 &quot; .</span><span class="sxs-lookup"><span data-stu-id="4bc4a-129">Default is &quot;20&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bc4a-130">Display Type</span><span class="sxs-lookup"><span data-stu-id="4bc4a-130">displayType</span></span></td>
<td><span data-ttu-id="4bc4a-131">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-131">Public.</span></span> <span data-ttu-id="4bc4a-132">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-132">Optional.</span></span> <span data-ttu-id="4bc4a-133">Der Standardwert ist &quot; String &quot; .</span><span class="sxs-lookup"><span data-stu-id="4bc4a-133">Default is &quot;String&quot;.</span></span> <span data-ttu-id="4bc4a-134">Gibt den Typ der Anzeige Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-134">Specifies the type of the display string.</span></span> <span data-ttu-id="4bc4a-135">Nachdem Sie hier festgelegt haben, werden die zugeordneten <strong>PROPDESC_DISPLAYTYPE</strong> Werte von <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>ipropertydescription:: getdisplaytype</strong></a>abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-135">Once set here, the associated <strong>PROPDESC_DISPLAYTYPE</strong> values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>IPropertyDescription::GetDisplayType</strong></a>.</span></span> <span data-ttu-id="4bc4a-136">Die folgenden Typen sind gültig.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-136">The following are valid types.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4bc4a-137">Wert</span><span class="sxs-lookup"><span data-stu-id="4bc4a-137">Value</span></span></th>
<th><span data-ttu-id="4bc4a-138">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4bc4a-138">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4bc4a-139">String</span><span class="sxs-lookup"><span data-stu-id="4bc4a-139">String</span></span></td>
<td><span data-ttu-id="4bc4a-140">Standard.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-140">Default.</span></span> <span data-ttu-id="4bc4a-141">Der Wert wird als Zeichenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-141">Value is displayed as a string.</span></span> <span data-ttu-id="4bc4a-142">Verwenden &quot; Sie StringFormat &quot; , um zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-142">Use &quot;stringFormat&quot; to format.</span></span> <span data-ttu-id="4bc4a-143">Die Methode gibt PDDT_STRING zurück.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-143">Method returns PDDT_STRING.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bc4a-144">Number</span><span class="sxs-lookup"><span data-stu-id="4bc4a-144">Number</span></span></td>
<td><span data-ttu-id="4bc4a-145">Standardwert für numerische Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-145">Default for numeric properties.</span></span> <span data-ttu-id="4bc4a-146">Der Wert wird als Zahl angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-146">Value is displayed as a number.</span></span> <span data-ttu-id="4bc4a-147">Verwenden &quot; Sie "NumFormat" &quot; zum Formatieren.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-147">Use &quot;numberFormat&quot; to format.</span></span> <span data-ttu-id="4bc4a-148">Die Methode gibt PDDT_NUMBER zurück.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-148">Method returns PDDT_NUMBER.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4bc4a-149">Boolean</span><span class="sxs-lookup"><span data-stu-id="4bc4a-149">Boolean</span></span></td>
<td><span data-ttu-id="4bc4a-150">Standardwert, wenn <typeInfo type=&quot;Boolean&quot;> .</span><span class="sxs-lookup"><span data-stu-id="4bc4a-150">Default if <typeInfo type=&quot;Boolean&quot;>.</span></span> <span data-ttu-id="4bc4a-151">Der Wert wird als boolescher Wert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-151">Value is displayed as a boolean.</span></span> <span data-ttu-id="4bc4a-152">Verwenden &quot; Sie BooleanFormat &quot; , um zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-152">Use &quot;booleanFormat&quot; to format.</span></span> <span data-ttu-id="4bc4a-153">Die Methode gibt PDDT_BOOLEAN zurück.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-153">Method returns PDDT_BOOLEAN.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bc4a-154">Datetime</span><span class="sxs-lookup"><span data-stu-id="4bc4a-154">DateTime</span></span></td>
<td><span data-ttu-id="4bc4a-155">Standardwert, wenn <typeInfo type=&quot;DateTime&quot;> .</span><span class="sxs-lookup"><span data-stu-id="4bc4a-155">Default if <typeInfo type=&quot;DateTime&quot;>.</span></span> <span data-ttu-id="4bc4a-156">Der Wert wird als Datum oder Uhrzeit angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-156">Value is displayed as a date or time.</span></span> <span data-ttu-id="4bc4a-157">Verwenden &quot; Sie DateTimeFormat &quot; , um zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-157">Use &quot;dateTimeFormat&quot; to format.</span></span> <span data-ttu-id="4bc4a-158">Die Methode gibt PDDT_DATETIME zurück.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-158">Method returns PDDT_DATETIME.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4bc4a-159">Enumeration</span><span class="sxs-lookup"><span data-stu-id="4bc4a-159">Enumeration</span></span></td>
<td><span data-ttu-id="4bc4a-160">Der Wert wird als Darstellung der Anzeige Zeichenfolge angezeigt, die vom &quot; enumeratedlist-Element bereitgestellt wird &quot; .</span><span class="sxs-lookup"><span data-stu-id="4bc4a-160">Value is displayed as a display string mapping provided by the &quot;enumeratedList&quot; element.</span></span> <span data-ttu-id="4bc4a-161">Die Methode gibt PDDT_ENUMERATED zurück.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-161">Method returns PDDT_ENUMERATED.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4bc4a-162">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="4bc4a-162">alignment</span></span></td>
<td><span data-ttu-id="4bc4a-163">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-163">Optional.</span></span> <span data-ttu-id="4bc4a-164">Der Standardwert ist &quot; left &quot; .</span><span class="sxs-lookup"><span data-stu-id="4bc4a-164">Default is &quot;Left&quot;.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4bc4a-165">Wert</span><span class="sxs-lookup"><span data-stu-id="4bc4a-165">Value</span></span></th>
<th><span data-ttu-id="4bc4a-166">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4bc4a-166">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4bc4a-167">Links</span><span class="sxs-lookup"><span data-stu-id="4bc4a-167">Left</span></span></td>
<td><span data-ttu-id="4bc4a-168">Standard.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-168">Default.</span></span> <span data-ttu-id="4bc4a-169">Links ausrichten.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-169">Align left.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bc4a-170">Zentrum</span><span class="sxs-lookup"><span data-stu-id="4bc4a-170">Center</span></span></td>
<td><span data-ttu-id="4bc4a-171">Zentriert ausrichten.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-171">Align center.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4bc4a-172">Rechts</span><span class="sxs-lookup"><span data-stu-id="4bc4a-172">Right</span></span></td>
<td><span data-ttu-id="4bc4a-173">Rechts ausrichten.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-173">Align right.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bc4a-174">relativedescriptiontype</span><span class="sxs-lookup"><span data-stu-id="4bc4a-174">relativeDescriptionType</span></span></td>
<td><span data-ttu-id="4bc4a-175">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-175">Optional.</span></span> <span data-ttu-id="4bc4a-176">Der Standardwert ist &quot; Allgemein &quot; .</span><span class="sxs-lookup"><span data-stu-id="4bc4a-176">Default is &quot;General&quot;.</span></span> <span data-ttu-id="4bc4a-177">Gibt an, wie zwei Werte dieser Eigenschaft beschrieben werden sollen, wenn Sie miteinander verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-177">Specifies how two values of this property should be described when they are compared with one another.</span></span> <span data-ttu-id="4bc4a-178">Im Fall von Äquivalenz &quot; &quot; wird immer derselbe verwendet.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-178">In the case of equivalency, &quot;Same&quot; is always used.</span></span> <span data-ttu-id="4bc4a-179"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>Ipropertydescription:: getrelativedescription</strong></a> und <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>ipropertydescription:: getrelativedescriptiontype</strong></a> verwenden Sie diesen Wert, um zu bestimmen, welche Namen für die relative Beschreibungs Anzeige verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-179"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>IPropertyDescription::GetRelativeDescription</strong></a> and <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>IPropertyDescription::GetRelativeDescriptionType</strong></a> use this value to determine what relative description display names to use.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4bc4a-180">Wert</span><span class="sxs-lookup"><span data-stu-id="4bc4a-180">Value</span></span></th>
<th><span data-ttu-id="4bc4a-181">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4bc4a-181">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4bc4a-182">Allgemein</span><span class="sxs-lookup"><span data-stu-id="4bc4a-182">General</span></span></td>
<td><span data-ttu-id="4bc4a-183">Standard.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-183">Default.</span></span> <span data-ttu-id="4bc4a-184">Verwendet &quot; unterschiedliche &quot;  /  &quot; &quot;  /  &quot; andere &quot; .</span><span class="sxs-lookup"><span data-stu-id="4bc4a-184">Uses &quot;Different&quot; / &quot;Same&quot; / &quot;Different&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bc4a-185">Date</span><span class="sxs-lookup"><span data-stu-id="4bc4a-185">Date</span></span></td>
<td><span data-ttu-id="4bc4a-186">Standardwert, wenn <typeInfo type=&quot;DateTime&quot;> .</span><span class="sxs-lookup"><span data-stu-id="4bc4a-186">Default if <typeInfo type=&quot;DateTime&quot;>.</span></span> <span data-ttu-id="4bc4a-187">&quot;Wird früher &quot;  /  &quot; gleich &quot;  /  &quot; später verwendet, oder es wird &quot; älter oder &quot; &quot;  /  &quot; &quot;  /  &quot; &quot; früher oder &quot; früher verwendet &quot;  /  &quot; &quot;  /  &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="4bc4a-187">Uses &quot;Earlier&quot; / &quot;Same&quot; / &quot;Later&quot;, or uses &quot;Older&quot; / &quot;Same&quot; / &quot;Newer&quot;, or uses &quot;Sooner&quot; / &quot;Same&quot; / &quot;Later&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4bc4a-188">Size</span><span class="sxs-lookup"><span data-stu-id="4bc4a-188">Size</span></span></td>
<td><span data-ttu-id="4bc4a-189">Von wird eine geringere Größe verwendet. &quot; &quot;  /  &quot; &quot;  /  &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="4bc4a-189">Uses &quot;Smaller&quot; / &quot;Same&quot; / &quot;Larger&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bc4a-190">Anzahl</span><span class="sxs-lookup"><span data-stu-id="4bc4a-190">Count</span></span></td>
<td><span data-ttu-id="4bc4a-191">Von wird eine geringere Größe verwendet. &quot; &quot;  /  &quot; &quot;  /  &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="4bc4a-191">Uses &quot;Smaller&quot; / &quot;Same&quot; / &quot;Larger&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4bc4a-192">Revision</span><span class="sxs-lookup"><span data-stu-id="4bc4a-192">Revision</span></span></td>
<td><span data-ttu-id="4bc4a-193">Wird &quot; früher &quot;  /  &quot; gleich &quot;  /  &quot; später verwendet&quot;</span><span class="sxs-lookup"><span data-stu-id="4bc4a-193">Uses &quot;Earlier&quot; / &quot;Same&quot; / &quot;Later&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bc4a-194">Länge</span><span class="sxs-lookup"><span data-stu-id="4bc4a-194">Length</span></span></td>
<td><span data-ttu-id="4bc4a-195">Verwendet &quot; kürzer und &quot;  /  &quot; &quot;  /  &quot; länger&quot;</span><span class="sxs-lookup"><span data-stu-id="4bc4a-195">Uses &quot;Shorter&quot; / &quot;Same&quot; / &quot;Longer&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4bc4a-196">Duration</span><span class="sxs-lookup"><span data-stu-id="4bc4a-196">Duration</span></span></td>
<td><span data-ttu-id="4bc4a-197">Verwendet &quot; kürzer und &quot;  /  &quot; &quot;  /  &quot; länger&quot;</span><span class="sxs-lookup"><span data-stu-id="4bc4a-197">Uses &quot;Shorter&quot; / &quot;Same&quot; / &quot;Longer&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bc4a-198">Geschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="4bc4a-198">Speed</span></span></td>
<td><span data-ttu-id="4bc4a-199">Verwendet &quot; langsamer und &quot;  /  &quot; &quot;  /  &quot; schneller&quot;</span><span class="sxs-lookup"><span data-stu-id="4bc4a-199">Uses &quot;Slower&quot; / &quot;Same&quot; / &quot;Faster&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4bc4a-200">Rate</span><span class="sxs-lookup"><span data-stu-id="4bc4a-200">Rate</span></span></td>
<td><span data-ttu-id="4bc4a-201">Verwendet &quot; langsamer und &quot;  /  &quot; &quot;  /  &quot; schneller&quot;</span><span class="sxs-lookup"><span data-stu-id="4bc4a-201">Uses &quot;Slower&quot; / &quot;Same&quot; / &quot;Faster&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bc4a-202">Rating</span><span class="sxs-lookup"><span data-stu-id="4bc4a-202">Rating</span></span></td>
<td><span data-ttu-id="4bc4a-203">Verwendet &quot; niedriger &quot;  /  &quot; gleich &quot;  /  &quot; höher&quot;</span><span class="sxs-lookup"><span data-stu-id="4bc4a-203">Uses &quot;Lower&quot; / &quot;Same&quot; / &quot;Higher&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4bc4a-204">Priorität</span><span class="sxs-lookup"><span data-stu-id="4bc4a-204">Priority</span></span></td>
<td><span data-ttu-id="4bc4a-205">Verwendet &quot; niedriger &quot;  /  &quot; gleich &quot;  /  &quot; höher&quot;</span><span class="sxs-lookup"><span data-stu-id="4bc4a-205">Uses &quot;Lower&quot; / &quot;Same&quot; / &quot;Higher&quot;</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4bc4a-206">defaultsortdirection</span><span class="sxs-lookup"><span data-stu-id="4bc4a-206">defaultSortDirection</span></span></td>
<td><span data-ttu-id="4bc4a-207">Gibt die Sortierrichtung an.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-207">Specifies sort direction.</span></span> <span data-ttu-id="4bc4a-208">Der Standardwert ist &quot; Aufsteigend &quot; .</span><span class="sxs-lookup"><span data-stu-id="4bc4a-208">Default is &quot;Ascending&quot;.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4bc4a-209">Wert</span><span class="sxs-lookup"><span data-stu-id="4bc4a-209">Value</span></span></th>
<th><span data-ttu-id="4bc4a-210">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4bc4a-210">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4bc4a-211">Aufsteigend</span><span class="sxs-lookup"><span data-stu-id="4bc4a-211">Ascending</span></span></td>
<td><span data-ttu-id="4bc4a-212">Sortiert Aufsteigend.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-212">Sorts ascending.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bc4a-213">Absteigend</span><span class="sxs-lookup"><span data-stu-id="4bc4a-213">Descending</span></span></td>
<td><span data-ttu-id="4bc4a-214">Sortiert absteigend.</span><span class="sxs-lookup"><span data-stu-id="4bc4a-214">Sorts descending.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
