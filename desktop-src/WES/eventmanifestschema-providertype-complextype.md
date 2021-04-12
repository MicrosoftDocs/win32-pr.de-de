---
title: Komplexer ProviderType-Typ
description: Definiert einen Anbieter und die Metadaten, die er verwendet, um seine Ereignisse zu definieren. | Komplexer ProviderType-Typ
ms.assetid: 70199cf5-a6d0-4780-9ff1-ed083a5b49ac
keywords:
- Provider Type Complex-Typ EventLog
topic_type:
- apiref
api_name:
- ProviderType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c258b3ff48cdd2f00f632fdce770b58182a531c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353369"
---
# <a name="providertype-complex-type"></a><span data-ttu-id="a7d2e-105">Komplexer ProviderType-Typ</span><span class="sxs-lookup"><span data-stu-id="a7d2e-105">ProviderType Complex Type</span></span>

<span data-ttu-id="a7d2e-106">Definiert einen Anbieter und die Metadaten, die er verwendet, um seine Ereignisse zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-106">Defines a provider and the metadata that it uses to define its events.</span></span>

``` syntax
<xs:complexType name="ProviderType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
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
         />
        <xs:element name="keywords"
            type="KeywordListType"
         />
        <xs:element name="maps"
            type="MapType"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
         />
        <xs:element name="templates"
            type="TemplateListType"
         />
        <xs:element name="events"
            type="DefinitionType"
         />
        <xs:element name="filters"
            type="FilterListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="guid"
        type="GUIDType"
        use="required"
     />
    <xs:attribute name="resourceFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="messageFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="parameterFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="helpLink"
        type="anyURI"
        use="optional"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="required"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:attribute name="source"
        use="optional"
        default="Xml"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="Xml"
                 />
                <xs:enumeration
                    value="Wbem"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="warnOnApplicationCompatibilityError"
        type="xs:boolean"
        use="optional"
        default="false"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a7d2e-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7d2e-107">Child elements</span></span>



| <span data-ttu-id="a7d2e-108">Element</span><span class="sxs-lookup"><span data-stu-id="a7d2e-108">Element</span></span>                                                                       | <span data-ttu-id="a7d2e-109">type</span><span class="sxs-lookup"><span data-stu-id="a7d2e-109">Type</span></span>                                                                         | <span data-ttu-id="a7d2e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7d2e-110">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7d2e-111">**channels**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-111">**channels**</span></span>](eventmanifestschema-channels-providertype-element.md)         | [<span data-ttu-id="a7d2e-112">**Channelellisttype**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-112">**ChannelListType**</span></span>](eventmanifestschema-channellisttype-complextype.md)   | <span data-ttu-id="a7d2e-113">Definiert eine Liste von Kanälen, zu denen Anbieter Ereignisse protokollieren können.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-113">Defines a list of channels to which providers can log events.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="a7d2e-114">**Fall**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-114">**events**</span></span>](eventmanifestschema-events-providertype-element.md)             | [<span data-ttu-id="a7d2e-115">**DefinitionType**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-115">**DefinitionType**</span></span>](eventmanifestschema-definitiontype-complextype.md)     | <span data-ttu-id="a7d2e-116">Definiert eine Liste der Ereignis Definitionen der Ereignisse, die der Anbieter protokollieren kann.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-116">Defines a list of event definitions of the events that the provider can log.</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="a7d2e-117">**Filter**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-117">**filters**</span></span>                                                                   | [<span data-ttu-id="a7d2e-118">**Filterlisttype**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-118">**FilterListType**</span></span>](eventmanifestschema-filterlisttype-complextype.md)     | <span data-ttu-id="a7d2e-119">Definiert eine Liste von Filtern, die Ihr Anbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-119">Defines a list of filters that your provider supports.</span></span> <span data-ttu-id="a7d2e-120">Sie können die Filter wie das Level und die Schlüsselwörter verwenden, um zu bestimmen, ob Sie ein Ereignis schreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-120">You can use the filters, as you would level and keywords, to determine if you want to write an event.</span></span> <br/> <span data-ttu-id="a7d2e-121">**Windows Server 2008 und Windows Vista:** Wird bis Windows 7 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-121">**Windows Server 2008 and Windows Vista:** Not supported until Windows 7.</span></span><br/> |
| [<span data-ttu-id="a7d2e-122">**Keywords**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-122">**keywords**</span></span>](eventmanifestschema-keywords-providertype-element.md)         | [<span data-ttu-id="a7d2e-123">**Keywordlisttype**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-123">**KeywordListType**</span></span>](eventmanifestschema-keywordlisttype-complextype.md)   | <span data-ttu-id="a7d2e-124">Definiert eine Liste von Schlüsselwörtern zum Kategorisieren von Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-124">Defines a list of keywords that categorize events.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="a7d2e-125">**Grad**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-125">**levels**</span></span>](eventmanifestschema-levels-providertype-element.md)             | [<span data-ttu-id="a7d2e-126">**Levellisttype**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-126">**LevelListType**</span></span>](eventmanifestschema-levellisttype-complextype.md)       | <span data-ttu-id="a7d2e-127">Definiert eine Liste von Ebenen, die den Schweregrad eines Ereignisses angeben.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-127">Defines a list of levels that specify the severity of an event.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="a7d2e-128">**Maps**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-128">**maps**</span></span>](eventmanifestschema-maps-providertype-element.md)                 | [<span data-ttu-id="a7d2e-129">**MapType**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-129">**MapType**</span></span>](eventmanifestschema-maptype-complextype.md)                   | <span data-ttu-id="a7d2e-130">Definiert eine Liste von Name-Wert-Paaren, auf die Sie im Vorlagen Abschnitt des Manifests verweisen können.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-130">Defines a list of name/value pairs that you can reference in the template section of the manifest.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="a7d2e-131">**namedqueries**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-131">**namedQueries**</span></span>](eventmanifestschema-namedqueries-providertype-element.md) | [<span data-ttu-id="a7d2e-132">**Namedquerytype**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-132">**NamedQueryType**</span></span>](eventmanifestschema-namedquerytype-complextype.md)     | <span data-ttu-id="a7d2e-133">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-133">Not used.</span></span> <span data-ttu-id="a7d2e-134">Definiert eine Liste benannter Abfragen, die die Ereignis Meldungs Zeichenfolge nach einem Wert Abfragen und eine angegebene Aktion ausführen, sofern gefunden.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-134">Defines a list of named queries that query the event message string for a value and perform a specified action if found.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="a7d2e-135">**OpCodes**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-135">**opcodes**</span></span>](eventmanifestschema-opcodes-providertype-element.md)           | [<span data-ttu-id="a7d2e-136">**Opcodelisttype**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-136">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md)     | <span data-ttu-id="a7d2e-137">Definiert eine Liste von Opcodes, die Sie zum Gruppieren von Ereignissen innerhalb einer Aufgabe verwenden können.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-137">Defines a list of opcodes that you can use to group events within a task.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="a7d2e-138">**erfüllen**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-138">**tasks**</span></span>](eventmanifestschema-tasks-providertype-element.md)               | [<span data-ttu-id="a7d2e-139">**Tasklisttype**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-139">**TaskListType**</span></span>](eventmanifestschema-tasklisttype-complextype.md)         | <span data-ttu-id="a7d2e-140">Definiert eine Liste von Aufgaben, die ein Anbieter zum Gruppieren von Ereignissen verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-140">Defines a list of tasks that a provider can use to group events.</span></span> <span data-ttu-id="a7d2e-141">In der Regel verwenden Sie Aufgaben, um Ereignisse für ein Feature oder eine Komponente des Anbieters zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-141">Typically, you use tasks to group events for a feature or component of the provider.</span></span><br/>                                                                                              |
| [<span data-ttu-id="a7d2e-142">**betrachtet**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-142">**templates**</span></span>](eventmanifestschema-templates-providertype-element.md)       | [<span data-ttu-id="a7d2e-143">**Templatelisttype**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-143">**TemplateListType**</span></span>](eventmanifestschema-templatelisttype-complextype.md) | <span data-ttu-id="a7d2e-144">Definiert eine Liste von Vorlagen, die die Daten angeben, die in die Ereignisse eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-144">Defines a list of templates that specify the data to include with the events.</span></span><br/>                                                                                                                                                                      |



## <a name="attributes"></a><span data-ttu-id="a7d2e-145">Attributes</span><span class="sxs-lookup"><span data-stu-id="a7d2e-145">Attributes</span></span>



| <span data-ttu-id="a7d2e-146">Name</span><span class="sxs-lookup"><span data-stu-id="a7d2e-146">Name</span></span>                                | <span data-ttu-id="a7d2e-147">type</span><span class="sxs-lookup"><span data-stu-id="a7d2e-147">Type</span></span>                                                              | <span data-ttu-id="a7d2e-148">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7d2e-148">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d2e-149">guid</span><span class="sxs-lookup"><span data-stu-id="a7d2e-149">guid</span></span>                                | [<span data-ttu-id="a7d2e-150">**Guidtype**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-150">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="a7d2e-151">Eine GUID, die den Anbieter eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-151">A GUID that uniquely identifies the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="a7d2e-152">HelpLink</span><span class="sxs-lookup"><span data-stu-id="a7d2e-152">helpLink</span></span>                            | <span data-ttu-id="a7d2e-153">anyURI</span><span class="sxs-lookup"><span data-stu-id="a7d2e-153">anyURI</span></span>                                                            | <span data-ttu-id="a7d2e-154">Die URL oder der MS-Link zu Inhalt, der Informationen zu den Ereignissen bereitstellt, die der Anbieter auslöst.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-154">The URL or MS help link to content that provides information about the events that the provider raises.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a7d2e-155">message</span><span class="sxs-lookup"><span data-stu-id="a7d2e-155">message</span></span>                             | [<span data-ttu-id="a7d2e-156">**"Strauch"**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-156">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="a7d2e-157">Der lokalisierte Anzeige Name für den Anbieter.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-157">The localized display name for the provider.</span></span> <span data-ttu-id="a7d2e-158">Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) -Abschnitt des Manifests.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-158">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a7d2e-159">messagefilename</span><span class="sxs-lookup"><span data-stu-id="a7d2e-159">messageFileName</span></span>                     | [<span data-ttu-id="a7d2e-160">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-160">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="a7d2e-161">Der vollständige Pfad zu der Datei, die die lokalisierten Nachrichten Ressourcen des Anbieters enthält.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-161">The full path to the file that contains the provider's localized message resources.</span></span> <span data-ttu-id="a7d2e-162">Die Datei kann eine ausführbare Datei oder eine DLL-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-162">The file can be an executable file or DLL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="a7d2e-163">name</span><span class="sxs-lookup"><span data-stu-id="a7d2e-163">name</span></span>                                | <span data-ttu-id="a7d2e-164">anyURI</span><span class="sxs-lookup"><span data-stu-id="a7d2e-164">anyURI</span></span>                                                            | <span data-ttu-id="a7d2e-165">Der Name des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-165">The name of the provider.</span></span> <span data-ttu-id="a7d2e-166">Der Name sollte das Format *Company* - *Product* - *Component* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-166">The name should be of the form, *Company*-*Product*-*Component*.</span></span><br/> <span data-ttu-id="a7d2e-167">Der Name darf nicht länger als 255 Zeichen sein und darf die folgenden Zeichen nicht enthalten: ' > ', ' < ', ' & ', ' ', ' \| ', ' \\ ', ': ', ' ', '? ', ' \* ' oder Zeichen mit Codes, die kleiner als 31 sind.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-167">The name cannot be longer than 255 characters, and cannot contain the characters: '>', '<', '&', '"', '\|', '\\', ':', '', '?', '\*', or characters with codes less than 31.</span></span> <span data-ttu-id="a7d2e-168">Außerdem muss der Name den allgemeinen Einschränkungen für Datei-und Registrierungsschlüssel Namen folgen.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-168">In addition, the name must follow the general constraints on file and registry key names.</span></span> <span data-ttu-id="a7d2e-169">Diese Einschränkungen finden Sie unter [Benennen einer Datei](/windows/desktop/FileIO/naming-a-file)und [Größenbeschränkungen von Registrierungs Elementen](/windows/desktop/SysInfo/registry-element-size-limits).</span><span class="sxs-lookup"><span data-stu-id="a7d2e-169">These constraints can be found at [Naming a File](/windows/desktop/FileIO/naming-a-file), and [Registry Element Size Limits](/windows/desktop/SysInfo/registry-element-size-limits).</span></span><br/> |
| <span data-ttu-id="a7d2e-170">parameterfilename</span><span class="sxs-lookup"><span data-stu-id="a7d2e-170">parameterFileName</span></span>                   | [<span data-ttu-id="a7d2e-171">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-171">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="a7d2e-172">Der vollständige Pfad zu der Datei, die die Parameter-Zeichen folgen Ressourcen des Anbieters enthält.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-172">The full path to the file that contain the provider's parameter string resources.</span></span> <span data-ttu-id="a7d2e-173">Die Datei kann eine ausführbare Datei oder eine DLL-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-173">The file can be an executable file or DLL file.</span></span> <span data-ttu-id="a7d2e-174">Sie können mehr als eine durch ein Semikolon getrennte Parameterdatei angeben.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-174">You can specify more than one parameter file separated by a semicolon.</span></span> <span data-ttu-id="a7d2e-175">Die Datei wird durchsucht, wenn die Meldungs Zeichenfolge eines Ereignisses eine Parameter Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-175">The file is searched when an event's message string contains a parameter string.</span></span> <span data-ttu-id="a7d2e-176">Mit Parametern können lokalisierbare Einfügezeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="a7d2e-176">Parameters let you provide localizable insert strings.</span></span> <span data-ttu-id="a7d2e-177">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-177">See Remarks for more information.</span></span><br/>                                                                                                                                                |
| <span data-ttu-id="a7d2e-178">resourceFileName</span><span class="sxs-lookup"><span data-stu-id="a7d2e-178">resourceFileName</span></span>                    | [<span data-ttu-id="a7d2e-179">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-179">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="a7d2e-180">Der vollständige Pfad zu der Datei, die die Metadatenressourcen des Anbieters enthält.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-180">The full path to the file that contains the provider's metadata resources.</span></span> <span data-ttu-id="a7d2e-181">Die Datei kann eine ausführbare Datei oder eine DLL-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-181">The file can be an executable file or DLL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a7d2e-182">source</span><span class="sxs-lookup"><span data-stu-id="a7d2e-182">source</span></span>                              |                                                                   | <span data-ttu-id="a7d2e-183">Nur zur internen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-183">For internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="a7d2e-184">Symbol</span><span class="sxs-lookup"><span data-stu-id="a7d2e-184">symbol</span></span>                              | [<span data-ttu-id="a7d2e-185">**Csymboltype**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-185">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="a7d2e-186">Das Symbol, mit dem auf die GUID des Anbieters in der Anwendung verwiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-186">The symbol to use to reference the provider's GUID in your application.</span></span> <span data-ttu-id="a7d2e-187">Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für die GUID des Anbieters in der vom Compiler generierten Header Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-187">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the provider's GUID in the header file that the compiler generates.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a7d2e-188">warnonapplicationcompatibilityerror</span><span class="sxs-lookup"><span data-stu-id="a7d2e-188">warnOnApplicationCompatibilityError</span></span> | <span data-ttu-id="a7d2e-189">**xs:boolean**</span><span class="sxs-lookup"><span data-stu-id="a7d2e-189">**xs:boolean**</span></span>                                                    | <span data-ttu-id="a7d2e-190">Nur zur internen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-190">For internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="a7d2e-191">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7d2e-191">Remarks</span></span>

<span data-ttu-id="a7d2e-192">Der Windows-Ereignisanzeige (Eventvwr.exe) verwendet die lokalisierte Meldungs Zeichenfolge, falls verfügbar. Andernfalls wird die Zeichenfolge aus dem Name-Attribut verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-192">The Windows Event Viewer (Eventvwr.exe) will use the localized message string if available; otherwise, it uses the string from the name attribute.</span></span>

<span data-ttu-id="a7d2e-193">Die Pfade für "resourceFileName", "messagefilename" und "parameterfilename" können Umgebungsvariablen enthalten.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-193">The paths for resourceFileName, messageFileName, and parameterFileName can contain environment variables.</span></span> <span data-ttu-id="a7d2e-194">Wenn Sie eine neue Umgebungsvariable definieren, die im Pfad verwendet werden soll, müssen Sie den Computer neu starten, damit der Ereignisprotokoll Dienst die neue Variable abrufen kann. Andernfalls ist der Dienst nicht in der Lage, die Ressourcen des Anbieters zu finden.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-194">If you define a new environment variable to use in the path, you must restart the computer so that the event log service can pick up the new variable; otherwise, the service will not be able to find your provider's resources.</span></span>

<span data-ttu-id="a7d2e-195">Die Meldungs Zeichenfolge eines Ereignisses kann Einfügungs-und Parameter Zeichenfolgen enthalten</span><span class="sxs-lookup"><span data-stu-id="a7d2e-195">An event's message string can contain insertion strings and parameter strings.</span></span> <span data-ttu-id="a7d2e-196">Eine Einfügezeichenfolge hat das Format%*n*, wobei *n* ein einbasierter Index ist, der ein Datenelement aus der Daten Vorlage des Ereignisses identifiziert, das Sie in die Nachricht einfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-196">An insertion string is of the form %*n*, where *n* is a one-based index that identifies a data item from the event's data template that you want to insert into the message.</span></span> <span data-ttu-id="a7d2e-197">Eine Parameter Zeichenfolge (siehe das **parameterfilename** -Attribut) hat die Form%%*n*, wobei n der Bezeichner einer Nachricht in der Nachrichten Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="a7d2e-197">A parameter string (see the **parameterFileName** attribute) is of the form %%*n*, where n is the identifier of a message in the message table.</span></span> <span data-ttu-id="a7d2e-198">Wenn die Meldungs Zeichenfolge des Ereignisses "%1% %11 = %2% %12" enthielt und die Datenelement Werte für "%1" und "%2" jeweils 8 bzw. 2 lauten und die Parameter Zeichenfolgen für% %11 und% %12 "Quarts" bzw</span><span class="sxs-lookup"><span data-stu-id="a7d2e-198">If the event's message string contained "%1 %%11 = %2 %%12" and the data item values for %1 and %2 were 8 and 2, respectively, and the parameter strings for %%11 and %%12 were "quarts" and "gallons", respectively, the formatted string would be "8 quarts = 2 gallons".</span></span>

## <a name="requirements"></a><span data-ttu-id="a7d2e-199">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7d2e-199">Requirements</span></span>



| <span data-ttu-id="a7d2e-200">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7d2e-200">Requirement</span></span> | <span data-ttu-id="a7d2e-201">Wert</span><span class="sxs-lookup"><span data-stu-id="a7d2e-201">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a7d2e-202">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7d2e-202">Minimum supported client</span></span><br/> | <span data-ttu-id="a7d2e-203">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7d2e-203">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a7d2e-204">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7d2e-204">Minimum supported server</span></span><br/> | <span data-ttu-id="a7d2e-205">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7d2e-205">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

