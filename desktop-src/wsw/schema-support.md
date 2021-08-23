---
title: Unterstützung von Schemas
description: WsUtil.exe unterstützt das unter XML-Schema angegebene XSD-Schema.
ms.assetid: 33096cda-9dbe-44d2-8d08-410bc33ae81c
keywords:
- Schemaunterstützung von Webdiensten für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c0f55c5ea3828c72456989f7053e2ff008e524e41552b281b88839653229863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962899"
---
# <a name="schema-support"></a>Unterstützung von Schemas

WsUtil.exe unterstützt das unter [XML-Schema](https://www.w3.org/XML/Schema)angegebene XSD-Schema. xsd file und wsdl:type sollten in derselben Kategorie behandelt werden, mit der Ausnahme in wsdl:type, wenn ein globales Element eine Parameterliste sein könnte. Wsutil.exe generiert Elementbeschreibungen für alle globalen Elementdefinitionen, die im Serialisierungsprogramm verwendet werden können, mit zusätzlicher Ausgabe für die in [WSDL](wsdl-support.md)angegebene Parameterstruktur.

## <a name="xsd-schema-support-level"></a>XSD-Schemaunterstützungsebene

WsUtil.exe unterstützt nicht den vollständigen Umfang des XSD-Schemas. Die aktuelle Supportebene ist unter [Schemaunterstützungsebene](schema-support-level.md)definiert.

Generierung von Bezeichnern

Elementname oder Typname im Schema ist möglicherweise kein gültiger C-Bezeichner, und die Namen werden auf generierte gültige C-Namen normalisiert. Ungültige C-Bezeichnerzeichen werden in den Hexadezimalnamen konvertiert, und ggf. wird dem Namen ein Unterstrich \_ "" vorangestellt. Anonyme Typen werden nach dem einschließenden Elementnamen benannt, aber mit dem Präfix \_ "" versehen, um Namenskonflikte zu vermeiden. Globale Typnamen werden so beibehalten, wie sie sind, nachdem ungültige Zeichen normalisiert wurden. Geschachtelten anonymen Typen wird der Name des übergeordneten Typs vorangestellt.

Für jede globale Elementdefinition generiert wsutil.exe eine [**\_ WS-ELEMENTBESCHREIBUNG \_**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) in der globalen Beschreibungsstruktur. Für jede globale Typdefinition generiert wsutil.exe eine Typbeschreibung in der globalen Beschreibungsstruktur, auf die von der Anwendung verwiesen werden soll.

Für jedes Feld in der -Struktur generiert wsutil.exe eine [**WS \_ FIELD \_ DESCRIPTION,**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description) die als Teil der Gehäusestruktur eingebettet ist.

## <a name="simple-types"></a>Einfache Typen

Werttypen, wie in [**WS \_ VALUE \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)aufgeführt, werden als einfache Typen behandelt. Beachten Sie, dass WS \_ VALUE TYPE tatsächlich eine \_ Teilmenge von [**WS \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type)ist. Sie enthält grundlegende integrale und float-Datentypen sowie DECIMAL, WS \_ DATETIME und UUID.

Im Dienstmodell werden in einfache Typen als Wert übergeben, während out und in,out einfache Typen als Verweis übergeben werden.

Wsutil erstellt eine einfache Elementbeschreibung wie unten für globales Element, das einfache Typen enthält.

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="helloworld" type="xs:int"></xs:element>
</xs:schema>
```

Wsutil generiert die folgende Elementbeschreibung:

``` syntax
...  // global elements
{ // helloworld
{
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.helloworldTypeName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.helloworldTypeNamespace,
WS_INT32_TYPE,
0,
},
}, // helloworld
... 
```

Diese Struktur wird als Teil der globalen Beschreibungsstruktur generiert, die in der Headerdatei generiert wird:

``` syntax
typedef struct _example_wsdl
{
WS_ELEMENT_DESCRIPTION helloworld;
} _example_wsdl;
```

## <a name="arrays"></a>Arrays

Ein Element mit maxOccurs größer als 1 oder eine Sequenz mit nur einem Element, und das untergeordnete Element hat maxOccurs größer als 1, wird als Array behandelt. Für ein Arrayelement im Schema generiert wsutil.exe zwei Felder: ein Count-Feld, das nicht verknüpft wird, und ein Zeigerfeld, das den Arraytyp enthält.

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="SimpleArray">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" maxOccurs="50" name="a" nillable="true" type="xs:int" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema>
```

Die Headerdatei enthält die C-Strukturdefinition für das Array, wobei das Feld aCount die Anzahl des Arrays angibt.

``` syntax
typedef struct SimpleArray
{
  unsigned int  aCount ;
  int  * a;
} SimpleArray;
```

Folgendes ist Teil des LocalDefinition-Prototyps, der das Array beschreibt:

``` syntax
... // globalElement part of the LocalDefinitions.
struct // SimpleArray
{
  struct // SimpleArray
  {
    WS_FIELD_DESCRIPTION a;
    WS_FIELD_DESCRIPTION * SimpleArrayFields [1];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleArraydescs; // SimpleArray
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleArray;

// Method with array parameters.
  typedef HRESULT (CALLBACK *SimpleMethodCallback)(
    const WS_OPERATION_CONTEXT* context,
    unsigned int aCount,
    int* a,
    unsigned int *bCount,
    int** b,
    unsigned int* cCount,
    int** c,
    const WS_ASYNC_CONTEXT* asyncContext,
    WS_ERROR* error);

  HRESULT CALLBACK SimpleMethod (
    WS_SERVICE_PROXY* serviceProxy,
    WS_HEAP* heap,
    unsigned int aCount,
    int* a,
    unsigned int *bCount,
    int** b,
    unsigned int* cCount,
    int** c,
    const WS_ASYNC_CONTEXT* asyncContext,
    WS_ERROR* error);
```

Im Folgenden sind die generierten Definitionen der obigen Beschreibungen aufgeführt. Beachten Sie die WS \_ REPEATING \_ ELEMENT FIELD \_ \_ MAPPING, die das Feld als Arrayfeld angibt.

``` syntax
...
{ // SimpleArray
  {   // SimpleArray
    { // field description for a
      WS_REPEATING_ELEMENT_FIELD_MAPPING,
      0,
      0,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(SimpleArray, a),
      0,
      0,
      WsOffsetOf(SimpleArray, aCount),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    },    // end of field description for a
    {    // fields description for SimpleArray
      (WS_FIELD_DESCRIPTION*)&example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.a,
    },
    {
      sizeof(SimpleArray),
      __alignof(SimpleArray),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.
      SimpleArrayFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.SimpleArrayFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    },   // struct description for SimpleArray
  },    // SimpleArray
  {
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.structDesc,
  },
}, // SimpleArray
...
```

Wenn das Array ein Parameterfeld in der Eingabe-/Ausgabenachricht ist, werden zwei tatsächliche Parameter für die Methode generiert. Wenn das Array ein out- oder in,out-Parameter ist, gibt es eine zusätzliche Dekonstruktionsebene für beide Felder in paramStruct.

## <a name="range-on-array"></a>Bereich auf Array

Es wird empfohlen, maxOccur="unbounded" für Arrays nicht anzugeben. Stattdessen sollte eine feste ganzzahlige Zahl angegeben werden, um eine Obergrenze der zulässigen Arrayanzahl festzulegen. range wird für integrale Typen sowie Zeichenfolgen, Bytearrays und generische Arrays unterstützt.

## <a name="heuristic-for-wrapped-as-opposed-to-unwrapped-array"></a>Heuristik für umschlossenes Array im Gegensatz zu entpackten Arrays

Manchmal werden Arrays in einer anderen Struktur umschlossen, um in eine Struktur der obersten Ebene eingebettet zu werden. In diesem Fall sollten wir die Zwischenwrapperebene entfernen. WsUtil.exe generiert den gleichen Prototyp und die gleichen Beschreibungen wie simpleArray, wie oben beschrieben.

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:complexType name="SimpleArray">
  <xs:sequence>
   <xs:element minOccurs="0" maxOccurs="50" name="aa" type="xs:int" />
  </xs:sequence>
 </xs:complexType>
 <xs:element name="SimpleArrayWrapper">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="SimpleArray" type="tns:SimpleArray" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema>
```

Wsutil erkennt, dass SimpleArrayWrapper ein Wrapper um SimpleArray ist, und generiert nur folgende Strukturen mit separater Struktur für SimpleArray.

``` syntax
typedef struct SimpleArrayWrapper
{
  unsigned int  SimpleArrayCount ;
  int  * SimpleArray;
} SimpleArrayWrapper;

.. // global element inside the LocalDefinitions prototype
struct // SimpleArrayWrapper
{
  struct // SimpleArrayWrapper
  {
    WS_FIELD_DESCRIPTION SimpleArray;
    WS_FIELD_DESCRIPTION * SimpleArrayWrapperFields [1];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleArrayWrapperdescs; // SimpleArrayWrapper
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleArrayWrapper;
...
```

wsutil.exe generiert die folgenden Definitionen für den entsprechenden Prototyp oben. Beachten Sie, dass in der Feldbeschreibung die Felder Wrappername und Wrappernamespace ausgefüllt sind.

``` syntax
... // global element part of the LocalDefinitions structure:
{ // SimpleArrayWrapper
  {   // SimpleArrayWrapper
    { // WS_FIELD_DESCRIPTION  for SimpleArray
      WS_REPEATING_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(SimpleArrayWrapper, SimpleArray),
      0,
      0,
      WsOffsetOf(SimpleArrayWrapper, SimpleArrayCount),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    },    // end of field description for SimpleArray
    {    // array of field descriptions for SimpleArrayWrapper
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArray,
    },
    {  // WS_STRUCT_DESCRIPTION for SimpleArrayWrapper
      sizeof(SimpleArrayWrapper),
      __alignof(SimpleArrayWrapper),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArrayWrapperFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArrayWrapperFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    },   // struct description for SimpleArrayWrapper
    },    // SimpleArrayWrapper
  {  // WS_ELEMENT_DESCRIPTION for SimpleArrayWrapper
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.structDesc,
  },
}, // SimpleArrayWrapper
```

## <a name="structures"></a>Strukturen

Ein complexType mit mehreren Elementen in einer Sequenz ist eine -Struktur. Beispiel:

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:complexType name="StructType">
  <xs:sequence>
   <xs:element minOccurs="0" name="FirstName" nillable="true" type="xs:string" />
   <xs:element minOccurs="0" name="LastName" nillable="true" type="xs:string" />
  </xs:sequence>
 </xs:complexType>
 <xs:element name="StructType" nillable="true" type="tns:StructType" />
</xs:schema>
```

Wsutil.exe generiert einen Strukturprototyp wie:

``` syntax
struct StructType
{
  WS_STRING FirstName;
  WS_STRING LastName;
};

// methods using structure parameters.
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT* context,
  StructType* a,
  StructType** b,
  StructType** c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);

HRESULT CALLBACK SimpleMethod (WS_SERVICE_PROXY* serviceProxy,
  WS_HEAP* heap,
  StructType* a,
  StructType** b,
  StructType** c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

wsutil generiert den folgenden Prototyp für LocalDefinition:

``` syntax
struct // StructType
{
  struct // StructType
  {
    WS_FIELD_DESCRIPTION FirstName;
    WS_FIELD_DESCRIPTION LastName;
    WS_FIELD_DESCRIPTION * StructTypeFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } StructTypedescs; // StructType
WS_ELEMENT_DESCRIPTION elementDesc;
}
```

Die Definition für die -Struktur sieht wie folgt aus, mit zwei Feldbeschreibungen in der -Struktur.

``` syntax
// global element inside LocalDefinitions.
{ // StructType
  {   // StructType
    { // field description for FirstName
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
      WS_STRING_TYPE,
      0,
      WsOffsetOf(StructType, FirstName),
      0,
      0,
    },    // end of field description for FirstName
    { // field description for LastName
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.LastNameLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
      WS_STRING_TYPE,
      0,
      WsOffsetOf(StructType, LastName),
      0,
      0,
    },    // end of field description for LastName
    {    // fields description for StructType
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.FirstName,
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.LastName,
    },
    { // WS_STRUCT_DESCRIPTION for StructType
      sizeof(StructType),
      __alignof(StructType),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.StructTypeFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.StructTypeFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.StructTypeTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
    },   // struct description for StructType
  },    // StructType
  {
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.StructTypeTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.structDesc,
  },
}, // StructType
```

Zur Unterstützung der Erweiterbarkeit werden eingebettete Strukturen immer als Verweis übergeben. Im Dienst werden alle Out- oder In-Out-Strukturen durch einen doppelten Zeiger übergeben, um eine zukünftige Erweiterung der Struktur sowie eine nillable-Struktur zu ermöglichen.

## <a name="recursive-structures"></a>Rekursive Strukturen

Rekursive Strukturen werden unterstützt, und die eingebetteten Typen werden als Verweis übergeben. Für die folgende wsdl:

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="SimpleMethod">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="a" type="xs:int" />
    <xs:element minOccurs="0" name="b" type="tns:example" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
 <xs:complexType name="example">
  <xs:sequence>
   <xs:element minOccurs="0" name="d" type="tns:example" />
   <xs:element minOccurs="0" name="c" type="xs:int" />
  </xs:sequence>
 </xs:complexType>
</xs:schema>
```

Wsutil generiert die folgenden Typdefinitionen sowie die Typbeschreibungen:

``` syntax
typedef struct example
{
  struct example  * d;
  int32   c;
} example;

typedef struct SimpleMethod
{
  unsigned __int32   a;
  struct example  * b;
} SimpleMethod;

// global element part of the LocalDefinitions.
...
struct // SimpleMethod
{
  struct // SimpleMethod
  {
    WS_FIELD_DESCRIPTION a;
    struct // example
    {
      WS_FIELD_DESCRIPTION d;
      WS_FIELD_DESCRIPTION c;
      WS_FIELD_DESCRIPTION * exampleFields [2];
      WS_STRUCT_DESCRIPTION structDesc;
    } exampledescs; // example
    WS_FIELD_DESCRIPTION b;
    WS_FIELD_DESCRIPTION * SimpleMethodFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleMethoddescs; // SimpleMethod
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleMethod;
...
```

Die Definition wird wie folgt generiert:

``` syntax
{   // SimpleMethod
  { // field description for a
    WS_ELEMENT_FIELD_MAPPING,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    WS_INT32_TYPE,
    0,
    WsOffsetOf(SimpleMethod, a),
    0,
    0,
  },    // end of field description for a
  {   // example
    { // field description for d
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.dLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
      WS_STRUCT_TYPE,
      (WS_STRUCT_DESCRIPTION*)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.structDesc,
      WsOffsetOf(example, d),
      WS_FIELD_POINTER,
      0,
    },    // end of field description for d
    { // field description for c
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.cLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(example, c),
      0,
      0,
    },    // end of field description for c
    {    // fields description for example
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.d,
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.c,
    },
  {
    sizeof(example),
    __alignof(example),
    (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.exampleFields,
    WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.exampleFields),
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.exampleTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  },   // struct description for example
}
```

## <a name="structure-inheritence"></a>Strukturvererbung

wsutil unterstützt komplexe Typerweiterungen, bei denen ein komplexer Typ eine Erweiterung für einen anderen komplexen Typ ist.

``` syntax
<s:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:s="http://www.w3.org/2001/XMLSchema">
 <s:complexType name="LinkList">
  <s:sequence>
   <s:element minOccurs="0" name="d" type="tns:LinkList" />
   <s:element minOccurs="0" name="c" type="s:int" />
  </s:sequence>
 </s:complexType> 
 <s:element name="DerivedLinkList">
  <s:complexType>
   <s:complexContent>
    <s:extension base="tns:LinkList">
     <s:sequence>
      <s:element name="derive1" type="s:int" />
     </s:sequence>
    </s:extension>
   </s:complexContent>
  </s:complexType>
 </s:element>
</s:schema>
```

Das obige xsd-Fragment gibt an, dass DerivedLinkList von LinkList abgeleitet wird.

Wsutil.exe generiert Hilfsprogrammroutinen für C und C++, um es der Anwendung zu erleichtern, die Typinformationen des Basistyps und der abgeleiteten Typen einzurichten. Im folgenden Code wird das \_ \_ WS-CPLUSPLUS-Makro verwendet, um die Definition für die Sprache C und C++ zu unterscheiden:

``` syntax
#if defined(_WS_CPLUSPLUS)
typedef struct LinkList
{
  LinkList();
  LinkList(WS_STRUCT_DESCRIPTION*);
  struct _DerivedLinkList* WINAPI As_DerivedLinkList();
  const struct _WS_STRUCT_DESCRIPTION* _type;
  struct LinkList * d;
  int  c;
} LinkList;
#endif

#if !defined(_WS_CPLUSPLUS)
typedef struct LinkList
{
  const struct _WS_STRUCT_DESCRIPTION* _type;
  struct LinkList * d;
  int  c;
} LinkList;

void WINAPI LinkList_Init(LinkList*);
#endif

#if defined(_WS_CPLUSPLUS)
typedef struct _DerivedLinkList:LinkList
{
  _DerivedLinkList();
  int  derive1;
} _DerivedLinkList;
#endif

#if !defined(_WS_CPLUSPLUS)
typedef struct _DerivedLinkList
{
  struct LinkList _base;
  int  derive1;
} _DerivedLinkList;

struct _DerivedLinkList* WINAPI LinkList_As_DerivedLinkList(LinkList*);
#endif
```

Im C-Stilhilfsprogramm ruft die Anwendung vor der Serialisierung wsutil generated routine LinkList \_ Init auf, um die Struktur zu initialisieren und die Typbeschreibung auf linkList type description festzulegen. Nach der Deserialisierung kann die Anwendung LinkList \_ als \_ DerivedLinkList aufrufen, um den abgeleiteten Typ abzurufen.

Um Typinformationen zur Laufzeit abzurufen, generiert wsutil das erste Feld des Basistyps mit dem [**\_ WS-Typ STRUCT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description) \* und der [**Feldzuordnung WS \_ TYPE ATTRIBUTE FIELD \_ \_ \_ MAPPING,**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping) um die xsi:type-Informationen zu beschreiben. Die Anwendung kann das Feld direkt festlegen oder überprüfen, um den tatsächlichen Typ von Strukturen zu bestimmen. Der folgende Code legt beispielsweise den Typ der -Struktur auf DrivedLinkList fest:

``` syntax
_DerivedLinkList derivedLinkList;
derivedLinkList._base._type = (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription;
WsWriteType(
    writer,
    WS_ELEMENT_TYPE_MAPPING,
    WS_STRUCT_TYPE,
    (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription,
    ...);
```

Nachdem die Struktur deserialisiert wurde, kann die Anwendung die Typbeschreibung direkt vergleichen, um den deserialisierten Typ zu bestimmen:

``` syntax
if (derviedLinkList._base._type == (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription)
{
    // the deserialized type is of type _DerivedLinkList
    ...
}
```

wsutil generate-Klasse sowohl für die Basisstruktur als auch für die abgeleitete Struktur. Der Standardkonstruktor initialisiert den Typ und die übereinstimmende Typbeschreibung. Die AsDerivedType-Routine hilft bei der sicheren Typzuteilung zwischen Typen.

``` syntax
  { // field description for typeOfLinkList
  WS_TYPE_ATTRIBUTE_FIELD_MAPPING,
  0,
  0,
  WS_DESCRIPTION_TYPE,
  0,
  WsOffsetOf(LinkList, typeOfLinkList),
  0,
  0,
  },    // end of field description for typeOfLinkList        ...
  {
  sizeof(LinkList),
  __alignof(LinkList),
  (WS_FIELD_DESCRIPTION**)&test_xsdLocalDefinitions.globalTypes.LinkListdescs.LinkListFields,
WsCountOf(test_xsdLocalDefinitions.globalTypes.LinkListdescs.LinkListFields),
(WS_XML_STRING*)&test_xsdLocalDefinitions.dictionary.xmlStrings.LinkListTypeName,
(WS_XML_STRING*)&test_xsdLocalDefinitions.dictionary.xmlStrings.LinkListTypeNamespace,
0,
(WS_STRUCT_DESCRIPTION**)&test_xsdLocalDefinitions.globalTypes.LinkListdescs.SubTypes,
  1,
  },   // struct description for LinkList
```

## <a name="nillable"></a>nillable

Ein nillable-Attribut wird für Zeichenfolgen, Strukturen und Bytearrays unterstützt. Das WS \_ FIELD \_ NILLABLE-Attribut wird Feldern mit dem nillable-Attribut hinzugefügt. Der Zeiger wird auf **NULL** festgelegt, wenn ein Element nillable ist. Ein nillable-Feld in einer -Struktur wird als Zeiger behandelt. Eine Parameterstruktur mit nillable-Attribut wird als Verweis übergeben.

## <a name="pointers"></a>Zeiger

Der Werttyp muss als Wert oder als Verweis für out-Parameter übergeben werden. Ein doppelter Zeiger ist nur für out-Strukturen zulässig.

## <a name="parameterless"></a>Parameterlos

Erinnern Sie sich an unsere vorherige Erörterung des Namens "parameter" für den Nachrichtenteil. Wenn dies angegeben ist, versuchen wir, einen kombinierten Frame für die Eingabe- und Ausgabenachricht für den resultierenden Dienstvorgang zu generieren. Wenn dies nicht angegeben wird, enthält der resultierende Dienstvorgang Eingabe- und Ausgabenachrichten als Strukturen als Parameter.

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Sapphire.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Sapphire.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="noparameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="noparameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

Daher sieht die Signatur für den Dienst und den Client für unseren SimpleMethod-Vorgang wie folgt aus.

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback)
  (const WS_OPERATION_CONTEXT* context,
  SimpleMethodRequest* inMessage,
  SimpleMethodResponse** outMessage,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);

HRESULT CALLBACK SimpleMethod (
  WS_SERVICE_PROXY* serviceProxy,
  WS_HEAP* heap,
  SimpleMethodRequest* inMessage,
  SimpleMethodResponse** outMessage,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

## <a name="security"></a>Sicherheit

Weitere Informationen finden Sie im Abschnitt "Sicherheit" im [Wsutil-Compilertool](wsutil-compiler-tool.md) sowie [in der Serialisierung.](serialization.md)

 

 




