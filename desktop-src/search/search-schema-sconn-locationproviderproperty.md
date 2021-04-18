---
description: Das optionale- <property> Element gibt die Eigenschaften an, die vom Speicherort Anbieter verwendet werden.
ms.assetid: c1120dea-cb0b-4746-a5c1-4c83cda6dd7c
title: Property-Element von locationprovider (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71081b8b04ec999daa90958a29708b8efc64bee0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106351913"
---
# <a name="property-element-of-locationprovider-search-connector-schema"></a><span data-ttu-id="f8023-103">Property-Element von locationprovider (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="f8023-103">property Element of locationProvider (Search Connector Schema)</span></span>

<span data-ttu-id="f8023-104">Das optionale- <property> Element gibt die Eigenschaften an, die vom Speicherort Anbieter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8023-104">The optional <property> element specifies the properties used by the location provider.</span></span> <span data-ttu-id="f8023-105">Diese Eigenschaften sind spezifisch für diesen Speicherort Anbieter. Daher gibt es keine vordefinierte Gruppe von Namen, die verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f8023-105">These properties are specific to this location provider, so there is no predefined set of names to use.</span></span> <span data-ttu-id="f8023-106">Das- <property> Element verfügt über zwei Attribute, wie in diesem Thema beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f8023-106">The <property> element has two attributes, as described in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8023-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8023-107">Syntax</span></span>


```
<!-- property element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
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



## <a name="property-element-information"></a><span data-ttu-id="f8023-108"><property> Element Informationen</span><span class="sxs-lookup"><span data-stu-id="f8023-108"><property> Element Information</span></span>



| <span data-ttu-id="f8023-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="f8023-109">Parent Element</span></span>                                                                                 | <span data-ttu-id="f8023-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f8023-110">Child Elements</span></span>                     |
|------------------------------------------------------------------------------------------------|------------------------------------|
| [<span data-ttu-id="f8023-111">locationprovider-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="f8023-111">locationProvider Element (Search Connector Schema)</span></span>](search-schema-sconn-locationprovider.md) | <span data-ttu-id="f8023-112">-Eigenschaft, die in diesem Thema beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f8023-112">property, described in this topic.</span></span> |



 


## <a name="property-attributes"></a><span data-ttu-id="f8023-113"><property> Legt</span><span class="sxs-lookup"><span data-stu-id="f8023-113"><property> Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8023-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="f8023-114">Attribute</span></span></th>
<th><span data-ttu-id="f8023-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8023-115">Description</span></span></th>
<th><span data-ttu-id="f8023-116">Werte</span><span class="sxs-lookup"><span data-stu-id="f8023-116">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f8023-117">name</span><span class="sxs-lookup"><span data-stu-id="f8023-117">name</span></span></td>
<td><span data-ttu-id="f8023-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f8023-118">Required.</span></span> <span data-ttu-id="f8023-119">Der Anzeigename der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f8023-119">The display name of the property.</span></span></td>
<td> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8023-120">type</span><span class="sxs-lookup"><span data-stu-id="f8023-120">type</span></span></td>
<td><span data-ttu-id="f8023-121">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f8023-121">Required.</span></span> <span data-ttu-id="f8023-122">Der Typ der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f8023-122">The type of property.</span></span></td>
<td><span data-ttu-id="f8023-123">Beliebig: Standardwert.</span><span class="sxs-lookup"><span data-stu-id="f8023-123">Any: Default.</span></span> <span data-ttu-id="f8023-124">Der Wert wird vom Eigenschafts Subsystem nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="f8023-124">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="f8023-125">VT_NULL wird von GetPropertyType zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8023-125">VT_NULL will be returned by GetPropertyType.</span></span>
<ul>
<li><span data-ttu-id="f8023-126">NULL: für diese Eigenschaft ist kein Wert vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f8023-126">Null: There is no value for this property.</span></span> <span data-ttu-id="f8023-127">VT_NULL wird von GetPropertyType zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8023-127">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="f8023-128">String: der Wert muss ein VT_LPWSTR sein.</span><span class="sxs-lookup"><span data-stu-id="f8023-128">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="f8023-129">Boolescher Wert: der Wert muss ein VT_BOOL sein.</span><span class="sxs-lookup"><span data-stu-id="f8023-129">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="f8023-130">Byte: der Wert muss ein VT_UI1 sein.</span><span class="sxs-lookup"><span data-stu-id="f8023-130">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="f8023-131">Buffer: der Wert muss ein VT_UI1 sein | VT_VECTOR Puffer bytes.</span><span class="sxs-lookup"><span data-stu-id="f8023-131">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="f8023-132">Int16: der Wert muss ein VT_I2 sein.</span><span class="sxs-lookup"><span data-stu-id="f8023-132">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="f8023-133">UInt16: der Wert muss ein VT_UI2 sein.</span><span class="sxs-lookup"><span data-stu-id="f8023-133">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="f8023-134">Int32: der Wert muss ein VT_I4 sein.</span><span class="sxs-lookup"><span data-stu-id="f8023-134">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="f8023-135">UInt32: der Wert muss ein VT_UI4 sein.</span><span class="sxs-lookup"><span data-stu-id="f8023-135">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="f8023-136">Int64: der Wert muss ein VT_I8 sein.</span><span class="sxs-lookup"><span data-stu-id="f8023-136">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="f8023-137">UInt64: der Wert muss ein VT_UI8</span><span class="sxs-lookup"><span data-stu-id="f8023-137">UInt64: The value must be a VT_UI8</span></span></li>
<li><span data-ttu-id="f8023-138">Double: der Wert muss ein VT_R8 sein.</span><span class="sxs-lookup"><span data-stu-id="f8023-138">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="f8023-139">DateTime: der Wert muss ein VT_FILETIME sein.</span><span class="sxs-lookup"><span data-stu-id="f8023-139">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="f8023-140">GUID: der Wert muss ein VT_CLSID sein.</span><span class="sxs-lookup"><span data-stu-id="f8023-140">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="f8023-141">BLOB: der Wert muss ein VT_BLOB sein.</span><span class="sxs-lookup"><span data-stu-id="f8023-141">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="f8023-142">Objekt: der Wert muss ein VT_UNKNOWN sein.</span><span class="sxs-lookup"><span data-stu-id="f8023-142">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="f8023-143">Stream: der Wert muss ein VT_STREAM sein.</span><span class="sxs-lookup"><span data-stu-id="f8023-143">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="f8023-144">Zwischenablage: der Wert muss ein VT_CF sein.</span><span class="sxs-lookup"><span data-stu-id="f8023-144">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="f8023-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8023-145">Remarks</span></span>

<span data-ttu-id="f8023-146">Für den OpenSearch-Anbieter werden die folgenden Eigenschaften verwendet:</span><span class="sxs-lookup"><span data-stu-id="f8023-146">For the OpenSearch provider, the following properties are used:</span></span>

-   <span data-ttu-id="f8023-147">Opensearchshortname: Kurzname des Such Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f8023-147">OpenSearchShortName: Short name of the search service</span></span>
-   <span data-ttu-id="f8023-148">Opensearchquerytemplate: Vorlage, die nach der OpenSearch-Vorlagen Konvention formatiert ist, für den Abfragedienst</span><span class="sxs-lookup"><span data-stu-id="f8023-148">OpenSearchQueryTemplate: Template, formatted following the OpenSearch template convention, for the query service</span></span>
-   <span data-ttu-id="f8023-149">Maximumresultcount: (Anzahl) maximale Anzahl von Ergebnissen, die vom Suchdienst zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f8023-149">MaximumResultCount: (number) Maximum number of results returned by the search service</span></span>
-   <span data-ttu-id="f8023-150">Linkisfilepath: (Boolean) Wenn true, versucht der Anbieter, die zurückgegebenen Elemente als Dateien zu interpretieren, wobei die Erweiterungen verwendet werden, um das richtige shellitem in der Ansicht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f8023-150">LinkIsFilePath: (Boolean) If true, the provider tries to interpret returned items as files, using their extensions to create the proper ShellItem in the view.</span></span> <span data-ttu-id="f8023-151">Bei "false" werden Elemente als URL-Verknüpfungen behandelt.</span><span class="sxs-lookup"><span data-stu-id="f8023-151">If false, items are treated as URL shortcuts.</span></span>

 

 



