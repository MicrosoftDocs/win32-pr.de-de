---
title: WSDL und Dienstverträge
description: Das Wsutil.exe-Hilfsprogramm generiert einen Stub der Programmiersprache C gemäß den angegebenen WSDL-Metadaten sowie Datentypdefinitionen und Beschreibungen für Datentypen, die von vom Benutzer erstellten XML-Schemas beschrieben werden.
ms.assetid: d3c147d6-e370-4e8a-96d8-6660f3a2b996
keywords:
- WSDL-Unterstützung
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 203ee1819a596d2d49a7d0b7c789d5f4e1269b6d8d75f78e2db0913b6a97ec78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880740"
---
# <a name="wsdl-and-service-contracts"></a>WSDL und Dienstverträge

Das [](web-service-compiler-tool.md)Wsutil.exe-Hilfsprogramm generiert einen C-Sprachstub gemäß den angegebenen WSDL-Metadaten sowie Datentypdefinitionen und Beschreibungen für Datentypen, die von vom Benutzer erstellten XML-Schemas beschrieben werden.


Im Folgenden finden Sie ein WSDL-Beispieldokument und EIN XML-Schema, das als Grundlage für die folgende Diskussion dient:

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

In diesem Beispiel wird der Vertrag ISimpleService mit einer einzelnen Methode, SimpleMethod, zur Hand. "SimpleMethod" verfügt über zwei Eingabeparameter vom Typ **integer**, *a* und *b*, die vom Client an den Dienst gesendet werden. Ebenso verfügt SimpleMethod über zwei Ausgabeparameter vom Typ integer **,** *b* und *c*, die nach erfolgreichem Abschluss an den Client zurückgegeben werden. In der mit SAL kommentierten C-Syntax wird die Methodendefinition wie folgt angezeigt:

``` syntax
void SimpleMethod(__in int a, __inout int *  b, __out int * c );
```

In dieser Definition ist ISimpleService ein Dienstvertrag mit einem einzelnen Dienstvorgang: SimpleMethod.

Die Ausgabeheaderdatei enthält Definitionen und Beschreibungen für externe Verweise. Dies schließt Folgendes ein:

-   C-Strukturdefinitionen für globale Elementtypen.
-   Ein Vorgangsprototyp, wie in der aktuellen Datei definiert.
-   Ein Funktionstabellenprototyp für die in der WSDL-Datei angegebenen Verträge.
-   Clientproxy- und Dienststubprototypen für alle in der aktuellen Datei angegebenen Funktionen.
-   Eine [**\_ WS-ELEMENTBESCHREIBUNG-Datenstruktur \_**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) für die globalen Schemaelemente, die in der aktuellen Datei definiert sind.
-   Eine [**WS \_ MESSAGE \_ DESCRIPTION-Datenstruktur**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) für alle in der aktuellen Datei angegebenen Nachrichten.
-   Eine [**WS \_ CONTRACT \_ DESCRIPTION-Datenstruktur**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) für alle in der aktuellen Datei angegebenen Verträge.

Eine globale Struktur wird generiert, um alle globalen Beschreibungen für die Schematypen und Dienstmodelltypen zu kapseln, auf die die Anwendung verweisen kann. Die Struktur wird mit einem normalisierten Dateinamen benannt. In diesem Beispiel generiert Wsutil.exe eine globale Definitionsstruktur namens "example \_ wsdl", die alle Webdienstbeschreibungen enthält. Die Strukturdefinition wird in der Stubdatei generiert.

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

Für globale Elementdefinitionen im XML-Schemadokument (XSD) werden ein [**WS \_ ELEMENT \_ DESCRIPTION-Prototyp**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) sowie die entsprechende C-Typdefinition für jedes der Elemente generiert. Die Prototypen für die Elementbeschreibungen für SimpleMethod und SimpleMethodResponse werden als Member in der obigen Struktur generiert. Die C-Strukturen werden wie folgt generiert:

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

Ähnlich wie bei globalen komplexen Typen generiert Wsutil.exe Typ C-Strukturdefinitionen wie oben ohne übereinstimmende Elementbeschreibungen.

Für WSDL-Eingaben generiert Wsutil.exe die folgenden Prototypen und Definitionen:

-   Für die Nachrichtenbeschreibung wird ein Prototyp der [**\_ \_ WS-NACHRICHTENBESCHREIBUNG**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) generiert. Diese Beschreibung kann vom Dienstmodell sowie von der Nachrichtenebene verwendet werden. Nachrichtenbeschreibungsstrukturen sind Felder mit dem Namen "messagename" in der globalen Struktur. In diesem Beispiel wird die Nachrichtenbeschreibung als ISimpleService \_ SimpleMethod InputMessage-Feld in der \_ ISimpleService SimpleMethod InputMessage-Struktur generiert, wie in der \_ \_ WSDL-Datei angegeben.
-   [**WS \_ Der CONTRACT \_ DESCRIPTION-Prototyp**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) wird für die Vertragsbeschreibung generiert. Diese Beschreibung wird vom Dienstmodell verwendet. Vertragsbeschreibungsstrukturen sind Felder mit dem Namen "contractname" in der globalen Struktur. In diesem Beispiel wird die Vertragsbeschreibung als DefaultBinding \_ ISimpleService-Feld in der Struktur \_ "example \_ wsdl" generiert.

Vorgangs- und Typspezifikationen gelten sowohl für Proxys als auch für Stubs und werden in beiden Dateien generiert. Wsutil.exe nur dann eine Kopie, wenn sowohl der Proxy als auch der Stub in derselben Datei generiert werden.

## <a name="identifier-generation"></a>Bezeichnergenerierung

Die oben aufgeführten automatisch generierten C-Strukturen werden basierend auf dem in der WSDL-Datei angegebenen Namen erstellt. Ein XML NCName wird häufig nicht als gültiger C-Bezeichner betrachtet, und die Namen werden bei Bedarf normalisiert. Hexadezimalwerte werden nicht konvertiert, und allgemeine Buchstaben wie ":", "/" und "." werden in den Unterstrich "" konvertiert, um die \_ Lesbarkeit zu verbessern.

## <a name="header-for-the-stub"></a>Header für den Stub

Für jeden Vorgang im Dienstvertrag wird eine Rückrufroutine mit dem Namen <operationname> "Rückruf" generiert. (Beispielsweise verfügt der Vorgang "SimpleMethod" im Beispieldienstvertrag über einen generierten Rückruf namens "SimpleMethodCallback".)

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT * context,
  int a, int *b, int *c,
  const WS_ASYNC_CONTEXT *asyncContext,
  WS_ERROR * error);
```

Für jeden **WSDL-portTypeWsutil.exe** wird eine Funktionstabelle generiert, die **portType darstellt.** Jeder Vorgang für **portType** verfügt über einen entsprechenden Funktionszeiger auf den Rückruf, der in der Funktionstabelle vorhanden ist.

``` syntax
struct ISimpleServiceMethodTable
{
  ISimpleService_SimpleMethodCallback SimpleMethod;
};
```

Proxyprototypen werden für alle Vorgänge generiert. Der Prototypname ist der Vorgangsname (in diesem Fall "SimpleMethod"), der in der WSDL-Datei für den Dienstvertrag angegeben ist.

``` syntax
HRESULT WINAPI SimpleMethod(WS_CHANNEL *channel,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error );
```

## <a name="local-only-description-prototype-generation"></a>Prototypgenerierung nur für lokale Beschreibungen

Die Proxy- undstubdateien enthalten die Definition für die globale Definitionsstruktur, einschließlich Prototypen und Definitionen für die Strukturen, die nur lokale Beschreibungen und Implementierungen von Clientproxy-/Dienststubs enthalten.

Alle Prototypen und Definitionen, die lokal in der Stubdatei enthalten sind, werden als Teil einer kapselnden Struktur generiert. Diese übergreifende lokale Beschreibungsstruktur bietet eine klare Hierarchie der Beschreibungen, die für die Serialisierungsebene und das Dienstmodell erforderlich sind. Die lokale Beschreibungsstruktur verfügt über Prototypen, die dem unten gezeigten ähneln:

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

Lokale Definitionen können auf Beschreibungen verweisen, die in einer anderen Datei generiert wurden. Beispielsweise kann die Nachricht in der C-Codedatei definiert werden, die aus der WSDL-Datei generiert wurde, aber das Nachrichtenelement kann an anderer Stelle in der aus der XSD-Datei generierten C-Codedatei definiert werden. In diesem Fall generiert Wsutil.exe verweis auf das globale Element aus der Datei, die die Nachrichtendefinition enthält, wie unten gezeigt:

``` syntax
{  // WS_MESSAGE_DESCRIPTION
...
(WS_ELEMENT_DESRIPTION *)b_xsd.globalElement.<elementname>
  };
```

## <a name="global-element-descriptions"></a>Beschreibungen globaler Elemente

Für jedes globale Element, das in einer wsdl:type- oder XSD-Datei definiert ist, befindet sich im **Feld GlobalElement** ein entsprechendes Feld namens **elementName.** In diesem Beispiel wird eine Struktur mit dem Namen SimpleMethod generiert:

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

Andere Beschreibungen, die für die Elementbeschreibung erforderlich sind, werden als Teil der enthaltenden -Struktur generiert. Wenn das Element ein einfaches Typelement ist, gibt es nur ein [**WS \_ ELEMENT \_ DESCRIPTION-Feld.**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) Wenn der Elementtyp eine -Struktur ist, werden alle zugehörigen Felder und Strukturbeschreibungen als Teil der Elementstruktur generiert. In diesem Beispiel ist das SimpleMethod-Element eine -Struktur, die zwei Felder enthält, **und** **b.** Wsutil.exe generiert die -Struktur wie folgt:

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

Wsutil.exe generiert ein Feld im WSDL-Abschnitt für jeden **portType-Wert,** der unter dem angegebenen wsdl:service definiert ist.

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

Wsutil.exe generiert ein Feld f, das alle für den Vorgang erforderlichen Beschreibungen enthält, ein Zeichenarray von Zeigern auf jede der Vorgangsbeschreibungen für jede Methode und eine [**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) für den angegebenen **portType.**

Alle beschreibungen, die von Vorgängen benötigt werden, werden im **Feld operationName** unter dem angegebenen **portType generiert.** Dazu gehören das [**Feld WS \_ ELEMENT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) sowie die Unterstruktur für Eingabe- und Ausgabeparameter. Ebenso werden die [**Felder WS \_ MESSAGE \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) für die Eingabenachricht und die optionale Ausgabenachricht zusammen mit eingeschlossen. [**WS \_ PARAMETER \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) list-Feld für alle Vorgangsparameter und das [**Feld WS OPERATION \_ \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) für den Vorgang selbst. In diesem Beispiel wird die Codestruktur für die SimpleMethod-Beschreibung wie unten dargestellt generiert:

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

## <a name="xml-dictionary-related-definitions"></a>Xml-Wörterbuchbezogene Definitionen

Namen und Namespaces, die in verschiedenen Beschreibungen verwendet werden, werden als Felder vom [**Typ WS \_ XML STRING \_ generiert.**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string) Alle diese Zeichenfolgen werden als Teil eines dateispezifischen Konstantenwörterbuchs generiert. Die Liste der Zeichenfolgen und das [**WS \_ XML \_ DICTIONARY-Feld**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) (im folgenden Beispiel als **dict** bezeichnet) werden als Teil des Wörterbuchfelds der **fileNameLocal-Struktur** generiert.

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

Das Array von [**WS \_ XML \_ STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)s wird als eine Reihe von Feldern vom Typ **WS \_ XML \_ STRING** generiert, die mit benutzerfreundlichen Namen benannt werden. Der generierte Stub verwendet die benutzerfreundlichen Namen in verschiedenen Beschreibungen, um die Lesbarkeit zu verbessern.

Clientproxy für WSDL-Vorgänge

Wsutil.exe generiert einen Clientproxy für alle Vorgänge. Anwendungen können die Methodensignatur mithilfe einer Präfixbefehlszeilenoption überschreiben.

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

Der Vorgangsaufrufer muss einen gültigen *Heapparameter* übergeben. Ausgabeparameter werden mithilfe des im Heapparameter angegebenen \_ WS-HEAP-Werts zugeordnet.  Die aufrufende Funktion kann den Heap zurücksetzen oder freisetzen, um Arbeitsspeicher für alle Ausgabeparameter frei zu geben. Wenn der Vorgang fehlschlägt, können zusätzliche Detailfehlerinformationen aus dem optionalen Fehlerobjekt abgerufen werden, sofern diese verfügbar sind.

Wsutil.exe generiert einen Dienststub für alle unter Bindung beschriebenen Vorgänge.

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

Im obigen Abschnitt wird der Prototyp der lokalen Struktur beschrieben, die alle Definitionen enthält, die nur lokal in der Stubdatei enthalten sind. In den nachfolgenden Abschnitten werden die Definitionen der Beschreibungen beschrieben.

## <a name="wsdl-definition-generation"></a>WSDL-Definitionsgenerierung

Wsutil.exe generiert eine konstante statische Struktur (**const static**) mit dem Namen<Dateiname *\_>* LocalDefinitions des Typs *<\_ Dienstname>* Local, die alle ausschließlich lokalen Definitionen enthält.

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

-   wsdl:service
-   wsdl:binding
-   wsdl:portType
-   wsdl:operation
-   wsdl:message

## <a name="processing-wsdloperation-and-wsdlmessage"></a>Verarbeiten von wsdl:operation und wsdl:message

Jeder im WSDL-Dokument angegebene Vorgang wird einem Dienstvorgang durch [Wsutil.exe](web-service-compiler-tool.md)zugeordnet. Das Tool generiert separate Definitionen der Dienstvorgänge für den Server und den Client.

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

Das Layout der Eingabe- und Ausgabenachrichtendatenelemente wird vom Tool ausgewertet, um die Serialisierungsmetadaten für die Infrastruktur zusammen mit der tatsächlichen Signatur des resultierenden Dienstvorgangs zu generieren, dem die Eingabe- und Ausgabemeldungen zugeordnet sind.

Die Metadaten für jeden Vorgang innerhalb eines bestimmten **portType** verfügen über Eingabe- und optional eine Ausgabenachricht. Jede dieser Nachrichten wird einer [**WS \_ MESSAGE \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)zugeordnet. In diesem Beispiel sind die Eingabe und die Ausgabenachricht für den Vorgang im portType inputMessageDescription zugeordnet und optional outputMessageDescription für [**WS \_ OPERATION \_ DESCRIPTION.**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)

Für jede WSDL-Nachricht generiert das Tool [**WS \_ MESSAGE \_ DESCRIPTION,**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) die auf die [**\_ WS-ELEMENTBESCHREIBUNGsdefinition \_**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) verweist, wie unten gezeigt:

``` syntax
... 
{    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

Die Nachrichtenbeschreibung bezieht sich auf die Beschreibung des Eingabeelements. Da das Element global definiert ist, verweist die Nachrichtenbeschreibung auf die globale Definition anstelle des lokalen statischen Elements. Wenn das Element in einer anderen Datei definiert ist, generiert Wsutil.exe auf ähnliche Weise einen Verweis auf die global definierte Struktur in dieser Datei. Wenn SimpleMethodResponse beispielsweise in einer anderen example.xsd-Datei definiert ist, generiert Wsutil.exe stattdessen Folgendes:

``` syntax
...
{    // message description for ISimpleService_SimpleMethod_InputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_xsd.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

Jede Nachrichtenbeschreibung enthält die Aktion und die spezifische Elementbeschreibung (ein Feld vom Typ [**WS \_ ELEMENT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)) für alle Nachrichtendatenelemente. Im Fall einer RPC-Nachricht oder einer Nachricht mit mehreren Teilen wird ein Wrapperelement erstellt, um die zusätzlichen Informationen zu kapseln.

## <a name="rpc-style-support"></a>RPC-Stilunterstützung

Wsutil.exe unterstützt Vorgänge im Dokumentstil und RPC-Stil gemäß der WSDL 1.1-Bindungserweiterung für SOAP 1.2. RPC- und Literalvorgänge werden als WS \_ RPC \_ LITERAL \_ OPERATION gekennzeichnet. Das Dienstmodell ignoriert den Namen für das Wrapperelement des Antworttexts in RPC-/Literalvorgängen.

Wsutil.exe unterstützt Codierungsvorgänge nicht nativ. Der WS \_ XML \_ BUFFER-Parameter wird für die Codierung von Nachrichten generiert, und Entwickler müssen den nicht transparenten Puffer direkt auffüllen.

## <a name="multiple-message-parts-support"></a>Unterstützung mehrerer Nachrichtenteile

Wsutil.exe unterstützt mehrere Nachrichtenteile in einer Nachricht. Eine mehrteilige Nachricht kann wie folgt angegeben werden:

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

Wsutil.exe generiert ein [**WS \_ STRUCT \_ TYPE-Feld**](/windows/desktop/api/WebServices/ne-webservices-ws_type) für das Nachrichtenelement, wenn die Nachricht mehrere Teile enthält. Wenn die Nachricht mithilfe des Dokumentstils dargestellt wird, generiert Wsutil.exe ein Wrapperelement mit Strukturtyp. Das Wrapperelement verfügt nicht über einen Namen oder einen bestimmten Namespace, und die Wrapperstruktur enthält alle Elemente in allen Teilen als Felder. Das Wrapperelement ist nur für die interne Verwendung vorgesehen und wird nicht im Nachrichtentext serialisiert.

Wenn die Nachricht RPC- oder Literalformatdarstellung verwendet, erstellt Wsutil.exe ein Wrapperelement mit dem Vorgangsnamen als Elementnamen und dem angegebenen Namespace als Dienstnamespace gemäß WSDL SOAP-Erweiterungsspezifikation. Die Struktur des -Elements enthält ein Array von Feldern, die die in den Nachrichtenteilen angegebenen Typen darstellen. Das Wrapperelement wird dem tatsächlichen obersten Element im Nachrichtentext zugeordnet, wie in der SOAP-Spezifikation angegeben.

Auf serverseitiger Seite führt jeder Vorgang zu einer Typedef des resultierenden Serverdienstvorgangs. Diese Typedef wird verwendet, um auf den Vorgang in der Funktionstabelle zu verweisen, wie zuvor beschrieben. Jeder Vorgang führt auch zur Generierung einer Stubfunktion, die nfrastructure im Namen des Delegaten an die tatsächliche Methode aufruft.

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

Für den SimpleMethod-Vorgang ist die SimpleMethodOperation-Typdefinition oben definiert. Beachten Sie, dass die generierte Methode über eine erweiterte Argumentliste mit dem Nachrichtenteil für die Eingabe- und Ausgabenachricht für den SimpleMethod-Vorgang als benannte Parameter verfügt.

Auf clientseitiger Seite wird jeder Vorgang einem Proxydienstvorgang zugeordnet.

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

## <a name="processing-wsdlbinding"></a>Verarbeiten von wsdl:binding

Das WWSAPI-Dienstmodell unterstützt dieSOAP-Bindungserweiterung. Für jede Bindung ist ein **portType** zugeordnet.

Der in der Soap-Bindungserweiterung angegebene Transport ist nur eine Empfehlung. Die Anwendung muss Beim Erstellen eines Kanals Transportinformationen bereitstellen. Derzeit werden die \_ \_ WS-HTTP-BINDUNGen und \_ WS-TCP-BINDUNGen \_ unterstützt.

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

In unserem WSDL-Beispieldokument haben wir nur einen **portType** für ISimpleService. Die bereitgestellte SOAP-Bindung gibt den HTTP-Transport an, der als \_ WS-HTTP-BINDUNG angegeben \_ wird. Beachten Sie, dass diese Struktur keine statische Verzierung aufweist, da diese Struktur für die Anwendung verfügbar sein muss.

Verarbeiten von wsdl:portType

Jeder **portType** in WSDL besteht aus einem oder mehreren Vorgängen. Der Vorgang sollte mit der soap-Bindungserweiterung konsistent sein, die in wsdl:binding angegeben ist.

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

In diesem Beispiel enthält ISimpleService **portType** nur den SimpleMethod-Vorgang. Dies entspricht dem Bindungsabschnitt, in dem nur ein WSDL-Vorgang einer SOAP-Aktion zugeordnet ist.

Da ISimpleService **portType** nur über einen Vorgang (SimpleMethod) verfügt, enthält die entsprechende Funktionstabelle nur SimpleMethod als Dienstvorgang.

Im Hinblick auf Metadaten wird jeder **portType** durch Wsutil.exe einer [**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)zugeordnet. Jeder Vorgang in einem **portType** wird einer [**WS \_ OPERATION \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)zugeordnet.

In diesem Beispiel generiert **portType** das Tool [**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) für ISimpleService. Diese Vertragsbeschreibung enthält die spezifische Anzahl von Vorgängen, die für ISimpleService **portType** verfügbar sind, sowie ein Array von [**WS \_ OPERATION \_ DESCRIPTION,**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) das die einzelnen vorgänge darstellt, die für portType für ISimpleService definiert sind. Da es nur einen Vorgang für ISimpleService portType für ISimpleService gibt, gibt es auch nur eine **WS \_ OPERATION \_ DESCRIPTION-Definition.**

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

## <a name="processing-wsdlservice"></a>Verarbeiten von wsdl:service

WsUtil.exe verwendet die Dienste, um Bindungs-/Porttypen zu suchen, und generiert eine Vertragsstruktur, die Typen, Nachrichten, Porttypdefinitionen usw. beschreibt. Vertragsbeschreibungen sind extern zugänglich und werden als Teil der globalen Definitionsstruktur generiert, die durch den generierten Header angegeben wird.

WsUtil.exe unterstützt in wsdl:port definierte EndpointReference-Erweiterungen. Der Endpunktverweis wird in WS-ADDRESSING definiert, um [Endpunktinformationen](endpoint-address.md) eines Diensts zu beschreiben. Der als [**\_ WS-XML-ZEICHENFOLGE \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)gespeicherte Text der Eingabeendpunktverweiserweiterung wird zusammen mit der entsprechenden [**\_ WS-ENDPUNKTADRESSENBESCHREIBUNG \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) im Abschnitt endpointReferences in der globalen Struktur generiert.

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

So erstellen Sie [**die \_ WS-ENDPUNKTADRESSE \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) mithilfe der von WsUtil generierten Metadaten:

``` syntax
WsCreateReader      // Create a WS_XML_READER
Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput          // Set the encoding and input of the reader to generated endpointReferenceString
WsReadType        // Read WS_ENDPOINT_ADDRESS from the reader
    // Using WS_ELEMENT_TYPE_MAPPING, WS_ENDPOINT_ADDRESS_TYPE and generated endpointAddressDescription, 
```

Konstante Zeichenfolgen im Clientproxy oder Dienststub werden als Felder vom Typ WS \_ XML \_ STRING generiert, und es gibt ein konstantes Wörterbuch für alle Zeichenfolgen in der Proxy- oder Stubdatei. Jede Zeichenfolge im Wörterbuch wird zur besseren Lesbarkeit als Feld im Wörterbuchteil der lokalen Struktur generiert.

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

## <a name="processing-wsdltype"></a>Verarbeiten von wsdl:type

Wsutil.exe unterstützt nur XSD-Dokumente (XML-Schema) in wsdl:type-Spezifikationen. Ein Sonderfall ist, wenn ein Nachrichtenport eine globale Elementdefinition angibt. Weitere Informationen zu den in diesen Fällen verwendeten Heuristiken finden Sie im folgenden Abschnitt.

## <a name="parameter-processing-heuristics"></a>Heuristik für die Parameterverarbeitung

Im Dienstmodell werden WSDL-Nachrichten bestimmten Parametern in einer Methode zugeordnet. Wsutil.exe verfügt über zwei Stile der Parametergenerierung: im ersten Stil verfügt der Vorgang über einen Parameter für die Eingabenachricht und einen Parameter für die Ausgabenachricht (falls erforderlich). im zweiten Stil verwendet Wsutil.exe eine Heuristik, um Felder in den Strukturen sowohl für Eingabenachrichten als auch für Ausgabenachrichten verschiedenen Parametern im Vorgang zuzuordnen und zu erweitern. Sowohl Eingabe- als auch Ausgabenachrichten müssen über Nachrichtenelemente vom Typ Struktur verfügen, um diesen zweiten Ansatz zu generieren.

Wsutil.exe verwendet beim Generieren von Vorgangsparametern aus den Eingabe- und Ausgabemeldungen die folgenden Regeln:

-   Für Eingabe- und Ausgabenachrichten mit mehreren Nachrichtenteilen ist jeder Nachrichtenteil ein separater Parameter im Vorgang, wobei der Name des Nachrichtenteils als Parametername verwendet wird.
-   Bei RPC-Nachrichten mit einem Nachrichtenteil ist der Nachrichtenteil ein Parameter im Vorgang, wobei der Name des Nachrichtenteils als Parametername verwendet wird.
-   Für Eingabe- und Ausgabenachrichten im Dokumentformat mit einem Nachrichtenteil:
    -   Wenn der Name eines Nachrichtenteils "parameters" ist und der Elementtyp eine Struktur ist, wird jedes Feld in der Struktur als separater Parameter behandelt, wobei der Feldname der Parametername ist.
    -   Wenn der Name des Nachrichtenteils nicht "parameters" ist, ist die Nachricht ein Parameter im Vorgang mit dem Nachrichtennamen, der als entsprechender Parametername verwendet wird.
-   Für die Eingabe- und Ausgabenachricht im Dokumentformat mit dem nillable-Element wird die Nachricht einem Parameter zugeordnet, wobei der Name des Nachrichtenteils als Parametername verwendet wird. Eine zusätzliche Dekonstruktionsebene wird hinzugefügt, um anzugeben, dass der Zeiger **NULL** sein kann.
-   Wenn ein Feld nur im Eingabemeldungselement angezeigt wird, wird das Feld als \[ \] in-Parameter behandelt.
-   Wenn ein Feld nur im Ausgabemeldungselement angezeigt wird, wird das Feld als \[ \] out-Parameter behandelt.
-   Wenn ein Feld mit dem gleichen Namen und Typ vorhanden ist, das sowohl in der Eingabenachricht als auch in der Ausgabenachricht angezeigt wird, wird das Feld als \[ in,out-Parameter \] behandelt.

Die folgenden Tools werden verwendet, um die Richtung von Parametern zu bestimmen:

-   Wenn ein Feld nur im Eingabenachrichtenelement angezeigt wird, wird das Feld als nur im -Parameter behandelt.
-   Wenn ein Feld nur im Ausgabemeldungselement angezeigt wird, wird das Feld als nur out-Parameter behandelt.
-   Wenn ein Feld mit dem gleichen Namen und Typ vorhanden ist, das sowohl in der Eingabenachricht als auch in der Ausgabenachricht angezeigt wird, wird das Feld als in,out-Parameter behandelt.

Wsutil.exe unterstützt nur sequenzierte Elemente. Die ungültige Sortierung in Bezug auf \[ in,out-Parameter wird \] abgelehnt, wenn Wsutil.exe die Parameter in und out nicht in einer einzigen Parameterliste kombinieren können. Suffixe können Parameternamen hinzugefügt werden, um Namenskonflikte zu vermeiden.

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

Wsutil.exe betrachtet Felder in tns:SimpleMethod und tns:SimpleMethodResponse ato als Parameter, wie in den folgenden Parameterdefinitionen zu sehen:

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

Wsutil.exe erweitert die Parameterliste aus den Feldern in der obigen Liste und generiert die **ParamStruct-Struktur** im folgenden Codebeispiel. Die Laufzeit des Dienstmodells kann diese Struktur verwenden, um Argumente an die Client- und Serverstubs zu übergeben.

``` syntax
typedef struct SimpleMethodParamStruct {
  unsigned int   a;  
  unsigned int   b;
  unsigned int   c;
} ;
```

Diese Struktur wird nur verwendet, um den Stapelrahmen auf Client- und Serverseite zu beschreiben. Es gibt keine Änderung an der Nachrichtenbeschreibung oder an den Elementbeschreibungen, auf die von der Nachrichtenbeschreibung verwiesen wird.

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

In der Regel wird eine Dekonstruktionsebene für alle \[ \] Out- und \[ In-Out-Parameter \] hinzugefügt.

## <a name="parameterless-operation"></a>Parameterloser Vorgang

Bei Dokument- und Literalvorgängen behandelt Wsutil.exe den Vorgang wie einen Eingabeparameter und einen Ausgabeparameter, wenn:

-   Die Eingabe- oder Ausgabenachricht hat mehr als einen Teil.
-   Es gibt nur einen Nachrichtenteil, und der Name des Nachrichtenteils ist nicht "parameters".

.. Wenn im obigen Beispiel die Nachrichtenteile *ParamIn*" und *ParamOut* heißen, wird die Methodensignatur zum folgenden Code:

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

Wsutil.exe generiert eine Versionssignatur für die Vorgangsbeschreibung, sodass die WsCall- und die serverseitige Dienstmodell-Engine überprüfen können, ob die generierte Beschreibung für die aktuelle Plattform gilt.

Diese Versionsinformationen werden als Teil der [**WS \_ OPERATION \_ DESCRIPTION-Struktur**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) generiert. Die Versionsnummer kann als Union-Arm-Selektor behandelt werden, um die Struktur erweiterbar zu machen. Derzeit ist **versionID** ohne nachfolgende Felder auf1 festgelegt. Zukünftige Versiosn kann die Versionsnummer erhöhen und bei Bedarf weitere Felder enthalten. Beispielsweise generiert Wsutil.exe derzeit den folgenden Code basierend auf der Versions-ID:

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

In Zukunft könnte sie wie folgt erweitert werden:

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

Weitere Informationen finden Sie im Abschnitt "Sicherheit" des [Themas Wsutil Compiler Tool.](wsutil-compiler-tool.md)

 

 




