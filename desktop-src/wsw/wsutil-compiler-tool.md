---
title: Wsutil-Compilertool
description: Das Windows-Webdienste-Compilertool (WsUtil.exe) unterstützt das Dienstmodell und die Serialisierung von Datentypen. Es verarbeitet WSDL-, XML-Schema-und-Richtlinien Dokumente und generiert C-Header und-Quelldateien.
ms.assetid: 7fc3f1bd-ead2-4095-9592-d2ad88d56e7a
keywords:
- Wsutil-Compilertool-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa83da50888fcf2d66fac7fb00b3a31ae2919738
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949235"
---
# <a name="wsutil-compiler-tool"></a><span data-ttu-id="b07b2-107">Wsutil-Compilertool</span><span class="sxs-lookup"><span data-stu-id="b07b2-107">WsUtil Compiler tool</span></span>

<span data-ttu-id="b07b2-108">Das Windows-Webdienste-Compilertool (WsUtil.exe) unterstützt das [Dienstmodell](service-model-layer-overview.md) und die [Serialisierung](serialization.md) von Datentypen.</span><span class="sxs-lookup"><span data-stu-id="b07b2-108">The Windows Web Services compiler tool, WsUtil.exe, supports the [service model](service-model-layer-overview.md) and [serialization](serialization.md) of data types.</span></span> <span data-ttu-id="b07b2-109">Es verarbeitet WSDL-, XML-Schema-und-Richtlinien Dokumente und generiert C-Header und-Quelldateien.</span><span class="sxs-lookup"><span data-stu-id="b07b2-109">It processes WSDL, XML schema and policy documents, and generates C headers and source files.</span></span> <span data-ttu-id="b07b2-110">Dieses Tool ähnelt dem WSDL-Compilertool für verwalteten Code, ist stattdessen jedoch auf nativen Code ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="b07b2-110">This tool is similar to WSDL compiler tool for managed code but is aimed at native code instead.</span></span>

<span data-ttu-id="b07b2-111">Zur Unterstützung des [Dienst Modells](service-model-layer-overview.md)generiert WsUtil.exe Header, die sowohl für den Client als auch für den Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b07b2-111">To support the [service model](service-model-layer-overview.md), WsUtil.exe generates headers to be used for both client and service.</span></span> <span data-ttu-id="b07b2-112">Es generiert bei Bedarf die c-Proxy Datei für die Clientseite und c-Stubdateien für die Dienst Seite.</span><span class="sxs-lookup"><span data-stu-id="b07b2-112">It generates C proxy file for the client side, and C stub files for the service side, as needed.</span></span>

<span data-ttu-id="b07b2-113">Zur Unterstützung der [Serialisierung](serialization.md)generiert der Compiler Header für Element Beschreibungen für globale Element Definitionen und alle typdefinitions Informationen in den Proxy Dateien, die von der Serialisierungs-Engine verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b07b2-113">To support [serialization](serialization.md), the compiler generates headers for element descriptions for global element definitions, and all the type definition information in the proxy files that is consumed by the serialization engine.</span></span>


<span data-ttu-id="b07b2-114">Informationen zu Befehlszeilenoptionen für die Verarbeitung von WSDL-Dateien, XML-Schema Dateien und Webdienst-Richtlinien Dateien finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b07b2-114">For command line options for processing WSDL files, XML Schema files, and web service policy files, see the following topics:</span></span>

-   [<span data-ttu-id="b07b2-115">Webdienst-Compilertool</span><span class="sxs-lookup"><span data-stu-id="b07b2-115">Web Service Compiler Tool</span></span>](web-service-compiler-tool.md)
-   [<span data-ttu-id="b07b2-116">WSDL und Dienstverträge</span><span class="sxs-lookup"><span data-stu-id="b07b2-116">WSDL and Service Contracts</span></span>](wsdl-support.md)
-   [<span data-ttu-id="b07b2-117">Unterstützung von Schemas</span><span class="sxs-lookup"><span data-stu-id="b07b2-117">Schema support</span></span>](schema-support.md)
-   [<span data-ttu-id="b07b2-118">Richtlinien Unterstützung</span><span class="sxs-lookup"><span data-stu-id="b07b2-118">Policy support</span></span>](policy-support.md)

## <a name="security"></a><span data-ttu-id="b07b2-119">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="b07b2-119">Security</span></span>

<span data-ttu-id="b07b2-120">Beachten Sie bei der Verwendung von wsutil die folgenden Probleme, und beachten Sie die entsprechenden Vorsichtsmaßnahmen:</span><span class="sxs-lookup"><span data-stu-id="b07b2-120">When you use WsUtil, be aware of the following issues and observe the appropriate precautions:</span></span>

-   <span data-ttu-id="b07b2-121">Wsutil ruft keine XML-Metadaten über das Netzwerk ab, und wsutil löst keine Import-und/oder include-Anweisungen in den eingabemetadatendateien aus.</span><span class="sxs-lookup"><span data-stu-id="b07b2-121">Wsutil does not retrieve XML metadata over the network, and wsutil does not resolve import and/or include statements in the input metadata files.</span></span> <span data-ttu-id="b07b2-122">Wsutil öffnet und liest WSDL-, XSD-und-Richtlinien Dateien.</span><span class="sxs-lookup"><span data-stu-id="b07b2-122">Wsutil opens and reads wsdl, xsd, and policy files.</span></span> <span data-ttu-id="b07b2-123">XML-Metadaten sind nicht Manipulations beständig.</span><span class="sxs-lookup"><span data-stu-id="b07b2-123">XML metadata is not tamper resistant.</span></span> <span data-ttu-id="b07b2-124">Stellen Sie sicher, dass Sie nur WSDL-, XSD-und Richtlinien Dateien verwenden, die von der vertrauenswürdigen Quelle abgerufen werden, und stellen Sie sicher, dass die Dateien vor und nach deren Verwendung manipuliert werden.</span><span class="sxs-lookup"><span data-stu-id="b07b2-124">Ensure that you only use wsdl, xsd and policy files are acquired from trusted source and make sure to protect the files from tampering before and after using them.</span></span> <span data-ttu-id="b07b2-125">Überprüfen Sie sorgfältig den Inhalt der Eingabedateien, und überprüfen Sie, ob der Inhalt der Dateien sicher für die Verwendung in der Anwendung ist.</span><span class="sxs-lookup"><span data-stu-id="b07b2-125">Carefully review the contents of the input files and validate that the contents of files are safe for use in the application.</span></span> <span data-ttu-id="b07b2-126">Wsutil.exe überprüft keine Echtheit der Metadatendateien.</span><span class="sxs-lookup"><span data-stu-id="b07b2-126">Wsutil.exe does not do any verification of authenticity of the metadata files.</span></span>
-   <span data-ttu-id="b07b2-127">Wsutil generiert Header-und Stubdateien, die nicht Manipulations beständig sind.</span><span class="sxs-lookup"><span data-stu-id="b07b2-127">Wsutil generates header and stub files, which are not tamper resistant.</span></span> <span data-ttu-id="b07b2-128">Sie müssen die richtigen zugriffszugriffsrechte für die von wsutil.exe generierten Quelldateien festlegen, um den nicht autorisierten Zugriff auf diese Dateien zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="b07b2-128">You need to set the correct level access rights on source files generated by wsutil.exe to prevent unauthoritized access to those files.</span></span> <span data-ttu-id="b07b2-129">Wsutil verwendet System. IO. StreamWriter zum Erstellen der Ausgabedateien.</span><span class="sxs-lookup"><span data-stu-id="b07b2-129">Wsutil uses System.IO.StreamWriter to create the output files.</span></span>
-   <span data-ttu-id="b07b2-130">Benutzer müssen sich bewusst sein, dass wsutil ihre lokalen Dateien überschreiben kann, und Sie sollten darauf achten, sichere Dateinamen und Verzeichnisse für Ausgabedateien mithilfe des/Out-Schalters anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b07b2-130">Users need to be aware that Wsutil can overwrite their local files, and they should be careful to specify safe file names and directories for output files using the /out switch.</span></span>
-   <span data-ttu-id="b07b2-131">Wsutil oder wsutilhelper.dll, die in wsutil.exe geladen werden, können unerwartet beendet werden oder eine große Menge an Systemressourcen verbrauchen, wenn Sie angegriffen werden oder wenn eine sehr große Menge von Eingabe Metadaten verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="b07b2-131">Wsutil or wsutilhelper.dll loaded in wsutil.exe, may terminate unexpectedly or consume large amount of system resources when under attack or in processing a very large amount of input metadata.</span></span> <span data-ttu-id="b07b2-132">Das Tool ist für die Verwendung während der Entwicklungszeit konzipiert. dieses Tool sollte nur als Entwicklungszeit Tool verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b07b2-132">The tool is designed to be used during development time only This tool should be used as a development time tool only.</span></span> <span data-ttu-id="b07b2-133">Es ist möglicherweise nicht sicher, dass Sie in der mittleren Ebene zur Verarbeitung von Richtlinien Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b07b2-133">It may not be safe for use in the middle tier to process policy information.</span></span>
-   <span data-ttu-id="b07b2-134">Wsutilhelper.dll-Hilfsprogramm-DLL wird in verwaltete wsutil.exe geladen, um Richtlinien Informationen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="b07b2-134">Wsutilhelper.dll helper DLL is loaded into managed wsutil.exe to process policy information.</span></span> <span data-ttu-id="b07b2-135">Der Benutzer sollte sicherstellen, dass im binären Pfad keine böswillige Binärdatei mit demselben Dateinamen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b07b2-135">User should make sure no malicious binary with same filename exists in the binary path.</span></span> <span data-ttu-id="b07b2-136">Ebenso sollte der Benutzer in der Buildumgebung sicherstellen, dass der binäre Pfad ordnungsgemäß eingerichtet ist, dass keine bösartige Binärdatei mit demselben "wsutil.exe"-Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b07b2-136">Similarly, user should make sure in the build environment, the binary path is setup correctly that there is no malicious binary with same "wsutil.exe" name exists.</span></span>
-   <span data-ttu-id="b07b2-137">Wsutil generiert eine SAL-Anmerkung für Vorgänge und Struktur Felder, wenn dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="b07b2-137">Wsutil generates SAL annotation for operations and structure fields when possible.</span></span> <span data-ttu-id="b07b2-138">Der Benutzer von Dateien, die von wsutil generiert wurden, sollte die mit SAL-Anmerkung angegebene Anforderung einhalten.</span><span class="sxs-lookup"><span data-stu-id="b07b2-138">User of wsutil generated files should follow the requirement specified through SAL annotation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b07b2-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b07b2-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b07b2-140">Übersicht über die Dienstmodell Ebene</span><span class="sxs-lookup"><span data-stu-id="b07b2-140">Service Model Layer Overview</span></span>](service-model-layer-overview.md)
</dt> <dt>

[<span data-ttu-id="b07b2-141">Serialisierung</span><span class="sxs-lookup"><span data-stu-id="b07b2-141">Serialization</span></span>](serialization.md)
</dt> <dt>

[<span data-ttu-id="b07b2-142">Webdienst-Compilertool</span><span class="sxs-lookup"><span data-stu-id="b07b2-142">Web Service Compiler Tool</span></span>](web-service-compiler-tool.md)
</dt> <dt>

[<span data-ttu-id="b07b2-143">WSDL-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="b07b2-143">WSDL support</span></span>](wsdl-support.md)
</dt> <dt>

[<span data-ttu-id="b07b2-144">Unterstützung von Schemas</span><span class="sxs-lookup"><span data-stu-id="b07b2-144">Schema support</span></span>](schema-support.md)
</dt> <dt>

[<span data-ttu-id="b07b2-145">Richtlinien Unterstützung</span><span class="sxs-lookup"><span data-stu-id="b07b2-145">Policy Support</span></span>](policy-support.md)
</dt> </dl>

 

 




