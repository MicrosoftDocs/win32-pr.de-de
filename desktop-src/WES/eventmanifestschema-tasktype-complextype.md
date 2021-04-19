---
title: Komplexer TaskType-Typ
description: Definiert eine Komponente oder eine Unterkomponente einer Anwendung. | Komplexer TaskType-Typ
ms.assetid: d117636d-6363-43b6-ac5a-52234ac7c729
keywords:
- TaskType komplexer Typ EventLog
topic_type:
- apiref
api_name:
- TaskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccad6813624d0a27a093ff4baa7fc8b9a6aa8b14
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106353693"
---
# <a name="tasktype-complex-type"></a><span data-ttu-id="68c49-105">Komplexer TaskType-Typ</span><span class="sxs-lookup"><span data-stu-id="68c49-105">TaskType Complex Type</span></span>

<span data-ttu-id="68c49-106">Definiert eine Komponente oder eine Unterkomponente einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="68c49-106">Defines a component or subcomponent of an application.</span></span>

``` syntax
<xs:complexType name="TaskType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt16Type"
        use="required"
     />
    <xs:attribute name="eventGUID"
        type="GUIDType"
        use="optional"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="68c49-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68c49-107">Child elements</span></span>



| <span data-ttu-id="68c49-108">Element</span><span class="sxs-lookup"><span data-stu-id="68c49-108">Element</span></span>                                                         | <span data-ttu-id="68c49-109">type</span><span class="sxs-lookup"><span data-stu-id="68c49-109">Type</span></span>                                                                     | <span data-ttu-id="68c49-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="68c49-110">Description</span></span>                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68c49-111">**OpCodes**</span><span class="sxs-lookup"><span data-stu-id="68c49-111">**opcodes**</span></span>](eventmanifestschema-opcodes-tasktype-element.md) | [<span data-ttu-id="68c49-112">**Opcodelisttype**</span><span class="sxs-lookup"><span data-stu-id="68c49-112">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md) | <span data-ttu-id="68c49-113">Definiert eine Liste von aufgabenspezifischen OpCodes.</span><span class="sxs-lookup"><span data-stu-id="68c49-113">Defines a list of task-specific opcodes.</span></span> <span data-ttu-id="68c49-114">Die in Winmeta.xml definierten opcodewerte können nicht für aufgabenspezifische Opcodes verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="68c49-114">You cannot use the opcode values defined in Winmeta.xml for task-specific opcodes.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="68c49-115">Attributes</span><span class="sxs-lookup"><span data-stu-id="68c49-115">Attributes</span></span>



| <span data-ttu-id="68c49-116">Name</span><span class="sxs-lookup"><span data-stu-id="68c49-116">Name</span></span>      | <span data-ttu-id="68c49-117">type</span><span class="sxs-lookup"><span data-stu-id="68c49-117">Type</span></span>                                                              | <span data-ttu-id="68c49-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="68c49-118">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68c49-119">eventguid</span><span class="sxs-lookup"><span data-stu-id="68c49-119">eventGUID</span></span> | [<span data-ttu-id="68c49-120">**Guidtype**</span><span class="sxs-lookup"><span data-stu-id="68c49-120">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="68c49-121">Eine Globally Unique Identifier im Registrierungs Format, die die Aufgabe identifiziert.</span><span class="sxs-lookup"><span data-stu-id="68c49-121">A globally unique identifier, in Registry format, that identifies the task.</span></span> <span data-ttu-id="68c49-122">Dieses Attribut ist erforderlich, wenn Sie das-MOF-Nachrichten Compiler-Argument verwenden, um eine MOF-Klasse für die Unterstützung von downlevels zu generieren.</span><span class="sxs-lookup"><span data-stu-id="68c49-122">This attribute is required if you use the -mof message compiler argument to generate a MOF class for downlevel support.</span></span><br/>                                                                                                   |
| <span data-ttu-id="68c49-123">message</span><span class="sxs-lookup"><span data-stu-id="68c49-123">message</span></span>   | [<span data-ttu-id="68c49-124">**"Strauch"**</span><span class="sxs-lookup"><span data-stu-id="68c49-124">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="68c49-125">Der lokalisierte Anzeige Name für die Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="68c49-125">The localized display name for the task.</span></span> <span data-ttu-id="68c49-126">Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) -Abschnitt des Manifests.</span><span class="sxs-lookup"><span data-stu-id="68c49-126">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                   |
| <span data-ttu-id="68c49-127">name</span><span class="sxs-lookup"><span data-stu-id="68c49-127">name</span></span>      | <span data-ttu-id="68c49-128">**QName**</span><span class="sxs-lookup"><span data-stu-id="68c49-128">**QName**</span></span>                                                         | <span data-ttu-id="68c49-129">Der Name der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="68c49-129">The name of the task.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="68c49-130">Symbol</span><span class="sxs-lookup"><span data-stu-id="68c49-130">symbol</span></span>    | [<span data-ttu-id="68c49-131">**Csymboltype**</span><span class="sxs-lookup"><span data-stu-id="68c49-131">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="68c49-132">Das Symbol, das verwendet werden soll, um auf die Aufgabe in Ihrer Anwendung zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="68c49-132">The symbol to use to reference the task in your application.</span></span> <span data-ttu-id="68c49-133">Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für den Task in der vom Compiler generierten Header Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="68c49-133">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the task in the header file that the compiler generates.</span></span> <span data-ttu-id="68c49-134">Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.</span><span class="sxs-lookup"><span data-stu-id="68c49-134">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="68c49-135">value</span><span class="sxs-lookup"><span data-stu-id="68c49-135">value</span></span>     | [<span data-ttu-id="68c49-136">**UInt16Type**</span><span class="sxs-lookup"><span data-stu-id="68c49-136">**UInt16Type**</span></span>](eventmanifestschema-hexint16type-simpletype.md) | <span data-ttu-id="68c49-137">Ein numerischer Wert, der diese Aufgabe innerhalb der Liste der vom Anbieter definierten Aufgaben eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="68c49-137">A numeric value that uniquely identifies this task within the list of tasks that the provider defines.</span></span> <span data-ttu-id="68c49-138">Der Wert muss zwischen 1 und 239 liegen.</span><span class="sxs-lookup"><span data-stu-id="68c49-138">The value must be in the range from 1 through 239.</span></span><br/>                                                                                                                                             |



## <a name="examples"></a><span data-ttu-id="68c49-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68c49-139">Examples</span></span>

<span data-ttu-id="68c49-140">Im folgenden Beispiel wird gezeigt, wie eine Aufgabe angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="68c49-140">The following example shows how to specify a task.</span></span>


```XML
<tasks>
  <task name="printspool:Disconnect" 
         symbol="PRINTSPOOL_TASK_DISCONNECT"
         value="0" 
         message="$(string.disconnect)"/>
 
  <task name="printspool:Connect" 
         symbol="PRINTSPOOL_TASK_CONNECT"
         value="1" 
         message="$(string.connect)">
       <opcodes>
          <opcode name="ReadRegistry" 
                  symbol="MYOPCODE_READ_REGISTRY" value="11"
                  message="$(string.ReadRegistry)"/>
       </opcodes>
   </task>
</tasks>
```



## <a name="requirements"></a><span data-ttu-id="68c49-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68c49-141">Requirements</span></span>



| <span data-ttu-id="68c49-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68c49-142">Requirement</span></span> | <span data-ttu-id="68c49-143">Wert</span><span class="sxs-lookup"><span data-stu-id="68c49-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="68c49-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68c49-144">Minimum supported client</span></span><br/> | <span data-ttu-id="68c49-145">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68c49-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="68c49-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68c49-146">Minimum supported server</span></span><br/> | <span data-ttu-id="68c49-147">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68c49-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





