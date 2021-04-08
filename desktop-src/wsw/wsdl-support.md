---
title: WSDL und Dienstverträge
description: Das Wsutil.exe-Hilfsprogramm generiert einen C-sprachenstub gemäß der bereitgestellten WSDL-Metadaten sowie Datentyp Definitionen und Beschreibungen für Datentypen, die von vom Benutzer erstellten XML-Schemas beschrieben werden.
ms.assetid: d3c147d6-e370-4e8a-96d8-6660f3a2b996
keywords:
- WSDL-Unterstützung
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19661e487c1a0dde871333376336bede239f9825
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734840"
---
# <a name="wsdl-and-service-contracts"></a><span data-ttu-id="9b3dc-106">WSDL und Dienstverträge</span><span class="sxs-lookup"><span data-stu-id="9b3dc-106">WSDL and Service Contracts</span></span>

<span data-ttu-id="9b3dc-107">Das [Wsutil.exe](web-service-compiler-tool.md) -Hilfsprogramm generiert einen C-sprachenstub gemäß der bereitgestellten WSDL-Metadaten sowie Datentyp Definitionen und Beschreibungen für Datentypen, die von vom Benutzer erstellten XML-Schemas beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-107">The [Wsutil.exe](web-service-compiler-tool.md) utility generates a C language stub according to supplied WSDL metadata, as well as data type definitions and descriptions for data types described by user-authored XML schemas.</span></span>


<span data-ttu-id="9b3dc-108">Im folgenden finden Sie ein Beispiel für ein WSDL-Dokument und ein XML-Schema, das als Grundlage für die nachfolgende Diskussion dient:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-108">The following is an example WSDL document and XML schema that serves as a basis for the discussion that follows:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
  targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
   <xs:element name="SimpleMethod">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="a" type="xs:int" />
      <xs:element name="b" type="xs:int" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
   <xs:element name="SimpleMethodResponse">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="b" type="xs:int" />
      <xs:element name="c" type="xs:int" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
  </xs:schema>
 </wsdl:types>
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   <wsdl:input wsaw:Action="http://Example.org/ISimpleService/SimpleMethod" 
   message="tns:ISimpleService_SimpleMethod_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ISimpleService/SimpleMethodResponse" 
   message="tns:ISimpleService_SimpleMethod_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
 <wsdl:binding name="DefaultBinding_ISimpleService" type="tns:ISimpleService">
  <soap:binding transport="http://schemas.xmlsoap.org/soap/http" />
  <wsdl:operation name="SimpleMethod">
   <soap:operation soapAction="http://Example.org/ISimpleService/SimpleMethod" 
   style="document" />
   <wsdl:input>
    <soap:body use="literal" />
   </wsdl:input>
   <wsdl:output>
    <soap:body use="literal" />
   </wsdl:output>
  </wsdl:operation>
 </wsdl:binding>
 <wsdl:service name="SimpleService">
  <wsdl:port name="ISimpleService" binding="tns:DefaultBinding_ISimpleService">
   <soap:address location="http://Example.org/ISimpleService" />
  </wsdl:port>
 </wsdl:service>
</wsdl:definitions>
```

<span data-ttu-id="9b3dc-109">In diesem Beispiel wird ein Vertrag, isimpleservice, mit einer einzigen Methode, simplemethod, bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-109">This example provides a contract, ISimpleService, with a single method, SimpleMethod.</span></span> <span data-ttu-id="9b3dc-110">"Simplemethod" verfügt über zwei Eingabeparameter vom Typ " **Integer**", " *a* " und " *b*", die vom Client an den Dienst gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-110">"SimpleMethod" has two input parameters of type **integer**, *a* and *b*, that are sent from the client to the service.</span></span> <span data-ttu-id="9b3dc-111">Ebenso hat simplemethod zwei Ausgabeparameter vom Typ " **Integer**", " *b* " und " *c*", die nach erfolgreichem Abschluss an den Client zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-111">Likewise, SimpleMethod has two output parameters of type **integer**, *b* and *c*, which are returned to the client after successful completion.</span></span> <span data-ttu-id="9b3dc-112">In der von Sal mit Anmerkungen versehene C-Syntax sieht die Methoden Definition wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-112">In SAL-annotated C syntax, the method definition appears as follows:</span></span>

``` syntax
void SimpleMethod(__in int a, __inout int *  b, __out int * c );
```

<span data-ttu-id="9b3dc-113">In dieser Definition ist isimpleservice ein Dienstvertrag mit einem einzelnen Dienst Vorgang: simplemethod.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-113">In this definition, ISimpleService is a service contract with a single service operation: SimpleMethod.</span></span>

<span data-ttu-id="9b3dc-114">Die Ausgabe Header Datei enthält Definitionen und Beschreibungen für einen externen Verweis.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-114">The output header file contains definitions and descriptions for external reference.</span></span> <span data-ttu-id="9b3dc-115">Dies schließt Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-115">This includes:</span></span>

-   <span data-ttu-id="9b3dc-116">C-Strukturdefinitionen für globale Elementtypen.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-116">C structure definitions for global element types.</span></span>
-   <span data-ttu-id="9b3dc-117">Ein Vorgangs Prototyp, wie in der aktuellen Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-117">An operation prototype as defined in current file.</span></span>
-   <span data-ttu-id="9b3dc-118">Ein Funktionstabellen Prototyp für die Verträge, die in der WSDL-Datei angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-118">A function table prototype for the contracts specified in the WSDL file.</span></span>
-   <span data-ttu-id="9b3dc-119">Client Proxy-und Dienst-Stub-Prototypen für alle in der aktuellen Datei angegebenen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-119">Client proxy and service stub prototypes for all the functions specified in current file.</span></span>
-   <span data-ttu-id="9b3dc-120">Eine [**WS- \_ Element \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) Datenstruktur für die globalen Schema Elemente, die in der aktuellen Datei definiert sind.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-120">A [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) data structure for the global schema elements defined in current file.</span></span>
-   <span data-ttu-id="9b3dc-121">Eine [**WS- \_ Nachrichten \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) Datenstruktur für alle Nachrichten, die in der aktuellen Datei angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-121">A [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) data structure for all the messages specified in current file.</span></span>
-   <span data-ttu-id="9b3dc-122">Eine [**WS- \_ Vertrags \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) Datenstruktur für alle Verträge, die in der aktuellen Datei angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-122">A [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) data structure for all the contracts specified in current file.</span></span>

<span data-ttu-id="9b3dc-123">Eine globale Struktur wird generiert, um alle globalen Beschreibungen der Schema Typen und Dienstmodell Typen zu kapseln, auf die die Anwendung verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-123">One global structure is generated to encapsulate all the global descriptions for the schema types and service model types to which the application can refer.</span></span> <span data-ttu-id="9b3dc-124">Die Struktur wird unter Verwendung eines normalisierten Datei namens benannt.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-124">The structure is named using a normalized file name.</span></span> <span data-ttu-id="9b3dc-125">In diesem Beispiel generiert Wsutil.exe eine globale Definitions Struktur mit dem Namen "example \_ WSDL", die alle Webdienst Beschreibungen enthält.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-125">In this example, Wsutil.exe generates a global definitions structure named "example\_wsdl" that contains all the web service descriptions.</span></span> <span data-ttu-id="9b3dc-126">Die Struktur Definition wird in der Stubdatei generiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-126">The structure definition is generated in the stub file.</span></span>

``` syntax
typedef struct _example_wsdl
{
  struct {
    WS_ELEMENT_DESCRIPTION SimpleMethod;
    WS_ELEMENT_DESCRIPTION SimpleMethodResponse;
  } elements;
  struct {
    WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_InputMessage;
    WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_OutputMessage;
  } messages;
  struct {
    WS_CONTRACT_DESCRIPTION DefaultBinding_ISimpleService;
  } contracts;
} _example_wsdl;

extern const _stockquote_wsdl stockquote_wsdl;
```

<span data-ttu-id="9b3dc-127">Für globale Element Definitionen im XML-Schema Dokument (XSD) werden ein [**WS- \_ Element- \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) Prototyp sowie die entsprechende C-Typdefinition für jedes der Elemente generiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-127">For global element definitions in the XML schema document (XSD), one [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) prototype, as well as the corresponding C type definition, are generated for each of the elements.</span></span> <span data-ttu-id="9b3dc-128">Die Prototypen für die Element Beschreibungen für simplemethod und simplemethodresponse werden als Elemente in der obigen Struktur generiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-128">The prototypes for the element descriptions for SimpleMethod and SimpleMethodResponse are generated as members in the structure above.</span></span> <span data-ttu-id="9b3dc-129">Die C-Strukturen werden wie folgt generiert:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-129">The C structures are generated as follows:</span></span>

``` syntax
typedef struct SimpleMethod
{
  int   a;
  int   b;
} SimpleMethod;

typedef struct SimpleMethodResponse
{
  int   b;
  int   c;
} SimpleMethodResponse;
```

<span data-ttu-id="9b3dc-130">Ähnlich wie bei globalen komplexen Typen generiert Wsutil.exe Typen-C-Strukturdefinitionen wie oben, ohne übereinstimmende Element Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-130">Similarly for global complex types, Wsutil.exe generates type C structure definitions like above, without matching element descriptions.</span></span>

<span data-ttu-id="9b3dc-131">Bei der WSDL-Eingabe generiert Wsutil.exe die folgenden Prototypen und Definitionen:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-131">For WSDL input, Wsutil.exe generates the following prototypes and definitions:</span></span>

-   <span data-ttu-id="9b3dc-132">Ein [**WS- \_ Nachrichten \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) Prototyp wird für die Nachrichten Beschreibung generiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-132">A [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) prototype is generated for the message description.</span></span> <span data-ttu-id="9b3dc-133">Diese Beschreibung kann vom Dienstmodell und der Nachrichten Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-133">This description can be used by the service model as well as the message layer.</span></span> <span data-ttu-id="9b3dc-134">Nachrichten Beschreibungs Strukturen sind Felder namens "MessageName" in der globalen Struktur.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-134">Message description structures are fields named "messagename" in the global structure.</span></span> <span data-ttu-id="9b3dc-135">In diesem Beispiel wird die Nachrichten Beschreibung als isimpleservice- \_ simplemethod- \_ inputmessage-Feld in der isimpleservice- \_ simplemethod- \_ inputmessage-Struktur generiert, wie in der WSDL-Datei angegeben.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-135">In this example, the message description is generated as the ISimpleService\_SimpleMethod\_InputMessage field in the ISimpleService\_SimpleMethod\_InputMessage structure as specified in the WSDL file.</span></span>
-   <span data-ttu-id="9b3dc-136">[**WS \_ Der Prototyp der Vertrags \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) wird für die Vertragsbeschreibung generiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-136">[**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) prototype is generated for the contract description.</span></span> <span data-ttu-id="9b3dc-137">Diese Beschreibung wird vom Dienstmodell verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-137">This description is used by service model.</span></span> <span data-ttu-id="9b3dc-138">Struktur von Vertrags Beschreibungen sind Felder mit dem Namen "Kontoname" in der globalen Struktur.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-138">Contract description structures are fields named "contractname" in the global structure.</span></span> <span data-ttu-id="9b3dc-139">In diesem Beispiel wird die Vertragsbeschreibung als DefaultBinding \_ isimpleservice-Feld in der Struktur " \_ example \_ WSDL" generiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-139">In this example, the contract description is generated as the DefaultBinding\_ISimpleService field in the structure "\_example\_wsdl".</span></span>

<span data-ttu-id="9b3dc-140">Vorgangs-und Typspezifikationen werden sowohl für den Proxy als auch für den Stub gemeinsam und in beiden Dateien generiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-140">Operation and type specifications are common to both proxy and stub and they are generated in both files.</span></span> <span data-ttu-id="9b3dc-141">Wsutil.exe generiert nur dann eine Kopie, wenn der Proxy und der Stub in derselben Datei generiert werden.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-141">Wsutil.exe generates one copy only if both the proxy and stub are generated in the same file.</span></span>

## <a name="identifier-generation"></a><span data-ttu-id="9b3dc-142">Bezeichnergenerierung</span><span class="sxs-lookup"><span data-stu-id="9b3dc-142">Identifier generation</span></span>

<span data-ttu-id="9b3dc-143">Die oben aufgeführten automatisch generierten C-Strukturen werden basierend auf dem in der WSDL-Datei angegebenen Namen erstellt.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-143">The autogenerated C structures listed above are created based on the name specified in WSDL file.</span></span> <span data-ttu-id="9b3dc-144">Ein XML-NcName wird in der Regel nicht als gültiger C-Bezeichner betrachtet, und die Namen werden nach Bedarf normalisiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-144">An XML NCName is not commonly considered a valid C identifier, and the names are normalized as needed.</span></span> <span data-ttu-id="9b3dc-145">Hexadezimale Werte werden nicht konvertiert, und häufige Buchstaben wie ': ', '/' und '. ' werden in den Unterstrich ' ' konvertiert, \_ um die Lesbarkeit zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-145">Hex values are not converted, and common letters like ':', '/' and '.' are converted to the underscore '\_' character to improve readability.</span></span>

## <a name="header-for-the-stub"></a><span data-ttu-id="9b3dc-146">Kopfzeile für den Stub</span><span class="sxs-lookup"><span data-stu-id="9b3dc-146">Header for the stub</span></span>

<span data-ttu-id="9b3dc-147">Für jeden Vorgang im Dienstvertrag wird eine Rückruf Routine mit dem Namen " <operationname> Callback" generiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-147">For each operation in the service contract, one callback routine named "<operationname>Callback" is generated.</span></span> <span data-ttu-id="9b3dc-148">(Der Vorgang "simplemethod" im Beispiel Dienstvertrag hat z. b. einen generierten Rückruf mit dem Namen "simplemethodcallback".)</span><span class="sxs-lookup"><span data-stu-id="9b3dc-148">(For example, the operation "SimpleMethod" in the example service contract has a generated callback named "SimpleMethodCallback".)</span></span>

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT * context,
  int a, int *b, int *c,
  const WS_ASYNC_CONTEXT *asyncContext,
  WS_ERROR * error);
```

<span data-ttu-id="9b3dc-149">Für jede WSDL- **portType** -Wsutil.exe eine Funktions Tabelle generiert, die **portType** darstellt.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-149">For each WSDL **portType** Wsutil.exe generates a function table representing **portType**.</span></span> <span data-ttu-id="9b3dc-150">Jeder Vorgang für den **portType** verfügt über einen entsprechenden Funktionszeiger auf den Rückruf, der in der Funktions Tabelle enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-150">Each operation on the **portType** has a corresponding function pointer to the callback present in the function table.</span></span>

``` syntax
struct ISimpleServiceMethodTable
{
  ISimpleService_SimpleMethodCallback SimpleMethod;
};
```

<span data-ttu-id="9b3dc-151">Proxy Prototypen werden für alle Vorgänge generiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-151">Proxy prototypes are generated for all operations.</span></span> <span data-ttu-id="9b3dc-152">Der prototypname ist der Vorgangs Name (in diesem Fall "simplemethod"), der in der WSDL-Datei für den Dienstvertrag angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-152">The prototype name is the operation name (in this case, "SimpleMethod") specified in WSDL file for the service contract.</span></span>

``` syntax
HRESULT WINAPI SimpleMethod(WS_CHANNEL *channel,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error );
```

## <a name="local-only-description-prototype-generation"></a><span data-ttu-id="9b3dc-153">Generierung von nur einem lokalen Beschreibungs Prototyp</span><span class="sxs-lookup"><span data-stu-id="9b3dc-153">Local-only Description Prototype Generation</span></span>

<span data-ttu-id="9b3dc-154">Die Proxy-und Stub-Dateien enthalten die Definition für die globale Definitions Struktur, einschließlich Prototypen und Definitionen für die Strukturen, die nur lokale Beschreibungen und Client Proxy-/dienststub-Implementierungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-154">The proxy andstub files contain the definition for the global definitions structure, including prototypes and definitions for the structures containing local-only descriptions and client proxy/service stub implementations.</span></span>

<span data-ttu-id="9b3dc-155">Alle Prototypen und Definitionen, die für die Stubdatei lokal sind, werden als Teil einer Kapselungs Struktur generiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-155">All prototypes and definitions that are local to the stub file are generated as part of an encapsulating structure.</span></span> <span data-ttu-id="9b3dc-156">Diese übergeordnete lokale Beschreibungs Struktur bietet eine klare Hierarchie der Beschreibungen, die für die serialisierungsschicht und das Dienstmodell erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-156">This overarching local description structure provides a clear hierarchy of the descriptions required by the serialization layer and the service model.</span></span> <span data-ttu-id="9b3dc-157">Die lokale Beschreibungs Struktur hat Prototypen, die der unten gezeigten ähneln:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-157">The local description structure has prototypes similar to the one shown below:</span></span>

``` syntax
struct _filenameLocalDefinitions
{
  struct {
  // schema related output for all the embedded 
  // descriptions that needs to describe global complex types.
  } globalTypes;
  // global elements.
  struct {
  // schema related output, like field description
  // structure description, element description etc.
  ...
  } globalElements;
  struct {
  // messages and related descriptions
  } messages;
  struct {
  // contract and related descriptions.
  } contracts;
  struct {
  // XML dictionary entries.
  } dictionary;
} _filenameLocalDefinitions;
```

## <a name="referencing-definitions-from-other-files"></a><span data-ttu-id="9b3dc-158">Verweisen auf Definitionen aus anderen Dateien</span><span class="sxs-lookup"><span data-stu-id="9b3dc-158">Referencing definitions from other files</span></span>

<span data-ttu-id="9b3dc-159">Lokale Definitionen können auf Beschreibungen verweisen, die in einer anderen Datei generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-159">Local definitions can reference descriptions generated in another file.</span></span> <span data-ttu-id="9b3dc-160">Beispielsweise kann die Nachricht in der von der WSDL-Datei generierten c-Codedatei definiert werden, das Message-Element kann jedoch an anderer Stelle in der aus der XSD-Datei generierten c-Codedatei definiert werden.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-160">For example, the message may be defined in the C code file generated from the WSDL file but the message element may be defined elsewhere in the C code file generated from the XSD file.</span></span> <span data-ttu-id="9b3dc-161">In diesem Fall generiert Wsutil.exe einen Verweis auf das globale Element aus der Datei, die die Nachrichten Definition enthält, wie unten gezeigt:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-161">In this case, Wsutil.exe generates reference to the global element from the file that contains the message definition, as demonstrated below:</span></span>

``` syntax
{  // WS_MESSAGE_DESCRIPTION
...
(WS_ELEMENT_DESRIPTION *)b_xsd.globalElement.<elementname>
  };
```

## <a name="global-element-descriptions"></a><span data-ttu-id="9b3dc-162">Beschreibungen von globalen Elementen</span><span class="sxs-lookup"><span data-stu-id="9b3dc-162">Global element descriptions</span></span>

<span data-ttu-id="9b3dc-163">Für jedes globale Element, das in einer WSDL: Type-oder XSD-Datei definiert ist, gibt es ein entsprechendes Feld mit dem Namen **ElementName** innerhalb des **Global Element** -Felds.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-163">For each global element defined in a wsdl:type or XSD file, there is a matching field named **elementName** inside the **GlobalElement** field.</span></span> <span data-ttu-id="9b3dc-164">In diesem Beispiel wird eine Struktur mit dem Namen simplemethod generiert:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-164">In this example, a structure named SimpleMethod is generated:</span></span>

``` syntax
typedef struct _SimpleServiceLocal
{
  struct  // global elements
  {
    struct // SimpleMethod
    {
    ...
    WS_ELEMENT_DESCRIPTION SimpleMethod;
    } SimpleMethod;
    ...
  } globalElements;
}
```

<span data-ttu-id="9b3dc-165">Andere Beschreibungen, die für die Element Beschreibung erforderlich sind, werden als Teil der enthaltenden Struktur generiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-165">Other descriptions required by the element description are generated as part of the containing structure.</span></span> <span data-ttu-id="9b3dc-166">Wenn es sich bei dem Element um ein einfaches Typelement handelt, gibt es nur ein [**WS- \_ Element- \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) Feld.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-166">If the element is a simple type element, there is only one [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) field.</span></span> <span data-ttu-id="9b3dc-167">Wenn der Elementtyp eine Struktur ist, werden alle zugehörigen Felder und Struktur Beschreibungen als Teil der Elementstruktur generiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-167">If the element type is a structure, all of the related fields and structure descriptions are generated as part of the element structure.</span></span> <span data-ttu-id="9b3dc-168">In diesem Beispiel ist das simplemethod-Element eine Struktur, die zwei Felder enthält: **a** und **b**.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-168">In this example, SimpleMethod element is a structure containing two fields, **a** and **b**.</span></span> <span data-ttu-id="9b3dc-169">Wsutil.exe generiert die Struktur wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-169">Wsutil.exe generates the structure as follows:</span></span>

``` syntax
...
struct // SimpleMethod
{
  struct // SimpleMethod structure
  {
    WS_FIELD_DESCRIPTION a;
    WS_FIELD_DESCRIPTION b;
    WS_FIELD_DESCRIPTION * SimpleMethodFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleMethoddescs; // SimpleMethod
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleMethod;
...
```

<span data-ttu-id="9b3dc-170">Eingebettete Strukturen und eingebettete Elemente werden bei Bedarf als Unterstrukturen generiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-170">Embedded structures and embedded elements are generated as sub-structures as needed.</span></span>

## <a name="wsdl-related-definitions"></a><span data-ttu-id="9b3dc-171">WSDL-bezogene Definitionen</span><span class="sxs-lookup"><span data-stu-id="9b3dc-171">WSDL related definitions</span></span>

<span data-ttu-id="9b3dc-172">Wsutil.exe generiert ein Feld im WSDL-Abschnitt für jeden der **portType** -Werte, die unter dem angegebenen WSDL: Service definiert sind.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-172">Wsutil.exe generates a field under WSDL section for each of the **portType** values defined under the specified wsdl:service.</span></span>

``` syntax
...
struct { // WSDL
    struct { // portTypeName
        struct { // operationName
        } operationName;
    ...
    WS_OPERATION_DESCRIPTION* operations[numOperations];
    WS_CONTRACT_DESCRIPTION contractDesc;
    } portTypeName;
}
...
```

<span data-ttu-id="9b3dc-173">Wsutil.exe generiert ein Feld f, das alle für den Vorgang erforderlichen Beschreibungen enthält, ein Single-Array von Zeigern auf die einzelnen Vorgangs Beschreibungen für jede Methode und eine [**WS- \_ Vertrags \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) für den angegebenen **portType**.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-173">Wsutil.exe generates one field f that contains all the descriptions needed for the operation, a signle array of pointers to each of the operation descriptions for each method, and one [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) for the specified **portType**.</span></span>

<span data-ttu-id="9b3dc-174">Alle von Vorgängen benötigten Beschreibungen werden im Feld **OperationName** unter dem angegebenen **portType** generiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-174">All the descriptions needed by operations are generated inside the **operationName** field under the specified **portType**.</span></span> <span data-ttu-id="9b3dc-175">Hierzu gehören das Feld für die [**\_ \_ Beschreibung der WS-Elemente**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) sowie die Unterstruktur für Eingabe-und Ausgabeparameter.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-175">These include the [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) field as well as the sub-structure for input and output parameter s.</span></span> <span data-ttu-id="9b3dc-176">Ebenso werden die [**WS- \_ Nachrichten \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) Felder für die Eingabe Nachricht und die optionale Ausgabe Meldung zusammen mit dem [**WS \_ Das Feld für die Parameter \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) Liste für alle Vorgangs Parameter und das [**\_ \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) Feld für die WS-Operation für den Vorgang selbst.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-176">Likewise, the [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) fields for the input message and the optional output message are included along with the; [**WS\_PARAMETER\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) list field for all of the operation parameters and the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) field for the operation itself.</span></span> <span data-ttu-id="9b3dc-177">In diesem Beispiel wird die Code Struktur für die simplemethod-Beschreibung wie unten gezeigt generiert:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-177">In this example, the code structure for the SimpleMethod description is generated as seen below:</span></span>

``` syntax
...
struct // messages
{
  WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_InputMessage;
  WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_OutputMessage;
} messages;
struct // contracts
{
  struct // DefaultBinding_ISimpleService
  {
    struct // SimpleMethod
    {
      WS_PARAMETER_DESCRIPTION params[3];
      WS_OPERATION_DESCRIPTION SimpleMethod;
    } SimpleMethod;
    WS_OPERATION_DESCRIPTION* operations[1];
    WS_CONTRACT_DESCRIPTION contractDesc;
  } DefaultBinding_ISimpleService;
} contracts;
...
```

## <a name="xml-dictionary-related-definitions"></a><span data-ttu-id="9b3dc-178">XML-Wörterbuch bezogene Definitionen</span><span class="sxs-lookup"><span data-stu-id="9b3dc-178">XML dictionary related definitions</span></span>

<span data-ttu-id="9b3dc-179">Namen und Namespaces, die in verschiedenen Beschreibungen verwendet werden, werden als Felder des Typs " [**WS \_ XML \_ String**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)" generiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-179">Names and namespaces used in various descriptions are generated as fields of type [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string).</span></span> <span data-ttu-id="9b3dc-180">Alle diese Zeichen folgen werden als Teil eines konstanten Verzeichnisses pro Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-180">All of these strings are generated as part a per-file constant dictionary.</span></span> <span data-ttu-id="9b3dc-181">Die Liste der Zeichen folgen und des [**WS- \_ XML- \_ Wörterbuch**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) Felds (mit dem Namen " **dict** " im folgenden Beispiel) werden als Teil des Wörterbuch Felds der dateinamelocal-Struktur generiert. </span><span class="sxs-lookup"><span data-stu-id="9b3dc-181">The list of strings and the [**WS\_XML\_DICTIONARY**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) field (named **dict** in the example below) are generated as part of the dictionary field of the **fileNameLocal** structure.</span></span>

``` syntax
struct { // fileNameLocal
...
  struct { // dictionary
    struct { // XML string list
      WS_XML_STRING firstFieldName;
      WS_XML_STRING firstFieldNS;
      ...
    } xmlStrings;
  WS_XML_DICTIONARY dict;
  } dictionary;
}; // fileNameLocal;
```

<span data-ttu-id="9b3dc-182">Das Array von [**WS \_ XML- \_ Zeichen**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)folgen s wird als eine Reihe von Feldern vom Typ " **WS \_ XML \_ String**" generiert, die mit benutzerfreundlichen Namen benannt sind.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-182">The array of [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)s are generated as a series of fields of type **WS\_XML\_STRING**, named with with user-friendly names.</span></span> <span data-ttu-id="9b3dc-183">Der generierte Stub verwendet die benutzerfreundlichen Namen in verschiedenen Beschreibungen, um die Lesbarkeit zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-183">The generated stub uses the user-friendly names in various descriptions for better readability.</span></span>

<span data-ttu-id="9b3dc-184">Client Proxy für WSDL-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="9b3dc-184">Client proxy for WSDL operations</span></span>

<span data-ttu-id="9b3dc-185">Wsutil.exe generiert einen Client Proxy für alle Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-185">Wsutil.exe generates a client proxy for all of the operations.</span></span> <span data-ttu-id="9b3dc-186">Anwendungen können die Methoden Signatur überschreiben, indem Sie eine Präfix-Befehlszeilenoption verwenden.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-186">Applications can overwrite the method signature using a prefix command-line option.</span></span>

``` syntax
HRESULT WINAPI bindingName_SimpleMethod(WS_SERVICE_PROXY *serviceProxy,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_CALL_PROPERTY* callProperties,
  ULONG callPropertyCount,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error )
{
  void* argList[] = {&a, &b, &c};
  return WsCall(_serviceProxy,
    (WS_OPERATION_DESCRIPTION*)&example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.SimpleMethod,
    (void **)&_argList,
    callProperties,
    callPropertyCount,
    heap,
    asyncContext,
    error
  );      
}
```

<span data-ttu-id="9b3dc-187">Der Vorgangs Aufrufer muss einen gültigen *Heap* Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-187">The operation caller must pass in a valid *heap* parameter.</span></span> <span data-ttu-id="9b3dc-188">Ausgabeparameter werden mithilfe des \_ im *Heap* -Parameter angegebenen WS-Heap Werts zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-188">Output parameters are allocated using the WS\_HEAP value specified in the *heap* parameter.</span></span> <span data-ttu-id="9b3dc-189">Die Aufruf Funktion kann den Heap zurücksetzen oder freigeben, um Speicher für alle Ausgabeparameter freizugeben.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-189">The calling function can reset or free the heap to release memory for all of the output parameters.</span></span> <span data-ttu-id="9b3dc-190">Wenn der Vorgang fehlschlägt, können zusätzliche Detail Fehlerinformationen aus dem optionalen Fehler Objekt abgerufen werden, sofern dieses verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-190">If the operation fails, additional detail error information can be retrieved from the optional error object if it is available.</span></span>

<span data-ttu-id="9b3dc-191">Wsutil.exe generiert einen Dienst-Stub für alle Vorgänge, die in Binding beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-191">Wsutil.exe generates a service stub for all of the operations described in binding.</span></span>

``` syntax
HRESULT CALLBACK ISimpleService_SimpleMethodStub(
  const WS_OPERATION_CONTEXT *context,
  void * stackStruct,
  void * callback,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR *error )
{
  SimpleMethodParamStruct *pstack = (SimpleMethodParamStruct *) stackstruct;
  SimpleMethodOperation operation = (SimpleMethodOperation)callback;
  return operation(context, pstack->a, &(pstack->b), &(pstack->c ), asyncContext, error );
}
```

<span data-ttu-id="9b3dc-192">Der obige Abschnitt beschreibt den Prototyp der lokalen Struktur, die alle Definitionen enthält, die nur für die Stubdatei lokal sind.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-192">The above section describes the prototype of the local structure containing all of the definitions local to the stub file only.</span></span> <span data-ttu-id="9b3dc-193">In den nachfolgenden Abschnitten werden die Definitionen der Beschreibungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-193">Subsequent sections describe the definitions of the descriptions.</span></span>

## <a name="wsdl-definition-generation"></a><span data-ttu-id="9b3dc-194">WSDL-Definitions Generierung</span><span class="sxs-lookup"><span data-stu-id="9b3dc-194">WSDL Definition Generation</span></span>

<span data-ttu-id="9b3dc-195">Wsutil.exe generiert eine Konstante statische (Konstante **statische**) Struktur namens *<Dateiname \_>* localdefinitionen vom Typ *<Dienst \_ Name>* local, das alle lokalen Definitionen enthält.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-195">Wsutil.exe generates a constant static (**const static**) structure named *<file\_name>* LocalDefinitions of type *<service\_name>* Local that contains all the local only definitions.</span></span>

``` syntax
const static _SimpleServiceLocal example_wsdlLocalDefinitions =
{
  {  // global types
  ...
  }, // global types
  {  // global elements
  ...
  }, // global elements
  {  // messages
  ...
  }, //messages
  ...
  {  // dictionary
  ...
  }, // dictionary
},
```

<span data-ttu-id="9b3dc-196">Die folgenden WSDL-Beschreibungen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-196">The following WSDL descriptions are supported:</span></span>

-   <span data-ttu-id="9b3dc-197">WSDL: Service</span><span class="sxs-lookup"><span data-stu-id="9b3dc-197">wsdl:service</span></span>
-   <span data-ttu-id="9b3dc-198">WSDL: Bindung</span><span class="sxs-lookup"><span data-stu-id="9b3dc-198">wsdl:binding</span></span>
-   <span data-ttu-id="9b3dc-199">WSDL: portType</span><span class="sxs-lookup"><span data-stu-id="9b3dc-199">wsdl:portType</span></span>
-   <span data-ttu-id="9b3dc-200">WSDL: Vorgang</span><span class="sxs-lookup"><span data-stu-id="9b3dc-200">wsdl:operation</span></span>
-   <span data-ttu-id="9b3dc-201">WSDL: Meldung</span><span class="sxs-lookup"><span data-stu-id="9b3dc-201">wsdl:message</span></span>

## <a name="processing-wsdloperation-and-wsdlmessage"></a><span data-ttu-id="9b3dc-202">Verarbeiten von WSDL: Operation und WSDL: Message</span><span class="sxs-lookup"><span data-stu-id="9b3dc-202">Processing wsdl:operation and wsdl:message</span></span>

<span data-ttu-id="9b3dc-203">Jeder im WSDL-Dokument angegebene Vorgang wird durch [Wsutil.exe](web-service-compiler-tool.md)einem Dienst Vorgang zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-203">Each operation specified in the WSDL document is mapped to a service operation by [Wsutil.exe](web-service-compiler-tool.md).</span></span> <span data-ttu-id="9b3dc-204">Das Tool generiert separate Definitionen der Dienst Vorgänge sowohl für den Server als auch für den Client.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-204">The tool generates separate definitions of the service operations for both the server and the client.</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   <wsdl:input wsaw:Action="http://Example.org/ISimpleService/SimpleMethod" 
   message="tns:ISimpleService_SimpleMethod_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ISimpleService/SimpleMethodResponse" 
   message="tns:ISimpleService_SimpleMethod_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

<span data-ttu-id="9b3dc-205">Das Layout der Eingabe-und Ausgabe Nachrichten Datenelemente wird vom Tool ausgewertet, um die Serialisierungsmetadaten für die Infrastruktur zusammen mit der tatsächlichen Signatur des resultierenden Dienst Vorgangs zu generieren, dem die Eingabe-und Ausgabe Nachrichten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-205">The layout of the input andoutput message data elements is evaluated by the tool to generate the serialization metadata for the infrastructure along with the actual signature of the resulting service operation to which the input and output messages are associated.</span></span>

<span data-ttu-id="9b3dc-206">Die Metadaten für jeden Vorgang in einem bestimmten **portType** haben eine Eingabe und optional eine Ausgabe Meldung. jede dieser Nachrichten wird einer [**WS- \_ Nachrichten \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-206">The metadata for each operation within a specific **portType** has input and optionally an output message, each of these messages is mapped to a [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description).</span></span> <span data-ttu-id="9b3dc-207">In diesem Beispiel werden die Eingabe-und die Ausgabe Meldung für den Vorgang im PortType in "inputmessagedescription" und optional für "outputmessagedescription" in der [**WS- \_ Vorgangs \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-207">In this example, the input and the output message on the operation in the portType mapped to inputMessageDescription and optionally the outputMessageDescription on the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) respectively.</span></span>

<span data-ttu-id="9b3dc-208">Für jede WSDL-Nachricht generiert das Tool eine [**WS- \_ Nachrichten \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) , die auf die Definition der [**WS- \_ Element \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) verweist, wie unten gezeigt:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-208">For each WSDL message the tool generates [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) that references the [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) definition, as demonstrated below:</span></span>

``` syntax
... 
{    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

<span data-ttu-id="9b3dc-209">Die Nachrichten Beschreibung verweist auf die Beschreibung des Eingabe Elements.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-209">The message description refers to the input element description.</span></span> <span data-ttu-id="9b3dc-210">Da das-Element global definiert ist, verweist die Nachrichten Beschreibung auf die globale Definition anstatt auf das lokale statische Element.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-210">Because the element is globally defined, the message description references the global definition instead of the local static element.</span></span> <span data-ttu-id="9b3dc-211">Wenn das Element in einer anderen Datei definiert ist, generiert Wsutil.exe einen Verweis auf die global definierte Struktur in dieser Datei.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-211">Similarly, if the element is defined in another file, Wsutil.exe generates a reference to the globally-defined structure in that file.</span></span> <span data-ttu-id="9b3dc-212">Wenn simplemethodresponse z. b. in einer anderen XSD-Beispieldatei definiert ist, generiert Wsutil.exe stattdessen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-212">For example, if SimpleMethodResponse is defined in another example.xsd file, Wsutil.exe generates the following instead:</span></span>

``` syntax
...
{    // message description for ISimpleService_SimpleMethod_InputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_xsd.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

<span data-ttu-id="9b3dc-213">Jede Nachrichten Beschreibung enthält die Aktion und die spezifische Element Beschreibung (ein Feld vom Typ " [**WS- \_ Element \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)") für alle Nachrichten Datenelemente.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-213">Each message description contains the action and the specific element description (a field of type [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)) for all the message data elements.</span></span> <span data-ttu-id="9b3dc-214">Bei einer Nachricht im RPC-Stil oder einer Nachricht mit mehreren Teilen wird ein Wrapper Element erstellt, um die zusätzlichen Informationen zu kapseln.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-214">In the case of an RPC-style message or a message with multiple parts, a wrapper element is created to encapsulate the additional information.</span></span>

## <a name="rpc-style-support"></a><span data-ttu-id="9b3dc-215">RPC-Formatunterstützung</span><span class="sxs-lookup"><span data-stu-id="9b3dc-215">RPC style support</span></span>

<span data-ttu-id="9b3dc-216">Wsutil.exe unterstützt Dokument-und RPC-Formatvorlagen gemäß der WSDL 1,1-Bindungs Erweiterung für SOAP 1,2.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-216">Wsutil.exe supports document-style as well as RPC-style operations according to the WSDL 1.1 Binding Extension for SOAP 1.2 specification.</span></span> <span data-ttu-id="9b3dc-217">Vorgänge im RPC-und literalstil werden als WS- \_ RPC- \_ \_ literalvorgang gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-217">RPC- and literal-style operations are marked as WS\_RPC\_LITERAL\_OPERATION.</span></span> <span data-ttu-id="9b3dc-218">Das Dienstmodell ignoriert den Namen für das Antworttext-Wrapper Element in RPC/literalvorgängen.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-218">The service model ignores the name for the response body wrapper element in RPC/literal operations.</span></span>

<span data-ttu-id="9b3dc-219">Wsutil.exe bietet keine systemeigene Unterstützung für Codierungs Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-219">Wsutil.exe does not natively support encoding-style operations.</span></span> <span data-ttu-id="9b3dc-220">Der WS \_ XML \_ -Puffer Parameter wird für Codierungs Nachrichten generiert, und Entwickler müssen den nicht transparenten Puffer direkt auffüllen.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-220">The WS\_XML\_BUFFER parameter is generated for encoding messages, and developers must populate the opaque buffer directly.</span></span>

## <a name="multiple-message-parts-support"></a><span data-ttu-id="9b3dc-221">Unterstützung mehrerer Nachrichten Teile</span><span class="sxs-lookup"><span data-stu-id="9b3dc-221">Multiple message parts support</span></span>

<span data-ttu-id="9b3dc-222">Wsutil.exe unterstützt mehrere Nachrichten Teile in einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-222">Wsutil.exe supports multiple message parts in one message.</span></span> <span data-ttu-id="9b3dc-223">Eine mehrteilige Nachricht kann wie folgt angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-223">A multi-part message can be specified as follows:</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_MutipleParts_InputMessage">
  <wsdl:part name="part1" element="tns:SimpleElement1" />
  <wsdl:part name="part2" element="tns:SimpleElement2" />
 </wsdl:message>
</wsdl:definitions>
```

<span data-ttu-id="9b3dc-224">Wsutil.exe generiert ein Feld vom [**Typ "WS \_ struct \_ Type**](/windows/desktop/api/WebServices/ne-webservices-ws_type) " für das Message-Element, wenn die Nachricht mehrere Teile enthält.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-224">Wsutil.exe generates a [**WS\_STRUCT\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type) field for the message element if the message contains multiple parts.</span></span> <span data-ttu-id="9b3dc-225">Wenn die Meldung mit dem Dokument Stil dargestellt wird, generiert Wsutil.exe ein Wrapper Element mit einem Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-225">If the message is represented using the document style, Wsutil.exe generates a wrapper element with struct type.</span></span> <span data-ttu-id="9b3dc-226">Das Wrapper Element weist keinen Namen oder einen bestimmten Namespace auf, und die Wrapper Struktur enthält alle Elemente in allen Teilen als Felder.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-226">The wrapper element does not have a name or a specific namespace, and the wrapper structure contains all of the elements in all of the parts as fields.</span></span> <span data-ttu-id="9b3dc-227">Das Wrapper Element ist nur für die interne Verwendung vorgesehen und wird nicht im Nachrichtentext serialisiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-227">The wrapper element is for internal use only and it will not be serialized in the message body.</span></span>

<span data-ttu-id="9b3dc-228">Wenn die Nachricht eine RPC-oder Literale Darstellung verwendet, erstellt Wsutil.exe ein Wrapper Element mit dem Vorgangs Namen als Elementnamen und dem angegebenen Namespace als Dienst Namespace entsprechend der WSDL-SOAP-Erweiterungs Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-228">If the message is using RPC or literal style representation , Wsutil.exe creates a wrapper element with the operation name as the element name and the specified namespace as service namespace according to WSDL SOAP extension specification.</span></span> <span data-ttu-id="9b3dc-229">Die Struktur des-Elements enthält ein Array von Feldern, die die in den Nachrichten teilen angegebenen Typen darstellen.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-229">The structure of the element contains an array of fields representing the types specified in the message parts.</span></span> <span data-ttu-id="9b3dc-230">Das Wrapper Element wird dem eigentlichen obersten Element im Nachrichtentext zugeordnet, wie in der SOAP-Spezifikation angegeben.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-230">The wrapper element is mapped to the actual top element in message body as indicated in the SOAP specification.</span></span>

<span data-ttu-id="9b3dc-231">Auf der Serverseite ergibt jeder Vorgang eine typedef des resultierenden Server Dienst Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-231">On the server side, each operation results in a typedef of the resulting server service operation.</span></span> <span data-ttu-id="9b3dc-232">Diese typedef wird verwendet, um auf den Vorgang in der Funktions Tabelle wie zuvor beschrieben zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-232">This typedef is used to refer to the operation in the function table as described previously.</span></span> <span data-ttu-id="9b3dc-233">Jeder Vorgang führt auch zur Generierung einer Stub-Funktion, die nfrastructure im Namen des Delegaten an die tatsächliche Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-233">Every operation also results in the generation of a stub function which nfrastructure calls on behalf of the delegate to the actual method.</span></span>

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT* context,
  unsigned int  a,
  unsigned int * b,
  unsigned int * c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error
  );
```

<span data-ttu-id="9b3dc-234">Für den simplemethod-Vorgang wird die simplemethodoperation-typedef oben definiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-234">For the SimpleMethod operation, the SimpleMethodOperation typedef is defined above.</span></span> <span data-ttu-id="9b3dc-235">Beachten Sie, dass die generierte Methode über ein erweitertes Argument mit dem Nachrichten Teil für den Eingabe-und Ausgabe Nachrichten Vorgang für den simplemethod-Vorgang als benannte Parameter verfügt.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-235">Note that the generated method has an expanded argument listwith the message part for the input and output message for SimpleMethod operation as named parameters.</span></span>

<span data-ttu-id="9b3dc-236">Auf der Clientseite wird jeder Vorgang einem Proxy Dienst Vorgang zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-236">On the client side each operation is mapped to a proxy service operation.</span></span>

``` syntax
HRESULT WINAPI SimpleMethod (
  WS_SERVICE_PROXY* serviceProxy,
  ws_heap *heap,
  unsigned int  a,
  unsigned int * b,
  unsigned int * c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

## <a name="processing-wsdlbinding"></a><span data-ttu-id="9b3dc-237">Verarbeiten von WSDL: Binding</span><span class="sxs-lookup"><span data-stu-id="9b3dc-237">Processing wsdl:binding</span></span>

<span data-ttu-id="9b3dc-238">Das wwsapi-Dienstmodell unterstützt die thesoap-Bindungs Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-238">The WWSAPI service model supports theSOAP binding extension.</span></span> <span data-ttu-id="9b3dc-239">Für jede Bindung ist ein **portType** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-239">For each binding there is an associated **portType**.</span></span>

<span data-ttu-id="9b3dc-240">Der in der SOAP-Bindungs Erweiterung angegebene Transport ist nur eine Empfehlung.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-240">The transport specified in soap binding extension is advisory only.</span></span> <span data-ttu-id="9b3dc-241">Die Anwendung muss Transportinformationen bereitstellen, wenn ein Kanal erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-241">Application needs to provide transport information when creating a channel.</span></span> <span data-ttu-id="9b3dc-242">Zurzeit unterstützen wir die WS \_ \_ -HTTP-Bindung und die WS \_ TCP- \_ Bindungs Bindungen.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-242">Currently we support the WS\_HTTP\_BINDING and WS\_TCP\_BINDING bindings.</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:binding name="DefaultBinding_ISimpleService" type="tns:ISimpleService">
  <soap:binding transport="http://schemas.xmlsoap.org/soap/http" />
  <wsdl:operation name="SimpleMethod">
   <soap:operation soapAction="http://Example.org/ISimpleService/SimpleMethod" 
   style="document" />
   <wsdl:input>
    <soap:body use="literal" />
   </wsdl:input>
   <wsdl:output>
    <soap:body use="literal" />
   </wsdl:output>
  </wsdl:operation>
 </wsdl:binding>
</wsdl:definitions>
```

<span data-ttu-id="9b3dc-243">In unserem Beispiel-WSDL-Dokument haben wir nur einen **portType** für isimpleservice.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-243">In our example WSDL document we only have one **portType** for ISimpleService.</span></span> <span data-ttu-id="9b3dc-244">Die bereitgestellte SOAP-Bindung gibt den HTTP-Transport an, der als WS-HTTP-Bindung angegeben wird \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9b3dc-244">The provided SOAP binding indicates the HTTP transport, which is specified as WS\_HTTP\_BINDING.</span></span> <span data-ttu-id="9b3dc-245">Beachten Sie, dass diese Struktur nicht über eine statische Dekoration verfügt, da diese Struktur für die Anwendung verfügbar sein muss.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-245">Notice that this structure does not have static decoration as this structure needs to be available to the application.</span></span>

<span data-ttu-id="9b3dc-246">Verarbeiten von WSDL: portType</span><span class="sxs-lookup"><span data-stu-id="9b3dc-246">Processing wsdl:portType</span></span>

<span data-ttu-id="9b3dc-247">Jeder **portType** in WSDL besteht aus mindestens einem Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-247">Each **portType** in WSDL is made up of one or more operations.</span></span> <span data-ttu-id="9b3dc-248">Der Vorgang sollte mit der SOAP-Bindungs Erweiterung übereinstimmen, die in WSDL: Binding angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-248">The operation should be consistent with the SOAP binding extension indicated in wsdl:binding.</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   ...
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

<span data-ttu-id="9b3dc-249">In diesem Beispiel enthält der isimpleservice- **portType** nur den simplemethod-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-249">In this example, the ISimpleService **portType** only contains the SimpleMethod operation.</span></span> <span data-ttu-id="9b3dc-250">Dies stimmt mit dem Bindungs Abschnitt überein, bei dem es nur einen WSDL-Vorgang gibt, der einer SOAP-Aktion zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-250">This is consistent with the binding section where there is only one WSDL operation that maps to a SOAP action.</span></span>

<span data-ttu-id="9b3dc-251">Da der isimpleservice- **portType** nur einen Vorgang aufweist (-simplemethod), enthält die entsprechende Funktions Tabelle nur simplemethod als Dienst Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-251">Since the ISimpleService **portType** only has one operation -- SimpleMethod -- the corresponding function table only contains SimpleMethod as a service operation.</span></span>

<span data-ttu-id="9b3dc-252">Im Hinblick auf die Metadaten werden die einzelnen **portType** Wsutil.exe einer [**WS- \_ Vertrags \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-252">In terms of metadata each **portType** is mapped by Wsutil.exe to a [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description).</span></span> <span data-ttu-id="9b3dc-253">Jeder Vorgang in einem **portType** wird einer WS- [**\_ Vorgangs \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-253">Each operation within a **portType** is mapped to a [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).</span></span>

<span data-ttu-id="9b3dc-254">In diesem Beispiel generiert **portType** das Tool eine [**WS- \_ Vertrags \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) für isimpleservice.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-254">In this example, **portType** the tool generates [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) for ISimpleService.</span></span> <span data-ttu-id="9b3dc-255">Diese Vertragsbeschreibung enthält eine bestimmte Anzahl von Vorgängen, die für isimpleservice **portType** verfügbar sind, zusammen mit einem Array von [**WS- \_ Vorgangs \_ Beschreibungen**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) , das die einzelnen Vorgänge darstellt, die für den PortType für isimpleservice definiert sind.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-255">This contract description contains the specific number of operations available on the ISimpleService **portType** along with an array of [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) representing the individual operations defined on the portType for ISimpleService.</span></span> <span data-ttu-id="9b3dc-256">Da es nur einen Vorgang für isimpleservice PortType für isimpleservice gibt, gibt es auch nur eine Definition der **WS- \_ Vorgangs \_ Beschreibung** .</span><span class="sxs-lookup"><span data-stu-id="9b3dc-256">Since there is only one operation on ISimpleService portType for ISimpleService, there is also only one **WS\_OPERATION\_DESCRIPTION** definition.</span></span>

``` syntax
...  part of LocalDefinitions structure
{    // array of operations for DefaultBinding_ISimpleService
(WS_OPERATION_DESCRIPTION*)&example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.SimpleMethod,
},    // array of operations for DefaultBinding_ISimpleService
{    // contract description for DefaultBinding_ISimpleService
1,
(WS_OPERATION_DESCRIPTION**)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.operations,
WS_HTTP_CHANNEL_BINDING,
},  // end of contract description for DefaultBinding_ISimpleService
},    // DefaultBinding_ISimpleService       ...
```

## <a name="processing-wsdlservice"></a><span data-ttu-id="9b3dc-257">Verarbeiten von WSDL: Service</span><span class="sxs-lookup"><span data-stu-id="9b3dc-257">Processing wsdl:service</span></span>

<span data-ttu-id="9b3dc-258">WsUtil.exe verwendet die-Dienste, um Bindungs-/PortTypes zu suchen, und generiert eine Vertragsstruktur, die Typen, Message, portType-Definitionen usw. beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-258">WsUtil.exe uses the services to find binding/porttypes, and generates contract structure that describes types, message, porttype definitions, and so on.</span></span> <span data-ttu-id="9b3dc-259">Vertrags Beschreibungen sind extern zugänglich und werden als Teil der globalen Definitions Struktur generiert, die durch den generierten Header angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-259">Contract descriptions are externally accessible, and they are generated as part of the global definition structure specified through generated header.</span></span>

<span data-ttu-id="9b3dc-260">WsUtil.exe unterstützt in WSDL: Port definierte endpointreferenzierungserweiterungen.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-260">WsUtil.exe supports EndpointReference extensions defined in wsdl:port.</span></span> <span data-ttu-id="9b3dc-261">Der Endpunkt Verweis wird in der WS-Adressierung als Möglichkeit zum Beschreiben von [Endpunkt](endpoint-address.md) Informationen eines dienstanweises definiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-261">Endpoint reference is defined in WS-ADDRESSING as a way to describe [endpoint](endpoint-address.md) information of a service.</span></span> <span data-ttu-id="9b3dc-262">Der in der [**\_ XML- \_ Zeichenfolge**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)gespeicherte Eingabe Endpunkt-Verweis Erweiterungs Text und die entsprechende [**Beschreibung der WS- \_ Endpunkt \_ Adresse \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) werden im Abschnitt "endpointreferences" der globalen Struktur generiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-262">The input endpoint reference extension text saved as [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string), together with matching [**WS\_ENDPOINT\_ADDRESS\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) are generated in endpointReferences section in the global structure.</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:service name="SimpleService">
  <wsdl:port name="ISimpleService" binding="tns:DefaultBinding_ISimpleService">
   <soap:address location="http://Example.org/ISimpleService" />
   <wsa:EndpointReference>
    <wsa:Address>http://example.org/wcfmetadata/WSHttpNon</wsa:Address>
   </wsa:EndpointReference> 
  </wsdl:port>
 </wsdl:service>
</wsdl:definitions>
```

``` syntax
  const _example_wsdl example_wsdl =
  {
  ... // global element description
  {// messages
  {    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethod,
},    // message description for ISimpleService_SimpleMethod_InputMessage
{    // message description for ISimpleService_SimpleMethod_OutputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_OutputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodResponse,
},    // message description for ISimpleService_SimpleMethod_OutputMessage
}, // messages
{// contracts
{   // DefaultBinding_ISimpleService
1,
(WS_OPERATION_DESCRIPTION**)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.operations,
WS_HTTP_CHANNEL_BINDING,
},    // end of DefaultBinding_ISimpleService
    }, // contracts
    {
        {
            {   // endpointAddressDescription
                WS_ADDRESSING_VERSION_0_9,
            },                    
            (WS_XML_STRING*)&xml_string_generated_in_stub // endpointReferenceString
        }, //DefaultBinding_ISimpleService
    }, // endpointReferences
}
```

<span data-ttu-id="9b3dc-263">So erstellen Sie eine [**WS- \_ Endpunkt \_ Adresse**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) mithilfe der von wsutil generierten Metadaten:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-263">To Create [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) using the WsUtil generated metadata:</span></span>

``` syntax
WsCreateReader      // Create a WS_XML_READER
Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput          // Set the encoding and input of the reader to generated endpointReferenceString
WsReadType        // Read WS_ENDPOINT_ADDRESS from the reader
    // Using WS_ELEMENT_TYPE_MAPPING, WS_ENDPOINT_ADDRESS_TYPE and generated endpointAddressDescription, 
```

<span data-ttu-id="9b3dc-264">Konstante Zeichen folgen im Client Proxy oder Dienst-Stub werden als Felder vom Typ "WS \_ XML String" generiert \_ , und es gibt ein konstantes Wörterbuch für alle Zeichen folgen in der Proxy-oder Stubdatei.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-264">Constant strings in the client proxy or service stub are generated as fields of type WS\_XML\_STRING, and there is a constant dictionary for all the strings in the proxy or stub file.</span></span> <span data-ttu-id="9b3dc-265">Jede Zeichenfolge im Wörterbuch wird als Feld im Wörterbuch Teil der lokalen Struktur generiert, um die Lesbarkeit zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-265">Each string in the dictionary is generated as a field in the dictionary part of the local structure for better readability.</span></span>

``` syntax
... // dictionary part of LocalDefinitions structure
{    // xmlStrings
  { // xmlStrings
    WS_XML_STRING_DICTIONARY_VALUE("a",&example_wsdlLocalDefinitions.dictionary.dict, 0), 
    WS_XML_STRING_DICTIONARY_VALUE("http://Sapphire.org",&example_wsdlLocalDefinitions.dictionary.dict, 1), 
    WS_XML_STRING_DICTIONARY_VALUE("b",&example_wsdlLocalDefinitions.dictionary.dict, 2), 
    WS_XML_STRING_DICTIONARY_VALUE("SimpleMethod",&example_wsdlLocalDefinitions.dictionary.dict, 3),
    ...
  },  // end of xmlStrings
  {   // SimpleServicedictionary
    // 45026280-d5dc-4570-8195-4d66d13bfa34
    { 0x45026280, 0xd5dc, 0x4570, { 0x81, 0x95, 0x4d,0x66, 0xd1, 0x3b, 0xfa, 0x34 } },
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings,
    stringCount,
    TRUE,
  },
}
...
```

## <a name="processing-wsdltype"></a><span data-ttu-id="9b3dc-266">Verarbeiten von WSDL: Type</span><span class="sxs-lookup"><span data-stu-id="9b3dc-266">Processing wsdl:type</span></span>

<span data-ttu-id="9b3dc-267">Wsutil.exe unterstützt nur XML-Schema Dokumente (XSD) in der WSDL: Type-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-267">Wsutil.exe only supports XML schema (XSD) documents in wsdl:type specification.</span></span> <span data-ttu-id="9b3dc-268">Ein Sonderfall ist, wenn ein Nachrichtenport eine globale Element Definition angibt.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-268">One special case is when a message port specifies a global element definition.</span></span> <span data-ttu-id="9b3dc-269">Weitere Informationen zu den in diesen Fällen verwendeten Heuristiken finden Sie im folgenden Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-269">See the following section for more details of the heuristics used in these cases.</span></span>

## <a name="parameter-processing-heuristics"></a><span data-ttu-id="9b3dc-270">Parameterverarbeitungs-Heuristik</span><span class="sxs-lookup"><span data-stu-id="9b3dc-270">Parameter Processing Heuristics</span></span>

<span data-ttu-id="9b3dc-271">Im Dienstmodell werden WSDL-Nachrichten bestimmten Parametern in einer Methode zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-271">In the service model, WSDL messages are mapped to specific parameters in a method.</span></span> <span data-ttu-id="9b3dc-272">Wsutil.exe hat zwei Stile der Parameter Generierung: im ersten Stil hat der Vorgang einen Parameter für die Eingabe Nachricht und einen Parameter für die Ausgabe Meldung (falls erforderlich). im zweiten Stil verwendet Wsutil.exe eine Heuristik, um Felder in den Strukturen sowohl für Eingabe-als auch für Ausgabe Nachrichten zu unterschiedlichen Parametern des Vorgangs zuzuordnen und zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-272">Wsutil.exe has two styles of parameter generation: in first style, the operation has one parameter for input message, and one parameter for output message (if necessary); in the second style, Wsutil.exe uses a heuristic to map and expand fields in the structures for both input messages and output messages to different parameters in the operation.</span></span> <span data-ttu-id="9b3dc-273">Sowohl Eingabe-als auch Ausgabe Nachrichten müssen den Strukturtyp "Message"-Elemente aufweisen, um diesen zweiten Ansatz zu generieren.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-273">Both input and output messages need to have structure type message elements to generate this second approach.</span></span>

<span data-ttu-id="9b3dc-274">Beim Erstellen von Vorgangs Parametern aus den Eingabe-und Ausgabe Nachrichten werden Wsutil.exe folgende Regeln verwendet:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-274">Wsutil.exe uses the following rules when generating operation parameters from the input and output messages:</span></span>

-   <span data-ttu-id="9b3dc-275">Bei Eingabe-und Ausgabe Nachrichten mit mehreren Nachrichten teilen ist jeder Nachrichten Teil ein separater Parameter im Vorgang, wobei der Nachrichten Teil Name als Parameter Name angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-275">For input and output messages with multiple message parts, each message part is a separate parameter in the operation, with the message part name as parameter name.</span></span>
-   <span data-ttu-id="9b3dc-276">Bei einer Nachricht im RPC-Stil mit einem Nachrichten Teil ist der Nachrichten Teil ein Parameter im Vorgang, wobei der Nachrichten Teil Name als Parameter Name angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-276">For RPC style message with one message part, the message part is a parameter in the operation, with message part name as parameter name.</span></span>
-   <span data-ttu-id="9b3dc-277">Für Eingabe-und Ausgabe Nachrichten im Dokument Stil mit einem Nachrichten Teil:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-277">For document-style input and output messages with one message part:</span></span>
    -   <span data-ttu-id="9b3dc-278">Wenn der Name eines Nachrichten Teils "Parameters" und der Elementtyp eine Struktur ist, wird jedes Feld in der Struktur als separater Parameter behandelt, wobei der Feldname dem Parameternamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-278">If the name of a message part is "parameters" and the element type is a structure, each field in the structure is treated as a separate parameter with the field name being the parameter name.</span></span>
    -   <span data-ttu-id="9b3dc-279">Wenn der Nachrichten Teil Name nicht "Parameters" ist, handelt es sich bei der Nachricht um einen Parameter im Vorgang mit dem Nachrichten Namen, der als entsprechender Parameter Name verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-279">If the message part name is not "parameters", the message is a parameter in the operation with the message name used as the corresponding parameter name.</span></span>
-   <span data-ttu-id="9b3dc-280">Für eine Eingabe-und Ausgabe Nachricht im Dokument Stil mit einem nillable-Element wird die Nachricht einem Parameter zugeordnet, wobei der Nachrichten Teil Name als Parameter Name angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-280">For document style input and output message with nillable element, the message is mapped to one parameter, with message part name as parameter name.</span></span> <span data-ttu-id="9b3dc-281">Eine zusätzliche Dereferenzierungsebene wird hinzugefügt, um anzugeben, dass der Zeiger **null** sein kann.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-281">One additional level of indirection is added to indicate the pointer can be **NULL**.</span></span>
-   <span data-ttu-id="9b3dc-282">Wenn ein Feld nur im Input Message-Element angezeigt wird, wird das Feld als \[ in- \] Parameter behandelt.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-282">If a field appears in the input message element only, the field is treated as an \[in\] parameter.</span></span>
-   <span data-ttu-id="9b3dc-283">Wenn ein Feld nur im Ausgabe Nachrichten Element angezeigt wird, wird das Feld als out- \[ \] Parameter behandelt.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-283">If a field appears in the output message element only, the field is treated as an \[out\] parameter.</span></span>
-   <span data-ttu-id="9b3dc-284">Wenn ein Feld mit dem gleichen Namen und dem gleichen Typ vorhanden ist, das sowohl in der Eingabe Nachricht als auch in der Ausgabe Meldung angezeigt wird, wird das Feld als \[ in-, out- \] Parameter behandelt.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-284">If there is a field with the same name and same type that appears in both the input message and the output message, the field is treated as an \[in,out\] parameter.</span></span>

<span data-ttu-id="9b3dc-285">Die folgenden Tools werden verwendet, um die Richtung der Parameter zu bestimmen:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-285">Following tools are used to determine the direction of parameters:</span></span>

-   <span data-ttu-id="9b3dc-286">Wenn ein Feld nur im Eingabe Nachrichten Element angezeigt wird, wird das Feld als einziger Parameter behandelt.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-286">If a field appears in input message element only, the field is treated as in only parameter.</span></span>
-   <span data-ttu-id="9b3dc-287">Wenn ein Feld nur im Ausgabe Nachrichten Element angezeigt wird, wird das Feld als nur Out-Parameter behandelt.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-287">If a field appears in output message element only, the field is treated as out only parameter.</span></span>
-   <span data-ttu-id="9b3dc-288">Wenn ein Feld mit dem gleichen Namen und dem gleichen Typ vorhanden ist, das sowohl in der Eingabe-als auch in der Ausgabe Meldung angezeigt wird, wird das Feld als in-, out-Parameter behandelt.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-288">If there is a field with the same name and same type that appears in both input message and output message, the field is treated as an in,out parameter.</span></span>

<span data-ttu-id="9b3dc-289">Wsutil.exe unterstützt nur sequenzierte Elemente.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-289">Wsutil.exe only supports sequenced elements.</span></span> <span data-ttu-id="9b3dc-290">Sie lehnt ungültige Reihen \[ Folge in, out- \] Parameter ab, wenn Wsutil.exe die in-Parameter und out-Parameter nicht in einer einzelnen Parameterliste kombinieren kann.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-290">It rejects invalid ordering with regard to \[in,out\] parameters if Wsutil.exe cannot combine the in parameters and out parameters into a single parameter list.</span></span> <span data-ttu-id="9b3dc-291">Suffixe können Parameternamen hinzugefügt werden, um Namenskollisionen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-291">Suffixes might be added to parameter names to avoid name collision.</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

<span data-ttu-id="9b3dc-292">Wsutil.exe berücksichtigt Felder in TNS: simplemethod-und TNS: simplemethodresponse-ATO-Parametern, wie in den folgenden Parameter Definitionen zu sehen ist:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-292">Wsutil.exe considers fields in tns:SimpleMethod and tns:SimpleMethodResponse ato be parameters, as seen in the parameter definitions below:</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
  targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
   <xs:import namespace="http://Example.org" />
   <xs:element name="SimpleMethod">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="a" type="xs:unsignedInt" />
      <xs:element name="b" type="xs:unsignedInt" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
   <xs:element name="SimpleMethodResponse">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="b" type="xs:unsignedInt" />
      <xs:element name="c" type="xs:unsignedInt" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
  </xs:schema>
 </wsdl:types>
</wsdl:definitions>
```

<span data-ttu-id="9b3dc-293">Wsutil.exe erweitert die Parameterliste aus den Feldern in der obigen Liste und generiert die **paramstruct** -Struktur im folgenden Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-293">Wsutil.exe expands the parameter list from the fields in the list above, and generates the **ParamStruct** structure in the following code example.</span></span> <span data-ttu-id="9b3dc-294">Die Lauf Zeit des Dienst Modells kann diese Struktur verwenden, um Argumente an den Client-und den serverstubpunkt zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-294">The service model run-time can use this structure to pass arguments to the client and server stubs.</span></span>

``` syntax
typedef struct SimpleMethodParamStruct {
  unsigned int   a;  
  unsigned int   b;
  unsigned int   c;
} ;
```

<span data-ttu-id="9b3dc-295">Diese Struktur wird nur verwendet, um den Stapel Rahmen auf Client-und Serverseite zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-295">This structure is only used to describe the stack frame on the client and server side.</span></span> <span data-ttu-id="9b3dc-296">Es gibt keine Änderung an der Nachrichten Beschreibung oder an den Element Beschreibungen, auf die in der Nachrichten Beschreibung verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-296">There is no change to the message description, or to the element descriptions referenced by the message description.</span></span>

``` syntax
  // following are local definitions for the complex type
  { // field description for a
  WS_ELEMENT_FIELD_MAPPING,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_INT32_TYPE,
  0,
  WsOffsetOf(_SimpleMethod, a),
  0,
  0,
  },    // end of field description for a
  { // field description for b
  WS_ELEMENT_FIELD_MAPPING,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.bLocalName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_INT32_TYPE,
  0,
  WsOffsetOf(_SimpleMethod, b),
  0,
  0,
  },    // end of field description for b
  {    // fields description for _SimpleMethod
  (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.a,
  (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.b,
  },
  {  // structure definition
  sizeof(_SimpleMethod),
  __alignof(_SimpleMethod),
  (WS_FIELD_DESCRIPTION**)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs._SimpleMethodFields,
  WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs._SimpleMethodFields),
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings._SimpleMethodTypeName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  0,
  },   // struct description for _SimpleMethod
  // following are global definitions for the out parameter
  ...
  {  // element description
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings._SimpleMethodTypeName,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_STRUCT_TYPE,
  (void *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.structDesc,
  },
  {    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethod,
  },    // message description for ISimpleService_SimpleMethod_InputMessage
```

<span data-ttu-id="9b3dc-297">Als allgemeine Regel wird eine Dereferenzierungsebene für alle \[ out \] -und \[ in-, out- \] Parameter hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-297">As a general rule, one level of indirection is added for all the \[out\] and \[in,out\] parameters.</span></span>

## <a name="parameterless-operation"></a><span data-ttu-id="9b3dc-298">Parameterloser Vorgang</span><span class="sxs-lookup"><span data-stu-id="9b3dc-298">Parameterless operation</span></span>

<span data-ttu-id="9b3dc-299">Bei Dokument-und literalvorgängen behandelt Wsutil.exe den Vorgang als einen Eingabeparameter und einen Ausgabeparameter, wenn Folgendes vorhanden ist:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-299">For document and literal operations, Wsutil.exe treats the operation as having one input parameter and one output parameter if:</span></span>

-   <span data-ttu-id="9b3dc-300">Die Eingabe-oder Ausgabe Nachricht verfügt über mehr als einen Teil.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-300">The input or output message has more than one part.</span></span>
-   <span data-ttu-id="9b3dc-301">Es ist nur ein Nachrichten Teil vorhanden, und der Nachrichten Teil Name ist nicht "Parameter".</span><span class="sxs-lookup"><span data-stu-id="9b3dc-301">There is only one message part and the message part name is not "parameters".</span></span>

<span data-ttu-id="9b3dc-302">..</span><span class="sxs-lookup"><span data-stu-id="9b3dc-302">..</span></span> <span data-ttu-id="9b3dc-303">Im obigen Beispiel wird angenommen, dass die Nachrichten Teile den Namen " *Parser*" und " *Paramout*" haben, die Methoden Signatur wird zum folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-303">In the example above, assuming the message parts are named *ParamIn*" and *ParamOut*, the method signature becomes the following code:</span></span>

``` syntax
typedef struct SimpleMethod{
unsigned int a;
unsigned int b;
};

typedef struct SimpleMethodResponse {
unsigned int b;
unsigned int c;
};

typedef  struct ISimpleService_SimpleMethodParamStruct
{
SimpleMethod  * SimpleMethod;
SimpleMethodResponse  * SimpleMethodResponse;
} ISimpleService_SimpleMethodParamStruct;
```

<span data-ttu-id="9b3dc-304">Wsutil.exe generiert eine Versions Signatur für die Vorgangs Beschreibung, sodass die wscall-und die serverseitige Dienstmodell-Engine prüfen können, ob die generierte Beschreibung für die aktuelle Plattform anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-304">Wsutil.exe generates a version signature for the operation description such that the WsCall and server-side service model engine can check if the generated description is applicable for the current platform.</span></span>

<span data-ttu-id="9b3dc-305">Diese Versionsinformationen werden als Teil der WS- [**\_ Vorgangs \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) Struktur generiert.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-305">This version info is generated as part of the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) structure.</span></span> <span data-ttu-id="9b3dc-306">Die Versionsnummer kann als Union-Arm-Selektor behandelt werden, um die Struktur erweiterbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-306">The version number can be treated as a union arm selector to make the structure extensible.</span></span> <span data-ttu-id="9b3dc-307">Derzeit ist die **versionID** auf to1 ohne nachfolgende Felder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-307">Currently, the **versionID** is set to1 with no subsequent fields.</span></span> <span data-ttu-id="9b3dc-308">Zukünftige versios-Versionen erhöhen möglicherweise die Versionsnummer und fügen nach Bedarf weitere Felder ein.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-308">Future versiosn may increment the version number and include more fields as needed.</span></span> <span data-ttu-id="9b3dc-309">Beispielsweise generiert Wsutil.exe aktuell den folgenden Code auf Grundlage der Versions-ID:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-309">For example, Wsutil.exe currently generates the following code based on the version ID:</span></span>

``` syntax
{ // SimpleMethod
{ // parameter descriptions for SimpleMethod
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)0, (USHORT)-1 },
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)1, (USHORT)-1 },
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)-1, (USHORT)1 },
},    // parameter descriptions for SimpleMethod
{    // operation description for SimpleMethod
1,
(WS_MESSAGE_DESCRIPTION*)&example_wsdl.messages.ISimpleService_SimpleMethod_InputMessage,
(WS_MESSAGE_DESCRIPTION*)&example_wsdl.messages.ISimpleService_SimpleMethod_OutputMessage,
3,
(WS_PARAMETER_DESCRIPTION*)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.params,
SimpleMethodOperationStub
}, //operation description for SimpleMethod
},  // SimpleMethod
```

<span data-ttu-id="9b3dc-310">In der Zukunft könnte Sie wie folgt erweitert werden:</span><span class="sxs-lookup"><span data-stu-id="9b3dc-310">In the future, it could be expanded as follows:</span></span>

``` syntax
WS_OPERATION_DESCRIPTION simpleMethodOperationDesc =
{
  2,
  &ISimpleService_SimpleMethod_InputputMessageDesc,
  &ISimpleService_SimpleMethod_OutputMessageDesc,
  WsCountOf(SimpleMethodParameters),
  SimpleMethodParameters,
  ISimpleService_SimpleMethod_Stub,
  &forwardToString;   // just as an example.
};
```

## <a name="security"></a><span data-ttu-id="9b3dc-311">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="9b3dc-311">Security</span></span>

<span data-ttu-id="9b3dc-312">Weitere Informationen finden Sie im Abschnitt "Sicherheit" des Themas " [wsutil Compiler Tool](wsutil-compiler-tool.md) ".</span><span class="sxs-lookup"><span data-stu-id="9b3dc-312">See the security section in the [Wsutil Compiler tool](wsutil-compiler-tool.md) topic.</span></span>

 

 




