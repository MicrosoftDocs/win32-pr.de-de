---
title: Schreiben eines Instrumentierungs Manifests
description: Anwendungen und DLLs verwenden ein Instrumentierungs Manifest, um die Instrumentierungs Anbieter und die Ereignisse zu identifizieren, die von den Anbietern geschrieben werden.
ms.assetid: eec9d129-acde-4302-9121-634b3fad8455
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdad802526ad177eb5daa8846535c434fff32eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390354"
---
# <a name="writing-an-instrumentation-manifest"></a><span data-ttu-id="e30b7-103">Schreiben eines Instrumentierungs Manifests</span><span class="sxs-lookup"><span data-stu-id="e30b7-103">Writing an Instrumentation Manifest</span></span>

<span data-ttu-id="e30b7-104">Anwendungen und DLLs verwenden ein Instrumentierungs Manifest, um die Instrumentierungs Anbieter und die Ereignisse zu identifizieren, die von den Anbietern geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e30b7-104">Applications and DLLs use an instrumentation manifest to identify their instrumentation providers and the events that the providers write.</span></span> <span data-ttu-id="e30b7-105">Ein Manifest ist eine XML-Datei, die die Elemente enthält, die Ihren Anbieter identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e30b7-105">A manifest is an XML file that contains the elements that identify your provider.</span></span> <span data-ttu-id="e30b7-106">Die Konvention besteht darin,. man als Erweiterung für das Manifest zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e30b7-106">The convention is to use .man as the extension for your manifest.</span></span> <span data-ttu-id="e30b7-107">Das Manifest muss der Ereignis Manifest-XSD entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e30b7-107">The manifest must conform to the event manifest XSD.</span></span> <span data-ttu-id="e30b7-108">Ausführliche Informationen zum Schema finden Sie unter [eventmanifest-Schema](eventmanifestschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="e30b7-108">For details on the schema, see [EventManifest Schema](eventmanifestschema-schema.md).</span></span>

<span data-ttu-id="e30b7-109">Bei einem Instrumentations Anbieter handelt es sich um eine beliebige Anwendung oder dll, die die Funktionen [**EventWrite-Ex**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWrite-String**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring)oder [**eventschreitetransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) zum Schreiben von Ereignissen in eine Ablauf Verfolgungs Sitzung ( [Event Tracing](/windows/desktop/ETW/event-tracing-portal) , etw) oder einen Ereignisprotokoll Kanal aufruft.</span><span class="sxs-lookup"><span data-stu-id="e30b7-109">An instrumentation provider is any application or DLL that calls the [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring), or [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) functions to write events to an [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) tracing session or an Event Log channel.</span></span> <span data-ttu-id="e30b7-110">Eine Anwendung kann einen einzelnen Instrumentierungs Anbieter definieren, der alle Ereignisse abdeckt, die geschrieben werden, oder es kann einen Anbieter für die Anwendung und einen Anbieter für jede seiner DLLs definieren.</span><span class="sxs-lookup"><span data-stu-id="e30b7-110">An application can define a single instrumentation provider that covers all events that it writes or it can define a provider for the application and a provider for each of its DLLs.</span></span> <span data-ttu-id="e30b7-111">Die Anzahl der Anbieter, die die Anwendung im Manifest definiert, hängt ausschließlich davon ab, wie die Anwendung die Ereignisse organisieren möchte, die Sie schreibt.</span><span class="sxs-lookup"><span data-stu-id="e30b7-111">The number of providers that the application defines in the manifest depends solely on how the application wants to organize the events that it writes.</span></span>

<span data-ttu-id="e30b7-112">Der Vorteil der Angabe eines Anbieters für jede DLL besteht darin, dass Sie die einzelnen Anbieter und somit die generierten Ereignisse aktivieren und deaktivieren können.</span><span class="sxs-lookup"><span data-stu-id="e30b7-112">The advantage of specifying a provider for each DLL is that you can then enable and disable the individual providers and thus the events that they generate.</span></span> <span data-ttu-id="e30b7-113">Dieser Vorteil gilt nur, wenn der Anbieter durch eine ETW-Ablauf Verfolgungs Sitzung aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="e30b7-113">This advantage applies only if the provider is enabled by an ETW tracing session.</span></span> <span data-ttu-id="e30b7-114">Alle Ereignisse, die einen Ereignisprotokoll Kanal angeben, werden immer in diesen Channel geschrieben.</span><span class="sxs-lookup"><span data-stu-id="e30b7-114">Any events that specify an event log channel are always written to that channel.</span></span>

<span data-ttu-id="e30b7-115">Das Manifest muss den Anbieter und die Ereignisse identifizieren, die es schreibt, aber die anderen Metadaten, z. b. Kanäle, Ebenen und Schlüsselwörter, sind optional. ob Sie die optionalen Metadaten definieren, hängt davon ab, wer die Ereignisse verbrauchen wird.</span><span class="sxs-lookup"><span data-stu-id="e30b7-115">The manifest must identify the provider and the events that it writes but the other metadata such as channels, levels, and keywords are optional; whether you define the optional metadata depends on who will be consuming the events.</span></span> <span data-ttu-id="e30b7-116">Wenn beispielsweise Administratoren oder Supportmitarbeiter die Ereignisse mit einem Tool wie dem Windows-Ereignisanzeige nutzen, das Ereignisse aus Ereignisprotokoll Kanälen liest, müssen Sie die Kanäle definieren, auf die die Ereignisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e30b7-116">For example, if administrators or support personnel consume the events using a tool like the Windows Event Viewer that reads events from event log channels, then you must define the channels to which the events are written.</span></span> <span data-ttu-id="e30b7-117">Wenn der Anbieter jedoch nur durch eine ETW-Ablauf Verfolgungs Sitzung aktiviert wird, müssen Sie keine Kanäle definieren.</span><span class="sxs-lookup"><span data-stu-id="e30b7-117">However, if the provider will only be enabled by an ETW tracing session, then you do not need to define channels.</span></span>

<span data-ttu-id="e30b7-118">Obwohl die Metadaten für Ebenen, Tasks, Opcodes und Schlüsselwörter optional sind, sollten Sie diese verwenden, um die Ereignisse logisch zu gruppieren oder zu Bucket.</span><span class="sxs-lookup"><span data-stu-id="e30b7-118">Although the levels, tasks, opcodes, and keywords metadata are optional, you should use them to logically group or bucket the events.</span></span> <span data-ttu-id="e30b7-119">Durch das Gruppieren der Ereignisse können die Consumer nur die Ereignisse nutzen, die von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="e30b7-119">Grouping the events helps the consumers consume only those events that are of interest.</span></span> <span data-ttu-id="e30b7-120">Der Consumer könnte beispielsweise alle Ereignisse Abfragen, bei denen die Ebene "kritisch" und das Schlüsselwort "Write" ist, oder eine Abfrage für alle Ereignisse, die von einer bestimmten Aufgabe geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="e30b7-120">For example, the consumer could query for all events where level is "critical" and keyword is "write", or query for all events written by a specific task.</span></span>

<span data-ttu-id="e30b7-121">Zusätzlich zu den Consumern, die Level und Schlüsselwörter verwenden, um bestimmte Ereignis Typen zu verarbeiten, kann eine ETW-Ablauf Verfolgungs Sitzung die Metadaten der Ebene und des Schlüssel Worts verwenden, um etw anzuweisen, die in das Ereignis Ablauf Verfolgungs Protokoll geschriebenen Ereignisse einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="e30b7-121">In addition to consumers using level and keywords to consume specific types of events, an ETW tracing session can use the level and keyword metadata to tell ETW to limit the events that are written to the event tracing log.</span></span> <span data-ttu-id="e30b7-122">Beispielsweise kann die Sitzung die Ereignisse auf Ereignisse beschränken, bei denen die Ebene "Error" oder "Critical" und das Schlüsselwort "Read" lauten.</span><span class="sxs-lookup"><span data-stu-id="e30b7-122">For example, the session could limit the events to only events where level is "error" or "critical" and keyword is "read".</span></span>

<span data-ttu-id="e30b7-123">Ein Anbieter kann Filter definieren, die eine Sitzung verwendet, um die Ereignisse auf der Grundlage von Ereignisdaten zu filtern.</span><span class="sxs-lookup"><span data-stu-id="e30b7-123">A provider can define filters that a session uses to filter the events based on event data.</span></span> <span data-ttu-id="e30b7-124">Mit den Ebenen und Schlüsselwörtern bestimmt etw, ob das Ereignis in das Protokoll geschrieben wird, aber mit Filtern. der Anbieter verwendet die Filterdaten Kriterien, um zu bestimmen, ob das Ereignis in diese Sitzung geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="e30b7-124">With level and keywords, ETW determines whether the event is written to the log but with filters, the provider uses the filter data criteria to determine whether it writes the event to that session.</span></span> <span data-ttu-id="e30b7-125">Die Filter sind nur anwendbar, wenn der Anbieter durch eine ETW-Ablauf Verfolgungs Sitzung aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="e30b7-125">The filters are applicable only when an ETW tracing session enables your provider.</span></span>

<span data-ttu-id="e30b7-126">In den folgenden Abschnitten wird gezeigt, wie die Komponenten des Manifests definiert werden:</span><span class="sxs-lookup"><span data-stu-id="e30b7-126">The following sections show how to define the components of the manifest:</span></span>

-   [<span data-ttu-id="e30b7-127">Identifizieren des Anbieters</span><span class="sxs-lookup"><span data-stu-id="e30b7-127">Identifying the provider</span></span>](identifying-the-provider.md)
-   [<span data-ttu-id="e30b7-128">Definieren der Kanäle, an die die Ereignisse geschrieben werden</span><span class="sxs-lookup"><span data-stu-id="e30b7-128">Defining the channels to where the events are written</span></span>](defining-channels.md)
-   [<span data-ttu-id="e30b7-129">Definieren der Schweregrade von Ereignissen, die vom Anbieter geschrieben werden</span><span class="sxs-lookup"><span data-stu-id="e30b7-129">Defining the severity levels of events that the provider writes</span></span>](defining-severity-levels.md)
-   [<span data-ttu-id="e30b7-130">Definieren von Aufgaben und Vorgängen, die der Anbieter ausführt</span><span class="sxs-lookup"><span data-stu-id="e30b7-130">Defining the tasks and operations that your provider performs</span></span>](defining-tasks-and-opcodes.md)
-   [<span data-ttu-id="e30b7-131">Definieren der Schlüsselwörter, mit denen die vom Anbieter Schreibvorgänge klassifiziert werden</span><span class="sxs-lookup"><span data-stu-id="e30b7-131">Defining the keywords that classify the events that the provider writes</span></span>](defining-keywords-used-to-classify-types-of-events.md)
-   [<span data-ttu-id="e30b7-132">Definieren der Filter, die der Anbieter zum Filtern der von ihm Schreibvorgänge verwendet</span><span class="sxs-lookup"><span data-stu-id="e30b7-132">Defining the filters that the provider uses to filter the events that it writes</span></span>](defining-filters.md)
-   [<span data-ttu-id="e30b7-133">Definieren von Name-Wert-Zuordnungen, auf die die Vorlagen Daten verweisen</span><span class="sxs-lookup"><span data-stu-id="e30b7-133">Defining the name/value maps that your template data references</span></span>](defining-name-value-mappings.md)
-   [<span data-ttu-id="e30b7-134">Definieren der Vorlagen, die ereignisspezifische Daten definieren</span><span class="sxs-lookup"><span data-stu-id="e30b7-134">Defining the templates that define the event-specific data</span></span>](defining-event-data-templates.md)
-   [<span data-ttu-id="e30b7-135">Definieren der vom Anbieter Schreibvorgänge</span><span class="sxs-lookup"><span data-stu-id="e30b7-135">Defining the events that the provider writes</span></span>](defining-events.md)

<span data-ttu-id="e30b7-136">Obwohl Sie ein Instrumentations Manifest manuell erstellen können, sollten Sie die Verwendung des ECManGen.exe Tools in Erwägung gezogen, das im \\ Ordner "bin" des Windows SDK enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e30b7-136">Although you can author an instrumentation manifest manually, you should consider using the ECManGen.exe tool that is included in the \\Bin folder of the Windows SDK.</span></span> <span data-ttu-id="e30b7-137">Das ECManGen.exe Tool verwendet eine GUI, die Sie durch die Erstellung eines Manifests von Grund auf neu führt, ohne dass Sie jemals XML-Tags verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="e30b7-137">The ECManGen.exe tool uses a GUI that guides you through creating a manifest from scratch without ever having to use XML tags.</span></span> <span data-ttu-id="e30b7-138">Wenn Sie die Informationen in diesem Abschnitt und im Abschnitt " [eventmanifest-Schema](eventmanifestschema-schema.md) " kennen, können Sie das Tool verwenden.</span><span class="sxs-lookup"><span data-stu-id="e30b7-138">Having knowledge of the information in this section and in the [EventManifest Schema](eventmanifestschema-schema.md) section will help when using the tool.</span></span>

<span data-ttu-id="e30b7-139">Wenn Sie Visual Studio als XML-Editor verwenden, können Sie dem Projekt das [Event Manifest](eventmanifestschema-schema.md) -Schema hinzufügen (siehe das XML-Menü), um IntelliSense, Inline Schema Validierung und andere Features zu nutzen, um das Schreiben des Manifests zu vereinfachen und zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="e30b7-139">If you use Visual Studio as your XML editor, you can add the [EventManifest](eventmanifestschema-schema.md) schema to the project (see the XML menu) to take advantage of Intellisense, inline schema validation, and other features to make writing the manifest easy and accurate.</span></span>

<span data-ttu-id="e30b7-140">Verwenden Sie nach dem Schreiben des Manifests den Nachrichten Compiler, um das Manifest zu validieren und die Ressourcen-und Header Dateien zu generieren, die Sie in Ihren Anbieter einschließen.</span><span class="sxs-lookup"><span data-stu-id="e30b7-140">After writing your manifest, use the message compiler to validate the manifest and generate the resource and header files that you include in your provider.</span></span> <span data-ttu-id="e30b7-141">Weitere Informationen finden Sie unter [Kompilieren eines Instrumentierungs Manifests](compiling-an-instrumentation-manifest.md).</span><span class="sxs-lookup"><span data-stu-id="e30b7-141">For more information, see [Compiling an Instrumentation Manifest](compiling-an-instrumentation-manifest.md).</span></span>

<span data-ttu-id="e30b7-142">Das folgende Beispiel zeigt das Gerüst eines vollständig definierten Ereignis Manifests.</span><span class="sxs-lookup"><span data-stu-id="e30b7-142">The following example shows the skeleton of a fully defined event manifest.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChannel .../>
                    <channel .../>
                </channels>
                <levels>
                    <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



 

 