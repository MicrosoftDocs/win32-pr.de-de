---
title: Komplexer DataDefinitionType-Typ
description: Definiert ein Datenelement, das Sie mit dem-Ereignis einschließen möchten. | Komplexer DataDefinitionType-Typ
ms.assetid: f4234e54-a5a8-48e4-941f-05107dcd3f88
keywords:
- DataDefinitionType komplexer Typ (Ereignisprotokoll)
topic_type:
- apiref
api_name:
- DataDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19584c28a7bdf7ae01b87d1f414b9464b7b4271d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354303"
---
# <a name="datadefinitiontype-complex-type"></a><span data-ttu-id="05d36-105">Komplexer DataDefinitionType-Typ</span><span class="sxs-lookup"><span data-stu-id="05d36-105">DataDefinitionType Complex Type</span></span>

<span data-ttu-id="05d36-106">Definiert ein Datenelement, das Sie mit dem-Ereignis einschließen möchten.</span><span class="sxs-lookup"><span data-stu-id="05d36-106">Defines a data item that you want to include with the event.</span></span>

``` syntax
<xs:complexType name="DataDefinitionType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="inType"
                type="QName"
                use="required"
             />
            <xs:attribute name="outType"
                type="QName"
                use="optional"
             />
            <xs:attribute name="map"
                type="string"
                use="optional"
             />
            <xs:attribute name="length"
                type="LengthType"
                use="optional"
             />
            <xs:attribute name="count"
                type="CountType"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="05d36-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="05d36-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="05d36-108">Name</span><span class="sxs-lookup"><span data-stu-id="05d36-108">Name</span></span></th>
<th><span data-ttu-id="05d36-109">type</span><span class="sxs-lookup"><span data-stu-id="05d36-109">Type</span></span></th>
<th><span data-ttu-id="05d36-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05d36-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="05d36-111">count</span><span class="sxs-lookup"><span data-stu-id="05d36-111">count</span></span></td>
<td><span data-ttu-id="05d36-112"><a href="eventmanifestschema-counttype-simpletype.md"><strong>"Count Type"</strong></a></span><span class="sxs-lookup"><span data-stu-id="05d36-112"><a href="eventmanifestschema-counttype-simpletype.md"><strong>CountType</strong></a></span></span></td>
<td><span data-ttu-id="05d36-113">Die Anzahl der Elemente im Array, wenn das Datenelement ein Array ist.</span><span class="sxs-lookup"><span data-stu-id="05d36-113">The number of elements in the array if the data item is an array.</span></span> <span data-ttu-id="05d36-114">Sie können die tatsächliche Anzahl oder den Namen eines anderen Datenelements angeben, das die Anzahl enthält.</span><span class="sxs-lookup"><span data-stu-id="05d36-114">You can specify the actual count or the name of another data item that contains the count.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05d36-115">intype</span><span class="sxs-lookup"><span data-stu-id="05d36-115">inType</span></span></td>
<td><span data-ttu-id="05d36-116"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="05d36-116"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="05d36-117">Der Datentyp für dieses Datenelement.</span><span class="sxs-lookup"><span data-stu-id="05d36-117">The data type for this data item.</span></span> <span data-ttu-id="05d36-118">Eine Liste der vordefinierten Eingabe Datentypen finden Sie unter der komplexe Typ " <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> ".</span><span class="sxs-lookup"><span data-stu-id="05d36-118">For a list of predefined input data types, see the <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> complex type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05d36-119">length</span><span class="sxs-lookup"><span data-stu-id="05d36-119">length</span></span></td>
<td><span data-ttu-id="05d36-120"><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>Längen-Typ</strong></a></span><span class="sxs-lookup"><span data-stu-id="05d36-120"><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>LengthType</strong></a></span></span></td>
<td><span data-ttu-id="05d36-121">Die Länge eines Datenelements variabler Länge, z. b. ein binäres Blob.</span><span class="sxs-lookup"><span data-stu-id="05d36-121">The length of a variable length data item, such as a binary blob.</span></span> <span data-ttu-id="05d36-122">Geben Sie für binäre Daten die Länge in Bytes an, und geben Sie für Zeichen folgen Daten die Länge in Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="05d36-122">For binary data, specify the length in bytes and for string data, specify the length in characters.</span></span> <span data-ttu-id="05d36-123">Sie können die tatsächliche Länge oder den Namen eines anderen Datenelements angeben, das die Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="05d36-123">You can specify the actual length or the name of another data item that contains the length.</span></span><br/> <span data-ttu-id="05d36-124">Wenn Sie das length-Attribut verwenden, um eine Zeichenfolge mit fester Länge anzugeben, müssen Sie die Zeichenfolge in die festgelegte Länge auffüllen, damit das NULL-Terminator-Zeichen am Ende zugelassen wird (wenn die Länge beispielsweise 5 beträgt, muss die Zeichenfolge &quot; ABC &quot; als ABC aufgefüllt werden &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="05d36-124">If you use the length attribute to specify a fixed length string, you must pad the string to its fixed length allowing for the null-terminator character at the end (for example, if the length is 5, the string &quot;abc&quot; must be padded as &quot;abc &quot;.</span></span> <span data-ttu-id="05d36-125">Die Zeichen folgen Länge muss das NULL-Terminator-Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="05d36-125">The string length must include the null-terminator character.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05d36-126">Karte</span><span class="sxs-lookup"><span data-stu-id="05d36-126">map</span></span></td>
<td><span data-ttu-id="05d36-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="05d36-127">string</span></span></td>
<td><span data-ttu-id="05d36-128">Der Name der Name-Wert-Zuordnung, die zum Zuordnen von ganzzahligen Werten zu Zeichen folgen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="05d36-128">The name of the name/value map to use to map integer values to strings.</span></span> <span data-ttu-id="05d36-129">Der Datentyp des Datenelements muss einen der folgenden Typen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="05d36-129">The data type of the data item must be of one of the following types:</span></span><br/>
<ul>
<li><span data-ttu-id="05d36-130">win:UInt8</span><span class="sxs-lookup"><span data-stu-id="05d36-130">win:UInt8</span></span></li>
<li><span data-ttu-id="05d36-131">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="05d36-131">win:UInt16</span></span></li>
<li><span data-ttu-id="05d36-132">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="05d36-132">win:UInt32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05d36-133">name</span><span class="sxs-lookup"><span data-stu-id="05d36-133">name</span></span></td>
<td><span data-ttu-id="05d36-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="05d36-134">string</span></span></td>
<td><span data-ttu-id="05d36-135">Der Name des Datenelements.</span><span class="sxs-lookup"><span data-stu-id="05d36-135">The name of the data item.</span></span> <span data-ttu-id="05d36-136">Sie können den Namen verwenden, um auf dieses Datenelement in Ihrem XML-Fragment zu verweisen, wenn Sie einen <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> -Abschnitt in ihrer Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="05d36-136">You can use the name to reference this data item in your XML fragment if you specify a <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> section in your template.</span></span> <span data-ttu-id="05d36-137">Sie können auch in einem length-oder count-Attribut eines anderen Datenelements auf diesen Namen verweisen, wenn dieses Datenelement seinen Längen-oder Anzahl Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="05d36-137">You can also reference this name in a length or count attribute of another data item if this data item contains its length or count value.</span></span><br/> <span data-ttu-id="05d36-138"><strong>Windows Vista:</strong> Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="05d36-138"><strong>Windows Vista:</strong> This attribute is optional.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05d36-139">outtype</span><span class="sxs-lookup"><span data-stu-id="05d36-139">outType</span></span></td>
<td><span data-ttu-id="05d36-140"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="05d36-140"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="05d36-141">Der Datentyp, der beim Rendern dieses Datenelements verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="05d36-141">The data type to use when rendering this data item.</span></span> <span data-ttu-id="05d36-142">Eine Liste der vordefinierten Ausgabe Datentypen finden Sie unter der komplexe Typ " <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType</strong></a> ".</span><span class="sxs-lookup"><span data-stu-id="05d36-142">For a list of predefined output data types, see the <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType</strong></a> complex type.</span></span><br/> <span data-ttu-id="05d36-143"><strong>Windows Vista:</strong> Der Ausgabetyp wird ignoriert, und der Dienst bestimmt den Typ basierend auf dem Eingabetyp.</span><span class="sxs-lookup"><span data-stu-id="05d36-143"><strong>Windows Vista:</strong> The output type is ignored, and the service determines the type based on the input type.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="05d36-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05d36-144">Remarks</span></span>

<span data-ttu-id="05d36-145">Für Eingabetypen mit variabler Länge (z. b. binäre BLOB) müssen Sie das length-Attribut verwenden, um die Größe der Daten explizit anzugeben.</span><span class="sxs-lookup"><span data-stu-id="05d36-145">For variable length input types, such as binary blobs, you must use the length attribute to explicitly specify the size of the data.</span></span> <span data-ttu-id="05d36-146">Geben Sie für Zeichen folgen nur dann das length-Attribut an, wenn die Zeichen folgen eine festgelegte Länge haben.</span><span class="sxs-lookup"><span data-stu-id="05d36-146">For strings, specify the length attribute only if the strings are of a fixed length.</span></span>

## <a name="examples"></a><span data-ttu-id="05d36-147">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05d36-147">Examples</span></span>

<span data-ttu-id="05d36-148">Im folgenden sind einige Beispiele für die Datenelement Definitionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="05d36-148">The following are a few examples of the data item definitions.</span></span>


```XML
<!-- The data item is an 8-bit integer -->
<data name="binaryChar" inType="win:UInt8">
 
<!-- The data item is a single ANSI character -->
<data name="ansiChar" inType="win:UInt8" outtype="xs:string">
 
<!-- The data item is a single Unicode character -->
<data name="unicodeChar" inType="win:UInt16" outtype="xs:string">
 
<!-- The data item is an IP address that is rendered as a dot separated list of interger values -->
<data name="ipAddress" inType="win:UInt32" outtype="win:IPv4">
 
<!-- The data item is a Boolean value -->
<data name="success" inType="win:boolean">
 
<!-- The data item is a null-terminated ANSI string -->
<data name="string" inType="win:AnsiString"> 

<!-- The data item is a fixed length ANSI string -->
<data name="string" inType="win:AnsiString" length="42"> 
 
<!-- The data item is a fixed length array of null-terminated ANSI strings -->
<data name="strings" inType="win:AnsiString" count="20">
 
<!-- The data item is a fixed length array of fixed length ANSI strings -->
<data name="strings" inType="win:AnsiString" length="42" count="20">
 
<!-- The data item is a variable length array of same sized ANSI strings -->
<data name="stringLength" inType="win:UInt16">
<data name="arrayCount" inType="win:Uint16">
<data name="strings" inType="win:AnsiString" length="stringLength" count="arrayCount"> 
 
<!-- For binary data, you must specify the size.
<!-- The data item is a fixed length array of fixed length binary blobs -->
<data name="blobs" inType="win:Binary" length="42" count="20">

<!-- The data item is a fixed length binary blob -->
<data name="blob" inType="win:Binary" length="42">

<!-- The following are illegal binary data definitions -->
<!-- This definition is illegal because no length is specified -->
<data name="blob" inType="win:Binary"> 
 
<!-- This definition is illegal because you cannot determine the length of each binary blob -->
<data name="blob" inType="win:Binary" count="20"> 
 
<!-- The data item is a variable length array of structures. Each structure -->
<!-- contains an array of same sized ANSI strings --> 
<data name="arrayStructCount" inType="win:UInt16">
<struct name="countedStrings" count="arrayStructCount">
      <data name="stringLength" inType="win:UInt16">
      <data name="string" inType="win:AnsiString" length="stringLength">
</struct>
 
<!-- The data item is a time stamp that is rendered in 100ns units -->
<data name="timestamp" inType="win:UInt32" outType="win:ETWTIME">

<!-- The data item is a fixed length array of integers --> 
<data name="integers" inType="win:UInt32" count="20">

<!-- The data item is a variable length array of integers -->
<data name="arrayCount" inType="win:UInt16"> 
<data name="integers" inType="win:UInt32" count="arrayCount"> 

<!-- The following is illegal because you cannot assign a length value to a data type of a known size -->
<data name="integer" inType="win:UInt32" length="42">
```



## <a name="requirements"></a><span data-ttu-id="05d36-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05d36-149">Requirements</span></span>



| <span data-ttu-id="05d36-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05d36-150">Requirement</span></span> | <span data-ttu-id="05d36-151">Wert</span><span class="sxs-lookup"><span data-stu-id="05d36-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05d36-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05d36-152">Minimum supported client</span></span><br/> | <span data-ttu-id="05d36-153">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05d36-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="05d36-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05d36-154">Minimum supported server</span></span><br/> | <span data-ttu-id="05d36-155">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05d36-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





