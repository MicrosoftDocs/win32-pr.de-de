---
title: Komplexer debugdatatype-Typ
description: Definiert die Daten, die für Windows-Software-Ablaufverfolgungs-präprozessorereignisse (WPP) protokolliert werden können.
ms.assetid: 75638e0f-7a26-473e-a0c4-bd8972ac171f
keywords:
- Ereignisprotokoll des komplexen debugdatatype-Typs
topic_type:
- apiref
api_name:
- DebugDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c190d3b2b0e870ac249fed03485828685d5dc770
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040033"
---
# <a name="debugdatatype-complex-type"></a><span data-ttu-id="3d10a-104">Komplexer debugdatatype-Typ</span><span class="sxs-lookup"><span data-stu-id="3d10a-104">DebugDataType Complex Type</span></span>

<span data-ttu-id="3d10a-105">Definiert die Daten, die für Windows-Software-Ablaufverfolgungs-präprozessorereignisse (WPP) protokolliert werden können.</span><span class="sxs-lookup"><span data-stu-id="3d10a-105">Defines the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span>

``` syntax
<xs:complexType name="DebugDataType">
    <xs:sequence>
        <xs:element name="SequenceNumber"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="FlagsName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="LevelName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Component"
            type="string"
         />
        <xs:element name="SubComponent"
            type="string"
            minOccurs="0"
         />
        <xs:element name="FileLine"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Function"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="Message"
            type="string"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3d10a-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3d10a-106">Child elements</span></span>



| <span data-ttu-id="3d10a-107">Element</span><span class="sxs-lookup"><span data-stu-id="3d10a-107">Element</span></span>                                                                    | <span data-ttu-id="3d10a-108">type</span><span class="sxs-lookup"><span data-stu-id="3d10a-108">Type</span></span>        | <span data-ttu-id="3d10a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d10a-109">Description</span></span>                                                                                                        |
|----------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d10a-110">**Komponente**</span><span class="sxs-lookup"><span data-stu-id="3d10a-110">**Component**</span></span>](eventschema-component-debugdatatype-element.md)           | <span data-ttu-id="3d10a-111">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3d10a-111">string</span></span>      | <span data-ttu-id="3d10a-112">Der Name der Komponente, die die Ablauf Verfolgungs Meldung protokolliert hat.</span><span class="sxs-lookup"><span data-stu-id="3d10a-112">The name of the component that logged the trace message.</span></span><br/>                                                |
| [<span data-ttu-id="3d10a-113">**FileLine**</span><span class="sxs-lookup"><span data-stu-id="3d10a-113">**FileLine**</span></span>](eventschema-fileline-debugdatatype-element.md)             | <span data-ttu-id="3d10a-114">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3d10a-114">string</span></span>      | <span data-ttu-id="3d10a-115">Der Name der Quelldatei und die Zeile in der Quelldatei, die die Ablauf Verfolgungs Meldung protokolliert hat.</span><span class="sxs-lookup"><span data-stu-id="3d10a-115">The name of the source file and the line within the source file that logged the trace message.</span></span><br/>          |
| [<span data-ttu-id="3d10a-116">**Flagsname**</span><span class="sxs-lookup"><span data-stu-id="3d10a-116">**FlagsName**</span></span>](eventschema-flagname-debugdatatype-element.md)            | <span data-ttu-id="3d10a-117">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3d10a-117">string</span></span>      | <span data-ttu-id="3d10a-118">Der Flagwert, der beim Aktivieren an den Anbieter übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="3d10a-118">The flag value passed to the provider when it was enabled.</span></span><br/>                                              |
| [<span data-ttu-id="3d10a-119">**Function**</span><span class="sxs-lookup"><span data-stu-id="3d10a-119">**Function**</span></span>](eventschema-function-debugdatatype-element.md)             | <span data-ttu-id="3d10a-120">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3d10a-120">unsignedInt</span></span> | <span data-ttu-id="3d10a-121">Der Name der Funktion, die die Ablauf Verfolgungs Meldung protokolliert hat.</span><span class="sxs-lookup"><span data-stu-id="3d10a-121">The name of the function that logged the trace message.</span></span><br/>                                                 |
| [<span data-ttu-id="3d10a-122">**LevelName**</span><span class="sxs-lookup"><span data-stu-id="3d10a-122">**LevelName**</span></span>](eventschema-levelname-debugdatatype-element.md)           | <span data-ttu-id="3d10a-123">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3d10a-123">string</span></span>      | <span data-ttu-id="3d10a-124">Der bei der Aktivierung an den Anbieter über gegebene levelwert.</span><span class="sxs-lookup"><span data-stu-id="3d10a-124">The level value passed to the provider when it was enabled.</span></span><br/>                                             |
| [<span data-ttu-id="3d10a-125">**`Message`**</span><span class="sxs-lookup"><span data-stu-id="3d10a-125">**Message**</span></span>](eventschema-message-debugdatatype-element.md)               | <span data-ttu-id="3d10a-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3d10a-126">string</span></span>      | <span data-ttu-id="3d10a-127">Die Meldungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3d10a-127">The message string.</span></span> <span data-ttu-id="3d10a-128">Der XML-Code enthält dieses Element, wenn das Feld "formattedstring" vom WPP-Ereignis angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3d10a-128">The XML contains this element if the WPP event specified the FormattedString field.</span></span><br/> |
| [<span data-ttu-id="3d10a-129">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="3d10a-129">**SequenceNumber**</span></span>](eventschema-sequencenumber-debugdatatype-element.md) | <span data-ttu-id="3d10a-130">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3d10a-130">unsignedInt</span></span> | <span data-ttu-id="3d10a-131">Die lokale oder globale Sequenznummer der Ablauf Verfolgungs Meldung.</span><span class="sxs-lookup"><span data-stu-id="3d10a-131">The local or global sequence number of the trace message.</span></span><br/>                                               |
| [<span data-ttu-id="3d10a-132">**Unterkomponente**</span><span class="sxs-lookup"><span data-stu-id="3d10a-132">**SubComponent**</span></span>](eventschema-subcomponent-debugdatatype-element.md)     | <span data-ttu-id="3d10a-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3d10a-133">string</span></span>      | <span data-ttu-id="3d10a-134">Der Name der Unterkomponente, die die Ablauf Verfolgungs Meldung protokolliert hat.</span><span class="sxs-lookup"><span data-stu-id="3d10a-134">The name of the subcomponent that logged the trace message.</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="3d10a-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d10a-135">Remarks</span></span>

<span data-ttu-id="3d10a-136">Die Elemente sind nur enthalten, wenn der Anbieter die \_ Umgebungsvariable% Trace Format Prefix% festgelegt hat \_ , um Sie einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="3d10a-136">The elements are included only if the provider set the %TRACE\_FORMAT\_PREFIX% environment variable to include them.</span></span> <span data-ttu-id="3d10a-137">Ausführliche Informationen zu diesen Elementen finden Sie unter Präfix der Ablauf Verfolgungs Meldung.</span><span class="sxs-lookup"><span data-stu-id="3d10a-137">For details on these elements, see Trace Message Prefix.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d10a-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d10a-138">Requirements</span></span>



| <span data-ttu-id="3d10a-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d10a-139">Requirement</span></span> | <span data-ttu-id="3d10a-140">Wert</span><span class="sxs-lookup"><span data-stu-id="3d10a-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3d10a-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d10a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3d10a-142">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d10a-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3d10a-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d10a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3d10a-144">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d10a-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





