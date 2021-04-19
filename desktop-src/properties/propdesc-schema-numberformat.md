---
description: 'Gibt an, wie ipropertydescription:: formatfordisplay den Wert der Eigenschaft als Zeichenfolge formatieren soll. Dies gilt nur, wenn <displayInfo displayType=&\#0034;Number&\#0034;> .'
ms.assetid: 9e8cfe5c-e17a-40d6-958f-a1bd1130c699
title: NumberFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6750a9fb4dcf6a7a56c350fccf80241644b956da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355624"
---
# <a name="numberformat"></a><span data-ttu-id="6fc09-104">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="6fc09-104">numberFormat</span></span>

<span data-ttu-id="6fc09-105">Gibt an, wie [**ipropertydescription:: formatfordisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) den Wert der Eigenschaft als Zeichenfolge formatieren soll.</span><span class="sxs-lookup"><span data-stu-id="6fc09-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="6fc09-106">Dies gilt nur, wenn <displayInfo displayType="Number"> .</span><span class="sxs-lookup"><span data-stu-id="6fc09-106">This is applicable only if <displayInfo displayType="Number">.</span></span> <span data-ttu-id="6fc09-107">Es darf nur ein " [infoformat]() "-Element für jedes " [DisplayInfo](./propdesc-schema-displayinfo.md) "-Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6fc09-107">There should be only one [numberFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="6fc09-108">Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet.</span><span class="sxs-lookup"><span data-stu-id="6fc09-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="6fc09-109">Wenn kein [NumFormat-]() Element bereitgestellt wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.</span><span class="sxs-lookup"><span data-stu-id="6fc09-109">If no [numberFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fc09-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fc09-110">Syntax</span></span>


```
      <!-- numberFormat -->
      <xs:element name="numberFormat"  minOccurs="0" maxOccurs="1">
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
              <xs:restriction base="xs:string">
                <xs:enumeration value="hh:mm"/>
                <xs:enumeration value="hh:mm:ss"/>
                <xs:enumeration value="hh:mm:ss.fff"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="6fc09-111">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="6fc09-111">Element Information</span></span>



| <span data-ttu-id="6fc09-112">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="6fc09-112">Parent Element</span></span>                                   | <span data-ttu-id="6fc09-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fc09-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="6fc09-114">Display Info</span><span class="sxs-lookup"><span data-stu-id="6fc09-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="6fc09-115">Keine</span><span class="sxs-lookup"><span data-stu-id="6fc09-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="6fc09-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="6fc09-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6fc09-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="6fc09-117">Attribute</span></span></th>
<th><span data-ttu-id="6fc09-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fc09-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6fc09-119">formatas</span><span class="sxs-lookup"><span data-stu-id="6fc09-119">formatAs</span></span></td>
<td><span data-ttu-id="6fc09-120">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="6fc09-120">Public.</span></span> <span data-ttu-id="6fc09-121">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="6fc09-121">Optional.</span></span> <span data-ttu-id="6fc09-122">Der Standardwert ist &quot; Allgemein &quot; .</span><span class="sxs-lookup"><span data-stu-id="6fc09-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="6fc09-123">Gibt das Anzeige Format an.</span><span class="sxs-lookup"><span data-stu-id="6fc09-123">Specifies the display format.</span></span> <span data-ttu-id="6fc09-124">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="6fc09-124">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6fc09-125">Wert</span><span class="sxs-lookup"><span data-stu-id="6fc09-125">Value</span></span></th>
<th><span data-ttu-id="6fc09-126">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6fc09-126">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6fc09-127">Allgemein</span><span class="sxs-lookup"><span data-stu-id="6fc09-127">General</span></span></td>
<td><span data-ttu-id="6fc09-128">Standard.</span><span class="sxs-lookup"><span data-stu-id="6fc09-128">Default.</span></span> <span data-ttu-id="6fc09-129">Zeigt den Wert als unformatierte Zahl an.</span><span class="sxs-lookup"><span data-stu-id="6fc09-129">Displays the value as an unformatted number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc09-130">Prozentwert</span><span class="sxs-lookup"><span data-stu-id="6fc09-130">Percentage</span></span></td>
<td><span data-ttu-id="6fc09-131">Formatiert den Wert als Prozentsatz.</span><span class="sxs-lookup"><span data-stu-id="6fc09-131">Formats the value as a percentage.</span></span> <span data-ttu-id="6fc09-132">Erfordert, dass die-Eigenschaft UInt32 ist.</span><span class="sxs-lookup"><span data-stu-id="6fc09-132">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc09-133">ByteSize</span><span class="sxs-lookup"><span data-stu-id="6fc09-133">ByteSize</span></span></td>
<td><span data-ttu-id="6fc09-134">Formatiert den Wert nach Bedarf als Byte, &quot; KB &quot; , &quot; MB &quot; oder &quot; GB &quot; .</span><span class="sxs-lookup"><span data-stu-id="6fc09-134">Formats the value as a byte, &quot;KB&quot;, &quot;MB&quot;, or &quot;GB&quot; as appropriate.</span></span> <span data-ttu-id="6fc09-135">Erfordert, dass die-Eigenschaft UInt64 ist.</span><span class="sxs-lookup"><span data-stu-id="6fc09-135">Requires the property to be UInt64.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc09-136">Kbsize</span><span class="sxs-lookup"><span data-stu-id="6fc09-136">KBSize</span></span></td>
<td><span data-ttu-id="6fc09-137">Formatiert den Wert in &quot; KB &quot; , unabhängig davon, was der Wert ist.</span><span class="sxs-lookup"><span data-stu-id="6fc09-137">Formats the value as a &quot;KB&quot;, no matter what the value is.</span></span> <span data-ttu-id="6fc09-138">Erfordert, dass die-Eigenschaft UInt64 ist.</span><span class="sxs-lookup"><span data-stu-id="6fc09-138">Requires the property to be UInt64.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc09-139">Sample Size (</span><span class="sxs-lookup"><span data-stu-id="6fc09-139">SampleSize</span></span></td>
<td><span data-ttu-id="6fc09-140">Formatiert den Wert als Anzahl von Bits.</span><span class="sxs-lookup"><span data-stu-id="6fc09-140">Formats the value as a number of bits.</span></span> <span data-ttu-id="6fc09-141">Erfordert, dass die-Eigenschaft UInt32 ist.</span><span class="sxs-lookup"><span data-stu-id="6fc09-141">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc09-142">BitRate</span><span class="sxs-lookup"><span data-stu-id="6fc09-142">BitRate</span></span></td>
<td><span data-ttu-id="6fc09-143">Formatiert den Wert in Kbit/s &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="6fc09-143">Formats the value in &quot;Kbps&quot;.</span></span> <span data-ttu-id="6fc09-144">Erfordert, dass die-Eigenschaft UInt32 ist.</span><span class="sxs-lookup"><span data-stu-id="6fc09-144">Requires the property to be UInt32.</span></span> <span data-ttu-id="6fc09-145">Der Wert muss in &quot; Bits-pro-Sekunde-Einheiten gespeichert werden &quot; .</span><span class="sxs-lookup"><span data-stu-id="6fc09-145">The value must be stored in &quot;bits-per-second&quot; units.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc09-146">Sample Rate</span><span class="sxs-lookup"><span data-stu-id="6fc09-146">SampleRate</span></span></td>
<td><span data-ttu-id="6fc09-147">Formatiert den Wert in &quot; kHz &quot; .</span><span class="sxs-lookup"><span data-stu-id="6fc09-147">Formats the value in &quot;KHz&quot;.</span></span> <span data-ttu-id="6fc09-148">Erfordert, dass die-Eigenschaft UInt32 ist.</span><span class="sxs-lookup"><span data-stu-id="6fc09-148">Requires the property to be UInt32.</span></span> <span data-ttu-id="6fc09-149">Der Wert muss in Hertz- &quot; Einheiten gespeichert werden &quot; .</span><span class="sxs-lookup"><span data-stu-id="6fc09-149">The value must be stored in &quot;Hertz&quot; units.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc09-150">FrameRate</span><span class="sxs-lookup"><span data-stu-id="6fc09-150">FrameRate</span></span></td>
<td><span data-ttu-id="6fc09-151">Formatiert den Wert in Frames/Sekunde.</span><span class="sxs-lookup"><span data-stu-id="6fc09-151">Formats the value in frames/second.</span></span> <span data-ttu-id="6fc09-152">Erfordert, dass die-Eigenschaft UInt32 ist.</span><span class="sxs-lookup"><span data-stu-id="6fc09-152">Requires the property to be UInt32.</span></span> <span data-ttu-id="6fc09-153">Der Wert muss in &quot; Kilo-Frames-pro Sekunde-Einheiten gespeichert werden &quot; .</span><span class="sxs-lookup"><span data-stu-id="6fc09-153">The value must be stored in &quot;kilo-frames-per-second&quot; units.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc09-154">Okkludierte</span><span class="sxs-lookup"><span data-stu-id="6fc09-154">Pixels</span></span></td>
<td><span data-ttu-id="6fc09-155">Formatiert den Wert in Pixel Einheiten.</span><span class="sxs-lookup"><span data-stu-id="6fc09-155">Formats the value in pixel units.</span></span> <span data-ttu-id="6fc09-156">Erfordert, dass die-Eigenschaft UInt32 ist.</span><span class="sxs-lookup"><span data-stu-id="6fc09-156">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc09-157">DPI</span><span class="sxs-lookup"><span data-stu-id="6fc09-157">DPI</span></span></td>
<td><span data-ttu-id="6fc09-158">Formatiert den Wert in Punkten pro Zoll.</span><span class="sxs-lookup"><span data-stu-id="6fc09-158">Formats the value in dots-per-inch.</span></span> <span data-ttu-id="6fc09-159">Erfordert, dass die-Eigenschaft UInt32 ist.</span><span class="sxs-lookup"><span data-stu-id="6fc09-159">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc09-160">Duration</span><span class="sxs-lookup"><span data-stu-id="6fc09-160">Duration</span></span></td>
<td><span data-ttu-id="6fc09-161">Formatiert den Wert als Dauer.</span><span class="sxs-lookup"><span data-stu-id="6fc09-161">Formats the value as a duration.</span></span> <span data-ttu-id="6fc09-162">Verwenden <formatDurationAs> Sie, um das Format für die Dauer anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6fc09-162">Use <formatDurationAs> to specify the duration format.</span></span> <span data-ttu-id="6fc09-163">Erfordert, dass die-Eigenschaft UInt64 ist.</span><span class="sxs-lookup"><span data-stu-id="6fc09-163">Requires the property to be UInt64.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc09-164">formatdurationas</span><span class="sxs-lookup"><span data-stu-id="6fc09-164">formatDurationAs</span></span></td>
<td><span data-ttu-id="6fc09-165">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="6fc09-165">Public.</span></span> <span data-ttu-id="6fc09-166">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="6fc09-166">Optional.</span></span> <span data-ttu-id="6fc09-167">Der Standardwert ist &quot; hh: mm: SS &quot; .</span><span class="sxs-lookup"><span data-stu-id="6fc09-167">Default is &quot;hh:mm:ss&quot;.</span></span> <span data-ttu-id="6fc09-168">Gilt nur, wenn <em>formatas &quot; = &quot; Duration</em>ist.</span><span class="sxs-lookup"><span data-stu-id="6fc09-168">Only applies if <em>formatAs=&quot;Duration&quot;</em>.</span></span> <span data-ttu-id="6fc09-169">Erfordert, dass die-Eigenschaft UInt64 ist.</span><span class="sxs-lookup"><span data-stu-id="6fc09-169">Requires the property to be UInt64.</span></span> <span data-ttu-id="6fc09-170">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="6fc09-170">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6fc09-171">Wert</span><span class="sxs-lookup"><span data-stu-id="6fc09-171">Value</span></span></th>
<th><span data-ttu-id="6fc09-172">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6fc09-172">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6fc09-173">hh:mm</span><span class="sxs-lookup"><span data-stu-id="6fc09-173">hh:mm</span></span></td>
<td><span data-ttu-id="6fc09-174">Formatiert den Wert in Stunden und Minuten.</span><span class="sxs-lookup"><span data-stu-id="6fc09-174">Formats the value in hours and minutes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc09-175">hh:mm:ss</span><span class="sxs-lookup"><span data-stu-id="6fc09-175">hh:mm:ss</span></span></td>
<td><span data-ttu-id="6fc09-176">Standard.</span><span class="sxs-lookup"><span data-stu-id="6fc09-176">Default.</span></span> <span data-ttu-id="6fc09-177">Formatiert den Wert in Stunden, Minuten und Sekunden.</span><span class="sxs-lookup"><span data-stu-id="6fc09-177">Formats the value in hours, minutes, and seconds.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc09-178">hh: mm: SS. fff</span><span class="sxs-lookup"><span data-stu-id="6fc09-178">hh:mm:ss.fff</span></span></td>
<td><span data-ttu-id="6fc09-179">Formatiert den Wert in Stunden, Minuten, Sekunden und Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="6fc09-179">Formats the value in hours, minutes, seconds, and milliseconds.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
