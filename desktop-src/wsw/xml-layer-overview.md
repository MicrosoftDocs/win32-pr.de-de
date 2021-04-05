---
title: Übersicht über XML-Ebenen
description: Die XML-API in wwsapi basiert auf den XML-Reader-und XML Writer-Objekten, die das Lesen oder Schreiben von XML-Dokumenten nur vorwärts ermöglichen. Die XML-Ebene erteilt der Anwendung Vollzugriff auf den Inhalt von Nachrichten und die Steuerung.
ms.assetid: 938ca257-fbb8-4569-b791-2148abb1a5a5
keywords:
- Übersicht über die XML-Ebene Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9b5d062754adea7b48bd42a6a501ce17d0e332b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710709"
---
# <a name="xml-layer-overview"></a><span data-ttu-id="74fc0-107">Übersicht über XML-Ebenen</span><span class="sxs-lookup"><span data-stu-id="74fc0-107">XML Layer Overview</span></span>

<span data-ttu-id="74fc0-108">Die XML-API in wwsapi basiert auf den [XML-Reader](xml-reader.md) -und [XML Writer](xml-writer.md) -Objekten, die das Lesen oder Schreiben von XML-Dokumenten nur vorwärts ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="74fc0-108">The XML API in WWSAPI is based on the [XML Reader](xml-reader.md) and [XML Writer](xml-writer.md) objects, which allow reading or writing of XML documents in a forward only fashion.</span></span> <span data-ttu-id="74fc0-109">Die XML-Ebene erteilt der Anwendung Vollzugriff auf den Inhalt von Nachrichten und die Steuerung.</span><span class="sxs-lookup"><span data-stu-id="74fc0-109">The XML Layer give the application full access to and control over the content of messages.</span></span>

## <a name="encoding"></a><span data-ttu-id="74fc0-110">Codierung</span><span class="sxs-lookup"><span data-stu-id="74fc0-110">Encoding</span></span>

<span data-ttu-id="74fc0-111">Die XML-API unterstützt folgende Dokumente:</span><span class="sxs-lookup"><span data-stu-id="74fc0-111">The XML API supports documents encoded as:</span></span>

-   <span data-ttu-id="74fc0-112">Text (UTF-8, UTF-16LE, UTF-16BE)</span><span class="sxs-lookup"><span data-stu-id="74fc0-112">Text (UTF-8, UTF-16LE, UTF-16BE)</span></span>
-   <span data-ttu-id="74fc0-113">Binary</span><span class="sxs-lookup"><span data-stu-id="74fc0-113">Binary</span></span>
-   <span data-ttu-id="74fc0-114">MTOM</span><span class="sxs-lookup"><span data-stu-id="74fc0-114">MTOM</span></span>

## <a name="storage"></a><span data-ttu-id="74fc0-115">Storage</span><span class="sxs-lookup"><span data-stu-id="74fc0-115">Storage</span></span>

<span data-ttu-id="74fc0-116">Die XML-API unterstützt die Verarbeitung von Dokumenten wie:</span><span class="sxs-lookup"><span data-stu-id="74fc0-116">The XML API supports processing documents stored as:</span></span>

-   <span data-ttu-id="74fc0-117">Ein Puffer im Arbeitsspeicher codierter Bytes</span><span class="sxs-lookup"><span data-stu-id="74fc0-117">An in-memory buffer of encoded bytes</span></span>
-   <span data-ttu-id="74fc0-118">Ein Datenstrom</span><span class="sxs-lookup"><span data-stu-id="74fc0-118">A stream</span></span>
-   <span data-ttu-id="74fc0-119">Ein [XML-Puffer](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="74fc0-119">An [XML Buffer](xml-buffer.md)</span></span>

<span data-ttu-id="74fc0-120">Ein [XML-Puffer](xml-buffer.md) ist eine strukturierte Darstellung eines XML-Dokuments im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="74fc0-120">An [XML Buffer](xml-buffer.md) is a structured in-memory representation of an XML document.</span></span> <span data-ttu-id="74fc0-121">Dies ist eine effizientere Darstellung als ein als Bytes codiertes Dokument.</span><span class="sxs-lookup"><span data-stu-id="74fc0-121">This is a more efficient representation than a document encoded as bytes.</span></span> <span data-ttu-id="74fc0-122">Ein XML-Dokument, das in einem XML-Puffer gespeichert ist, kann navigiert, gelesen oder geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="74fc0-122">An XML document stored in an An XML Buffer can be navigated, read, or written.</span></span>

## <a name="io"></a><span data-ttu-id="74fc0-123">E/A</span><span class="sxs-lookup"><span data-stu-id="74fc0-123">I/O</span></span>

<span data-ttu-id="74fc0-124">Die XML-API führt niemals e/a-Vorgänge aus, sofern nicht ausdrücklich angefordert</span><span class="sxs-lookup"><span data-stu-id="74fc0-124">The XML API will never perform I/O unless specifically requested.</span></span> <span data-ttu-id="74fc0-125">Außerdem können e/a-Vorgänge auf asynchrone Weise initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="74fc0-125">Furthermore, any I/O may be initiated in an asynchronous fashion.</span></span> <span data-ttu-id="74fc0-126">Ausführliche Informationen zur asynchronen Verarbeitung mit der XML-API finden Sie unter [**wsfillreader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader) und [**wsflushwriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter) .</span><span class="sxs-lookup"><span data-stu-id="74fc0-126">See [**WsFillReader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader) and [**WsFlushWriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter) for details on asynchronous processing with the XML API.</span></span>

## <a name="processing"></a><span data-ttu-id="74fc0-127">Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="74fc0-127">Processing</span></span>

<span data-ttu-id="74fc0-128">Die XML-API verfügt über drei unterschiedliche Ebenen, auf denen das Dokument verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="74fc0-128">The XML API has three distinct levels at which the document may be processed.</span></span>

<span data-ttu-id="74fc0-129">Ein Dokument kann jeweils auf einem [**Knoten**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node) verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="74fc0-129">A document may be processed a [**node**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node) at a time.</span></span> <span data-ttu-id="74fc0-130">Dies bietet die präzisere Behandlung des XML-Inhalts und bietet eine umfassende Treue der Daten aus dem Dokument.</span><span class="sxs-lookup"><span data-stu-id="74fc0-130">This offers the most fine-grained handling of the XML content, and provides complete fidelity of data from the document.</span></span> <span data-ttu-id="74fc0-131">Auf dieser Ebene werden die Funktionen [**wslonode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode) und [**wsschreitenode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode) und [**wscopynode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode) verwendet.</span><span class="sxs-lookup"><span data-stu-id="74fc0-131">At this level, the functions [**WsReadNode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode) and [**WsWriteNode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode) and [**WsCopyNode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode) would be used.</span></span>

<span data-ttu-id="74fc0-132">Die nächste Steuerungsebene sind APIs wie [**wsread Startelements**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement), [**wsread Value**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue) und [**wsleserumdelta**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement).</span><span class="sxs-lookup"><span data-stu-id="74fc0-132">The next level of control are APIs like [**WsReadStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement), [**WsReadValue**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue) and [**WsReadEndElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement).</span></span> <span data-ttu-id="74fc0-133">Diese APIs bieten zahlreiche Überprüfungen, überspringen Leerzeichen und Kommentare und normalisieren Text und CDATA, um dem Consumer eine einfachere Ansicht des XML-Codes zu präsentieren.</span><span class="sxs-lookup"><span data-stu-id="74fc0-133">These APIs provide numerous kinds of validation, skip whitespace and comments, and normalize text and CDATA to present the consumer with a simpler view of the xml.</span></span>

<span data-ttu-id="74fc0-134">Die höchste Steuerungsebene ist die Verwendung der Serialisierungs-API.</span><span class="sxs-lookup"><span data-stu-id="74fc0-134">The highest level of control is to use the Serialization API.</span></span> <span data-ttu-id="74fc0-135">Diese APIs werden aus einer Zuordnung zwischen C-Datentypen und XML gesteuert und können eine komplexe in-Memory-Struktur in XML und zurück mit einer einzelnen Funktion wie [**wswrite-Element**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement) und [**wsleelement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)lesen oder schreiben.</span><span class="sxs-lookup"><span data-stu-id="74fc0-135">These APIs are driven off a mapping between C data types and XML, and can read or write a complex in-memory structure to xml and back with a single function like [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement) and [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement).</span></span>

<span data-ttu-id="74fc0-136">Die XML-kanonisierungsapis können verwendet werden, um eine kanonische Form von XML zu generieren, die wiederum zum Generieren kryptografischer Signaturen über XML-Inhalte verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="74fc0-136">The XML Canonicalization APIs may be used to generate a canonical form of XML which may in turn be used for generating cryptographic signatures over XML content.</span></span>

## <a name="creating-a-writer"></a><span data-ttu-id="74fc0-137">Erstellen eines Writers</span><span class="sxs-lookup"><span data-stu-id="74fc0-137">Creating a writer</span></span>

<span data-ttu-id="74fc0-138">So erstellen und verwenden Sie einen Writer zum Schreiben in einen Puffer im Arbeitsspeicher:</span><span class="sxs-lookup"><span data-stu-id="74fc0-138">To create and use a writer to write to an in-memory buffer:</span></span>

``` syntax
WsCreateWriter              // Create an instance of a WS_XML_WRITER
// Initialize a WS_XML_WRITER_BUFFER_OUTPUT
WsSetOutput                 // Set the encoding and output of the writer along with any other writer properties
// Write Elements
WsGetWriterProperty(..., WS_XML_WRITER_PROPERTY_BYTES, ...)  // Get the generated bytes as a single byte array
// Use the generated bytes
WsFreeWriter                // Free the writer
```

<span data-ttu-id="74fc0-139">So erstellen und verwenden Sie einen Writer zum Schreiben in einen Stream:</span><span class="sxs-lookup"><span data-stu-id="74fc0-139">To create and use a writer to write to a stream:</span></span>

``` syntax
WsCreateWriter              // Create an instance of a WS_XML_WRITER
// Initialize a WS_XML_WRITER_STREAM_OUTPUT
WsSetOutput                 // Set the encoding and output of the writer along with any other writer properties
// Write Elements
WsFlushWriter               // Force any buffered data to be written
WsFreeWriter                // Free the writer
```

<span data-ttu-id="74fc0-140">So erstellen und verwenden Sie einen Writer zum Schreiben in einen [WS \_ XML- \_ Puffer](ws-xml-buffer.md):</span><span class="sxs-lookup"><span data-stu-id="74fc0-140">To create and use a writer to write to a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax
WsCreateXmlBuffer           // Create the buffer to write to
WsCreateWriter              // Create an instance of a WS_XML_WRITER
WsSetOutputToBuffer         // Set the output buffer along with any other writer properties
// Write Elements
WsFreeWriter                // Free the writer
// The buffer has the generated document
```

<span data-ttu-id="74fc0-141">In allen Fällen kann die Eigenschaft [**WS \_ XML \_ Writer- \_ Eigenschaften \_ Einzug**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id) eingeschlossen werden, um den XML-Code zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="74fc0-141">In all cases, the property [**WS\_XML\_WRITER\_PROPERTY\_INDENT**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id) may be included to format the xml.</span></span>

## <a name="writing-elements"></a><span data-ttu-id="74fc0-142">Schreiben von Elementen</span><span class="sxs-lookup"><span data-stu-id="74fc0-142">Writing Elements</span></span>

<span data-ttu-id="74fc0-143">So schreiben Sie ein Element in einen Writer:</span><span class="sxs-lookup"><span data-stu-id="74fc0-143">To write an element to a writer:</span></span>

``` syntax
WsWriteStartElement          // Write a start element
for each attribute
{
// Write an attribute using either
WsWriteStartAttribute    // Write a start attribute
// Write Content
WsWriteEndAttribute      // Write an end attribute
// Or one of the following
WsWriteXmlnsAttribute    // Write an explicit xmlns attribute
}
// Write Elements or Content
WsWriteEndElement
```

<span data-ttu-id="74fc0-144">Außerdem kann Folgendes verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="74fc0-144">The following may also be used:</span></span>

``` syntax
WsWriteArray                 // Write an array of primitive values as a series of repeated elements
```

## <a name="writing-content"></a><span data-ttu-id="74fc0-145">Schreiben von Inhalten</span><span class="sxs-lookup"><span data-stu-id="74fc0-145">Writing Content</span></span>

<span data-ttu-id="74fc0-146">Zum Schreiben von Inhalt in ein Element oder Attribut kann Folgendes verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="74fc0-146">To write content to an element or attribute, the following may be used:</span></span>

``` syntax
WsWriteChars                 // Write unicode characters from memory
WsWriteCharsUtf8             // Write UTF-8 encoded characters from memory
WsWriteBytes                 // Write binary data encoded as base64
WsPushBytes                  // Direct the writer to request that bytes be written
WsPullBytes                  // Direct the writer to read the bytes to be written
WsWriteValue                 // Write primitive values such as ints and BOOLs
WsWriteText                  // Write an WS_XML_TEXT
WsWriteQualifiedName         // Write a qualified name
```

<span data-ttu-id="74fc0-147">Folgendes kann zum Schreiben in ein Dokument verwendet werden, kann jedoch nicht verwendet werden, wenn es sich um ein Attribut handelt.</span><span class="sxs-lookup"><span data-stu-id="74fc0-147">The following can be used to write to a document, but may not be used when within an attribute.</span></span>

``` syntax
WsWriteNode                  // Write a single WS_XML_NODE
WsCopyNode                   // Copy a single node, or an entire WS_XML_ELEMENT_NODE and children from an WS_XML_READER
```

<span data-ttu-id="74fc0-148">Folgendes kann verwendet werden, um einen CDATA-Abschnitt in einem Textdokument zu schreiben:</span><span class="sxs-lookup"><span data-stu-id="74fc0-148">The following may be used to write a CDATA section in a text document:</span></span>

``` syntax
WsWriteStartCData            // Start a CDATA section in a text encoding
// Write Content
WsWriteEndCData              // End a CDATA section in text encoding
```

## <a name="miscellaneous"></a><span data-ttu-id="74fc0-149">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="74fc0-149">Miscellaneous</span></span>

``` syntax
WsGetPrefixFromNamespace     // Find a prefix bound to a namespace
```

## <a name="creating-a-reader"></a><span data-ttu-id="74fc0-150">Erstellen eines Readers</span><span class="sxs-lookup"><span data-stu-id="74fc0-150">Creating a reader</span></span>

<span data-ttu-id="74fc0-151">So erstellen und verwenden Sie einen Reader zum Lesen aus einem in-Memory-Puffer:</span><span class="sxs-lookup"><span data-stu-id="74fc0-151">To create and use a reader to read from an in-memory buffer:</span></span>

``` syntax
WsCreateReader              // Create an instance of a WS_XML_READER
// Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput                  // Set the encoding and input of the reader along with any other reader properties
// Read Elements
WsFreeReader                // Free the reader
```

<span data-ttu-id="74fc0-152">So erstellen Sie einen Reader und verwenden ihn aus einem Stream</span><span class="sxs-lookup"><span data-stu-id="74fc0-152">To create and use a reader to reader from a stream:</span></span>

``` syntax
WsCreateReader              // Create an instance of a WS_XML_READER
// Initialize a WS_XML_READER_STREAM_INPUT
WsSetInput                  // Set the encoding and input of the reader along with any other reader properties
WsFillReader                // Populate the reader with data from the underlying stream
// Read Elements
WsFreeReader                // Free the reader
```

<span data-ttu-id="74fc0-153">So erstellen und verwenden Sie einen Reader zum Lesen aus einem [WS \_ XML- \_ Puffer](ws-xml-buffer.md):</span><span class="sxs-lookup"><span data-stu-id="74fc0-153">To create and use a reader to read from a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax
WsCreateXmlBuffer           // Create the buffer to write to
WsCreateReader              // Create an instance of a WS_XML_READER
WsSetInputToBuffer          // Set the input buffer along with any other reader properties
// Read Elements
WsFreeReader                // Free the reader
```

## <a name="reading-elements"></a><span data-ttu-id="74fc0-154">Lesen von Elementen</span><span class="sxs-lookup"><span data-stu-id="74fc0-154">Reading Elements</span></span>

<span data-ttu-id="74fc0-155">So lesen Sie ein Element aus einem Reader:</span><span class="sxs-lookup"><span data-stu-id="74fc0-155">To read an element from a reader:</span></span>

``` syntax
WsReadToStartElement         // Skip whitespace and comments to position the reader on a specific element
for each attribute of interest
{
WsFindAttribute          // Try Locate the attribute
if (found)
{
WsReadStartAttribute // Set the reader to read the attribute
// Read Content
WsReadEndAttribute   // Return the reader to the element
}
}
WsReadStartElement           // Advance the reader past the current element
// Read Elements or Content
WsWriteEndElement            // Advance the reader past the corresponding end element
```

<span data-ttu-id="74fc0-156">Außerdem kann Folgendes verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="74fc0-156">The following may also be used:</span></span>

``` syntax
WsReadArray                  // Read an array of primitive values as a series of repeated elements
```

## <a name="reading-content"></a><span data-ttu-id="74fc0-157">Lesen von Inhalten</span><span class="sxs-lookup"><span data-stu-id="74fc0-157">Reading Content</span></span>

<span data-ttu-id="74fc0-158">Zum Lesen von Inhalt aus einem Element oder Attribut kann Folgendes verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="74fc0-158">To read content from an element or attribute, the following may be used:</span></span>

``` syntax
WsReadChars                 // Read characters to memory as unicode
WsReadCharsUtf8             // Read characters to memory encoded as UTF-8
WsReadBytes                 // Read binary data encoded as base64
WsReadValue                 // Read primitive values such as ints and BOOLs
WsReadQualifiedName         // Read a qualified name
```

<span data-ttu-id="74fc0-159">Folgendes kann verwendet werden, um den aktuellen Knoten zu überprüfen, auf dem der Reader positioniert ist:</span><span class="sxs-lookup"><span data-stu-id="74fc0-159">The following may be used to inspect the current node the reader is positioned on:</span></span>

``` syntax
WsGetReaderNode             // Get the current node
```

## <a name="using-a-buffer"></a><span data-ttu-id="74fc0-160">Verwenden eines Puffers</span><span class="sxs-lookup"><span data-stu-id="74fc0-160">Using a buffer</span></span>

<span data-ttu-id="74fc0-161">Beim Schreiben in einen [WS \_ XML- \_ Puffer](ws-xml-buffer.md) kann Folgendes verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="74fc0-161">When writing to a [WS\_XML\_BUFFER](ws-xml-buffer.md) the following may be used:</span></span>

``` syntax
WsGetWriterPosition          // Get the current position of the writer in the document
WsSetWriterPosition          // Set the current position of the writer in the document
WsMoveWriter                 // Move relative to the current position in the document
WsRemoveNode                 // Delete an element or text from a document
```

<span data-ttu-id="74fc0-162">Beim Lesen aus einem [WS \_ XML- \_ Puffer](ws-xml-buffer.md) kann Folgendes verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="74fc0-162">When reading from a [WS\_XML\_BUFFER](ws-xml-buffer.md) the following may be used:</span></span>

``` syntax
WsGetReaderPosition          // Get the current position of the reader in the document
WsSetReaderPosition          // Set the current position of the reader in the document
WsMoveReader                 // Move relative to the current position in the document
```

<span data-ttu-id="74fc0-163">Folgendes kann verwendet werden, um einen [WS \_ XML- \_ Puffer](ws-xml-buffer.md)zu ändern:</span><span class="sxs-lookup"><span data-stu-id="74fc0-163">The following may be used to modify a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax

WsRemoveNode                 // Delete an element or text from a document
```

## <a name="other"></a><span data-ttu-id="74fc0-164">Andere</span><span class="sxs-lookup"><span data-stu-id="74fc0-164">Other</span></span>

``` syntax
WsGetNamespaceFromPrefix     // Find a namespace bound to a prefix
WsGetXmlAttribute            // Find an "xml:space" or "xml:lang" attribute in scope
```

 

 




