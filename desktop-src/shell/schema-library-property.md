---
description: Das- <property> Element gibt eine Eigenschaft an, die von der Bibliothek verwendet wird. Diese Eigenschaften sind spezifisch für die Bibliothek. Daher gibt es keinen vordefinierten Satz von Eigenschaftsnamen, die verwendet werden können. Dieses Element ist optional und verfügt über keine untergeordneten Elemente.
ms.assetid: 8BF6EC7A-A87E-45fe-A8F0-4B49594E9E7B
title: Property-Element (Bibliotheks Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b269e8914cf1f5da92d96e1922f7347a161daf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993766"
---
# <a name="property-element-library-schema"></a><span data-ttu-id="c27c7-105">Property-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="c27c7-105">property Element (Library Schema)</span></span>

<span data-ttu-id="c27c7-106">Das- <property> Element gibt eine Eigenschaft an, die von der Bibliothek verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c27c7-106">The <property> element specifies a property used by the library.</span></span> <span data-ttu-id="c27c7-107">Diese Eigenschaften sind spezifisch für die Bibliothek. Daher gibt es keinen vordefinierten Satz von Eigenschaftsnamen, die verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c27c7-107">These properties are specific to the library, so there is no predefined set of property names to use.</span></span> <span data-ttu-id="c27c7-108">Dieses Element ist optional und verfügt über keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="c27c7-108">This element is optional and has no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="c27c7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c27c7-109">Syntax</span></span>

``` syntax
<!-- property -->
<xs:element name="property" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension base="xs:anyType">
                <xs:attribute name="name" type="canonical-name" use="required"/>
                    <xs:simpleType name="canonical-name">
                        <xs:restriction base="xs:string">
                            <xs:maxLength value="63"/>
                            <xs:pattern value="[0-9A-Za-z.]*"/>
                        </xs:restriction>
                    </xs:simpleType>
                <xs:attribute name="type"/>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="c27c7-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c27c7-110">Element Information</span></span>



| <span data-ttu-id="c27c7-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="c27c7-111">Parent Element</span></span>                                                             | <span data-ttu-id="c27c7-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c27c7-112">Child Elements</span></span> |
|----------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="c27c7-113">PropertyStore-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="c27c7-113">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md) | <span data-ttu-id="c27c7-114">Keine</span><span class="sxs-lookup"><span data-stu-id="c27c7-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="c27c7-115">Attributes</span><span class="sxs-lookup"><span data-stu-id="c27c7-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c27c7-116">attribute</span><span class="sxs-lookup"><span data-stu-id="c27c7-116">Attribute</span></span></th>
<th><span data-ttu-id="c27c7-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c27c7-117">Description</span></span></th>
<th><span data-ttu-id="c27c7-118">Werte</span><span class="sxs-lookup"><span data-stu-id="c27c7-118">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c27c7-119">name</span><span class="sxs-lookup"><span data-stu-id="c27c7-119">name</span></span></td>
<td><span data-ttu-id="c27c7-120">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="c27c7-120">Public.</span></span> <span data-ttu-id="c27c7-121">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c27c7-121">Required.</span></span> <span data-ttu-id="c27c7-122">Der Anzeigename der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c27c7-122">The display name of the property.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c27c7-123">type</span><span class="sxs-lookup"><span data-stu-id="c27c7-123">type</span></span></td>
<td><span data-ttu-id="c27c7-124">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="c27c7-124">Public.</span></span> <span data-ttu-id="c27c7-125">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c27c7-125">Required.</span></span> <span data-ttu-id="c27c7-126">Der Typ der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c27c7-126">The type of property.</span></span></td>
<td><ul>
<li><span data-ttu-id="c27c7-127">Beliebig: Standardwert.</span><span class="sxs-lookup"><span data-stu-id="c27c7-127">Any: Default.</span></span> <span data-ttu-id="c27c7-128">Der Wert wird vom Eigenschafts Subsystem nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="c27c7-128">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="c27c7-129">VT_NULL wird von GetPropertyType zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c27c7-129">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="c27c7-130">NULL: für diese Eigenschaft ist kein Wert vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c27c7-130">Null: There is no value for this property.</span></span> <span data-ttu-id="c27c7-131">VT_NULL wird von GetPropertyType zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c27c7-131">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="c27c7-132">String: der Wert muss ein VT_LPWSTR sein.</span><span class="sxs-lookup"><span data-stu-id="c27c7-132">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="c27c7-133">Boolescher Wert: der Wert muss ein VT_BOOL sein.</span><span class="sxs-lookup"><span data-stu-id="c27c7-133">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="c27c7-134">Byte: der Wert muss ein VT_UI1 sein.</span><span class="sxs-lookup"><span data-stu-id="c27c7-134">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="c27c7-135">Buffer: der Wert muss ein VT_UI1 sein | VT_VECTOR Puffer bytes.</span><span class="sxs-lookup"><span data-stu-id="c27c7-135">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="c27c7-136">Int16: der Wert muss ein VT_I2 sein.</span><span class="sxs-lookup"><span data-stu-id="c27c7-136">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="c27c7-137">UInt16: der Wert muss ein VT_UI2 sein.</span><span class="sxs-lookup"><span data-stu-id="c27c7-137">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="c27c7-138">Int32: der Wert muss ein VT_I4 sein.</span><span class="sxs-lookup"><span data-stu-id="c27c7-138">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="c27c7-139">UInt32: der Wert muss ein VT_UI4 sein.</span><span class="sxs-lookup"><span data-stu-id="c27c7-139">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="c27c7-140">Int64: der Wert muss ein VT_I8 sein.</span><span class="sxs-lookup"><span data-stu-id="c27c7-140">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="c27c7-141">UInt64: der Wert muss ein VT_UI8 sein.</span><span class="sxs-lookup"><span data-stu-id="c27c7-141">UInt64: The value must be a VT_UI8.</span></span></li>
<li><span data-ttu-id="c27c7-142">Double: der Wert muss ein VT_R8 sein.</span><span class="sxs-lookup"><span data-stu-id="c27c7-142">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="c27c7-143">DateTime: der Wert muss ein VT_FILETIME sein.</span><span class="sxs-lookup"><span data-stu-id="c27c7-143">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="c27c7-144">GUID: der Wert muss ein VT_CLSID sein.</span><span class="sxs-lookup"><span data-stu-id="c27c7-144">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="c27c7-145">BLOB: der Wert muss ein VT_BLOB sein.</span><span class="sxs-lookup"><span data-stu-id="c27c7-145">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="c27c7-146">Objekt: der Wert muss ein VT_UNKNOWN sein.</span><span class="sxs-lookup"><span data-stu-id="c27c7-146">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="c27c7-147">Stream: der Wert muss ein VT_STREAM sein.</span><span class="sxs-lookup"><span data-stu-id="c27c7-147">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="c27c7-148">Zwischenablage: der Wert muss ein VT_CF sein.</span><span class="sxs-lookup"><span data-stu-id="c27c7-148">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="c27c7-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c27c7-149">Remarks</span></span>

<span data-ttu-id="c27c7-150">Die Anforderungen für das <kanonische Name-> Element entsprechen den Anforderungen für Windows Search und das Windows-Eigenschaften System.</span><span class="sxs-lookup"><span data-stu-id="c27c7-150">The requirements for the <canonical-name> element match the requirements for Windows Search and the Windows property system.</span></span> <span data-ttu-id="c27c7-151">Die Zeichenfolge muss den Typ "Canonical-Type" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c27c7-151">The string must be of type canonical-type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c27c7-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c27c7-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c27c7-153">Bibliotheks Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="c27c7-153">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="c27c7-154">Eigenschaftsschemas</span><span class="sxs-lookup"><span data-stu-id="c27c7-154">Property Schemas</span></span>](../properties/building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="c27c7-155">Suchdienst-Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="c27c7-155">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
