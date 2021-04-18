---
title: Webdienst-Compilertool
description: Zur Unterstützung des Dienst Modells generiert wsutil.exe sowohl auf Client-als auch auf Dienst Seite zu verwendende Header. Es generiert bei Bedarf die c-Proxy Datei für die Clientseite und die c-Stub-Datei für die Dienst Seite.
ms.assetid: 1c73297d-0d3d-421c-9e19-44a6012a5c65
keywords:
- Webdienst-Compilertool-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9931f228a36832fc83d84d584a151de41f5868d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391253"
---
# <a name="web-service-compiler-tool"></a><span data-ttu-id="c821d-107">Webdienst-Compilertool</span><span class="sxs-lookup"><span data-stu-id="c821d-107">Web Service Compiler Tool</span></span>

<span data-ttu-id="c821d-108">Zur Unterstützung des Dienst Modells generiert wsutil.exe sowohl auf Client-als auch auf Dienst Seite zu verwendende Header.</span><span class="sxs-lookup"><span data-stu-id="c821d-108">To support service model, wsutil.exe generates header to be used in both client and service side.</span></span> <span data-ttu-id="c821d-109">Es generiert bei Bedarf die c-Proxy Datei für die Clientseite und die c-Stub-Datei für die Dienst Seite.</span><span class="sxs-lookup"><span data-stu-id="c821d-109">It generates C proxy file for client side, and C stub file for service side, as needed.</span></span>


<span data-ttu-id="c821d-110">Zur Unterstützung der [Serialisierung](serialization.md)generiert der Compiler Header für Element Beschreibungen für globale Element Definitionen und alle typdefinitions Informationen in der Proxy Datei, die von der Serialisierungs-Engine verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c821d-110">To support [serialization](serialization.md), the compiler generates headers for element descriptions for global element definitions, and all type definition information in proxy file to be consumed by the serialization engine.</span></span>

<span data-ttu-id="c821d-111">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="c821d-111">Usage</span></span>

<span data-ttu-id="c821d-112">**\[Schalter Optionen fürWsUtil.exe Befehls Zeilenschalter \[ \] :\]<filename>**</span><span class="sxs-lookup"><span data-stu-id="c821d-112">**WsUtil.exe \[command-line-switches \[switch-options\]:\]<filename>**</span></span>

<span data-ttu-id="c821d-113">Befehls Zeilenschalter</span><span class="sxs-lookup"><span data-stu-id="c821d-113">command-line-switches</span></span>

<span data-ttu-id="c821d-114">Gibt WsUtil.exe Compileroptionen an.</span><span class="sxs-lookup"><span data-stu-id="c821d-114">Specifies WsUtil.exe compiler options.</span></span> <span data-ttu-id="c821d-115">Schalter können in beliebiger Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c821d-115">Switches can appear in any order.</span></span> <span data-ttu-id="c821d-116">Bindestrich ("-") und Schrägstrich ("/") werden als identisch behandelt.</span><span class="sxs-lookup"><span data-stu-id="c821d-116">Dash ('-') and slash ('/') are treated as the same.</span></span>

<span data-ttu-id="c821d-117">Liste der Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="c821d-117">List of command line options</span></span>

-   <span data-ttu-id="c821d-118">@filename Gibt an, dass die Eingabedatei als Antwortdatei behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c821d-118">@filename Specifies that the input file should be treated as a response file.</span></span> <span data-ttu-id="c821d-119">Diese Option kann an beliebigen Stellen in der Argumentliste mehrmals verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c821d-119">This option can be used multiple times, in any places in the argument list.</span></span>
-   <span data-ttu-id="c821d-120">/WSDL: <filename> : <optionale \_ URL> gibt an, dass die Eingabedatei als WSDL-Datei behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c821d-120">/wsdl:<filename>:<optional\_url> Specifies that the input file should be treated as a wsdl file.</span></span> <span data-ttu-id="c821d-121">Mehrere WSDL-Eingaben sind zulässig, und alle angegebenen WSDL-Dateien werden verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c821d-121">Multiple wsdl inputs are allowed and all specified wsdl files are processed.</span></span> <span data-ttu-id="c821d-122">Die optionale \_ URL gibt den Speicherort an, von dem die Metadaten abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="c821d-122">The optional\_url specifies the location where the metadata was retrieved from.</span></span> <span data-ttu-id="c821d-123">Wenn keine optionale \_ URL angegeben ist, wird von wsutil intern eine eindeutige URL generiert.</span><span class="sxs-lookup"><span data-stu-id="c821d-123">If no optional\_url is specified, Wsutil generates a unique url internally.</span></span> <span data-ttu-id="c821d-124">Siehe auch [Richtlinien Unterstützung](policy-support.md).</span><span class="sxs-lookup"><span data-stu-id="c821d-124">See also [Policy Support](policy-support.md).</span></span>
-   <span data-ttu-id="c821d-125">/XSD: <filename> gibt an, dass der Eingabe Dateiname als Schema Datei behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c821d-125">/xsd:<filename> Specifies that the input filename should be treated as a schema file.</span></span> <span data-ttu-id="c821d-126">Mehrere XSD-Eingaben sind zulässig, und alle angegebenen Schema Dateien werden verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c821d-126">Multiple xsd inputs are allowed and all specified schema files are processed.</span></span>
-   <span data-ttu-id="c821d-127">/wsp: <filename> : <optionale \_ URL> gibt an, dass der Eingabe Dateiname als Richtlinien Metadaten behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c821d-127">/wsp:<filename>:<optional\_url> Specifies that the input filename should be treated as policy metadata.</span></span> <span data-ttu-id="c821d-128">Mehrere WSP-Eingaben sind zulässig, und alle angegebenen Richtlinien Dateien werden verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c821d-128">Multiple wsp inputs are allowed and all specified policy files are processed.</span></span> <span data-ttu-id="c821d-129">Die optionale \_ URL gibt den Speicherort an, von dem die Metadaten abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="c821d-129">The optional\_url specifies the location where the metadata was retrieved from.</span></span> <span data-ttu-id="c821d-130">Wenn keine optionale \_ URL angegeben ist, wird von wsutil intern eine eindeutige URL generiert.</span><span class="sxs-lookup"><span data-stu-id="c821d-130">If no optional\_url is specified, Wsutil generates a unique url internally.</span></span> <span data-ttu-id="c821d-131">Richtlinien Dateien werden ignoriert, wenn/nopolicy-Flag angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c821d-131">Policy files are ignored if /nopolicy flag is specified.</span></span> <span data-ttu-id="c821d-132">Siehe auch [Richtlinien Unterstützung](policy-support.md).</span><span class="sxs-lookup"><span data-stu-id="c821d-132">See also [Policy Support](policy-support.md).</span></span>
-   <span data-ttu-id="c821d-133">/nopolicy deaktivieren Sie die Richtlinien Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="c821d-133">/nopolicy Disable policy processing.</span></span>
-   <span data-ttu-id="c821d-134">/Out: <dirname> gibt den Verzeichnisnamen für Ausgabedateien an.</span><span class="sxs-lookup"><span data-stu-id="c821d-134">/out:<dirname> Specifies directory name for output files</span></span>
-   <span data-ttu-id="c821d-135">/noclient generieren Sie den Client seitigen Stub nicht.</span><span class="sxs-lookup"><span data-stu-id="c821d-135">/noclient Do not generate the client side stub.</span></span>
-   <span data-ttu-id="c821d-136">/noservice generieren Sie den Dienst seitigen Stub nicht.</span><span class="sxs-lookup"><span data-stu-id="c821d-136">/noservice Do not generate the service side stub.</span></span>
-   <span data-ttu-id="c821d-137">/Prefix: <string> die angegebene Zeichenfolge wird allen generierten bezeichchern vorangesteht.</span><span class="sxs-lookup"><span data-stu-id="c821d-137">/prefix:<string> Prepend specified string to all generated identifiers.</span></span>
-   <span data-ttu-id="c821d-138">/FullName fügt einem generierten Bezeichner den normalisierten Dateinamen voran.</span><span class="sxs-lookup"><span data-stu-id="c821d-138">/fullname Prepend normalized filename to generated identifiers.</span></span> <span data-ttu-id="c821d-139">Standardmäßig wird nur der im Attribut "Name" angegebene Name verwendet, um Bezeichner für Verwandte Beschreibungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="c821d-139">By default only name specified in "name" attribute will be used to generate identifiers for related descriptions.</span></span>
-   <span data-ttu-id="c821d-140">/String: <WS \_ String>\|<WCHAR- \*> standardmäßig generiert wsutil WCHAR \* für den XSD: String-Typ.</span><span class="sxs-lookup"><span data-stu-id="c821d-140">/string:<WS\_STRING>\|<WCHAR\*> By default, wsutil generates WCHAR\* for xsd:string type.</span></span> <span data-ttu-id="c821d-141">Die Anwendung kann dieses-Flag verwenden, um dieses Verhalten zu überschreiben, und generiert stattdessen die WS- \_ Zeichenfolge für XSD: Type.</span><span class="sxs-lookup"><span data-stu-id="c821d-141">Application can use this flag to overwrite that behavior, and generates WS\_STRING for xsd:type instead.</span></span>
-   <span data-ttu-id="c821d-142">/Help Anzeigen der Hilfe Meldung</span><span class="sxs-lookup"><span data-stu-id="c821d-142">/help Display help message</span></span>
-   <span data-ttu-id="c821d-143">/?</span><span class="sxs-lookup"><span data-stu-id="c821d-143">/?</span></span> <span data-ttu-id="c821d-144">Identisch mit/Help</span><span class="sxs-lookup"><span data-stu-id="c821d-144">Same as /help</span></span>
-   <span data-ttu-id="c821d-145">/W: x Fehler Behandlungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="c821d-145">/W:x Error handling options.</span></span> <span data-ttu-id="c821d-146">Kann "w:0-W: 4 \| WX" lauten.</span><span class="sxs-lookup"><span data-stu-id="c821d-146">Could be W:0-W:4 \| WX</span></span>
-   <span data-ttu-id="c821d-147">/nologo generieren Sie keine compilerspezifischen Informationen zur Konsolenausgabe.</span><span class="sxs-lookup"><span data-stu-id="c821d-147">/nologo Do not generate compiler specific information on console output.</span></span>
-   <span data-ttu-id="c821d-148">/nostamp generiert keine compilerspezifischen Informationen zu generierten Dateien.</span><span class="sxs-lookup"><span data-stu-id="c821d-148">/nostamp Do not generate compiler specific information on generated files.</span></span>

<span data-ttu-id="c821d-149">Standardmäßig generiert der Compiler die folgenden Dateien für die WSDL-Datei oder WSDL, die vom Metadatenaustausch zurückgegeben wurde:</span><span class="sxs-lookup"><span data-stu-id="c821d-149">By default, the compiler generates the following files for WSDL file, or WSDL returned from metadata exchange:</span></span>

-   <span data-ttu-id="c821d-150">Client Proxy ({InputFilename}. c)</span><span class="sxs-lookup"><span data-stu-id="c821d-150">Client proxy ({inputfilename}.c)</span></span>
-   <span data-ttu-id="c821d-151">Dienstub ({InputFilename}. c)</span><span class="sxs-lookup"><span data-stu-id="c821d-151">Service Stub ({inputfilename}.c)</span></span>
-   <span data-ttu-id="c821d-152">Header Datei ({InputFilename}. h)</span><span class="sxs-lookup"><span data-stu-id="c821d-152">Header file ({inputfilename}.h)</span></span>

    <span data-ttu-id="c821d-153">Der Stamm des generierten Datei namens ist der Name der Eingabedatei.</span><span class="sxs-lookup"><span data-stu-id="c821d-153">The root of the generated filename is the input file name.</span></span> <span data-ttu-id="c821d-154">Die ursprünglichen Eingabedatei Erweiterungen werden beibehalten, um den Dateinamen Konflikt für generierte Dateien zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="c821d-154">Original input file extensions are preserved to prevent file name collision for generated files.</span></span> <span data-ttu-id="c821d-155">Standardmäßig werden Client-und dienststubs in der gleichen Datei generiert, wobei ein Stub-Dienst Code nach dem Proxycode generiert wird.</span><span class="sxs-lookup"><span data-stu-id="c821d-155">By default client and service stubs are generated in the same file, with service stub code generated after the proxy code.</span></span>

    <span data-ttu-id="c821d-156">Standardmäßig generiert der Compiler die folgenden Dateien für eine XSD-Datei für das Schema, das vom Metadatenaustausch zurückgegeben wird:</span><span class="sxs-lookup"><span data-stu-id="c821d-156">By default, the compiler generates the following files for a XSD file for schema returned from metadata exchange:</span></span>

-   <span data-ttu-id="c821d-157">serialisierungsbeschreibungen ({InputFilename}. c)</span><span class="sxs-lookup"><span data-stu-id="c821d-157">serialization descriptions ({inputfilename}.c)</span></span>
-   <span data-ttu-id="c821d-158">Header Datei ({InputFilename}. h)</span><span class="sxs-lookup"><span data-stu-id="c821d-158">Header file ({inputfilename}.h)</span></span>

    <span data-ttu-id="c821d-159">Der Stamm des Datei namens ist der Dienst Name.</span><span class="sxs-lookup"><span data-stu-id="c821d-159">The root of the filename is the service name.</span></span>

<span data-ttu-id="c821d-160">Wsutil.exe generiert einen "Stempel"-Abschnitt am Anfang aller generierten Dateien, die die Compileroption, die Tool Version, die Befehlszeilenoption anwendbar usw. angeben. Dieser Abschnitt kann mithilfe der Option/nostamp deaktiviert werden, um das Vergleichen generierter Dateien zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="c821d-160">Wsutil.exe generates a "stamp" section at the beginning of all the generated files, indicating the compiler option, tool version, command line option applicable, etc. This section can be turned off by using /nostamp option to avoid noise with comparing generated files.</span></span>

<span data-ttu-id="c821d-161">Wsutil unterstützt das Herunterladen von Metadaten nicht</span><span class="sxs-lookup"><span data-stu-id="c821d-161">Wsutil does not support downloading metadata</span></span>

<span data-ttu-id="c821d-162">Der wsutil-Compiler funktioniert nur aus der lokalen Metadatendatei.</span><span class="sxs-lookup"><span data-stu-id="c821d-162">Wsutil compiler works from local metadata file only.</span></span> <span data-ttu-id="c821d-163">Das Tool unterstützt nicht das Herunterladen von Metadaten aus dem Ausführen von Webdiensten.</span><span class="sxs-lookup"><span data-stu-id="c821d-163">The tool does not support downloading metadata from running web services.</span></span> <span data-ttu-id="c821d-164">Entwickler können andere unterstützte Webdienst Tools, wie z. b. Svcutil, verwenden, um Metadaten auf den lokalen Computer herunterzuladen, die gespeicherten Dateien zu überprüfen und diese Dateien an wsutil.exe zur Kompilierung zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="c821d-164">Developers can use other supported webservice tools, like svcutil, to download metadata to local machine, inspect the saved files, and pass those files to wsutil.exe for compilation.</span></span>

<span data-ttu-id="c821d-165">Unterstützung mehrerer Eingabe-/Ausgabedateien</span><span class="sxs-lookup"><span data-stu-id="c821d-165">Multiple input/output file support</span></span>

<span data-ttu-id="c821d-166">WSDL und XML-Schema ermöglichen das einschließen/Importieren von Definitionen aus anderen Namespaces, die in anderen Speicherorten/Dateien angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c821d-166">WSDL and XML schema allows including/importing definitions from other name spaces specified in other location/files.</span></span> <span data-ttu-id="c821d-167">Wsutil unterstützt mehrere Schema-/WSDL-/richtlinieneingaben und generiert eine Gruppe von Stub/Header für jede Eingabedatei.</span><span class="sxs-lookup"><span data-stu-id="c821d-167">Wsutil supports multiple schema/wsdl/policy input, and generate one set of stub/header for each input files.</span></span> <span data-ttu-id="c821d-168">Wsutil befolgt nicht die include-und Import-Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="c821d-168">Wsutil does not follow through the include and import statements.</span></span> <span data-ttu-id="c821d-169">Stattdessen sollte die Anwendung Dateien, die alle erforderlichen Namespaces enthalten, an wsutil übergeben, sodass das Tool alle Abhängigkeiten während der Kompilierung auflösen kann.</span><span class="sxs-lookup"><span data-stu-id="c821d-169">Instead, application should pass in files containing all necessary namespaces to wsutil such that the tool can resolve all dependencies during compilation.</span></span>

<span data-ttu-id="c821d-170">**WsUtil.exe/XSD: StockQuote. xsd/WSDL: StockQuote. WSDL/WSDL: StockQuoteService. WSDL**</span><span class="sxs-lookup"><span data-stu-id="c821d-170">**WsUtil.exe /xsd:stockquote.xsd /wsdl:stockquote.wsdl /wsdl:stockquoteservice.wsdl**</span></span>

<span data-ttu-id="c821d-171">wsutil generiert drei Sätze von Ausgabedateien:</span><span class="sxs-lookup"><span data-stu-id="c821d-171">wsutil generates three sets of output files:</span></span>

-   <span data-ttu-id="c821d-172">StockQuote. xsd. c StockQuote. xsd. h</span><span class="sxs-lookup"><span data-stu-id="c821d-172">stockquote.xsd.c stockquote.xsd.h</span></span>
-   <span data-ttu-id="c821d-173">StockQuote. WSDL. c StockQuote. WSDL. h</span><span class="sxs-lookup"><span data-stu-id="c821d-173">stockquote.wsdl.c stockquote.wsdl.h</span></span>
-   <span data-ttu-id="c821d-174">StockQuoteService. WSDL. h stockquoteservices. WSDL. c</span><span class="sxs-lookup"><span data-stu-id="c821d-174">stockquoteservice.wsdl.h stockquoteservices.wsdl.c</span></span>

<span data-ttu-id="c821d-175">Format der Ausgabedatei</span><span class="sxs-lookup"><span data-stu-id="c821d-175">Output file format</span></span>

<span data-ttu-id="c821d-176">Für jede Ausgabedatei generiert wsutil extern verfügbare Definitionen in der Header Datei.</span><span class="sxs-lookup"><span data-stu-id="c821d-176">For each output file, wsutil generates externally available definitions in the header file.</span></span> <span data-ttu-id="c821d-177">Abgesehen von C-Strukturdefinitionen und Stub-Funktionsprototypen werden alle anderen Webdienst bezogenen Definitionen in einer globalen Struktur mit dem Namen mit dem normalisierten Dateinamen gekapselt.</span><span class="sxs-lookup"><span data-stu-id="c821d-177">Other than C structure definitions and stub function prototypes, all the other web services related definitions are encapsulated in a global structure named with normalized filename.</span></span>

``` syntax
typedef struct _stockquote_wsdl {
  struct {
  ... // list of WS_STRUCT_DESCRIPTION for all global complex types.
  } globalTypes;
  struct {
  ... // WS_ELEMENT_DESCRIPTION for all global elements.
  } globalElements;
  struct {
  ...
  } messages;
  struct {
  ...
  } contracts;
} _stockquote_wsdl;

EXTERN_C _stockquote_wsdl stockquote_wsdl;
```

<span data-ttu-id="c821d-178">Beachten Sie, dass nicht alle Felder für die globale Struktur generiert werden.</span><span class="sxs-lookup"><span data-stu-id="c821d-178">Notice that not all the fields are generated for the global structure.</span></span> <span data-ttu-id="c821d-179">Ein Feld der obersten Ebene wird nur generiert, wenn die zugehörigen Definitionen in der Eingabedatei angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c821d-179">A top level field is generated only when the related definitions are specified in the input file.</span></span> <span data-ttu-id="c821d-180">Beispielsweise werden keine Nachrichten-, Vorgangs-und Vertrags Felder für XSD-Dateien generiert.</span><span class="sxs-lookup"><span data-stu-id="c821d-180">For example, no message, operations, and contracts fields are generated for xsd files.</span></span>

<span data-ttu-id="c821d-181">Warn Stufen und Fehlerstufe</span><span class="sxs-lookup"><span data-stu-id="c821d-181">Warning Levels and error level</span></span>

<span data-ttu-id="c821d-182">Ähnlich wie der C-Compiler unterstützt WsUtil.exe vier Warn Stufen und eine Fehlerstufe:</span><span class="sxs-lookup"><span data-stu-id="c821d-182">Similar to C compiler, WsUtil.exe supports four warning levels and one error level:</span></span>

-   <span data-ttu-id="c821d-183">WsUtil.exe generiert Fehler mit nicht BEHEB baren Fehlern, z. b. ungültige WSDL-Dateien, ungültige Compileroptionen usw.</span><span class="sxs-lookup"><span data-stu-id="c821d-183">WsUtil.exe generates errors with unrecoverable failures, like invalid wsdl file, invalid compiler options etc.</span></span>
-   <span data-ttu-id="c821d-184">Wsutil generiert W1-Warnungen mit schwerwiegenden BEHEB baren Problemen.</span><span class="sxs-lookup"><span data-stu-id="c821d-184">WsUtil generates W1 warnings with serious recoverable issues.</span></span> <span data-ttu-id="c821d-185">Der Compiler kann fortfahren, aber der Benutzer sollte das Problem beachten.</span><span class="sxs-lookup"><span data-stu-id="c821d-185">The compiler can go on but user should be aware of the issue.</span></span> <span data-ttu-id="c821d-186">Beispielsweise wird eine Warnung mit dem Wert W1 generiert, wenn nicht unterstützte Attribute, wie z. b. einige WSDL-Facetten, in WSDL vorhanden sind, die sich nicht auf die Codegenerierung auswirken.</span><span class="sxs-lookup"><span data-stu-id="c821d-186">For example, a W1 warning will be generated if there are unsupported attributes, like some WSDL facets, in wsdl that does not affect code generation.</span></span>
-   <span data-ttu-id="c821d-187">Wsutil generiert W2-Warnungen mit weniger ernsten Problemen.</span><span class="sxs-lookup"><span data-stu-id="c821d-187">WsUtil generates W2 warnings with less serious problems.</span></span> <span data-ttu-id="c821d-188">Die Funktionalität ist nicht verloren, aber der Anwendungsentwickler möchte dies möglicherweise wissen.</span><span class="sxs-lookup"><span data-stu-id="c821d-188">There is no lost of functionality, but application developer might want to know that.</span></span> <span data-ttu-id="c821d-189">Wie Verhalten, die sich von anderen Plattformen unterscheiden können.</span><span class="sxs-lookup"><span data-stu-id="c821d-189">Like behaviors that might be different from other platforms.</span></span>
-   <span data-ttu-id="c821d-190">Wsutil generiert w3-Warnungen mit minimalen Auswirkungen auf generierten Code.</span><span class="sxs-lookup"><span data-stu-id="c821d-190">WsUtil generates W3 warnings with minimal impact on generated code.</span></span> <span data-ttu-id="c821d-191">Beispielsweise generiert wsutil.exe eine w3-Warnung, wenn sich die normalisierte Zeichenfolge von der ursprünglichen Zeichenfolge unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="c821d-191">For example, wsutil.exe generates a W3 warning when normalized string is different from original string.</span></span>
-   <span data-ttu-id="c821d-192">W4 Warning ähnelt eher "Informations Warnungen" und "wsutil Issue W4" in Fällen wie das Ignorieren von Dokumentations Attributen in WSDL.</span><span class="sxs-lookup"><span data-stu-id="c821d-192">W4 warning is more like "informational" warnings, and WsUtil issue W4 in cases like ignoring documentation attribute in WSDL.</span></span>
-   <span data-ttu-id="c821d-193">WX gibt an, dass der Compiler die Warnung als Fehler behandelt.</span><span class="sxs-lookup"><span data-stu-id="c821d-193">WX indicates the compiler treats warning as error.</span></span> <span data-ttu-id="c821d-194">Wsutil generiert beispielsweise für alle W1-Warnungen einen Fehler, wenn/W: 1/WX angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c821d-194">For example, wsutil generates error for all W1 warnings if /W:1 /WX is specified.</span></span>

<span data-ttu-id="c821d-195">/W: {N} geben Sie an, welche Warnstufe der Warnung generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c821d-195">/W:{N} specify which level of warning message should be generated.</span></span> <span data-ttu-id="c821d-196">/W: 1 bedeutet, dass Warnungen der Stufe 1 generiert werden müssen. Warnungen der Warnstufe 2 und darunter sollten maskiert und nicht vom Tool generiert werden.</span><span class="sxs-lookup"><span data-stu-id="c821d-196">/W:1 means warning level 1 warnings should be generated, and warnings of warning level 2 and below should be masked and not generated by the tool.</span></span>

## <a name="fullname"></a><span data-ttu-id="c821d-197">/fullname</span><span class="sxs-lookup"><span data-stu-id="c821d-197">/fullname</span></span>

<span data-ttu-id="c821d-198">Diese Option gibt an, dass WsUtil.exe vollständigen Namen für Bezeichner generiert, um einen potenziellen namens Konflikt zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="c821d-198">This option indicates that WsUtil.exe generates full name for identifiers to avoid potential name collision.</span></span> <span data-ttu-id="c821d-199">Beispielsweise haben wir in "Beispiel. xsd" Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c821d-199">For example, in example.xsd we have:</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:element name="SimpleStruct">
   <xs:complexType>
    <xs:sequence>
     <xs:element name="a" type="xs:int" />
     <xs:element name="b" type="xs:int" />
    </xs:sequence>
   </xs:complexType>
  </xs:element>
 </wsdl:types>
</wsdl:definitions>
```

<span data-ttu-id="c821d-200">Standardmäßig WsUtil.exe generiert:</span><span class="sxs-lookup"><span data-stu-id="c821d-200">By default WsUtil.exe generates:</span></span>

``` syntax
typedef struct SimpleStruct {
  int a;
  int b;
};
```

<span data-ttu-id="c821d-201">Wenn jedoch die/FullName-Befehlszeilenoption angegeben ist, generiert WsUtil.exe stattdessen die folgende Struktur Definition:</span><span class="sxs-lookup"><span data-stu-id="c821d-201">But if /fullname command line option is specified, WsUtil.exe generates the following structure definition instead:</span></span>

``` syntax
typedef struct exmaple_xsd_SimpleStruct {
  int a;
  int b;
};
```

## <a name="globalization"></a><span data-ttu-id="c821d-202">Globalisierung</span><span class="sxs-lookup"><span data-stu-id="c821d-202">Globalization</span></span>

<span data-ttu-id="c821d-203">Das Tool ist sprachneutral und kann in verschiedenen Sprachen lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c821d-203">The tool is language neutral and can be localized to different languages.</span></span> <span data-ttu-id="c821d-204">Alle Fehlermeldungen/Konsolenausgabe können lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c821d-204">All error messages / console output can be localized.</span></span> <span data-ttu-id="c821d-205">Die Befehlszeilenoptionen bleiben jedoch in englischer Sprache.</span><span class="sxs-lookup"><span data-stu-id="c821d-205">However, the command line options remain in English.</span></span>

## <a name="environment-variable"></a><span data-ttu-id="c821d-206">Umgebungsvariable</span><span class="sxs-lookup"><span data-stu-id="c821d-206">Environment Variable</span></span>

<span data-ttu-id="c821d-207">WsUtil.exe verwendet keine Umgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="c821d-207">WsUtil.exe does not use any environment variables.</span></span>

## <a name="platform-independent"></a><span data-ttu-id="c821d-208">Plattformunabhängig</span><span class="sxs-lookup"><span data-stu-id="c821d-208">Platform independent</span></span>

<span data-ttu-id="c821d-209">Ausgabedateien aus WsUtil.exe sind plattformunabhängig.</span><span class="sxs-lookup"><span data-stu-id="c821d-209">Output files from WsUtil.exe are platform independent.</span></span> <span data-ttu-id="c821d-210">Im Stub wurde kein Architektur abhängiger Code generiert. der C-Compiler kümmert sich um eine beliebige Architektur spezifischer.</span><span class="sxs-lookup"><span data-stu-id="c821d-210">There is no architecture dependent code generated in the stub; anything architecture specific will be taken care of by the C compiler.</span></span> <span data-ttu-id="c821d-211">Der Stub kann auf allen Plattformen verwendet werden, die wir unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c821d-211">The stub can be used in all the platforms we support.</span></span>

<span data-ttu-id="c821d-212">Eine Beschreibung der wsutil.exe Ausgabe finden Sie unter [WSDL-Unterstützung](wsdl-support.md) und unter [Stützung für Schema Unterstützung](schema-support.md) .</span><span class="sxs-lookup"><span data-stu-id="c821d-212">Description for wsutil.exe output can be found at [WSDL support](wsdl-support.md) and [Schema support](schema-support.md) part.</span></span>

 

 




