---
title: Komplexer templateitemtype-Typ
description: Eine Vorlage, die die Daten definiert, die in einem Ereignis enthalten sein sollen. | Komplexer templateitemtype-Typ
ms.assetid: 1681af7d-03ef-47bc-bc02-ce1a9903fb44
keywords:
- "\"Templateitemtype Complex Type Event Log\""
topic_type:
- apiref
api_name:
- TemplateItemType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94ae108ceed3285fe7e57461611d94b1147d94e7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219270"
---
# <a name="templateitemtype-complex-type"></a><span data-ttu-id="bbfd2-105">Komplexer templateitemtype-Typ</span><span class="sxs-lookup"><span data-stu-id="bbfd2-105">TemplateItemType Complex Type</span></span>

<span data-ttu-id="bbfd2-106">Eine Vorlage, die die Daten definiert, die in einem Ereignis enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-106">A template that defines the data to include with an event.</span></span>

``` syntax
<xs:complexType name="TemplateItemType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:choice
            maxOccurs="unbounded"
            minOccurs="0"
        >
            <xs:element name="data"
                type="DataDefinitionType"
             />
            <xs:element name="struct"
                type="StructDefinitionType"
             />
        </xs:choice>
        <xs:element name="binary"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="name"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="UserData"
            type="XmlType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="tid"
        type="token"
        use="required"
     />
    <xs:attribute name="name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="bbfd2-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bbfd2-107">Child elements</span></span>



| <span data-ttu-id="bbfd2-108">Element</span><span class="sxs-lookup"><span data-stu-id="bbfd2-108">Element</span></span>                                                                   | <span data-ttu-id="bbfd2-109">type</span><span class="sxs-lookup"><span data-stu-id="bbfd2-109">Type</span></span>                                                                                 | <span data-ttu-id="bbfd2-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bbfd2-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbfd2-111">**ärer**</span><span class="sxs-lookup"><span data-stu-id="bbfd2-111">**binary**</span></span>](eventmanifestschema-binary-templateitemtype-element.md)     |                                                                                      | <span data-ttu-id="bbfd2-112">Nur für die interne Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-112">Reserved for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="bbfd2-113">**Vorrats**</span><span class="sxs-lookup"><span data-stu-id="bbfd2-113">**data**</span></span>](eventmanifestschema-data-templateitemtype-element.md)         | [<span data-ttu-id="bbfd2-114">**DataDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="bbfd2-114">**DataDefinitionType**</span></span>](eventmanifestschema-datadefinitiontype-complextype.md)     | <span data-ttu-id="bbfd2-115">Definiert ein Datenelement, das Sie mit dem-Ereignis einschließen möchten.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-115">Defines a data item that you want to include with the event.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="bbfd2-116">**struct**</span><span class="sxs-lookup"><span data-stu-id="bbfd2-116">**struct**</span></span>](eventmanifestschema-struct-templateitemtype-element.md)     | [<span data-ttu-id="bbfd2-117">**StructDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="bbfd2-117">**StructDefinitionType**</span></span>](eventmanifestschema-structdefinitiontype-complextype.md) | <span data-ttu-id="bbfd2-118">Definiert eine-Struktur, die ein oder mehrere Datenelemente enthält, die Sie mit dem-Ereignis einschließen möchten.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-118">Defines a structure that includes one or more data items that you want to include with the event.</span></span> <span data-ttu-id="bbfd2-119">Anbieter schreiben die Struktur als BLOB und nicht als einzelne Member der Struktur.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-119">Providers write the structure as a blob and not as individual members of the structure.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="bbfd2-120">**UserData**</span><span class="sxs-lookup"><span data-stu-id="bbfd2-120">**UserData**</span></span>](eventmanifestschema-userdata-templateitemtype-element.md) | [<span data-ttu-id="bbfd2-121">**XmlType**</span><span class="sxs-lookup"><span data-stu-id="bbfd2-121">**XmlType**</span></span>](eventmanifestschema-xmltype-complextype.md)                           | <span data-ttu-id="bbfd2-122">Ein XML-Fragment, das zum Rendering der Ereignisdaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-122">An XML fragment that is used to render the event data.</span></span> <span data-ttu-id="bbfd2-123">Wenn Sie das Fragment nicht einschließen, werden die Ereignisdaten in der Reihenfolge gerendert, in der die Datenelemente in der Vorlage definiert sind.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-123">If you do not include the fragment, the event data is rendered in the order that the data items are defined in the template.</span></span> <span data-ttu-id="bbfd2-124">Der Inhalt dieses Elements ist ein beliebiges gültiges XML-Fragment.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-124">The contents of this element is any valid XML fragment.</span></span> <span data-ttu-id="bbfd2-125">Das Fragment darf nur einen Knoten der obersten Ebene enthalten, und der Knoten der obersten Ebene muss einen eigenen Namespace angeben.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-125">The fragment must contain only one top-level node and the top-level node must specify its own namespace.</span></span> <br/> <span data-ttu-id="bbfd2-126">Wenn Sie auf ein Datenelement im Fragment verweisen möchten, legen Sie den Textkörper für einen Knoten im Fragment auf%*n* fest, wobei *n* der einbasierte Index der Datenelemente der obersten Ebene in der Liste der Datenelemente ist (Sie können nicht auf Member einer Struktur verweisen).</span><span class="sxs-lookup"><span data-stu-id="bbfd2-126">To reference a data item in the fragment, set the text body for a node in the fragment to %*n*, where *n* is the one-based index of the top-level data items in the list of data items (you cannot reference members of a structure).</span></span> <span data-ttu-id="bbfd2-127">Der Indexwert, den Sie angeben, darf nicht größer sein als die Anzahl der Datenelemente der obersten Ebene in der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-127">The index value that you specify must not be greater than the number of top-level data items in the template.</span></span><br/> <span data-ttu-id="bbfd2-128">Dieses Element folgt allen **Daten** -und **Struktur** Elementen.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-128">This element follows all **data** and **struct** elements.</span></span> <br/> |



## <a name="attributes"></a><span data-ttu-id="bbfd2-129">Attributes</span><span class="sxs-lookup"><span data-stu-id="bbfd2-129">Attributes</span></span>



| <span data-ttu-id="bbfd2-130">Name</span><span class="sxs-lookup"><span data-stu-id="bbfd2-130">Name</span></span> | <span data-ttu-id="bbfd2-131">type</span><span class="sxs-lookup"><span data-stu-id="bbfd2-131">Type</span></span>   | <span data-ttu-id="bbfd2-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bbfd2-132">Description</span></span>                                                                                                                                                                                           |
|------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbfd2-133">name</span><span class="sxs-lookup"><span data-stu-id="bbfd2-133">name</span></span> | <span data-ttu-id="bbfd2-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bbfd2-134">string</span></span> | <span data-ttu-id="bbfd2-135">Nur für die interne Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-135">Reserved for internal use only.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="bbfd2-136">name</span><span class="sxs-lookup"><span data-stu-id="bbfd2-136">name</span></span> | <span data-ttu-id="bbfd2-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bbfd2-137">string</span></span> | <span data-ttu-id="bbfd2-138">Der Name der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-138">The name of the template.</span></span><br/>                                                                                                                                                                  |
| <span data-ttu-id="bbfd2-139">tid</span><span class="sxs-lookup"><span data-stu-id="bbfd2-139">tid</span></span>  | <span data-ttu-id="bbfd2-140">token</span><span class="sxs-lookup"><span data-stu-id="bbfd2-140">token</span></span>  | <span data-ttu-id="bbfd2-141">Ein Bezeichner, der die Vorlage eindeutig in der Liste der Vorlagen identifiziert, die der Anbieter definiert.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-141">An identifier that uniquely identifies the template within the list of templates that the provider defines.</span></span> <span data-ttu-id="bbfd2-142">Verwenden Sie diesen Namen, um auf die Vorlage zu verweisen, wenn Sie die Ereignis Definition definieren.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-142">Use this name to reference the template when you define your event definition.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bbfd2-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbfd2-143">Remarks</span></span>

<span data-ttu-id="bbfd2-144">Die Vorlagen Definition muss mindestens ein untergeordnetes Daten-oder Strukturelement aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-144">The template definition must have at least one data or struct child element.</span></span> <span data-ttu-id="bbfd2-145">Der Anbieter muss die Ereignisdaten in der Reihenfolge der Datenelemente schreiben, die in der Vorlage definiert sind.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-145">The provider must write the event data in the order of the data items defined in the template.</span></span>

<span data-ttu-id="bbfd2-146">Die Größe aller Datenelemente in der Vorlage muss kleiner als 64 KB sein.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-146">The size of all the data items in the template must be less than 64 KB.</span></span>

## <a name="examples"></a><span data-ttu-id="bbfd2-147">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bbfd2-147">Examples</span></span>

<span data-ttu-id="bbfd2-148">Im folgenden Beispiel wird gezeigt, wie eine Vorlagen Definition erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-148">The following example shows how to create a template definition.</span></span>


```XML
<templates>
   <template tid="T1">
       <data name="PrinterName" intype="win:UnicodeString" />
       <UserData>
          <PrinterConnectionFailure 
              xmlns="schemas.microsoft.com/schemas/event/Microsoft.Windows.PrintSpooler/1.0.1.0/6382e26fc390d748">
              <PrinterName>%1</PrinterName>
          </PrinterConnectionFailure>
       </xml>
   </template>
</templates>
```



## <a name="requirements"></a><span data-ttu-id="bbfd2-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbfd2-149">Requirements</span></span>



| <span data-ttu-id="bbfd2-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbfd2-150">Requirement</span></span> | <span data-ttu-id="bbfd2-151">Wert</span><span class="sxs-lookup"><span data-stu-id="bbfd2-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bbfd2-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bbfd2-152">Minimum supported client</span></span><br/> | <span data-ttu-id="bbfd2-153">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bbfd2-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bbfd2-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bbfd2-154">Minimum supported server</span></span><br/> | <span data-ttu-id="bbfd2-155">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bbfd2-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





