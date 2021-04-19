---
title: Komplexer StructDefinitionType-Typ
description: Definiert eine-Struktur, die ein oder mehrere Datenelemente enthält, die Sie mit dem-Ereignis einschließen möchten. | Komplexer StructDefinitionType-Typ
ms.assetid: eb6b3682-1035-472b-8027-583d43c31748
keywords:
- StructDefinitionType komplexer Typ (Ereignisprotokoll)
topic_type:
- apiref
api_name:
- StructDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 01e739077d38dec94c0a407e5779bec90369ffb9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366406"
---
# <a name="structdefinitiontype-complex-type"></a><span data-ttu-id="2cd5f-105">Komplexer StructDefinitionType-Typ</span><span class="sxs-lookup"><span data-stu-id="2cd5f-105">StructDefinitionType Complex Type</span></span>

<span data-ttu-id="2cd5f-106">Definiert eine-Struktur, die ein oder mehrere Datenelemente enthält, die Sie mit dem-Ereignis einschließen möchten.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-106">Defines a structure that includes one or more data items that you want to include with the event.</span></span>

``` syntax
<xs:complexType name="StructDefinitionType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="data"
            type="DataDefinitionType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
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
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="2cd5f-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2cd5f-107">Child elements</span></span>



| <span data-ttu-id="2cd5f-108">Element</span><span class="sxs-lookup"><span data-stu-id="2cd5f-108">Element</span></span>                                                               | <span data-ttu-id="2cd5f-109">type</span><span class="sxs-lookup"><span data-stu-id="2cd5f-109">Type</span></span>                                                                             | <span data-ttu-id="2cd5f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2cd5f-110">Description</span></span>                                                               |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="2cd5f-111">**Vorrats**</span><span class="sxs-lookup"><span data-stu-id="2cd5f-111">**data**</span></span>](eventmanifestschema-data-structdefinitiontype-element.md) | [<span data-ttu-id="2cd5f-112">**DataDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="2cd5f-112">**DataDefinitionType**</span></span>](eventmanifestschema-datadefinitiontype-complextype.md) | <span data-ttu-id="2cd5f-113">Definiert ein Datenelement, das Sie in die Struktur einschließen möchten.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-113">Defines a data item that you want to include in the structure.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="2cd5f-114">Attributes</span><span class="sxs-lookup"><span data-stu-id="2cd5f-114">Attributes</span></span>



| <span data-ttu-id="2cd5f-115">Name</span><span class="sxs-lookup"><span data-stu-id="2cd5f-115">Name</span></span>   | <span data-ttu-id="2cd5f-116">type</span><span class="sxs-lookup"><span data-stu-id="2cd5f-116">Type</span></span>                                                            | <span data-ttu-id="2cd5f-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2cd5f-117">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd5f-118">count</span><span class="sxs-lookup"><span data-stu-id="2cd5f-118">count</span></span>  | [<span data-ttu-id="2cd5f-119">**"Count Type"**</span><span class="sxs-lookup"><span data-stu-id="2cd5f-119">**CountType**</span></span>](eventmanifestschema-counttype-simpletype.md)   | <span data-ttu-id="2cd5f-120">Die Anzahl der Elemente in einem Array von-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-120">The number of elements in an array of structures.</span></span> <span data-ttu-id="2cd5f-121">Dieses Attribut gibt an, dass die Struktur ein Array von Strukturen definiert.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-121">This attribute indicates that the structure is defining an array of structures.</span></span> <span data-ttu-id="2cd5f-122">Sie können die tatsächliche Anzahl oder den Namen eines Datenelements außerhalb der Struktur angeben, die die Anzahl enthält.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-122">You can specify the actual count or the name of a data item outside of the structure that contains the count.</span></span> <br/>                               |
| <span data-ttu-id="2cd5f-123">length</span><span class="sxs-lookup"><span data-stu-id="2cd5f-123">length</span></span> | [<span data-ttu-id="2cd5f-124">**Längen-Typ**</span><span class="sxs-lookup"><span data-stu-id="2cd5f-124">**LengthType**</span></span>](eventmanifestschema-lengthtype-simpletype.md) | <span data-ttu-id="2cd5f-125">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-125">Not available.</span></span><br/> <span data-ttu-id="2cd5f-126">**Windows Server 2008 und Windows Vista:** Die Länge dieser-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-126">**Windows Server 2008 and Windows Vista:** The length of this structure, in bytes.</span></span> <span data-ttu-id="2cd5f-127">Ab Windows 7 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-127">Not available starting with Windows 7.</span></span><br/>                                                                                                                            |
| <span data-ttu-id="2cd5f-128">name</span><span class="sxs-lookup"><span data-stu-id="2cd5f-128">name</span></span>   | <span data-ttu-id="2cd5f-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2cd5f-129">string</span></span>                                                          | <span data-ttu-id="2cd5f-130">Der Name der-Struktur.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-130">The name to the structure.</span></span> <span data-ttu-id="2cd5f-131">Sie können den Namen verwenden, um auf das Datenelement in Ihrem XML-Fragment zu verweisen, wenn Sie einen [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) -Abschnitt in ihrer Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-131">You can use the name to reference the data item in your XML fragment if you specify a [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) section in your template.</span></span><br/> <span data-ttu-id="2cd5f-132">**Windows Vista:** Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-132">**Windows Vista:** This attribute is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2cd5f-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cd5f-133">Remarks</span></span>

<span data-ttu-id="2cd5f-134">Anbieter schreiben die Struktur als BLOB und nicht als einzelne Member der Struktur.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-134">Providers write the structure as a blob and not as individual members of the structure.</span></span> <span data-ttu-id="2cd5f-135">Wenn die C-Struktur, die Sie schreiben, Zeiger enthält (z. b. ein Zeiger vom Typ LPWSTR), enthalten die Ereignisdaten den Zeiger Wert, nicht die dereferenzierten Daten.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-135">If the C structure that you are writing contains pointers (for example, a pointer of type LPWSTR), the event data will contain the pointer value, not the dereferenced data.</span></span>

<span data-ttu-id="2cd5f-136">Strukturen sollten nicht verwendet werden, stattdessen sollten Sie für jedes Elementdaten Elemente definieren und diese separat schreiben.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-136">You should not use structures but instead should define data items for each member and write them separately.</span></span> <span data-ttu-id="2cd5f-137">Wenn Sie sich dafür entscheiden, die Struktur zu verwenden, sollte die Struktur nur ganzzahlige Typen enthalten, und Sie müssen sicherstellen, dass die Elemente der Struktur an einer 8-Byte-Grenze ausgerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-137">If you decide to use structure, the structure should contain only integral types and you must ensure that the members of the structure align to an 8-byte boundary.</span></span> <span data-ttu-id="2cd5f-138">Wenn Sie dies nicht tun, erhalten Sie wahrscheinlich Ausrichtungsfehler, wenn Sie versuchen, auf die Daten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-138">If you do not, you will likely receive alignment errors when you try to access the data.</span></span> <span data-ttu-id="2cd5f-139">Verwenden Sie die \# pragma pack ()-Direktive, um die Ausrichtung an einer 8-Byte-Grenze zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-139">Consider using the \#pragma pack() directive to force alignment on an 8-byte boundary.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cd5f-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2cd5f-140">Requirements</span></span>



| <span data-ttu-id="2cd5f-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2cd5f-141">Requirement</span></span> | <span data-ttu-id="2cd5f-142">Wert</span><span class="sxs-lookup"><span data-stu-id="2cd5f-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2cd5f-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2cd5f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="2cd5f-144">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2cd5f-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2cd5f-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2cd5f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="2cd5f-146">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2cd5f-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





