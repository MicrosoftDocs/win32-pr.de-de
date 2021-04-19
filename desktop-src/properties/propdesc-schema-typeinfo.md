---
description: Gibt die Typinformationen einer Eigenschaft an.
ms.assetid: ae1f8835-ef6c-42bb-b44f-ad374337a012
title: TypeInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa783a606066163fd8b17f53ef8a0fe2da44e539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356631"
---
# <a name="typeinfo"></a><span data-ttu-id="ce241-103">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="ce241-103">typeInfo</span></span>

<span data-ttu-id="ce241-104">Gibt die Typinformationen einer Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="ce241-104">Specifies a property's type information.</span></span> <span data-ttu-id="ce241-105">Es darf nur ein [TypeInfo]() -Element für jede [propertydescription](./propdesc-schema-propertydescription.md)vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ce241-105">There should be only one [typeInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md).</span></span> <span data-ttu-id="ce241-106">Dieses Element wurde für Windows 7 geändert.</span><span class="sxs-lookup"><span data-stu-id="ce241-106">This element has changed for Windows 7.</span></span>

<span data-ttu-id="ce241-107">Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce241-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="ce241-108">Wenn kein [TypeInfo]() -Element bereitgestellt wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.</span><span class="sxs-lookup"><span data-stu-id="ce241-108">If no [typeInfo]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="ce241-109">Syntax für Windows 7</span><span class="sxs-lookup"><span data-stu-id="ce241-109">Syntax for Windows 7</span></span>


```
<!-- typeInfo for Windows 7-->
<xs:element name="typeInfo">
    <xs:complexType>
        <xs:attribute name="type" default="Any">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Any"/>
                    <xs:enumeration value="Null"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Byte"/>
                    <xs:enumeration value="Buffer"/>
                    <xs:enumeration value="Int16"/>
                    <xs:enumeration value="UInt16"/>
                    <xs:enumeration value="Int32"/>
                    <xs:enumeration value="UInt32"/>
                    <xs:enumeration value="Int64"/>
                    <xs:enumeration value="UInt64"/>
                    <xs:enumeration value="Double"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Guid"/>
                    <xs:enumeration value="Blob"/>
                    <xs:enumeration value="Stream"/>
                    <xs:enumeration value="Clipboard"/>
                    <xs:enumeration value="Object"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="groupingRange">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Discrete"/>
                    <xs:enumeration value="Alphanumeric"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Dynamic"/>
                    <xs:enumeration value="Percent"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isInnate" type="xs:boolean" default="false"/>
        <xs:attribute name="canBePurged" type="xs:boolean"/>
        <xs:attribute name="multipleValues" type="xs:boolean" default="false"/>
        <xs:attribute name="isGroup" type="xs:boolean" default="false"/>
        <xs:attribute name="aggregationType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="First"/>
                    <xs:enumeration value="Sum"/>
                    <xs:enumeration value="Average"/>
                    <xs:enumeration value="DateRange"/>
                    <xs:enumeration value="Union"/>
                    <xs:enumeration value="Maximum"/>
                    <xs:enumeration value="Minimum"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isTreeProperty" type="xs:boolean" default="false"/>
        <xs:attribute name="isViewable" type="xs:boolean" default="false"/>
        <xs:attribute name="isQueryable" type="xs:boolean" default="false"/>
        <xs:attribute name="includeInFullTextQuery" type="xs:boolean" default="false"/>
        <xs:attribute name="searchRawValue" type="xs:boolean" default="false"/>
        <xs:attribute name="conditionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="None"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Size"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultOperation">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Equal"/>
                    <xs:enumeration value="NotEqual"/>
                    <xs:enumeration value="LessThan"/>
                    <xs:enumeration value="GreaterThan"/>
                    <xs:enumeration value="Contains"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="ce241-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ce241-110">Element Information</span></span>



| <span data-ttu-id="ce241-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="ce241-111">Parent Element</span></span>                                                   | <span data-ttu-id="ce241-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ce241-112">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="ce241-113">propertydescription</span><span class="sxs-lookup"><span data-stu-id="ce241-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="ce241-114">Keine</span><span class="sxs-lookup"><span data-stu-id="ce241-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="ce241-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="ce241-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce241-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="ce241-116">Attribute</span></span></th>
<th><span data-ttu-id="ce241-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce241-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce241-118">type</span><span class="sxs-lookup"><span data-stu-id="ce241-118">type</span></span></td>
<td><span data-ttu-id="ce241-119">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="ce241-119">Public.</span></span> <span data-ttu-id="ce241-120">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ce241-120">Optional.</span></span> <span data-ttu-id="ce241-121">Der Standardwert ist &quot; Any &quot; .</span><span class="sxs-lookup"><span data-stu-id="ce241-121">Default is &quot;Any&quot;.</span></span> <span data-ttu-id="ce241-122">Gibt den Typ der Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="ce241-122">Indicates the type of the property.</span></span> <span data-ttu-id="ce241-123">Die folgenden Typen sind gültig, und die zugehörigen Variant-Typen werden von <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>ipropertydescription:: GetPropertyType</strong></a>abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ce241-123">The following are valid types and their associated variant types are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a>.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ce241-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ce241-124">Value</span></span></th>
<th><span data-ttu-id="ce241-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ce241-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce241-126">Any</span><span class="sxs-lookup"><span data-stu-id="ce241-126">Any</span></span></td>
<td><span data-ttu-id="ce241-127">Standard.</span><span class="sxs-lookup"><span data-stu-id="ce241-127">Default.</span></span> <span data-ttu-id="ce241-128">Das Eigenschafts Subsystem erzwingt oder wandelt den Eigenschafts Wert nicht um.</span><span class="sxs-lookup"><span data-stu-id="ce241-128">The property subsystem will not enforce or coerce the property value.</span></span> <span data-ttu-id="ce241-129"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>Ipropertydescription:: GetPropertyType</strong></a> gibt VT_NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="ce241-129"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a> returns VT_NULL.</span></span> <span data-ttu-id="ce241-130">Unabhängigen Softwareanbietern (ISVs) wird dringend empfohlen, einen Typ bereitzustellen, anstatt diesen Standardwert zu überschreiten.</span><span class="sxs-lookup"><span data-stu-id="ce241-130">Independent software vendors (ISVs) are strongly encouraged to provide a type rather than fall back on this default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-131">Null</span><span class="sxs-lookup"><span data-stu-id="ce241-131">Null</span></span></td>
<td><span data-ttu-id="ce241-132">Für diese Eigenschaft ist kein Wert vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ce241-132">There is no value for this property.</span></span> <span data-ttu-id="ce241-133"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>Ipropertydescription:: GetPropertyType</strong></a> gibt VT_NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="ce241-133"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a> returns VT_NULL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-134">String</span><span class="sxs-lookup"><span data-stu-id="ce241-134">String</span></span></td>
<td><span data-ttu-id="ce241-135">Der Wert muss eine VT_LPWSTR sein, die eine Unicode-Zeichenfolge ist, die durch einen NULL-Verweis beendet wird.</span><span class="sxs-lookup"><span data-stu-id="ce241-135">The value must be a VT_LPWSTR, which is a Unicode string terminated by a null reference.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-136">Boolean</span><span class="sxs-lookup"><span data-stu-id="ce241-136">Boolean</span></span></td>
<td><span data-ttu-id="ce241-137">Der Wert muss ein VT_BOOL sein, bei dem es sich um einen booleschen Wert handelt.</span><span class="sxs-lookup"><span data-stu-id="ce241-137">The value must be a VT_BOOL, which is a boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-138">Byte</span><span class="sxs-lookup"><span data-stu-id="ce241-138">Byte</span></span></td>
<td><span data-ttu-id="ce241-139">Der Wert muss ein VT_UI1 sein, d. h. ein Byte.</span><span class="sxs-lookup"><span data-stu-id="ce241-139">The value must be a VT_UI1, which is a byte.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-140">Buffer</span><span class="sxs-lookup"><span data-stu-id="ce241-140">Buffer</span></span></td>
<td><span data-ttu-id="ce241-141">Der Wert muss ein VT_UI1 sein | VT_VECTOR Puffer bytes.</span><span class="sxs-lookup"><span data-stu-id="ce241-141">The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-142">Int16</span><span class="sxs-lookup"><span data-stu-id="ce241-142">Int16</span></span></td>
<td><span data-ttu-id="ce241-143">Der Wert muss eine VT_I2 sein, bei der es sich um eine 16-Bit-Ganzzahl handelt.</span><span class="sxs-lookup"><span data-stu-id="ce241-143">The value must be a VT_I2, which is a 16-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-144">UInt16</span><span class="sxs-lookup"><span data-stu-id="ce241-144">UInt16</span></span></td>
<td><span data-ttu-id="ce241-145">Der Wert muss eine VT_UI2 sein, bei der es sich um eine 16-Bit-Ganzzahl ohne Vorzeichen handelt.</span><span class="sxs-lookup"><span data-stu-id="ce241-145">The value must be a VT_UI2, which is a 16-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-146">Int32</span><span class="sxs-lookup"><span data-stu-id="ce241-146">Int32</span></span></td>
<td><span data-ttu-id="ce241-147">Der Wert muss eine VT_I4 sein, eine ganze Zahl mit 32 Bit.</span><span class="sxs-lookup"><span data-stu-id="ce241-147">The value must be a VT_I4, which is a 32-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-148">UInt32</span><span class="sxs-lookup"><span data-stu-id="ce241-148">UInt32</span></span></td>
<td><span data-ttu-id="ce241-149">Der Wert muss eine VT_UI4 sein, bei der es sich um eine 32-Bit-Ganzzahl ohne Vorzeichen handelt.</span><span class="sxs-lookup"><span data-stu-id="ce241-149">The value must be a VT_UI4, which is a 32-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-150">Int64</span><span class="sxs-lookup"><span data-stu-id="ce241-150">Int64</span></span></td>
<td><span data-ttu-id="ce241-151">Der Wert muss eine VT_I8 sein, eine ganze Zahl mit 64 Bit.</span><span class="sxs-lookup"><span data-stu-id="ce241-151">The value must be a VT_I8, which is a 64-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-152">UInt64</span><span class="sxs-lookup"><span data-stu-id="ce241-152">UInt64</span></span></td>
<td><span data-ttu-id="ce241-153">Der Wert muss eine VT_UI8 sein, bei der es sich um eine 64-Bit-Ganzzahl ohne Vorzeichen handelt.</span><span class="sxs-lookup"><span data-stu-id="ce241-153">The value must be a VT_UI8, which is a 64-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-154">Double</span><span class="sxs-lookup"><span data-stu-id="ce241-154">Double</span></span></td>
<td><span data-ttu-id="ce241-155">Der Wert muss eine VT_R8 sein, bei der es sich um einen Double-Wert handelt.</span><span class="sxs-lookup"><span data-stu-id="ce241-155">The value must be a VT_R8, which is a double.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-156">Datetime</span><span class="sxs-lookup"><span data-stu-id="ce241-156">DateTime</span></span></td>
<td><span data-ttu-id="ce241-157">Der Wert muss eine VT_FILETIME sein, die eine <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a>ist.</span><span class="sxs-lookup"><span data-stu-id="ce241-157">The value must be a VT_FILETIME, which is a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-158">GUID</span><span class="sxs-lookup"><span data-stu-id="ce241-158">Guid</span></span></td>
<td><span data-ttu-id="ce241-159">Der Wert muss eine VT_CLSID sein, bei der es sich um einen Klassen Bezeichner (CLSID) handelt.</span><span class="sxs-lookup"><span data-stu-id="ce241-159">The value must be a VT_CLSID, which is a class identifier (CLSID).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-160">Blob</span><span class="sxs-lookup"><span data-stu-id="ce241-160">Blob</span></span></td>
<td><span data-ttu-id="ce241-161">Der Wert muss ein VT_BLOB sein, bei dem es sich um ein Byte mit Längen Präfix handelt.</span><span class="sxs-lookup"><span data-stu-id="ce241-161">The value must be a VT_BLOB, which are length-prefixed bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-162">Datenstrom</span><span class="sxs-lookup"><span data-stu-id="ce241-162">Stream</span></span></td>
<td><span data-ttu-id="ce241-163">Der Wert muss ein VT_STREAM sein, bei dem es sich um ein Objekt handelt, das <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>implementiert.</span><span class="sxs-lookup"><span data-stu-id="ce241-163">The value must be a VT_STREAM, which is an object that implements <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-164">Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="ce241-164">Clipboard</span></span></td>
<td><span data-ttu-id="ce241-165">Der Wert muss eine VT_CF sein, bei der es sich um ein Zwischenablage Format handelt.</span><span class="sxs-lookup"><span data-stu-id="ce241-165">The value must be a VT_CF, which is a clipboard format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-166">Object</span><span class="sxs-lookup"><span data-stu-id="ce241-166">Object</span></span></td>
<td><span data-ttu-id="ce241-167">Der Wert muss ein VT_UNKNOWN sein, bei dem es sich um ein Objekt handelt, das <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>implementiert.</span><span class="sxs-lookup"><span data-stu-id="ce241-167">The value must be a VT_UNKNOWN, which is an object that implements <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-168">groupingrange</span><span class="sxs-lookup"><span data-stu-id="ce241-168">groupingRange</span></span></td>
<td><span data-ttu-id="ce241-169">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ce241-169">Optional.</span></span> <span data-ttu-id="ce241-170">Der Standardwert ist &quot; diskret &quot; .</span><span class="sxs-lookup"><span data-stu-id="ce241-170">Default is &quot;Discrete&quot;.</span></span> <span data-ttu-id="ce241-171">Gibt an, wie die-Eigenschaft angezeigt wird, wenn eine Ansicht nach dieser Eigenschaft gruppiert wird.</span><span class="sxs-lookup"><span data-stu-id="ce241-171">Specifies how the property is displayed when a view is grouped by this property.</span></span> <span data-ttu-id="ce241-172">Nachdem diese Werte hier festgelegt wurden, werden Sie von <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>ipropertydescription:: getgroupingrange</strong></a>abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ce241-172">Once set here, these values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription::GetGroupingRange</strong></a>.</span></span> <span data-ttu-id="ce241-173">Die folgenden Typen sind gültig.</span><span class="sxs-lookup"><span data-stu-id="ce241-173">The following are valid types.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ce241-174">Wert</span><span class="sxs-lookup"><span data-stu-id="ce241-174">Value</span></span></th>
<th><span data-ttu-id="ce241-175">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ce241-175">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce241-176">Discrete</span><span class="sxs-lookup"><span data-stu-id="ce241-176">Discrete</span></span></td>
<td><span data-ttu-id="ce241-177">Standard.</span><span class="sxs-lookup"><span data-stu-id="ce241-177">Default.</span></span> <span data-ttu-id="ce241-178">Zeigt einzelne Werte an.</span><span class="sxs-lookup"><span data-stu-id="ce241-178">Displays individual values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-179">Alphanumerisch</span><span class="sxs-lookup"><span data-stu-id="ce241-179">Alphanumeric</span></span></td>
<td><span data-ttu-id="ce241-180">Zeigt statische alphanumerische Bereiche für-Werte an.</span><span class="sxs-lookup"><span data-stu-id="ce241-180">Displays static alphanumeric ranges for values.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-181">Size</span><span class="sxs-lookup"><span data-stu-id="ce241-181">Size</span></span></td>
<td><span data-ttu-id="ce241-182">Zeigt statische Größenbereiche für Werte an.</span><span class="sxs-lookup"><span data-stu-id="ce241-182">Displays static size ranges for values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-183">Date</span><span class="sxs-lookup"><span data-stu-id="ce241-183">Date</span></span></td>
<td><span data-ttu-id="ce241-184">Zeigt Monat/Jahr-Gruppen an.</span><span class="sxs-lookup"><span data-stu-id="ce241-184">Displays month/year groups.</span></span> <span data-ttu-id="ce241-185">Der Standardwert für Eigenschaften vom Typ = &quot; DateTime &quot; .</span><span class="sxs-lookup"><span data-stu-id="ce241-185">Default for properties of type=&quot;DateTime&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-186">Timerelative</span><span class="sxs-lookup"><span data-stu-id="ce241-186">TimeRelative</span></span></td>
<td><span data-ttu-id="ce241-187">Wird in Zeit relativen Gruppen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ce241-187">Displays in time-relative groups.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-188">Dynamisch</span><span class="sxs-lookup"><span data-stu-id="ce241-188">Dynamic</span></span></td>
<td><span data-ttu-id="ce241-189">Zeigt dynamisch erstellte Bereiche für die Werte an.</span><span class="sxs-lookup"><span data-stu-id="ce241-189">Displays dynamically created ranges for the values.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-190">Percent</span><span class="sxs-lookup"><span data-stu-id="ce241-190">Percent</span></span></td>
<td><span data-ttu-id="ce241-191">Zeigt Prozent Behälter an.</span><span class="sxs-lookup"><span data-stu-id="ce241-191">Displays percent buckets.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-192">isinnate</span><span class="sxs-lookup"><span data-stu-id="ce241-192">isInnate</span></span></td>
<td><span data-ttu-id="ce241-193">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="ce241-193">Public.</span></span> <span data-ttu-id="ce241-194">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ce241-194">Optional.</span></span> <span data-ttu-id="ce241-195">Die Standardeinstellung lautet &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce241-195">Default is &quot;false&quot;.</span></span> <span data-ttu-id="ce241-196">Gibt an, ob die Eigenschaft als "als" festgelegt</span><span class="sxs-lookup"><span data-stu-id="ce241-196">Specifies whether the property is considered innate.</span></span> <span data-ttu-id="ce241-197">Eine angeborene Eigenschaft ist eine Eigenschaft, die entweder aus dem Inhalt einer Datei oder aus anderen Ressourcen oder Systemen berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="ce241-197">An innate property is one which is either calculated from the content of a file, or from other resources or systems.</span></span> <span data-ttu-id="ce241-198">System. Size ist beispielsweise eine angeborene Eigenschaft, die vom Datei System bereitgestellt wird. Das Ändern des Werts der-Eigenschaft in und von sich selbst bewirkt nichts.</span><span class="sxs-lookup"><span data-stu-id="ce241-198">For example, System.Size is an innate property provided by the file system; changing the value of the property in and of itself does nothing.</span></span> <span data-ttu-id="ce241-199">Weitere Beispiele sind System. Image. Dimensions und System.Doc-Umschlag. PageCount, die von Programmen basierend auf dem Inhalt der Datei berechnet werden, nicht basierend auf einer Benutzer veränderlichen Einstellung.</span><span class="sxs-lookup"><span data-stu-id="ce241-199">Other examples are System.Image.Dimensions and System.Document.PageCount, which are calculated by programs based upon the content of the file, not based upon a user-changeable setting.</span></span> <span data-ttu-id="ce241-200">Das Festlegen von isinnate = &quot; true bedeutet, dass &quot; der Benutzer diese Eigenschaft nicht direkt über ein Eigenschaften Steuerelement bearbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="ce241-200">Setting isInnate=&quot;true&quot; means the user cannot edit this property directly via a property control.</span></span> <span data-ttu-id="ce241-201">Dieser Wert wird dem PDTF_ISINNATE Flag zugeordnet, das in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> definiert und in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>ipropertydescription:: gettypeer Flags</strong></a>verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ce241-201">This value maps to the PDTF_ISINNATE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-202">canbebereinigt</span><span class="sxs-lookup"><span data-stu-id="ce241-202">canBePurged</span></span></td>
<td><span data-ttu-id="ce241-203"><strong>Nur Windows Vista mit Service Pack 1 (SP1) und</strong>höher.</span><span class="sxs-lookup"><span data-stu-id="ce241-203"><strong>Windows Vista with Service Pack 1 (SP1) and later only</strong>.</span></span> <span data-ttu-id="ce241-204">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="ce241-204">Public.</span></span> <span data-ttu-id="ce241-205">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ce241-205">Optional.</span></span> <span data-ttu-id="ce241-206">Wenn diese Eigenschaft auf true festgelegt &quot; &quot; ist, kann eine angeborene Eigenschaft gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="ce241-206">When set to &quot;true&quot;, allows an innate property to be deleted.</span></span> <span data-ttu-id="ce241-207">Angeborene Eigenschaften, die aus anderen Eigenschaften berechnet werden, sind definitionsgemäß schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ce241-207">Innate properties, which are calculated from other properties, are read-only by definition.</span></span> <span data-ttu-id="ce241-208">Der Standardwert für dieses Attribut hängt vom <em>isinnate</em> -Wert ab.</span><span class="sxs-lookup"><span data-stu-id="ce241-208">The default value for this attribute depends on the <em>isInnate</em> value.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ce241-209">isinnate</span><span class="sxs-lookup"><span data-stu-id="ce241-209">isInnate</span></span></th>
<th><span data-ttu-id="ce241-210">der Standardwert für canbebereinigt</span><span class="sxs-lookup"><span data-stu-id="ce241-210">canBePurged Default Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce241-211">true</span><span class="sxs-lookup"><span data-stu-id="ce241-211">true</span></span></td>
<td><span data-ttu-id="ce241-212">false</span><span class="sxs-lookup"><span data-stu-id="ce241-212">false</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-213">false</span><span class="sxs-lookup"><span data-stu-id="ce241-213">false</span></span></td>
<td><span data-ttu-id="ce241-214">true</span><span class="sxs-lookup"><span data-stu-id="ce241-214">true</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="ce241-215">Eine Eigenschaft, deren <em>isinnate</em> -Wert &quot; false ist &quot; (was bedeutet, dass die Eigenschaft Lese-/Schreibzugriff ist), kann den <em>canbepuredwert</em> nicht auch auf &quot; false festlegen &quot; .</span><span class="sxs-lookup"><span data-stu-id="ce241-215">A property whose <em>isInnate</em> value is &quot;false&quot; (meaning that the property is read/write) cannot also set the <em>canBePurged</em> value to &quot;false&quot;.</span></span> <span data-ttu-id="ce241-216">Diese Einschränkung wird vom Betriebssystem erzwungen.</span><span class="sxs-lookup"><span data-stu-id="ce241-216">This restriction is enforced by the operating system.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="ce241-217">Obwohl dieses Attribut in Windows Vista mit Service Pack 1 (SP1) eingeführt wurde, ist eine. PropDesc-Datei mit diesem Attribut vor Windows Vista mit SP1 mit Windows Vista kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ce241-217">Although this attribute was introduced in Windows Vista with Service Pack 1 (SP1), a .propdesc file that includes this attribute is compatible with Windows Vista prior to Windows Vista with SP1.</span></span> <span data-ttu-id="ce241-218">Das <em>canbepuring</em> -Attribut wird in dieser Situation einfach ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ce241-218">The <em>canBePurged</em> attribute is simply ignored in that situation.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-219">multiplevalues</span><span class="sxs-lookup"><span data-stu-id="ce241-219">multipleValues</span></span></td>
<td><span data-ttu-id="ce241-220">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="ce241-220">Public.</span></span> <span data-ttu-id="ce241-221">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ce241-221">Optional.</span></span> <span data-ttu-id="ce241-222">Die Standardeinstellung lautet &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce241-222">Default is &quot;false&quot;.</span></span> <span data-ttu-id="ce241-223">Gibt an, ob diese Eigenschaft mehrere Werte aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="ce241-223">Specifies whether this property can have multiple values.</span></span> <span data-ttu-id="ce241-224">Dieser Wert wird dem PDTF_MULTIPLEVALUES Flag zugeordnet, das in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> definiert und in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>ipropertydescription:: gettypeer Flags</strong></a>verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ce241-224">This value maps to the PDTF_MULTIPLEVALUES flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span> <span data-ttu-id="ce241-225">Dies wirkt sich auch darauf aus, ob VT_VECTOR oder auf den VarType-Wert des Eigenschafts Werts folgt.</span><span class="sxs-lookup"><span data-stu-id="ce241-225">This also influences whether VT_VECTOR is OR'd to the VARTYPE of the property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-226">isGroup</span><span class="sxs-lookup"><span data-stu-id="ce241-226">isGroup</span></span></td>
<td><span data-ttu-id="ce241-227">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="ce241-227">Public.</span></span> <span data-ttu-id="ce241-228">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ce241-228">Optional.</span></span> <span data-ttu-id="ce241-229">Die Standardeinstellung lautet &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce241-229">Default is &quot;false&quot;.</span></span> <span data-ttu-id="ce241-230">Gibt an, ob die Eigenschaft eine Gruppen Überschrift ist.</span><span class="sxs-lookup"><span data-stu-id="ce241-230">Specifies whether the property is a group heading.</span></span> <span data-ttu-id="ce241-231">Eine Gruppen Überschrift wird in proplists strikt verwendet, hat keinen Wert, wird nie in einer Datei gespeichert und sollte auch über verfügen <typeInfo type=&quot;Null&quot;> .</span><span class="sxs-lookup"><span data-stu-id="ce241-231">A group heading is strictly used in proplists, has no value, is never stored in a file, and should also have <typeInfo type=&quot;Null&quot;>.</span></span> <span data-ttu-id="ce241-232">Eine Benutzeroberfläche im System verwendet proplists, um die Reihenfolge der anzuzeigenden Eigenschaften anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ce241-232">Some UI in the system use proplists to indicate the sequence of the properties to display.</span></span> <span data-ttu-id="ce241-233">Diese proplists können Verweise auf Gruppen Überschriften (z. b. System. propgroup. Camera) enthalten, die der Benutzeroberfläche mitteilen, dass ein neuer Gruppenabschnitt (z. b. &quot; Kameraeinstellungen) gestartet werden soll &quot; .</span><span class="sxs-lookup"><span data-stu-id="ce241-233">These proplists may include references to group headings (eg, System.PropGroup.Camera), which tell the UI to start a new group section (eg, &quot;Camera Settings&quot;).</span></span> <span data-ttu-id="ce241-234">Eine Eigenschafts Beschreibung mit isGroup = &quot; true &quot; sollte einen angeben <labelInfo label=&quot;Some localized label&quot;> , andernfalls ist Sie keine nützliche Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ce241-234">A property description with isGroup=&quot;true&quot; should specify a <labelInfo label=&quot;Some localized label&quot;>, otherwise it isn't a useful property.</span></span> <span data-ttu-id="ce241-235">Dieser Wert wird dem PDTF_ISGROUP Flag zugeordnet, das in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> definiert und in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>ipropertydescription:: gettypeer Flags</strong></a>verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ce241-235">This value maps to the PDTF_ISGROUP flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-236">aggregationType</span><span class="sxs-lookup"><span data-stu-id="ce241-236">aggregationType</span></span></td>
<td><span data-ttu-id="ce241-237">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="ce241-237">Public.</span></span> <span data-ttu-id="ce241-238">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ce241-238">Optional.</span></span> <span data-ttu-id="ce241-239">Der Standardwert ist Default &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="ce241-239">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="ce241-240">Gibt an, wie Aggregat Eigenschaften angezeigt werden, wenn mehrere Elemente ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="ce241-240">Specifies how aggregate properties are displayed when multiple items are selected.</span></span> <span data-ttu-id="ce241-241">Nachdem diese Werte hier festgelegt wurden, werden Sie von <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>ipropertydescription:: getaggregationtype</strong></a> als <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ce241-241">Once set here, these values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription::GetAggregationType</strong></a> as an <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>.</span></span> <span data-ttu-id="ce241-242">Die folgenden Typen sind gültig.</span><span class="sxs-lookup"><span data-stu-id="ce241-242">The following are valid types.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ce241-243">Wert</span><span class="sxs-lookup"><span data-stu-id="ce241-243">Value</span></span></th>
<th><span data-ttu-id="ce241-244">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ce241-244">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce241-245">Standard</span><span class="sxs-lookup"><span data-stu-id="ce241-245">Default</span></span></td>
<td><span data-ttu-id="ce241-246">Standard.</span><span class="sxs-lookup"><span data-stu-id="ce241-246">Default.</span></span> <span data-ttu-id="ce241-247">Zeigt einen Platzhalter für <strong>mehrere Werte</strong> in der Benutzeroberfläche an.</span><span class="sxs-lookup"><span data-stu-id="ce241-247">Displays a <strong>Multiple Values</strong> placeholder in the UI.</span></span> <span data-ttu-id="ce241-248">Dies ist die Standardeinstellung, wenn der <em>Typ</em> mit dem angegebenen <em>AggregationType</em>nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="ce241-248">This is the default if the <em>type</em> is incompatible with the specified <em>aggregationType</em>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-249">First</span><span class="sxs-lookup"><span data-stu-id="ce241-249">First</span></span></td>
<td><span data-ttu-id="ce241-250">Zeigt den Eigenschafts Wert des ersten Elements in der Auswahl oder Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="ce241-250">Displays the property value of the first item in the selection or collection.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-251">SUM</span><span class="sxs-lookup"><span data-stu-id="ce241-251">Sum</span></span></td>
<td><span data-ttu-id="ce241-252">Zeigt die Summe der numerischen Werte an.</span><span class="sxs-lookup"><span data-stu-id="ce241-252">Displays the sum of the numerical values.</span></span> <span data-ttu-id="ce241-253">Nützlich für Eigenschaften wie z. b. System. Media. Duration oder System. Size.</span><span class="sxs-lookup"><span data-stu-id="ce241-253">Useful for properties such as System.Media.Duration or System.Size.</span></span> <span data-ttu-id="ce241-254">Dieser Wert ist nicht mit nicht numerischen Typen kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ce241-254">This value is not compatible with non-numeric types.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-255">Average</span><span class="sxs-lookup"><span data-stu-id="ce241-255">Average</span></span></td>
<td><span data-ttu-id="ce241-256">Zeigt den Durchschnitt der numerischen Werte an.</span><span class="sxs-lookup"><span data-stu-id="ce241-256">Displays the average of the numerical values.</span></span> <span data-ttu-id="ce241-257">Nützlich für Eigenschaften wie z. b. System. Rating.</span><span class="sxs-lookup"><span data-stu-id="ce241-257">Useful for properties such as System.Rating.</span></span> <span data-ttu-id="ce241-258">Dieser Wert ist nicht mit nicht numerischen Typen kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ce241-258">This value is not compatible with non-numeric types.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-259">DateRange</span><span class="sxs-lookup"><span data-stu-id="ce241-259">DateRange</span></span></td>
<td><span data-ttu-id="ce241-260">Zeigt einen Datumsbereich an.</span><span class="sxs-lookup"><span data-stu-id="ce241-260">Displays a range of dates.</span></span> <span data-ttu-id="ce241-261">Nützlich für Eigenschaften wie z. b. System. Photo. DateTaken.</span><span class="sxs-lookup"><span data-stu-id="ce241-261">Useful for properties like System.Photo.DateTaken.</span></span> <span data-ttu-id="ce241-262">Dieser Wert ist mit Ausnahme von Type = &quot; DateTime nicht kompatibel &quot; und ist der Standardwert für Eigenschaften dieses Typs.</span><span class="sxs-lookup"><span data-stu-id="ce241-262">This value is not compatible with anything except type=&quot;DateTime&quot; and is the default for properties of that type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-263">Union</span><span class="sxs-lookup"><span data-stu-id="ce241-263">Union</span></span></td>
<td><span data-ttu-id="ce241-264">Zeigt eine Vereinigung aller Werte in der Auswahl oder Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="ce241-264">Displays a union of all the values in the selection or collection.</span></span> <span data-ttu-id="ce241-265">Die Reihenfolge, in der die Werte angezeigt werden, ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="ce241-265">The order in which the values are shown is undefined.</span></span> <span data-ttu-id="ce241-266">Dieser Wert ist der Standardwert für Eigenschaften vom Typ = &quot; String &quot; und multiplevalues = &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="ce241-266">This value is the default for properties of type=&quot;String&quot; and multipleValues=&quot;true&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-267">Maximum</span><span class="sxs-lookup"><span data-stu-id="ce241-267">Maximum</span></span></td>
<td><span data-ttu-id="ce241-268">Zeigt den maximalen Wert in der Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="ce241-268">Displays the maximum value in the collection.</span></span> <span data-ttu-id="ce241-269">Nützlich für Eigenschaften wie z. b. System. DateModified.</span><span class="sxs-lookup"><span data-stu-id="ce241-269">Useful for properties like System.DateModified.</span></span> <span data-ttu-id="ce241-270">Nicht mit nicht numerischen oder nicht Datums Typen kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ce241-270">Not compatible with non-numeric or non-date types.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-271">Minimum</span><span class="sxs-lookup"><span data-stu-id="ce241-271">Minimum</span></span></td>
<td><span data-ttu-id="ce241-272">Zeigt den minimalen Wert in der Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="ce241-272">Displays the minimum value in the collection.</span></span> <span data-ttu-id="ce241-273">Nicht mit nicht numerischen oder nicht Datums Typen kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ce241-273">Not compatible with non-numeric or non-date types.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-274">istreeproperty</span><span class="sxs-lookup"><span data-stu-id="ce241-274">isTreeProperty</span></span></td>
<td><span data-ttu-id="ce241-275">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="ce241-275">Public.</span></span> <span data-ttu-id="ce241-276">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ce241-276">Optional.</span></span> <span data-ttu-id="ce241-277">Der Standardwert ist &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce241-277">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-278">isviewable</span><span class="sxs-lookup"><span data-stu-id="ce241-278">isViewable</span></span></td>
<td><span data-ttu-id="ce241-279">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="ce241-279">Public.</span></span> <span data-ttu-id="ce241-280">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ce241-280">Optional.</span></span> <span data-ttu-id="ce241-281">Der Standardwert ist &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce241-281">Default value is &quot;false&quot;.</span></span> <span data-ttu-id="ce241-282">Gibt an, ob diese Eigenschaft für den Benutzer sichtbar sein soll.</span><span class="sxs-lookup"><span data-stu-id="ce241-282">Specifies whether this property is intended to be viewable to the user.</span></span> <span data-ttu-id="ce241-283">Beispielsweise werden in der Benutzeroberfläche für die Spaltenauswahl nur die Eigenschaften angezeigt, die isviewable = &quot; true aufweisen &quot; .</span><span class="sxs-lookup"><span data-stu-id="ce241-283">For example, the Column Chooser UI only shows the properties that have isViewable=&quot;true&quot;.</span></span> <span data-ttu-id="ce241-284">Bei der Ausnahme handelt es sich um eine Benutzeroberfläche, die durch eine proplist gesteuert wird, die immer die-Eigenschaft anzeigt.</span><span class="sxs-lookup"><span data-stu-id="ce241-284">The exception is UI that is driven by a proplist, which will always show the property.</span></span> <span data-ttu-id="ce241-285">Wenn Sie über eine Eigenschaft verfügen, die nur für das überführen von Daten zwischen zwei Objekten vorgesehen ist und nie vom Benutzer angezeigt werden soll, sollte dieses Attribut "false" lauten.</span><span class="sxs-lookup"><span data-stu-id="ce241-285">If you have a property that is only meant to shuttle data between two objects, and never intended to be viewed by the user, this attribute should be false.</span></span> <span data-ttu-id="ce241-286">Dieser Wert wird dem PDTF_ISVIEWABLE Flag zugeordnet, das in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> definiert und in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>ipropertydescription:: gettypeer Flags</strong></a>verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ce241-286">This value maps to the PDTF_ISVIEWABLE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-287">isquerable</span><span class="sxs-lookup"><span data-stu-id="ce241-287">isQueryable</span></span></td>
<td><span data-ttu-id="ce241-288">Nur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ce241-288">Windows Vista only.</span></span> <span data-ttu-id="ce241-289">Wird in Windows 7 und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ce241-289">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="ce241-290">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="ce241-290">Public.</span></span> <span data-ttu-id="ce241-291">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ce241-291">Optional.</span></span> <span data-ttu-id="ce241-292">Der Standardwert ist &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce241-292">Default value is &quot;false&quot;.</span></span> <span data-ttu-id="ce241-293">Gibt an, ob diese Eigenschaft in der Such Abfrage-Generator-Benutzeroberfläche verfügbar sein soll.</span><span class="sxs-lookup"><span data-stu-id="ce241-293">Specifies whether this property is intended to be available in the Search Query Builder UI.</span></span> <span data-ttu-id="ce241-294">Für eine Eigenschaft muss isviewable = true festgelegt sein, &quot; &quot; bevor isquervable = &quot; true &quot; respektiert wird.</span><span class="sxs-lookup"><span data-stu-id="ce241-294">A property must have isViewable=&quot;true&quot; before isQueryable=&quot;true&quot; is respected.</span></span> <span data-ttu-id="ce241-295">Dieser Wert wird dem PDTF_ISQUERYABLE Flag zugeordnet, das in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> definiert und in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>ipropertydescription:: gettypeer Flags</strong></a>verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ce241-295">This value maps to the PDTF_ISQUERYABLE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-296">searchrawvalue</span><span class="sxs-lookup"><span data-stu-id="ce241-296">searchRawValue</span></span></td>
<td><span data-ttu-id="ce241-297"><strong>Windows 7 und höher.</strong></span><span class="sxs-lookup"><span data-stu-id="ce241-297"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="ce241-298">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="ce241-298">Public.</span></span> <span data-ttu-id="ce241-299">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ce241-299">Optional.</span></span> <span data-ttu-id="ce241-300">Der Standardwert ist &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce241-300">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-301">includeinfulltextquery</span><span class="sxs-lookup"><span data-stu-id="ce241-301">includeInFullTextQuery</span></span></td>
<td><span data-ttu-id="ce241-302">Nur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ce241-302">Windows Vista only.</span></span> <span data-ttu-id="ce241-303">Wird in Windows 7 und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ce241-303">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="ce241-304">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="ce241-304">Public.</span></span> <span data-ttu-id="ce241-305">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ce241-305">Optional.</span></span> <span data-ttu-id="ce241-306">Der Standardwert ist &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce241-306">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-307">conditionType</span><span class="sxs-lookup"><span data-stu-id="ce241-307">conditionType</span></span></td>
<td><span data-ttu-id="ce241-308">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="ce241-308">Public.</span></span> <span data-ttu-id="ce241-309">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ce241-309">Optional.</span></span> <span data-ttu-id="ce241-310">Der Standardwert ist &quot; String &quot; .</span><span class="sxs-lookup"><span data-stu-id="ce241-310">Default is &quot;String&quot;.</span></span> <span data-ttu-id="ce241-311">Gibt einen Hinweis für die Such Abfrage-Generator Benutzeroberfläche an, damit die Liste möglicher Bedingungs Operatoren innerhalb eines Prädikats bestimmt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ce241-311">Specifies a hint to the Search Query Builder UI so that it can determine the list of possible condition operators inside a predicate.</span></span> <span data-ttu-id="ce241-312">Die folgenden Werte werden erkannt.</span><span class="sxs-lookup"><span data-stu-id="ce241-312">The following are recognized values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ce241-313">Wert</span><span class="sxs-lookup"><span data-stu-id="ce241-313">Value</span></span></th>
<th><span data-ttu-id="ce241-314">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ce241-314">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce241-315">String</span><span class="sxs-lookup"><span data-stu-id="ce241-315">String</span></span></td>
<td><span data-ttu-id="ce241-316">Standard.</span><span class="sxs-lookup"><span data-stu-id="ce241-316">Default.</span></span> <span data-ttu-id="ce241-317">Die folgenden Operatoren werden verwendet: &quot; ist &quot; , &quot; ist nicht &quot; , &quot; &lt; &quot; , &quot; &gt; &quot; , &quot; <= &quot; , &quot; >= &quot; , &quot; beginnt mit &quot; , &quot; endet mit &quot; , &quot; enthält, enthält nicht, &quot; &quot; &quot; &quot; entspricht &quot; .</span><span class="sxs-lookup"><span data-stu-id="ce241-317">The following operators will be used: &quot;is&quot;, &quot;is not&quot;, &quot;&lt;&quot;, &quot;&gt;&quot;, &quot;<=&quot;, &quot;>=&quot;, &quot;starts with&quot;, &quot;ends with&quot;, &quot;contains&quot;, &quot;doesn't contain&quot;, &quot;is like&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-318">Number</span><span class="sxs-lookup"><span data-stu-id="ce241-318">Number</span></span></td>
<td><span data-ttu-id="ce241-319">Standardwert für numerische Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ce241-319">Default for numeric properties.</span></span> <span data-ttu-id="ce241-320">Die folgenden Operatoren werden verwendet: ist &quot; gleich &quot; , ist &quot; nicht gleich &quot; , &quot; ist kleiner als &quot; , &quot; ist größer als &quot; , &quot; ist kleiner als oder gleich &quot; , &quot; ist größer als oder gleich &quot; .</span><span class="sxs-lookup"><span data-stu-id="ce241-320">The following operators will be used: &quot;equals&quot;, &quot;doesn't equal&quot;, &quot;is less than&quot;, &quot;is greater than&quot;, &quot;is less than or equal to&quot;, &quot;is greater than or equal to&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-321">Datetime</span><span class="sxs-lookup"><span data-stu-id="ce241-321">DateTime</span></span></td>
<td><span data-ttu-id="ce241-322">Der Standardwert für Eigenschaften vom Typ = &quot; DateTime &quot; .</span><span class="sxs-lookup"><span data-stu-id="ce241-322">Default for properties of type=&quot;DateTime&quot;.</span></span> <span data-ttu-id="ce241-323">Die folgenden Operatoren werden verwendet: &quot; ist &quot; , &quot; ist nicht &quot; , &quot; ist vor &quot; , &quot; ist after &quot; , &quot; ist vor, ist &quot; jedoch, &quot; ist after, aber enthält &quot; .</span><span class="sxs-lookup"><span data-stu-id="ce241-323">The following operators will be used: &quot;is&quot;, &quot;is not&quot;, &quot;is before&quot;, &quot;is after&quot;, &quot;is before but includes&quot;, &quot;is after but includes&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-324">Boolean</span><span class="sxs-lookup"><span data-stu-id="ce241-324">Boolean</span></span></td>
<td><span data-ttu-id="ce241-325">Der Standardwert für Eigenschaften vom Typ = &quot; boolescher Wert &quot; .</span><span class="sxs-lookup"><span data-stu-id="ce241-325">Default for properties of type=&quot;Boolean&quot;.</span></span> <span data-ttu-id="ce241-326">Identisch mit der Zahl.</span><span class="sxs-lookup"><span data-stu-id="ce241-326">Same as Number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-327">Size</span><span class="sxs-lookup"><span data-stu-id="ce241-327">Size</span></span></td>
<td><span data-ttu-id="ce241-328">Identisch mit der Zahl.</span><span class="sxs-lookup"><span data-stu-id="ce241-328">Same as Number.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-329">DefaultOperation</span><span class="sxs-lookup"><span data-stu-id="ce241-329">defaultOperation</span></span></td>
<td><span data-ttu-id="ce241-330">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="ce241-330">Public.</span></span> <span data-ttu-id="ce241-331">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ce241-331">Optional.</span></span> <span data-ttu-id="ce241-332">Der Standardwert ist &quot; gleich &quot; .</span><span class="sxs-lookup"><span data-stu-id="ce241-332">Default is &quot;Equal&quot;.</span></span> <span data-ttu-id="ce241-333">Gibt einen Hinweis für das Such Abfrage-Generator Tool an, damit der Standard Operator bestimmt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ce241-333">Specifies a hint to the Search Query Builder tool so that it can determine the default operator.</span></span> <span data-ttu-id="ce241-334">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="ce241-334">The possible values are as follows:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ce241-335">Wert</span><span class="sxs-lookup"><span data-stu-id="ce241-335">Value</span></span></th>
<th><span data-ttu-id="ce241-336">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ce241-336">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce241-337">Equal</span><span class="sxs-lookup"><span data-stu-id="ce241-337">Equal</span></span></td>
<td><span data-ttu-id="ce241-338">Standard.</span><span class="sxs-lookup"><span data-stu-id="ce241-338">Default.</span></span> <span data-ttu-id="ce241-339">Gibt ein entsprechendes an.</span><span class="sxs-lookup"><span data-stu-id="ce241-339">Indicates equivalent.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-340">NotEqual</span><span class="sxs-lookup"><span data-stu-id="ce241-340">NotEqual</span></span></td>
<td><span data-ttu-id="ce241-341">Gibt nicht äquivalent an.</span><span class="sxs-lookup"><span data-stu-id="ce241-341">Indicates not equivalent.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-342">LessThan</span><span class="sxs-lookup"><span data-stu-id="ce241-342">LessThan</span></span></td>
<td><span data-ttu-id="ce241-343">Gibt weniger als an.</span><span class="sxs-lookup"><span data-stu-id="ce241-343">Indicates less than.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce241-344">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="ce241-344">GreaterThan</span></span></td>
<td><span data-ttu-id="ce241-345">Der Standardwert für die Eigenschaften von ConditionType = &quot; size &quot; .</span><span class="sxs-lookup"><span data-stu-id="ce241-345">Default for properties of conditionType=&quot;Size&quot;.</span></span> <span data-ttu-id="ce241-346">Gibt einen größer als an.</span><span class="sxs-lookup"><span data-stu-id="ce241-346">Indicates greater than.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce241-347">Enthält</span><span class="sxs-lookup"><span data-stu-id="ce241-347">Contains</span></span></td>
<td><span data-ttu-id="ce241-348">Der Standardwert für die Eigenschaften von ConditionType = &quot; String &quot; .</span><span class="sxs-lookup"><span data-stu-id="ce241-348">Default for properties of conditionType=&quot;String&quot;.</span></span> <span data-ttu-id="ce241-349">Gibt die Aufnahme an.</span><span class="sxs-lookup"><span data-stu-id="ce241-349">Indicates inclusion.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
