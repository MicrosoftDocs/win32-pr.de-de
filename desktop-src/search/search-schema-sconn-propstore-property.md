---
description: Das optionale- <property> Element gibt eine Eigenschaft an, die vom Suchconnector verwendet wird. Diese Eigenschaften sind spezifisch für diesen Suchconnector. Daher gibt es keine vordefinierte Gruppe von Namen, die verwendet werden können. Dieses Element hat keine untergeordneten Elemente.
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: Property-Element von PropertyStore (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2e4cee6f26ee65ba03d9225eafcea4a03a7c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525451"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a><span data-ttu-id="053fd-105">Property-Element von PropertyStore (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="053fd-105">property Element of propertyStore (Search Connector Schema)</span></span>

<span data-ttu-id="053fd-106">Das optionale- <property> Element gibt eine Eigenschaft an, die vom Suchconnector verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="053fd-106">The optional <property> element specifies a property used by the search connector.</span></span> <span data-ttu-id="053fd-107">Diese Eigenschaften sind spezifisch für diesen Suchconnector. Daher gibt es keine vordefinierte Gruppe von Namen, die verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="053fd-107">These properties are specific to this search connector, so there is no predefined set of names to use.</span></span> <span data-ttu-id="053fd-108">Dieses Element hat keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="053fd-108">This element has no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="053fd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="053fd-109">Syntax</span></span>


```
<!-- property for propertyStore element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded">
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension base="xs:anyType">
                        <xs:attribute name="name" type="canonical-name" use="required"/>
                        <xs:attribute name="type"/>
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="053fd-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="053fd-110">Element Information</span></span>



| <span data-ttu-id="053fd-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="053fd-111">Parent Element</span></span>                                                                           | <span data-ttu-id="053fd-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="053fd-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="053fd-113">PropertyStore-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="053fd-113">propertyStore Element (Search Connector Schema)</span></span>](search-schema-sconn-propertystore.md) |                |



 

## <a name="attributes"></a><span data-ttu-id="053fd-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="053fd-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="053fd-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="053fd-115">Attribute</span></span></th>
<th><span data-ttu-id="053fd-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="053fd-116">Description</span></span></th>
<th><span data-ttu-id="053fd-117">Werte</span><span class="sxs-lookup"><span data-stu-id="053fd-117">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="053fd-118">name</span><span class="sxs-lookup"><span data-stu-id="053fd-118">name</span></span></td>
<td><span data-ttu-id="053fd-119">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="053fd-119">Public.</span></span> <span data-ttu-id="053fd-120">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="053fd-120">Required.</span></span> <span data-ttu-id="053fd-121">Der Anzeigename der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="053fd-121">The display name of the property.</span></span></td>
<td> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="053fd-122">type</span><span class="sxs-lookup"><span data-stu-id="053fd-122">type</span></span></td>
<td><span data-ttu-id="053fd-123">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="053fd-123">Public.</span></span> <span data-ttu-id="053fd-124">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="053fd-124">Required.</span></span> <span data-ttu-id="053fd-125">Der Typ der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="053fd-125">The type of property.</span></span></td>
<td><span data-ttu-id="053fd-126">Beliebig: Standardwert.</span><span class="sxs-lookup"><span data-stu-id="053fd-126">Any: Default.</span></span> <span data-ttu-id="053fd-127">Der Wert wird vom Eigenschafts Subsystem nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="053fd-127">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="053fd-128">VT_NULL wird von GetPropertyType zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="053fd-128">VT_NULL will be returned by GetPropertyType.</span></span>
<ul>
<li><span data-ttu-id="053fd-129">NULL: für diese Eigenschaft ist kein Wert vorhanden.</span><span class="sxs-lookup"><span data-stu-id="053fd-129">Null: There is no value for this property.</span></span> <span data-ttu-id="053fd-130">VT_NULL wird von GetPropertyType zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="053fd-130">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="053fd-131">String: der Wert muss ein VT_LPWSTR sein.</span><span class="sxs-lookup"><span data-stu-id="053fd-131">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="053fd-132">Boolescher Wert: der Wert muss ein VT_BOOL sein.</span><span class="sxs-lookup"><span data-stu-id="053fd-132">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="053fd-133">Byte: der Wert muss ein VT_UI1 sein.</span><span class="sxs-lookup"><span data-stu-id="053fd-133">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="053fd-134">Buffer: der Wert muss ein VT_UI1 sein | VT_VECTOR Puffer bytes.</span><span class="sxs-lookup"><span data-stu-id="053fd-134">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="053fd-135">Int16: der Wert muss ein VT_I2 sein.</span><span class="sxs-lookup"><span data-stu-id="053fd-135">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="053fd-136">UInt16: der Wert muss ein VT_UI2 sein.</span><span class="sxs-lookup"><span data-stu-id="053fd-136">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="053fd-137">Int32: der Wert muss ein VT_I4 sein.</span><span class="sxs-lookup"><span data-stu-id="053fd-137">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="053fd-138">UInt32: der Wert muss ein VT_UI4 sein.</span><span class="sxs-lookup"><span data-stu-id="053fd-138">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="053fd-139">Int64: der Wert muss ein VT_I8 sein.</span><span class="sxs-lookup"><span data-stu-id="053fd-139">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="053fd-140">UInt64: der Wert muss ein VT_UI8</span><span class="sxs-lookup"><span data-stu-id="053fd-140">UInt64: The value must be a VT_UI8</span></span></li>
<li><span data-ttu-id="053fd-141">Double: der Wert muss ein VT_R8 sein.</span><span class="sxs-lookup"><span data-stu-id="053fd-141">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="053fd-142">DateTime: der Wert muss ein VT_FILETIME sein.</span><span class="sxs-lookup"><span data-stu-id="053fd-142">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="053fd-143">GUID: der Wert muss ein VT_CLSID sein.</span><span class="sxs-lookup"><span data-stu-id="053fd-143">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="053fd-144">BLOB: der Wert muss ein VT_BLOB sein.</span><span class="sxs-lookup"><span data-stu-id="053fd-144">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="053fd-145">Objekt: der Wert muss ein VT_UNKNOWN sein.</span><span class="sxs-lookup"><span data-stu-id="053fd-145">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="053fd-146">Stream: der Wert muss ein VT_STREAM sein.</span><span class="sxs-lookup"><span data-stu-id="053fd-146">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="053fd-147">Zwischenablage: der Wert muss ein VT_CF sein.</span><span class="sxs-lookup"><span data-stu-id="053fd-147">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="053fd-148">schema</span><span class="sxs-lookup"><span data-stu-id="053fd-148">schema</span></span></td>
<td><span data-ttu-id="053fd-149">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="053fd-149">Public.</span></span> <span data-ttu-id="053fd-150">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="053fd-150">Optional.</span></span> <span data-ttu-id="053fd-151">Das Schema, in dem die Eigenschaft definiert ist.</span><span class="sxs-lookup"><span data-stu-id="053fd-151">The schema where the property is defined.</span></span></td>
<td> </td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="053fd-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="053fd-152">Remarks</span></span>

<span data-ttu-id="053fd-153">OpenSearch-Suchconnectors können die opensearchhtmlrollovertemplate-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="053fd-153">OpenSearch search connectors can use the OpenSearchHTMLRolloverTemplate property.</span></span> <span data-ttu-id="053fd-154">Diese Eigenschaft identifiziert eine Vorlage, die nach der OpenSearch-Vorlagen Konvention formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="053fd-154">This property identifies a template that is formatted following the OpenSearch template convention.</span></span> <span data-ttu-id="053fd-155">Die Vorlage "opensearchhtmlrollovertemplate" wird verwendet, wenn der Benutzer in der Befehlsleiste auf die Schaltfläche "Suche nach Website" klickt.</span><span class="sxs-lookup"><span data-stu-id="053fd-155">The OpenSearchHTMLRolloverTemplate template is used when the user clicks on the "Search on website" button in the command bar.</span></span>

## <a name="example"></a><span data-ttu-id="053fd-156">Beispiel</span><span class="sxs-lookup"><span data-stu-id="053fd-156">Example</span></span>

<span data-ttu-id="053fd-157">Das folgende Beispiel zeigt ein- <propertyStore> Element mit zwei- <property> Elementen.</span><span class="sxs-lookup"><span data-stu-id="053fd-157">The following example shows a <propertyStore> element with two <property> elements.</span></span>


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



