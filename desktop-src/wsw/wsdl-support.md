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
# <a name="wsdl-and-service-contracts"></a>WSDL und Dienstverträge

Das [Wsutil.exe](web-service-compiler-tool.md) -Hilfsprogramm generiert einen C-sprachenstub gemäß der bereitgestellten WSDL-Metadaten sowie Datentyp Definitionen und Beschreibungen für Datentypen, die von vom Benutzer erstellten XML-Schemas beschrieben werden.


Im folgenden finden Sie ein Beispiel für ein WSDL-Dokument und ein XML-Schema, das als Grundlage für die nachfolgende Diskussion dient:

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

In diesem Beispiel wird ein Vertrag, isimpleservice, mit einer einzigen Methode, simplemethod, bereitstellt. "Simplemethod" verfügt über zwei Eingabeparameter vom Typ " **Integer**", " *a* " und " *b*", die vom Client an den Dienst gesendet werden. Ebenso hat simplemethod zwei Ausgabeparameter vom Typ " **Integer**", " *b* " und " *c*", die nach erfolgreichem Abschluss an den Client zurückgegeben werden. In der von Sal mit Anmerkungen versehene C-Syntax sieht die Methoden Definition wie folgt aus:

``` syntax
void SimpleMethod(__in int a, __inout int *  b, __out int * c );
```

In dieser Definition ist isimpleservice ein Dienstvertrag mit einem einzelnen Dienst Vorgang: simplemethod.

Die Ausgabe Header Datei enthält Definitionen und Beschreibungen für einen externen Verweis. Dies schließt Folgendes ein:

-   C-Strukturdefinitionen für globale Elementtypen.
-   Ein Vorgangs Prototyp, wie in der aktuellen Datei definiert.
-   Ein Funktionstabellen Prototyp für die Verträge, die in der WSDL-Datei angegeben sind.
-   Client Proxy-und Dienst-Stub-Prototypen für alle in der aktuellen Datei angegebenen Funktionen.
-   Eine [**WS- \_ Element \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) Datenstruktur für die globalen Schema Elemente, die in der aktuellen Datei definiert sind.
-   Eine [**WS- \_ Nachrichten \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) Datenstruktur für alle Nachrichten, die in der aktuellen Datei angegeben sind.
-   Eine [**WS- \_ Vertrags \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) Datenstruktur für alle Verträge, die in der aktuellen Datei angegeben sind.

Eine globale Struktur wird generiert, um alle globalen Beschreibungen der Schema Typen und Dienstmodell Typen zu kapseln, auf die die Anwendung verweisen kann. Die Struktur wird unter Verwendung eines normalisierten Datei namens benannt. In diesem Beispiel generiert Wsutil.exe eine globale Definitions Struktur mit dem Namen "example \_ WSDL", die alle Webdienst Beschreibungen enthält. Die Struktur Definition wird in der Stubdatei generiert.

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

Für globale Element Definitionen im XML-Schema Dokument (XSD) werden ein [**WS- \_ Element- \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) Prototyp sowie die entsprechende C-Typdefinition für jedes der Elemente generiert. Die Prototypen für die Element Beschreibungen für simplemethod und simplemethodresponse werden als Elemente in der obigen Struktur generiert. Die C-Strukturen werden wie folgt generiert:

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

Ähnlich wie bei globalen komplexen Typen generiert Wsutil.exe Typen-C-Strukturdefinitionen wie oben, ohne übereinstimmende Element Beschreibungen.

Bei der WSDL-Eingabe generiert Wsutil.exe die folgenden Prototypen und Definitionen:

-   Ein [**WS- \_ Nachrichten \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) Prototyp wird für die Nachrichten Beschreibung generiert. Diese Beschreibung kann vom Dienstmodell und der Nachrichten Ebene verwendet werden. Nachrichten Beschreibungs Strukturen sind Felder namens "MessageName" in der globalen Struktur. In diesem Beispiel wird die Nachrichten Beschreibung als isimpleservice- \_ simplemethod- \_ inputmessage-Feld in der isimpleservice- \_ simplemethod- \_ inputmessage-Struktur generiert, wie in der WSDL-Datei angegeben.
-   [**WS \_ Der Prototyp der Vertrags \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) wird für die Vertragsbeschreibung generiert. Diese Beschreibung wird vom Dienstmodell verwendet. Struktur von Vertrags Beschreibungen sind Felder mit dem Namen "Kontoname" in der globalen Struktur. In diesem Beispiel wird die Vertragsbeschreibung als DefaultBinding \_ isimpleservice-Feld in der Struktur " \_ example \_ WSDL" generiert.

Vorgangs-und Typspezifikationen werden sowohl für den Proxy als auch für den Stub gemeinsam und in beiden Dateien generiert. Wsutil.exe generiert nur dann eine Kopie, wenn der Proxy und der Stub in derselben Datei generiert werden.

## <a name="identifier-generation"></a>Bezeichnergenerierung

Die oben aufgeführten automatisch generierten C-Strukturen werden basierend auf dem in der WSDL-Datei angegebenen Namen erstellt. Ein XML-NcName wird in der Regel nicht als gültiger C-Bezeichner betrachtet, und die Namen werden nach Bedarf normalisiert. Hexadezimale Werte werden nicht konvertiert, und häufige Buchstaben wie ': ', '/' und '. ' werden in den Unterstrich ' ' konvertiert, \_ um die Lesbarkeit zu verbessern.

## <a name="header-for-the-stub"></a>Kopfzeile für den Stub

Für jeden Vorgang im Dienstvertrag wird eine Rückruf Routine mit dem Namen " <operationname> Callback" generiert. (Der Vorgang "simplemethod" im Beispiel Dienstvertrag hat z. b. einen generierten Rückruf mit dem Namen "simplemethodcallback".)

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT * context,
  int a, int *b, int *c,
  const WS_ASYNC_CONTEXT *asyncContext,
  WS_ERROR * error);
```

Für jede WSDL- **portType** -Wsutil.exe eine Funktions Tabelle generiert, die **portType** darstellt. Jeder Vorgang für den **portType** verfügt über einen entsprechenden Funktionszeiger auf den Rückruf, der in der Funktions Tabelle enthalten ist.

``` syntax
struct ISimpleServiceMethodTable
{
  ISimpleService_SimpleMethodCallback SimpleMethod;
};
```

Proxy Prototypen werden für alle Vorgänge generiert. Der prototypname ist der Vorgangs Name (in diesem Fall "simplemethod"), der in der WSDL-Datei für den Dienstvertrag angegeben ist.

``` syntax
HRESULT WINAPI SimpleMethod(WS_CHANNEL *channel,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error );
```

## <a name="local-only-description-prototype-generation"></a>Generierung von nur einem lokalen Beschreibungs Prototyp

Die Proxy-und Stub-Dateien enthalten die Definition für die globale Definitions Struktur, einschließlich Prototypen und Definitionen für die Strukturen, die nur lokale Beschreibungen und Client Proxy-/dienststub-Implementierungen enthalten.

Alle Prototypen und Definitionen, die für die Stubdatei lokal sind, werden als Teil einer Kapselungs Struktur generiert. Diese übergeordnete lokale Beschreibungs Struktur bietet eine klare Hierarchie der Beschreibungen, die für die serialisierungsschicht und das Dienstmodell erforderlich sind. Die lokale Beschreibungs Struktur hat Prototypen, die der unten gezeigten ähneln:

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

## <a name="referencing-definitions-from-other-files"></a>Verweisen auf Definitionen aus anderen Dateien

Lokale Definitionen können auf Beschreibungen verweisen, die in einer anderen Datei generiert wurden. Beispielsweise kann die Nachricht in der von der WSDL-Datei generierten c-Codedatei definiert werden, das Message-Element kann jedoch an anderer Stelle in der aus der XSD-Datei generierten c-Codedatei definiert werden. In diesem Fall generiert Wsutil.exe einen Verweis auf das globale Element aus der Datei, die die Nachrichten Definition enthält, wie unten gezeigt:

``` syntax
{  // WS_MESSAGE_DESCRIPTION
...
(WS_ELEMENT_DESRIPTION *)b_xsd.globalElement.<elementname>
  };
```

## <a name="global-element-descriptions"></a>Beschreibungen von globalen Elementen

Für jedes globale Element, das in einer WSDL: Type-oder XSD-Datei definiert ist, gibt es ein entsprechendes Feld mit dem Namen **ElementName** innerhalb des **Global Element** -Felds. In diesem Beispiel wird eine Struktur mit dem Namen simplemethod generiert:

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

Andere Beschreibungen, die für die Element Beschreibung erforderlich sind, werden als Teil der enthaltenden Struktur generiert. Wenn es sich bei dem Element um ein einfaches Typelement handelt, gibt es nur ein [**WS- \_ Element- \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) Feld. Wenn der Elementtyp eine Struktur ist, werden alle zugehörigen Felder und Struktur Beschreibungen als Teil der Elementstruktur generiert. In diesem Beispiel ist das simplemethod-Element eine Struktur, die zwei Felder enthält: **a** und **b**. Wsutil.exe generiert die Struktur wie folgt:

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

Eingebettete Strukturen und eingebettete Elemente werden bei Bedarf als Unterstrukturen generiert.

## <a name="wsdl-related-definitions"></a>WSDL-bezogene Definitionen

Wsutil.exe generiert ein Feld im WSDL-Abschnitt für jeden der **portType** -Werte, die unter dem angegebenen WSDL: Service definiert sind.

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

Wsutil.exe generiert ein Feld f, das alle für den Vorgang erforderlichen Beschreibungen enthält, ein Single-Array von Zeigern auf die einzelnen Vorgangs Beschreibungen für jede Methode und eine [**WS- \_ Vertrags \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) für den angegebenen **portType**.

Alle von Vorgängen benötigten Beschreibungen werden im Feld **OperationName** unter dem angegebenen **portType** generiert. Hierzu gehören das Feld für die [**\_ \_ Beschreibung der WS-Elemente**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) sowie die Unterstruktur für Eingabe-und Ausgabeparameter. Ebenso werden die [**WS- \_ Nachrichten \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) Felder für die Eingabe Nachricht und die optionale Ausgabe Meldung zusammen mit dem [**WS \_ Das Feld für die Parameter \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) Liste für alle Vorgangs Parameter und das [**\_ \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) Feld für die WS-Operation für den Vorgang selbst. In diesem Beispiel wird die Code Struktur für die simplemethod-Beschreibung wie unten gezeigt generiert:

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

## <a name="xml-dictionary-related-definitions"></a>XML-Wörterbuch bezogene Definitionen

Namen und Namespaces, die in verschiedenen Beschreibungen verwendet werden, werden als Felder des Typs " [**WS \_ XML \_ String**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)" generiert. Alle diese Zeichen folgen werden als Teil eines konstanten Verzeichnisses pro Datei generiert. Die Liste der Zeichen folgen und des [**WS- \_ XML- \_ Wörterbuch**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) Felds (mit dem Namen " **dict** " im folgenden Beispiel) werden als Teil des Wörterbuch Felds der dateinamelocal-Struktur generiert. 

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

Das Array von [**WS \_ XML- \_ Zeichen**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)folgen s wird als eine Reihe von Feldern vom Typ " **WS \_ XML \_ String**" generiert, die mit benutzerfreundlichen Namen benannt sind. Der generierte Stub verwendet die benutzerfreundlichen Namen in verschiedenen Beschreibungen, um die Lesbarkeit zu verbessern.

Client Proxy für WSDL-Vorgänge

Wsutil.exe generiert einen Client Proxy für alle Vorgänge. Anwendungen können die Methoden Signatur überschreiben, indem Sie eine Präfix-Befehlszeilenoption verwenden.

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

Der Vorgangs Aufrufer muss einen gültigen *Heap* Parameter übergeben. Ausgabeparameter werden mithilfe des \_ im *Heap* -Parameter angegebenen WS-Heap Werts zugeordnet. Die Aufruf Funktion kann den Heap zurücksetzen oder freigeben, um Speicher für alle Ausgabeparameter freizugeben. Wenn der Vorgang fehlschlägt, können zusätzliche Detail Fehlerinformationen aus dem optionalen Fehler Objekt abgerufen werden, sofern dieses verfügbar ist.

Wsutil.exe generiert einen Dienst-Stub für alle Vorgänge, die in Binding beschrieben werden.

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

Der obige Abschnitt beschreibt den Prototyp der lokalen Struktur, die alle Definitionen enthält, die nur für die Stubdatei lokal sind. In den nachfolgenden Abschnitten werden die Definitionen der Beschreibungen beschrieben.

## <a name="wsdl-definition-generation"></a>WSDL-Definitions Generierung

Wsutil.exe generiert eine Konstante statische (Konstante **statische**) Struktur namens *<Dateiname \_>* localdefinitionen vom Typ *<Dienst \_ Name>* local, das alle lokalen Definitionen enthält.

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

Die folgenden WSDL-Beschreibungen werden unterstützt:

-   WSDL: Service
-   WSDL: Bindung
-   WSDL: portType
-   WSDL: Vorgang
-   WSDL: Meldung

## <a name="processing-wsdloperation-and-wsdlmessage"></a>Verarbeiten von WSDL: Operation und WSDL: Message

Jeder im WSDL-Dokument angegebene Vorgang wird durch [Wsutil.exe](web-service-compiler-tool.md)einem Dienst Vorgang zugeordnet. Das Tool generiert separate Definitionen der Dienst Vorgänge sowohl für den Server als auch für den Client.

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

Das Layout der Eingabe-und Ausgabe Nachrichten Datenelemente wird vom Tool ausgewertet, um die Serialisierungsmetadaten für die Infrastruktur zusammen mit der tatsächlichen Signatur des resultierenden Dienst Vorgangs zu generieren, dem die Eingabe-und Ausgabe Nachrichten zugeordnet sind.

Die Metadaten für jeden Vorgang in einem bestimmten **portType** haben eine Eingabe und optional eine Ausgabe Meldung. jede dieser Nachrichten wird einer [**WS- \_ Nachrichten \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)zugeordnet. In diesem Beispiel werden die Eingabe-und die Ausgabe Meldung für den Vorgang im PortType in "inputmessagedescription" und optional für "outputmessagedescription" in der [**WS- \_ Vorgangs \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) zugeordnet.

Für jede WSDL-Nachricht generiert das Tool eine [**WS- \_ Nachrichten \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) , die auf die Definition der [**WS- \_ Element \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) verweist, wie unten gezeigt:

``` syntax
... 
{    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

Die Nachrichten Beschreibung verweist auf die Beschreibung des Eingabe Elements. Da das-Element global definiert ist, verweist die Nachrichten Beschreibung auf die globale Definition anstatt auf das lokale statische Element. Wenn das Element in einer anderen Datei definiert ist, generiert Wsutil.exe einen Verweis auf die global definierte Struktur in dieser Datei. Wenn simplemethodresponse z. b. in einer anderen XSD-Beispieldatei definiert ist, generiert Wsutil.exe stattdessen Folgendes:

``` syntax
...
{    // message description for ISimpleService_SimpleMethod_InputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_xsd.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

Jede Nachrichten Beschreibung enthält die Aktion und die spezifische Element Beschreibung (ein Feld vom Typ " [**WS- \_ Element \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)") für alle Nachrichten Datenelemente. Bei einer Nachricht im RPC-Stil oder einer Nachricht mit mehreren Teilen wird ein Wrapper Element erstellt, um die zusätzlichen Informationen zu kapseln.

## <a name="rpc-style-support"></a>RPC-Formatunterstützung

Wsutil.exe unterstützt Dokument-und RPC-Formatvorlagen gemäß der WSDL 1,1-Bindungs Erweiterung für SOAP 1,2. Vorgänge im RPC-und literalstil werden als WS- \_ RPC- \_ \_ literalvorgang gekennzeichnet. Das Dienstmodell ignoriert den Namen für das Antworttext-Wrapper Element in RPC/literalvorgängen.

Wsutil.exe bietet keine systemeigene Unterstützung für Codierungs Vorgänge. Der WS \_ XML \_ -Puffer Parameter wird für Codierungs Nachrichten generiert, und Entwickler müssen den nicht transparenten Puffer direkt auffüllen.

## <a name="multiple-message-parts-support"></a>Unterstützung mehrerer Nachrichten Teile

Wsutil.exe unterstützt mehrere Nachrichten Teile in einer Nachricht. Eine mehrteilige Nachricht kann wie folgt angegeben werden:

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

Wsutil.exe generiert ein Feld vom [**Typ "WS \_ struct \_ Type**](/windows/desktop/api/WebServices/ne-webservices-ws_type) " für das Message-Element, wenn die Nachricht mehrere Teile enthält. Wenn die Meldung mit dem Dokument Stil dargestellt wird, generiert Wsutil.exe ein Wrapper Element mit einem Strukturtyp. Das Wrapper Element weist keinen Namen oder einen bestimmten Namespace auf, und die Wrapper Struktur enthält alle Elemente in allen Teilen als Felder. Das Wrapper Element ist nur für die interne Verwendung vorgesehen und wird nicht im Nachrichtentext serialisiert.

Wenn die Nachricht eine RPC-oder Literale Darstellung verwendet, erstellt Wsutil.exe ein Wrapper Element mit dem Vorgangs Namen als Elementnamen und dem angegebenen Namespace als Dienst Namespace entsprechend der WSDL-SOAP-Erweiterungs Spezifikation. Die Struktur des-Elements enthält ein Array von Feldern, die die in den Nachrichten teilen angegebenen Typen darstellen. Das Wrapper Element wird dem eigentlichen obersten Element im Nachrichtentext zugeordnet, wie in der SOAP-Spezifikation angegeben.

Auf der Serverseite ergibt jeder Vorgang eine typedef des resultierenden Server Dienst Vorgangs. Diese typedef wird verwendet, um auf den Vorgang in der Funktions Tabelle wie zuvor beschrieben zu verweisen. Jeder Vorgang führt auch zur Generierung einer Stub-Funktion, die nfrastructure im Namen des Delegaten an die tatsächliche Methode aufruft.

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

Für den simplemethod-Vorgang wird die simplemethodoperation-typedef oben definiert. Beachten Sie, dass die generierte Methode über ein erweitertes Argument mit dem Nachrichten Teil für den Eingabe-und Ausgabe Nachrichten Vorgang für den simplemethod-Vorgang als benannte Parameter verfügt.

Auf der Clientseite wird jeder Vorgang einem Proxy Dienst Vorgang zugeordnet.

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

## <a name="processing-wsdlbinding"></a>Verarbeiten von WSDL: Binding

Das wwsapi-Dienstmodell unterstützt die thesoap-Bindungs Erweiterung. Für jede Bindung ist ein **portType** zugeordnet.

Der in der SOAP-Bindungs Erweiterung angegebene Transport ist nur eine Empfehlung. Die Anwendung muss Transportinformationen bereitstellen, wenn ein Kanal erstellt wird. Zurzeit unterstützen wir die WS \_ \_ -HTTP-Bindung und die WS \_ TCP- \_ Bindungs Bindungen.

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

In unserem Beispiel-WSDL-Dokument haben wir nur einen **portType** für isimpleservice. Die bereitgestellte SOAP-Bindung gibt den HTTP-Transport an, der als WS-HTTP-Bindung angegeben wird \_ \_ . Beachten Sie, dass diese Struktur nicht über eine statische Dekoration verfügt, da diese Struktur für die Anwendung verfügbar sein muss.

Verarbeiten von WSDL: portType

Jeder **portType** in WSDL besteht aus mindestens einem Vorgang. Der Vorgang sollte mit der SOAP-Bindungs Erweiterung übereinstimmen, die in WSDL: Binding angegeben ist.

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

In diesem Beispiel enthält der isimpleservice- **portType** nur den simplemethod-Vorgang. Dies stimmt mit dem Bindungs Abschnitt überein, bei dem es nur einen WSDL-Vorgang gibt, der einer SOAP-Aktion zugeordnet ist.

Da der isimpleservice- **portType** nur einen Vorgang aufweist (-simplemethod), enthält die entsprechende Funktions Tabelle nur simplemethod als Dienst Vorgang.

Im Hinblick auf die Metadaten werden die einzelnen **portType** Wsutil.exe einer [**WS- \_ Vertrags \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)zugeordnet. Jeder Vorgang in einem **portType** wird einer WS- [**\_ Vorgangs \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)zugeordnet.

In diesem Beispiel generiert **portType** das Tool eine [**WS- \_ Vertrags \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) für isimpleservice. Diese Vertragsbeschreibung enthält eine bestimmte Anzahl von Vorgängen, die für isimpleservice **portType** verfügbar sind, zusammen mit einem Array von [**WS- \_ Vorgangs \_ Beschreibungen**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) , das die einzelnen Vorgänge darstellt, die für den PortType für isimpleservice definiert sind. Da es nur einen Vorgang für isimpleservice PortType für isimpleservice gibt, gibt es auch nur eine Definition der **WS- \_ Vorgangs \_ Beschreibung** .

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

## <a name="processing-wsdlservice"></a>Verarbeiten von WSDL: Service

WsUtil.exe verwendet die-Dienste, um Bindungs-/PortTypes zu suchen, und generiert eine Vertragsstruktur, die Typen, Message, portType-Definitionen usw. beschreibt. Vertrags Beschreibungen sind extern zugänglich und werden als Teil der globalen Definitions Struktur generiert, die durch den generierten Header angegeben wird.

WsUtil.exe unterstützt in WSDL: Port definierte endpointreferenzierungserweiterungen. Der Endpunkt Verweis wird in der WS-Adressierung als Möglichkeit zum Beschreiben von [Endpunkt](endpoint-address.md) Informationen eines dienstanweises definiert. Der in der [**\_ XML- \_ Zeichenfolge**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)gespeicherte Eingabe Endpunkt-Verweis Erweiterungs Text und die entsprechende [**Beschreibung der WS- \_ Endpunkt \_ Adresse \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) werden im Abschnitt "endpointreferences" der globalen Struktur generiert.

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

So erstellen Sie eine [**WS- \_ Endpunkt \_ Adresse**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) mithilfe der von wsutil generierten Metadaten:

``` syntax
WsCreateReader      // Create a WS_XML_READER
Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput          // Set the encoding and input of the reader to generated endpointReferenceString
WsReadType        // Read WS_ENDPOINT_ADDRESS from the reader
    // Using WS_ELEMENT_TYPE_MAPPING, WS_ENDPOINT_ADDRESS_TYPE and generated endpointAddressDescription, 
```

Konstante Zeichen folgen im Client Proxy oder Dienst-Stub werden als Felder vom Typ "WS \_ XML String" generiert \_ , und es gibt ein konstantes Wörterbuch für alle Zeichen folgen in der Proxy-oder Stubdatei. Jede Zeichenfolge im Wörterbuch wird als Feld im Wörterbuch Teil der lokalen Struktur generiert, um die Lesbarkeit zu verbessern.

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

## <a name="processing-wsdltype"></a>Verarbeiten von WSDL: Type

Wsutil.exe unterstützt nur XML-Schema Dokumente (XSD) in der WSDL: Type-Spezifikation. Ein Sonderfall ist, wenn ein Nachrichtenport eine globale Element Definition angibt. Weitere Informationen zu den in diesen Fällen verwendeten Heuristiken finden Sie im folgenden Abschnitt.

## <a name="parameter-processing-heuristics"></a>Parameterverarbeitungs-Heuristik

Im Dienstmodell werden WSDL-Nachrichten bestimmten Parametern in einer Methode zugeordnet. Wsutil.exe hat zwei Stile der Parameter Generierung: im ersten Stil hat der Vorgang einen Parameter für die Eingabe Nachricht und einen Parameter für die Ausgabe Meldung (falls erforderlich). im zweiten Stil verwendet Wsutil.exe eine Heuristik, um Felder in den Strukturen sowohl für Eingabe-als auch für Ausgabe Nachrichten zu unterschiedlichen Parametern des Vorgangs zuzuordnen und zu erweitern. Sowohl Eingabe-als auch Ausgabe Nachrichten müssen den Strukturtyp "Message"-Elemente aufweisen, um diesen zweiten Ansatz zu generieren.

Beim Erstellen von Vorgangs Parametern aus den Eingabe-und Ausgabe Nachrichten werden Wsutil.exe folgende Regeln verwendet:

-   Bei Eingabe-und Ausgabe Nachrichten mit mehreren Nachrichten teilen ist jeder Nachrichten Teil ein separater Parameter im Vorgang, wobei der Nachrichten Teil Name als Parameter Name angegeben wird.
-   Bei einer Nachricht im RPC-Stil mit einem Nachrichten Teil ist der Nachrichten Teil ein Parameter im Vorgang, wobei der Nachrichten Teil Name als Parameter Name angegeben wird.
-   Für Eingabe-und Ausgabe Nachrichten im Dokument Stil mit einem Nachrichten Teil:
    -   Wenn der Name eines Nachrichten Teils "Parameters" und der Elementtyp eine Struktur ist, wird jedes Feld in der Struktur als separater Parameter behandelt, wobei der Feldname dem Parameternamen entspricht.
    -   Wenn der Nachrichten Teil Name nicht "Parameters" ist, handelt es sich bei der Nachricht um einen Parameter im Vorgang mit dem Nachrichten Namen, der als entsprechender Parameter Name verwendet wird.
-   Für eine Eingabe-und Ausgabe Nachricht im Dokument Stil mit einem nillable-Element wird die Nachricht einem Parameter zugeordnet, wobei der Nachrichten Teil Name als Parameter Name angegeben wird. Eine zusätzliche Dereferenzierungsebene wird hinzugefügt, um anzugeben, dass der Zeiger **null** sein kann.
-   Wenn ein Feld nur im Input Message-Element angezeigt wird, wird das Feld als \[ in- \] Parameter behandelt.
-   Wenn ein Feld nur im Ausgabe Nachrichten Element angezeigt wird, wird das Feld als out- \[ \] Parameter behandelt.
-   Wenn ein Feld mit dem gleichen Namen und dem gleichen Typ vorhanden ist, das sowohl in der Eingabe Nachricht als auch in der Ausgabe Meldung angezeigt wird, wird das Feld als \[ in-, out- \] Parameter behandelt.

Die folgenden Tools werden verwendet, um die Richtung der Parameter zu bestimmen:

-   Wenn ein Feld nur im Eingabe Nachrichten Element angezeigt wird, wird das Feld als einziger Parameter behandelt.
-   Wenn ein Feld nur im Ausgabe Nachrichten Element angezeigt wird, wird das Feld als nur Out-Parameter behandelt.
-   Wenn ein Feld mit dem gleichen Namen und dem gleichen Typ vorhanden ist, das sowohl in der Eingabe-als auch in der Ausgabe Meldung angezeigt wird, wird das Feld als in-, out-Parameter behandelt.

Wsutil.exe unterstützt nur sequenzierte Elemente. Sie lehnt ungültige Reihen \[ Folge in, out- \] Parameter ab, wenn Wsutil.exe die in-Parameter und out-Parameter nicht in einer einzelnen Parameterliste kombinieren kann. Suffixe können Parameternamen hinzugefügt werden, um Namenskollisionen zu vermeiden.

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

Wsutil.exe berücksichtigt Felder in TNS: simplemethod-und TNS: simplemethodresponse-ATO-Parametern, wie in den folgenden Parameter Definitionen zu sehen ist:

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

Wsutil.exe erweitert die Parameterliste aus den Feldern in der obigen Liste und generiert die **paramstruct** -Struktur im folgenden Codebeispiel. Die Lauf Zeit des Dienst Modells kann diese Struktur verwenden, um Argumente an den Client-und den serverstubpunkt zu übergeben.

``` syntax
typedef struct SimpleMethodParamStruct {
  unsigned int   a;  
  unsigned int   b;
  unsigned int   c;
} ;
```

Diese Struktur wird nur verwendet, um den Stapel Rahmen auf Client-und Serverseite zu beschreiben. Es gibt keine Änderung an der Nachrichten Beschreibung oder an den Element Beschreibungen, auf die in der Nachrichten Beschreibung verwiesen wird.

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

Als allgemeine Regel wird eine Dereferenzierungsebene für alle \[ out \] -und \[ in-, out- \] Parameter hinzugefügt.

## <a name="parameterless-operation"></a>Parameterloser Vorgang

Bei Dokument-und literalvorgängen behandelt Wsutil.exe den Vorgang als einen Eingabeparameter und einen Ausgabeparameter, wenn Folgendes vorhanden ist:

-   Die Eingabe-oder Ausgabe Nachricht verfügt über mehr als einen Teil.
-   Es ist nur ein Nachrichten Teil vorhanden, und der Nachrichten Teil Name ist nicht "Parameter".

.. Im obigen Beispiel wird angenommen, dass die Nachrichten Teile den Namen " *Parser*" und " *Paramout*" haben, die Methoden Signatur wird zum folgenden Code:

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

Wsutil.exe generiert eine Versions Signatur für die Vorgangs Beschreibung, sodass die wscall-und die serverseitige Dienstmodell-Engine prüfen können, ob die generierte Beschreibung für die aktuelle Plattform anwendbar ist.

Diese Versionsinformationen werden als Teil der WS- [**\_ Vorgangs \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) Struktur generiert. Die Versionsnummer kann als Union-Arm-Selektor behandelt werden, um die Struktur erweiterbar zu machen. Derzeit ist die **versionID** auf to1 ohne nachfolgende Felder festgelegt. Zukünftige versios-Versionen erhöhen möglicherweise die Versionsnummer und fügen nach Bedarf weitere Felder ein. Beispielsweise generiert Wsutil.exe aktuell den folgenden Code auf Grundlage der Versions-ID:

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

In der Zukunft könnte Sie wie folgt erweitert werden:

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

## <a name="security"></a>Sicherheit

Weitere Informationen finden Sie im Abschnitt "Sicherheit" des Themas " [wsutil Compiler Tool](wsutil-compiler-tool.md) ".

 

 




