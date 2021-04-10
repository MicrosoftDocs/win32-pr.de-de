---
description: 'Gibt an, wie ipropertydescription:: formatfordisplay den Wert der Eigenschaft als Zeichenfolge formatieren soll. Dies gilt nur, wenn <displayInfo displayType=&\#0034;DateTime&\#0034;> .'
ms.assetid: c290fb2e-ef5b-4dea-ba42-7c9e273a89dc
title: dateTimeFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091898f77f4dcc37bbe65515f8606104a4d968bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215399"
---
# <a name="datetimeformat"></a><span data-ttu-id="17411-104">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="17411-104">dateTimeFormat</span></span>

<span data-ttu-id="17411-105">Gibt an, wie [**ipropertydescription:: formatfordisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) den Wert der Eigenschaft als Zeichenfolge formatieren soll.</span><span class="sxs-lookup"><span data-stu-id="17411-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="17411-106">Dies gilt nur, wenn <displayInfo displayType="DateTime"> .</span><span class="sxs-lookup"><span data-stu-id="17411-106">This is applicable only if <displayInfo displayType="DateTime">.</span></span> <span data-ttu-id="17411-107">Es darf nur ein [DateTimeFormat]() -Element für jedes [DisplayInfo](./propdesc-schema-displayinfo.md) -Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="17411-107">There should be only one [dateTimeFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="17411-108">Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet.</span><span class="sxs-lookup"><span data-stu-id="17411-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="17411-109">Wenn kein [DateTimeFormat]() -Element angegeben wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.</span><span class="sxs-lookup"><span data-stu-id="17411-109">If no [dateTimeFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="17411-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="17411-110">Syntax</span></span>


```
      <!-- dateTimeFormat -->
      <xs:element name="dateTimeFormat"  minOccurs="0" maxOccurs="1">
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
```



## <a name="element-information"></a><span data-ttu-id="17411-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="17411-111">Element Information</span></span>



| <span data-ttu-id="17411-112">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="17411-112">Parent Element</span></span>                                   | <span data-ttu-id="17411-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17411-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="17411-114">Display Info</span><span class="sxs-lookup"><span data-stu-id="17411-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="17411-115">Keine</span><span class="sxs-lookup"><span data-stu-id="17411-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="17411-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="17411-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="17411-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="17411-117">Attribute</span></span></th>
<th><span data-ttu-id="17411-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17411-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="17411-119">formatas</span><span class="sxs-lookup"><span data-stu-id="17411-119">formatAs</span></span></td>
<td><span data-ttu-id="17411-120">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="17411-120">Public.</span></span> <span data-ttu-id="17411-121">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="17411-121">Optional.</span></span> <span data-ttu-id="17411-122">Der Standardwert ist &quot; Allgemein &quot; .</span><span class="sxs-lookup"><span data-stu-id="17411-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="17411-123">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="17411-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="17411-124">Wert</span><span class="sxs-lookup"><span data-stu-id="17411-124">Value</span></span></th>
<th><span data-ttu-id="17411-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="17411-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="17411-126">Allgemein</span><span class="sxs-lookup"><span data-stu-id="17411-126">General</span></span></td>
<td><span data-ttu-id="17411-127">Standard.</span><span class="sxs-lookup"><span data-stu-id="17411-127">Default.</span></span> <span data-ttu-id="17411-128">Formatiert den Datums-/Uhrzeitwert mit " <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>shformatdatetime</strong></a>".</span><span class="sxs-lookup"><span data-stu-id="17411-128">Formats the date-time value using <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a>.</span></span> <span data-ttu-id="17411-129">Verwenden Sie die Attribute <em>formattimeas</em> und <em>formatdateas</em> , um anzugeben, wie Uhrzeit und Datum formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="17411-129">Use the <em>formatTimeAs</em> and <em>formatDateAs</em> attributes to specify how the time and date are formatted.</span></span> <span data-ttu-id="17411-130">Erfordert, dass der Eigenschaftentyp DateTime ist.</span><span class="sxs-lookup"><span data-stu-id="17411-130">Requires the property type to be DateTime.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17411-131">Monat</span><span class="sxs-lookup"><span data-stu-id="17411-131">Month</span></span></td>
<td><span data-ttu-id="17411-132">Formatiert den Wert in einem der Monate des Jahres.</span><span class="sxs-lookup"><span data-stu-id="17411-132">Formats the value as one of the months of the year.</span></span> <span data-ttu-id="17411-133">Erfordert, dass der Eigenschaftentyp Int32 ist.</span><span class="sxs-lookup"><span data-stu-id="17411-133">Requires the property type to be Int32.</span></span> <span data-ttu-id="17411-134">Der Wert muss als numerischer Wert mit 1 gespeichert werden, der den ersten Monat des Jahres darstellt.</span><span class="sxs-lookup"><span data-stu-id="17411-134">The value must be stored as a numeric value with 1 representing the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17411-135">Jährlicher Monat</span><span class="sxs-lookup"><span data-stu-id="17411-135">YearMonth</span></span></td>
<td><span data-ttu-id="17411-136">Formatiert den Wert als &quot; Jahr-Monat &quot; .</span><span class="sxs-lookup"><span data-stu-id="17411-136">Formats the value as &quot;Year - Month&quot;.</span></span> <span data-ttu-id="17411-137">Erfordert, dass der Eigenschaftentyp Int32 ist.</span><span class="sxs-lookup"><span data-stu-id="17411-137">Requires the property type to be Int32.</span></span> <span data-ttu-id="17411-138">Der Wert muss so gespeichert werden, dass die beiden höchsten Bytes das Jahr und die unteren zwei Bytes den Monat angeben.</span><span class="sxs-lookup"><span data-stu-id="17411-138">The value must be stored such that the two highest bytes specify the year and the lower two bytes specify the month.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17411-139">Year</span><span class="sxs-lookup"><span data-stu-id="17411-139">Year</span></span></td>
<td><span data-ttu-id="17411-140">Formatiert den Wert als einfache Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="17411-140">Formats the value as a simple string.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17411-141">formattimeas</span><span class="sxs-lookup"><span data-stu-id="17411-141">formatTimeAs</span></span></td>
<td><span data-ttu-id="17411-142">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="17411-142">Public.</span></span> <span data-ttu-id="17411-143">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="17411-143">Optional.</span></span> <span data-ttu-id="17411-144">Der Standardwert ist &quot; Kurzzeit &quot; .</span><span class="sxs-lookup"><span data-stu-id="17411-144">Default is &quot;ShortTime&quot;.</span></span> <span data-ttu-id="17411-145">Gibt das Format an, in dem die Uhrzeit angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="17411-145">Specifies the format in which to display time.</span></span> <span data-ttu-id="17411-146">Gilt, wenn <strong>formatas &quot; = &quot; Allgemein</strong>.</span><span class="sxs-lookup"><span data-stu-id="17411-146">Applies when <strong>formatAs=&quot;General&quot;</strong>.</span></span> <span data-ttu-id="17411-147">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="17411-147">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="17411-148">Wert</span><span class="sxs-lookup"><span data-stu-id="17411-148">Value</span></span></th>
<th><span data-ttu-id="17411-149">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="17411-149">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="17411-150">Kurzzeit</span><span class="sxs-lookup"><span data-stu-id="17411-150">ShortTime</span></span></td>
<td><span data-ttu-id="17411-151">Standard.</span><span class="sxs-lookup"><span data-stu-id="17411-151">Default.</span></span> <span data-ttu-id="17411-152">Zeigen Sie die Zeit wie &quot; 7:48 pm an &quot; .</span><span class="sxs-lookup"><span data-stu-id="17411-152">Show the time like &quot;7:48 PM&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17411-153">Jährige</span><span class="sxs-lookup"><span data-stu-id="17411-153">LongTime</span></span></td>
<td><span data-ttu-id="17411-154">Zeigen Sie die Zeit wie &quot; 7:48:33 pm an &quot; .</span><span class="sxs-lookup"><span data-stu-id="17411-154">Show the time like &quot;7:48:33 PM&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17411-155">Hidetime</span><span class="sxs-lookup"><span data-stu-id="17411-155">HideTime</span></span></td>
<td><span data-ttu-id="17411-156">Zeigen Sie den Uhrzeit Teil des Datums nicht an.</span><span class="sxs-lookup"><span data-stu-id="17411-156">Do not display the time portion of the date.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17411-157">formatdateas</span><span class="sxs-lookup"><span data-stu-id="17411-157">formatDateAs</span></span></td>
<td><span data-ttu-id="17411-158">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="17411-158">Public.</span></span> <span data-ttu-id="17411-159">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="17411-159">Optional.</span></span> <span data-ttu-id="17411-160">Der Standardwert ist &quot; SHORTDATE &quot; .</span><span class="sxs-lookup"><span data-stu-id="17411-160">Default is &quot;ShortDate&quot;.</span></span> <span data-ttu-id="17411-161">Gibt das Format an, in dem das Datum angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="17411-161">Specifies the format in which to display the date.</span></span> <span data-ttu-id="17411-162">Gilt, wenn <strong>formatas &quot; = &quot; Allgemein</strong>.</span><span class="sxs-lookup"><span data-stu-id="17411-162">Applies when <strong>formatAs=&quot;General&quot;</strong>.</span></span> <span data-ttu-id="17411-163">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="17411-163">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="17411-164">Wert</span><span class="sxs-lookup"><span data-stu-id="17411-164">Value</span></span></th>
<th><span data-ttu-id="17411-165">Beispiel</span><span class="sxs-lookup"><span data-stu-id="17411-165">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="17411-166">SHORTDATE</span><span class="sxs-lookup"><span data-stu-id="17411-166">ShortDate</span></span></td>
<td><span data-ttu-id="17411-167">Standard.</span><span class="sxs-lookup"><span data-stu-id="17411-167">Default.</span></span> <span data-ttu-id="17411-168">Zeigt das Datum wie &quot; 5/13/59 an &quot; .</span><span class="sxs-lookup"><span data-stu-id="17411-168">Show the date like &quot;5/13/59&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17411-169">LongDate</span><span class="sxs-lookup"><span data-stu-id="17411-169">LongDate</span></span></td>
<td><span data-ttu-id="17411-170">Zeigt das Datum wie &quot; Mittwoch, 13. Mai 1959 an &quot; .</span><span class="sxs-lookup"><span data-stu-id="17411-170">Show the date like &quot;Wednesday, May 13, 1959&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17411-171">Hidedate</span><span class="sxs-lookup"><span data-stu-id="17411-171">HideDate</span></span></td>
<td><span data-ttu-id="17411-172">Der Datums Teil wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17411-172">Do not display the date portion.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17411-173">Relativeshortdate</span><span class="sxs-lookup"><span data-stu-id="17411-173">RelativeShortDate</span></span></td>
<td><span data-ttu-id="17411-174">Zeigen Sie das Datum wie &quot; SHORTDATE an &quot; , aber verwenden Sie relative Beschreibungen wie &quot; gestern, &quot; wann immer dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="17411-174">Show the date like &quot;ShortDate&quot;, but use relative descriptions, such as &quot;yesterday&quot;, whenever possible.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17411-175">Relativelongdate</span><span class="sxs-lookup"><span data-stu-id="17411-175">RelativeLongDate</span></span></td>
<td><span data-ttu-id="17411-176">Zeigen Sie das Datum wie &quot; longDate an &quot; , aber verwenden Sie relative Beschreibungen, z &quot; . b &quot; . gestern, wann immer möglich.</span><span class="sxs-lookup"><span data-stu-id="17411-176">Show the date like &quot;LongDate&quot;, but use relative descriptions, such as &quot;yesterday&quot;, whenever possible.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
