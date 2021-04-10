---
title: Komplexer metadataType-Typ
description: Definiert die Metadatentypen, die Sie im Metadatenabschnitt des Manifests definieren können.
ms.assetid: 602bafe7-940e-4313-9da5-54c6aa7f60a2
keywords:
- MetadataType komplexer Typ (Ereignisprotokoll)
topic_type:
- apiref
api_name:
- MetadataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69b140a2b65d47d563fd88f49d6818efc13613f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040965"
---
# <a name="metadatatype-complex-type"></a><span data-ttu-id="35b2b-104">Komplexer metadataType-Typ</span><span class="sxs-lookup"><span data-stu-id="35b2b-104">MetadataType Complex Type</span></span>

<span data-ttu-id="35b2b-105">Definiert die Metadatentypen, die Sie im Metadatenabschnitt des Manifests definieren können.</span><span class="sxs-lookup"><span data-stu-id="35b2b-105">Defines the metadata types that you can define in the metadata section of the manifest.</span></span>

``` syntax
<xs:complexType name="MetadataType">
    <xs:sequence>
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="KeywordListType"
            minOccurs="0"
         />
        <xs:element name="types"
            type="TypeListType"
            minOccurs="0"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
            minOccurs="0"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="35b2b-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="35b2b-106">Child elements</span></span>



| <span data-ttu-id="35b2b-107">Element</span><span class="sxs-lookup"><span data-stu-id="35b2b-107">Element</span></span>                                                                       | <span data-ttu-id="35b2b-108">type</span><span class="sxs-lookup"><span data-stu-id="35b2b-108">Type</span></span>                                                                       | <span data-ttu-id="35b2b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35b2b-109">Description</span></span>                                                                                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35b2b-110">**channels**</span><span class="sxs-lookup"><span data-stu-id="35b2b-110">**channels**</span></span>](eventmanifestschema-channels-metadatatype-element.md)         | [<span data-ttu-id="35b2b-111">**Channelellisttype**</span><span class="sxs-lookup"><span data-stu-id="35b2b-111">**ChannelListType**</span></span>](eventmanifestschema-channellisttype-complextype.md) | <span data-ttu-id="35b2b-112">Definiert eine Liste von Kanälen, zu denen Anbieter Ereignisse protokollieren können.</span><span class="sxs-lookup"><span data-stu-id="35b2b-112">Defines a list of channels to which providers can log events.</span></span> <span data-ttu-id="35b2b-113">Ein Anbieter kann dann einen oder mehrere der Kanäle in seinem Manifest importieren.</span><span class="sxs-lookup"><span data-stu-id="35b2b-113">A provider can then import one or more of the channels in their manifest.</span></span><br/>               |
| [<span data-ttu-id="35b2b-114">**Keywords**</span><span class="sxs-lookup"><span data-stu-id="35b2b-114">**keywords**</span></span>](eventmanifestschema-keywords-metadatatype-element.md)         | [<span data-ttu-id="35b2b-115">**Keywordlisttype**</span><span class="sxs-lookup"><span data-stu-id="35b2b-115">**KeywordListType**</span></span>](eventmanifestschema-keywordlisttype-complextype.md) | <span data-ttu-id="35b2b-116">Definiert eine Liste von Schlüsselwörtern, die die Kategorie der vom Anbieter schreibenden Ereignisse bestimmen.</span><span class="sxs-lookup"><span data-stu-id="35b2b-116">Defines a list of keywords that determine the category of events that the provider writes.</span></span><br/>                                                            |
| [<span data-ttu-id="35b2b-117">**Grad**</span><span class="sxs-lookup"><span data-stu-id="35b2b-117">**levels**</span></span>](eventmanifestschema-levels-metadatatype-element.md)             | [<span data-ttu-id="35b2b-118">**Levellisttype**</span><span class="sxs-lookup"><span data-stu-id="35b2b-118">**LevelListType**</span></span>](eventmanifestschema-levellisttype-complextype.md)     | <span data-ttu-id="35b2b-119">Definiert eine Liste von Ebenen, die den Schweregrad eines Ereignisses angeben.</span><span class="sxs-lookup"><span data-stu-id="35b2b-119">Defines a list of levels that specify the severity of an event.</span></span><br/>                                                                                       |
| <span data-ttu-id="35b2b-120">**Nachricht**</span><span class="sxs-lookup"><span data-stu-id="35b2b-120">**message**</span></span>                                                                   |                                                                            | <span data-ttu-id="35b2b-121">Definiert eine Meldungs Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="35b2b-121">Defines a message string.</span></span><br/>                                                                                                                             |
| <span data-ttu-id="35b2b-122">**messagetable**</span><span class="sxs-lookup"><span data-stu-id="35b2b-122">**messageTable**</span></span>                                                              |                                                                            | <span data-ttu-id="35b2b-123">Definiert eine Liste von Meldungs Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="35b2b-123">Defines a list of message strings.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="35b2b-124">**namedqueries**</span><span class="sxs-lookup"><span data-stu-id="35b2b-124">**namedQueries**</span></span>](eventmanifestschema-namedqueries-metadatatype-element.md) | [<span data-ttu-id="35b2b-125">**Namedquerytype**</span><span class="sxs-lookup"><span data-stu-id="35b2b-125">**NamedQueryType**</span></span>](eventmanifestschema-namedquerytype-complextype.md)   | <span data-ttu-id="35b2b-126">Definiert eine Liste benannter Abfragen, die reguläre Ausdrücke verwenden, um Aktionen zum Suchen und ersetzen in der Meldungs Zeichenfolge eines Ereignisses auszuführen.</span><span class="sxs-lookup"><span data-stu-id="35b2b-126">Defines a list of named queries that use regular expressions to perform find and replace actions on an event's message string.</span></span><br/>                        |
| [<span data-ttu-id="35b2b-127">**OpCodes**</span><span class="sxs-lookup"><span data-stu-id="35b2b-127">**opcodes**</span></span>](eventmanifestschema-opcodes-metadatatype-element.md)           | [<span data-ttu-id="35b2b-128">**Opcodelisttype**</span><span class="sxs-lookup"><span data-stu-id="35b2b-128">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md)   | <span data-ttu-id="35b2b-129">Definiert eine Liste von Opcodes, die Sie zum Gruppieren von Ereignissen innerhalb einer Aufgabe verwenden können.</span><span class="sxs-lookup"><span data-stu-id="35b2b-129">Defines a list of opcodes that you can use to group events within a task.</span></span><br/>                                                                             |
| <span data-ttu-id="35b2b-130">**tasks**</span><span class="sxs-lookup"><span data-stu-id="35b2b-130">**tasks**</span></span>                                                                     | [<span data-ttu-id="35b2b-131">**Tasklisttype**</span><span class="sxs-lookup"><span data-stu-id="35b2b-131">**TaskListType**</span></span>](eventmanifestschema-tasklisttype-complextype.md)       | <span data-ttu-id="35b2b-132">Definiert eine Liste von Aufgaben, die ein Anbieter zum Gruppieren von Ereignissen verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="35b2b-132">Defines a list of tasks that a provider can use to group events.</span></span> <span data-ttu-id="35b2b-133">In der Regel verwenden Sie Aufgaben, um Ereignisse für ein Feature oder eine Komponente des Anbieters zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="35b2b-133">Typically, you use tasks to group events for a feature or component of the provider.</span></span><br/> |
| [<span data-ttu-id="35b2b-134">**solche**</span><span class="sxs-lookup"><span data-stu-id="35b2b-134">**types**</span></span>](eventmanifestschema-types-metadatatype-element.md)               | [<span data-ttu-id="35b2b-135">**Typelisttype**</span><span class="sxs-lookup"><span data-stu-id="35b2b-135">**TypeListType**</span></span>](eventmanifestschema-typelisttype-complextype.md)       | <span data-ttu-id="35b2b-136">Definiert eine Liste von XML-Typen.</span><span class="sxs-lookup"><span data-stu-id="35b2b-136">Defines a list of XML types.</span></span><br/>                                                                                                                          |



## <a name="attributes"></a><span data-ttu-id="35b2b-137">Attributes</span><span class="sxs-lookup"><span data-stu-id="35b2b-137">Attributes</span></span>



| <span data-ttu-id="35b2b-138">Name</span><span class="sxs-lookup"><span data-stu-id="35b2b-138">Name</span></span>    | <span data-ttu-id="35b2b-139">type</span><span class="sxs-lookup"><span data-stu-id="35b2b-139">Type</span></span>                                                              | <span data-ttu-id="35b2b-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35b2b-140">Description</span></span>                                                                                        |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35b2b-141">message</span><span class="sxs-lookup"><span data-stu-id="35b2b-141">message</span></span> | [<span data-ttu-id="35b2b-142">**"Strauch"**</span><span class="sxs-lookup"><span data-stu-id="35b2b-142">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="35b2b-143">Ein Verweis auf die lokalisierte Zeichenfolge in der Zeichen folgen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="35b2b-143">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="35b2b-144">mId</span><span class="sxs-lookup"><span data-stu-id="35b2b-144">mid</span></span>     | <span data-ttu-id="35b2b-145">xs:string</span><span class="sxs-lookup"><span data-stu-id="35b2b-145">xs:string</span></span>                                                         | <span data-ttu-id="35b2b-146">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="35b2b-146">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="35b2b-147">name</span><span class="sxs-lookup"><span data-stu-id="35b2b-147">name</span></span>    | <span data-ttu-id="35b2b-148">anyURI</span><span class="sxs-lookup"><span data-stu-id="35b2b-148">anyURI</span></span>                                                            | <span data-ttu-id="35b2b-149">Der URI der Metadatendatei.</span><span class="sxs-lookup"><span data-stu-id="35b2b-149">The URI of the meta file.</span></span> <br/>                                                              |
| <span data-ttu-id="35b2b-150">Symbol</span><span class="sxs-lookup"><span data-stu-id="35b2b-150">symbol</span></span>  | [<span data-ttu-id="35b2b-151">**Csymboltype**</span><span class="sxs-lookup"><span data-stu-id="35b2b-151">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="35b2b-152">Der symbolische Name, den der Nachrichten Compiler für diese Meldungs Zeichenfolge erstellen soll.</span><span class="sxs-lookup"><span data-stu-id="35b2b-152">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="35b2b-153">value</span><span class="sxs-lookup"><span data-stu-id="35b2b-153">value</span></span>   | [<span data-ttu-id="35b2b-154">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="35b2b-154">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="35b2b-155">Die Zahl, die als Nachrichten-ID für diese Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="35b2b-155">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="remarks"></a><span data-ttu-id="35b2b-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35b2b-156">Remarks</span></span>

<span data-ttu-id="35b2b-157">Obwohl Sie ein Manifest erstellen können, das einen Metadatenabschnitt enthält, wird es vom Dienst nicht verwendet. die einzigen Metadaten, die der Dienst erkennt, sind die Metadaten, die in der Winmeta.xml-Datei gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="35b2b-157">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="requirements"></a><span data-ttu-id="35b2b-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35b2b-158">Requirements</span></span>



| <span data-ttu-id="35b2b-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35b2b-159">Requirement</span></span> | <span data-ttu-id="35b2b-160">Wert</span><span class="sxs-lookup"><span data-stu-id="35b2b-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="35b2b-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35b2b-161">Minimum supported client</span></span><br/> | <span data-ttu-id="35b2b-162">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35b2b-162">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="35b2b-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35b2b-163">Minimum supported server</span></span><br/> | <span data-ttu-id="35b2b-164">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35b2b-164">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





