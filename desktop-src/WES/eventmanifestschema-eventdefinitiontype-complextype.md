---
title: Komplexer EventDefinitionType-Typ
description: Definiert ein Ereignis, das von Ihrem Anbieter geschrieben werden kann.
ms.assetid: 09ea89c9-6618-4874-ac72-5ee19cde4040
keywords:
- EventDefinitionType komplexer Typ (Ereignisprotokoll)
topic_type:
- apiref
api_name:
- EventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b7719abea1e97cae88edd47d176e5c578d73f0b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343891"
---
# <a name="eventdefinitiontype-complex-type"></a><span data-ttu-id="6648d-104">Komplexer EventDefinitionType-Typ</span><span class="sxs-lookup"><span data-stu-id="6648d-104">EventDefinitionType Complex Type</span></span>

<span data-ttu-id="6648d-105">Definiert ein Ereignis, das von Ihrem Anbieter geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="6648d-105">Defines an event that your provider can write.</span></span>

``` syntax
<xs:complexType name="EventDefinitionType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
                use="required"
             />
            <xs:attribute name="level"
                type="QName"
                use="optional"
             />
            <xs:attribute name="template"
                type="token"
                use="optional"
             />
            <xs:attribute name="channel"
                type="token"
                use="optional"
             />
            <xs:attribute name="keywords"
                type="QNameList"
                use="optional"
             />
            <xs:attribute name="task"
                type="QName"
                use="optional"
             />
            <xs:attribute name="opcode"
                type="QName"
                use="optional"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="version"
                type="unsignedByte"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="notLogged"
                type="boolean"
                use="optional"
                default="false"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="6648d-106">Attributes</span><span class="sxs-lookup"><span data-stu-id="6648d-106">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6648d-107">Name</span><span class="sxs-lookup"><span data-stu-id="6648d-107">Name</span></span></th>
<th><span data-ttu-id="6648d-108">type</span><span class="sxs-lookup"><span data-stu-id="6648d-108">Type</span></span></th>
<th><span data-ttu-id="6648d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6648d-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6648d-110">Kanal</span><span class="sxs-lookup"><span data-stu-id="6648d-110">channel</span></span></td>
<td><span data-ttu-id="6648d-111">token</span><span class="sxs-lookup"><span data-stu-id="6648d-111">token</span></span></td>
<td><span data-ttu-id="6648d-112">Ein Bezeichner, der den Kanal identifiziert, an den das Ereignis geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="6648d-112">An identifier that identifies the channel to where the event is written.</span></span> <span data-ttu-id="6648d-113">Geben Sie einen Kanal Bezeichner für einen der Kanäle an, den Sie definiert oder importiert haben.</span><span class="sxs-lookup"><span data-stu-id="6648d-113">Specify a channel identifier of one of the channels that you defined or imported.</span></span> <span data-ttu-id="6648d-114">Wenn der Kanal keinen channelbezeichner angibt, verwenden Sie den Namen des Kanals.</span><span class="sxs-lookup"><span data-stu-id="6648d-114">If the channel does not specify a channel identifier, use the channel's name.</span></span> <span data-ttu-id="6648d-115">Ausführliche Informationen zum Definieren oder Importieren eines Kanals finden Sie unter der komplexe Typ " <a href="eventmanifestschema-channellisttype-complextype.md"><strong>channelellisttype</strong></a> ".</span><span class="sxs-lookup"><span data-stu-id="6648d-115">For details on defining or importing a channel, see the <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType</strong></a> complex type.</span></span><br/> <span data-ttu-id="6648d-116">Wenn Sie keinen Kanal angeben, wird das Ereignis nicht in einen Channel geschrieben.</span><span class="sxs-lookup"><span data-stu-id="6648d-116">If you do not specify a channel, the event is not written to a channel.</span></span> <span data-ttu-id="6648d-117">In der Regel ist der einzige Grund für die Angabe eines Kanals, dass Sie nur Ereignisse in eine ETW-Sitzung schreiben.</span><span class="sxs-lookup"><span data-stu-id="6648d-117">Typically, the only reason not to specify a channel is if you are writing events only to an ETW session.</span></span> <span data-ttu-id="6648d-118">Weitere Informationen finden Sie unter Erstellen einer ETW-Sitzung, siehe <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">Steuern von Ereignis Ablauf Verfolgungs Sitzungen</a>.</span><span class="sxs-lookup"><span data-stu-id="6648d-118">For details, see creating an ETW session, see <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">Controlling Event Tracing Sessions</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6648d-119">keywords</span><span class="sxs-lookup"><span data-stu-id="6648d-119">keywords</span></span></td>
<td><span data-ttu-id="6648d-120"><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>Qnamelist</strong></a></span><span class="sxs-lookup"><span data-stu-id="6648d-120"><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a></span></span></td>
<td><span data-ttu-id="6648d-121">Eine durch Leerzeichen getrennte Liste von Schlüsselwort Namen, die die Kategorie der Ereignisse identifizieren, zu denen dieses Ereignis gehört.</span><span class="sxs-lookup"><span data-stu-id="6648d-121">A space-separated list of keyword names that identify the category of events to which this event belongs.</span></span> <span data-ttu-id="6648d-122">Geben Sie einen Schlüsselwort Namen aus der Liste der Schlüsselwörter an, die Sie definieren.</span><span class="sxs-lookup"><span data-stu-id="6648d-122">Specify a keyword name from the list of keywords that you define.</span></span> <span data-ttu-id="6648d-123">Ausführliche Informationen zum Definieren von Schlüsselwörtern finden Sie unter der komplexe Typ " <a href="eventmanifestschema-keywordtype-complextype.md"><strong>keywordtype</strong></a> ".</span><span class="sxs-lookup"><span data-stu-id="6648d-123">For details on defining keywords, see the <a href="eventmanifestschema-keywordtype-complextype.md"><strong>KeywordType</strong></a> complex type.</span></span><br/> <span data-ttu-id="6648d-124">Wenn Sie keine Schlüsselwörter angeben, enthält der Ereignis Deskriptor eine 0 (null) für Schlüsselwörter.</span><span class="sxs-lookup"><span data-stu-id="6648d-124">If you do not specify keywords, the event descriptor will contain a zero for keywords.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6648d-125">Level</span><span class="sxs-lookup"><span data-stu-id="6648d-125">level</span></span></td>
<td><span data-ttu-id="6648d-126"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="6648d-126"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="6648d-127">Die Ebene der Ausführlichkeit, die beim Schreiben des Ereignisses verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6648d-127">The level of verbosity to use when writing the event.</span></span> <span data-ttu-id="6648d-128">Geben Sie den Namen einer Ebene an, die Sie im Manifest definiert haben, oder eine der Ebenen, die in der \Include\Winmeta.xml-Datei definiert sind, die im Windows SDK enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6648d-128">Specify the name of a level that you defined in the manifest or one of the levels defined in the \Include\Winmeta.xml file that is included in the Windows SDK.</span></span> <span data-ttu-id="6648d-129">Ausführliche Informationen zum Definieren einer Ebene finden Sie unter dem komplexen <a href="eventmanifestschema-leveltype-complextype.md"><strong>leveltype</strong></a> -Typ.</span><span class="sxs-lookup"><span data-stu-id="6648d-129">For details on defining a level, see the <a href="eventmanifestschema-leveltype-complextype.md"><strong>LevelType</strong></a> complex type.</span></span><br/> <span data-ttu-id="6648d-130">Wenn Sie keine Ebene angeben, enthält der Ereignis Deskriptor eine 0 (null) für die Ebene.</span><span class="sxs-lookup"><span data-stu-id="6648d-130">If you do not specify a level, the event descriptor will contain a zero for level.</span></span><br/> <span data-ttu-id="6648d-131">Sie müssen eine Ebene angeben, wenn der Kanaltyp, auf den das Ereignis geschrieben ist, admin ist. die Ebene muss eine der folgenden Ebenen sein, die in Winmeata.xml definiert sind:</span><span class="sxs-lookup"><span data-stu-id="6648d-131">You must specify a level if the channel type to which the event is written is Admin; the level must be one of the following levels defined in Winmeata.xml:</span></span>
<ul>
<li><span data-ttu-id="6648d-132">win:Critical</span><span class="sxs-lookup"><span data-stu-id="6648d-132">win:Critical</span></span></li>
<li><span data-ttu-id="6648d-133">win:Error</span><span class="sxs-lookup"><span data-stu-id="6648d-133">win:Error</span></span></li>
<li><span data-ttu-id="6648d-134">win:Warning</span><span class="sxs-lookup"><span data-stu-id="6648d-134">win:Warning</span></span></li>
<li><span data-ttu-id="6648d-135">win:Informational</span><span class="sxs-lookup"><span data-stu-id="6648d-135">win:Informational</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6648d-136">message</span><span class="sxs-lookup"><span data-stu-id="6648d-136">message</span></span></td>
<td><span data-ttu-id="6648d-137"><a href="eventmanifestschema-strtableref-simpletype.md"><strong>"Strauch"</strong></a></span><span class="sxs-lookup"><span data-stu-id="6648d-137"><a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a></span></span></td>
<td><span data-ttu-id="6648d-138">Die lokalisierte Meldung für das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6648d-138">The localized message for the event.</span></span> <span data-ttu-id="6648d-139">Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im <a href="eventmanifestschema-stringtable-resources-element.md"><strong>STRINGTABLE</strong></a> -Abschnitt des Manifests.</span><span class="sxs-lookup"><span data-stu-id="6648d-139">The message string references a localized string in the <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> section of the manifest.</span></span><br/> <span data-ttu-id="6648d-140">Sie müssen eine Meldung angeben, wenn der Kanaltyp, für den das Ereignis geschrieben ist, admin ist.</span><span class="sxs-lookup"><span data-stu-id="6648d-140">You must specify a message if the channel type to which the event is written is Admin.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6648d-141">nicht protokolliert</span><span class="sxs-lookup"><span data-stu-id="6648d-141">notLogged</span></span></td>
<td><span data-ttu-id="6648d-142">boolean</span><span class="sxs-lookup"><span data-stu-id="6648d-142">boolean</span></span></td>
<td><span data-ttu-id="6648d-143">Bestimmt, ob der Anbieter dieses Ereignis protokolliert.</span><span class="sxs-lookup"><span data-stu-id="6648d-143">Determines whether the provider logs this event.</span></span> <span data-ttu-id="6648d-144">Geben Sie true an, wenn der Anbieter dieses Ereignis protokolliert. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="6648d-144">Specify true if the provider logs this event; otherwise, false.</span></span> <span data-ttu-id="6648d-145">Verwenden Sie dieses Attribut, um anzugeben, dass der Anbieter dieses Ereignis nicht mehr protokolliert, anstatt das Ereignis aus dem Manifest zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="6648d-145">Use this attribute to indicate that the provider is no longer logging this event instead of removing the event from the manifest.</span></span> <span data-ttu-id="6648d-146">Durch die Beibehaltung des Ereignisses im Manifest können Consumer ältere ETL-Dateien decodieren, die das Ereignis enthalten.</span><span class="sxs-lookup"><span data-stu-id="6648d-146">Retaining the event in the manifest will let consumers decode older etl files that include the event.</span></span><br/> <span data-ttu-id="6648d-147"><strong>Windows Server 2008 und Windows Vista:</strong> Dieses Attribut wird in Versionen des Nachrichten Compilers, die vor der Windows 7-Version des Windows SDK ausgeliefert wurden, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6648d-147"><strong>Windows Server 2008 and Windows Vista:</strong> This attribute is not supported in versions of the message compiler that shipped prior to the Windows 7 version of the Windows SDK.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6648d-148">OpCode</span><span class="sxs-lookup"><span data-stu-id="6648d-148">opcode</span></span></td>
<td><span data-ttu-id="6648d-149"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="6648d-149"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="6648d-150">Der Name eines Opcodes, der einen Vorgang innerhalb der Aufgabe identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6648d-150">The name of an opcode that identifies an operation within the task.</span></span> <span data-ttu-id="6648d-151">Geben Sie den Namen eines Opcodes an, den Sie im Manifest definiert haben, oder einen der OpCodes, die in Winmeta.xml definiert sind.</span><span class="sxs-lookup"><span data-stu-id="6648d-151">Specify the name of an opcode that you defined in the manifest or one of the opcodes defined in Winmeta.xml.</span></span> <span data-ttu-id="6648d-152">Ausführliche Informationen zum Definieren eines Opcodes finden Sie unter der komplexe <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpCodeType</strong></a> -Typ.</span><span class="sxs-lookup"><span data-stu-id="6648d-152">For details on defining an opcode, see the <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpcodeType</strong></a> complex type.</span></span><br/> <span data-ttu-id="6648d-153">Wenn der Task, auf den Sie verweisen, aufgabenspezifische (lokale) Opcodes enthält, können Sie einen der aufgabenspezifischen Opcodes oder einen Opcode angeben, der auf der Anbieter Ebene (globaler OpCode) definiert ist.</span><span class="sxs-lookup"><span data-stu-id="6648d-153">If the task that you reference contains task-specific (local) opcodes, you can specify one of its task-specific opcodes or an opcode defined at the provider level (a global opcode).</span></span> <span data-ttu-id="6648d-154">Wenn Sie einen globalen Opcode angeben, darf der Wert des globalen Opcodes nicht mit einem der lokalen Opcodes für die Aufgabe identisch sein.</span><span class="sxs-lookup"><span data-stu-id="6648d-154">If you specify a global opcode, the value of the global opcode cannot be the same as one of the local opcodes for the task.</span></span><br/> <span data-ttu-id="6648d-155">Wenn Sie auf einen lokalen Opcode verweisen, muss das Task-Attribut auf die Aufgabe verweisen, zu der der lokale Opcode gehört.</span><span class="sxs-lookup"><span data-stu-id="6648d-155">If you reference a local opcode, the task attribute must reference the task to which the local opcode belongs.</span></span><br/> <span data-ttu-id="6648d-156">Wenn Sie keinen Opcode angeben, enthält der Ereignis Deskriptor für Opcode eine NULL.</span><span class="sxs-lookup"><span data-stu-id="6648d-156">If you do not specify an opcode, the event descriptor will contain a zero for opcode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6648d-157">Symbol</span><span class="sxs-lookup"><span data-stu-id="6648d-157">symbol</span></span></td>
<td><span data-ttu-id="6648d-158"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>Csymboltype</strong></a></span><span class="sxs-lookup"><span data-stu-id="6648d-158"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="6648d-159">Das Symbol, mit dem auf den Ereignis Deskriptor für dieses Ereignis in der Anwendung verwiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6648d-159">The symbol to use to reference the event descriptor for this event in your application.</span></span> <span data-ttu-id="6648d-160">Der <a href="message-compiler--mc-exe-.md"><strong>Nachrichten Compiler (MC.exe)</strong></a> verwendet das Symbol, um eine Konstante für den Ereignis Deskriptor in der vom Compiler generierten Header Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6648d-160">The <a href="message-compiler--mc-exe-.md"><strong>Message Compiler (MC.exe)</strong></a> uses the symbol to create a constant for the event descriptor in the header file that the compiler generates.</span></span> <span data-ttu-id="6648d-161">Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.</span><span class="sxs-lookup"><span data-stu-id="6648d-161">If you do not specify a symbol, the compiler generates one for you.</span></span> <span data-ttu-id="6648d-162">Sie verwenden den Deskriptor, wenn Sie die <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> -Funktion zum Schreiben des Ereignisses aufruft.</span><span class="sxs-lookup"><span data-stu-id="6648d-162">You use the descriptor when you call the <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> function to write the event.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6648d-163">task</span><span class="sxs-lookup"><span data-stu-id="6648d-163">task</span></span></td>
<td><span data-ttu-id="6648d-164"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="6648d-164"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="6648d-165">Der Name eines Tasks, der die Komponente oder Unterkomponente identifiziert, die dieses Ereignis generiert.</span><span class="sxs-lookup"><span data-stu-id="6648d-165">The name of a task that identifies the component or subcomponent that generates this event.</span></span> <span data-ttu-id="6648d-166">Geben Sie den Namen einer Aufgabe an, die Sie im Manifest definiert haben.</span><span class="sxs-lookup"><span data-stu-id="6648d-166">Specify the name of a task that you defined in the manifest.</span></span> <span data-ttu-id="6648d-167">Ausführliche Informationen zum Definieren einer Aufgabe finden Sie unter <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> Complex Type.</span><span class="sxs-lookup"><span data-stu-id="6648d-167">For details on defining a task, see the <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> complex type.</span></span><br/> <span data-ttu-id="6648d-168">Wenn Sie keine Aufgabe angeben, enthält der Ereignis Deskriptor eine NULL für den Task.</span><span class="sxs-lookup"><span data-stu-id="6648d-168">If you do not specify a task, the event descriptor will contain a zero for task.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6648d-169">Vorlage</span><span class="sxs-lookup"><span data-stu-id="6648d-169">template</span></span></td>
<td><span data-ttu-id="6648d-170">token</span><span class="sxs-lookup"><span data-stu-id="6648d-170">token</span></span></td>
<td><span data-ttu-id="6648d-171">Der Vorlagen Bezeichner der Vorlage, mit der die Datenelemente definiert werden, die in diesem Ereignis enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6648d-171">The template identifier of the template that defines the data items that this event includes.</span></span> <span data-ttu-id="6648d-172">Geben Sie den Bezeichner einer Vorlage an, die Sie im Manifest definiert haben.</span><span class="sxs-lookup"><span data-stu-id="6648d-172">Specify the identifier of a template that you defined in the manifest.</span></span> <span data-ttu-id="6648d-173">Ausführliche Informationen zum Definieren einer Vorlage finden Sie unter der komplexe Typ " <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>templateitemtype</strong></a> ".</span><span class="sxs-lookup"><span data-stu-id="6648d-173">For details on defining a template, see the <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>TemplateItemType</strong></a> complex type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6648d-174">value</span><span class="sxs-lookup"><span data-stu-id="6648d-174">value</span></span></td>
<td><span data-ttu-id="6648d-175"><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="6648d-175"><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="6648d-176">Der Ereignisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="6648d-176">The event identifier.</span></span> <span data-ttu-id="6648d-177">Der Bezeichner muss innerhalb der Liste von Ereignissen, die Sie definieren, eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="6648d-177">The identifier must be unique within the list of events that you define.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6648d-178">version</span><span class="sxs-lookup"><span data-stu-id="6648d-178">version</span></span></td>
<td><span data-ttu-id="6648d-179">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="6648d-179">unsignedByte</span></span></td>
<td><span data-ttu-id="6648d-180">Eine 1-Byte-Versionsnummer der Ereignis Definition.</span><span class="sxs-lookup"><span data-stu-id="6648d-180">A one-byte version number of the event definition.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="6648d-181">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6648d-181">Remarks</span></span>

<span data-ttu-id="6648d-182">Wenn Sie [**evtformatmessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) verwenden, um die Meldungs Zeichenfolge für das Ereignis zu formatieren (oder die Ereignisanzeige zum Anzeigen der Meldungs Zeichenfolge verwenden), kann die Meldungs Zeichenfolge Einfügungs Zeichenfolgen und alle Format Zeichenfolgen enthalten, die die Win32 **FormatMessage**</span><span class="sxs-lookup"><span data-stu-id="6648d-182">If you use [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) to format the message string for the event (or use the Event Viewer to view the message string), the message string can contain insertion strings and any of the format strings that the Win32 **FormatMessage** function supports.</span></span> <span data-ttu-id="6648d-183">Die Einfügezeichenfolgen sind auf%*n* oder%*n*! s! beschränkt.</span><span class="sxs-lookup"><span data-stu-id="6648d-183">The insertion strings are limited to %*n* or %*n*!s!</span></span> <span data-ttu-id="6648d-184">(z. b. %1), wobei *n* der einbasierte Verweis auf die Datenelemente ist, die in der-Vorlage des Ereignisses definiert sind.</span><span class="sxs-lookup"><span data-stu-id="6648d-184">(for example, %1) where *n* is the one-based reference the data items defined in the event's template.</span></span> <span data-ttu-id="6648d-185">Die Meldungs Zeichenfolge kann auch Parameter Einfügungs Zeichenfolgen im Format%%*n* (z. b .% %4) enthalten.</span><span class="sxs-lookup"><span data-stu-id="6648d-185">The message string can also contain parameter insertion strings in the form %%*n* (for example, %%4).</span></span> <span data-ttu-id="6648d-186">Die maximale Anzahl von Einfügezeichenfolgen, die die Nachricht enthalten kann, ist 100.</span><span class="sxs-lookup"><span data-stu-id="6648d-186">The maximum number of insertion strings that the message can contain is 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="6648d-187">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6648d-187">Requirements</span></span>



| <span data-ttu-id="6648d-188">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6648d-188">Requirement</span></span> | <span data-ttu-id="6648d-189">Wert</span><span class="sxs-lookup"><span data-stu-id="6648d-189">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6648d-190">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6648d-190">Minimum supported client</span></span><br/> | <span data-ttu-id="6648d-191">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6648d-191">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6648d-192">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6648d-192">Minimum supported server</span></span><br/> | <span data-ttu-id="6648d-193">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6648d-193">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

