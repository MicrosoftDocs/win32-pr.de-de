---
title: Unterstützung von Schemas
description: WsUtil.exe unterstützt das im XML-Schema angegebene XSD-Schema.
ms.assetid: 33096cda-9dbe-44d2-8d08-410bc33ae81c
keywords:
- Schema Unterstützung für Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dcf9d192c999333ee8b4e341e7722cd6bd59ff5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "103948467"
---
# <a name="schema-support"></a><span data-ttu-id="7517a-106">Unterstützung von Schemas</span><span class="sxs-lookup"><span data-stu-id="7517a-106">Schema support</span></span>

<span data-ttu-id="7517a-107">WsUtil.exe unterstützt das im [XML-Schema](https://www.w3.org/XML/Schema)angegebene XSD-Schema.</span><span class="sxs-lookup"><span data-stu-id="7517a-107">WsUtil.exe supports the XSD schema specified at [XML Schema](https://www.w3.org/XML/Schema).</span></span> <span data-ttu-id="7517a-108">die XSD-Datei und der WSDL: Type sollten in derselben Kategorie behandelt werden, mit der Ausnahme in WSDL: Type, wenn ein globales Element eine Parameterliste sein könnte.</span><span class="sxs-lookup"><span data-stu-id="7517a-108">xsd file and wsdl:type should be treated in the same category, with the exception in wsdl:type when a global element could be a parameter list.</span></span> <span data-ttu-id="7517a-109">Wsutil.exe generiert Element Beschreibungen für alle Definitionen globaler Elemente, die im Serialisierungsprogramm verwendet werden können, mit zusätzlicher Ausgabe für die Parameter Struktur, die in der [WSDL-Unterstützung](wsdl-support.md)angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7517a-109">Wsutil.exe generates element descriptions for all global element definitions that can be used in serializer, with additional output for parameter structure specified in [WSDL support](wsdl-support.md).</span></span>

## <a name="xsd-schema-support-level"></a><span data-ttu-id="7517a-110">Unterstützungs Ebene für das XSD-Schema</span><span class="sxs-lookup"><span data-stu-id="7517a-110">XSD Schema Support Level</span></span>

<span data-ttu-id="7517a-111">WsUtil.exe unterstützt nicht den vollständigen Umfang des XSD-Schemas.</span><span class="sxs-lookup"><span data-stu-id="7517a-111">WsUtil.exe does not support the full extent of XSD schema.</span></span> <span data-ttu-id="7517a-112">Die aktuelle Unterstützungs Ebene wird auf der [Ebene des Schema Supports](schema-support-level.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="7517a-112">The current support level is defined in [Schema support level](schema-support-level.md).</span></span>

<span data-ttu-id="7517a-113">Bezeichnergenerierung</span><span class="sxs-lookup"><span data-stu-id="7517a-113">Identifier generation</span></span>

<span data-ttu-id="7517a-114">Der Element Name oder Typname im Schema ist möglicherweise kein gültiger c-Bezeichner, und die Namen werden in generierte gültige c-Namen normalisiert.</span><span class="sxs-lookup"><span data-stu-id="7517a-114">Element name or type name in the schema might not be valid C identifier, and the names are normalized to generated valid C names.</span></span> <span data-ttu-id="7517a-115">Ungültige C-Bezeichnerzeichen werden in den Hexadezimal Namen konvertiert, und ein Unterstrich " \_ " kann ggf. dem Namen vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7517a-115">Invalid C identifier characters are converted to the hex name, and a underscore '\_' might be prefixed to the name if necessary.</span></span> <span data-ttu-id="7517a-116">Anonyme Typen werden nach dem einschließenden Elementnamen benannt, haben aber den Unterstrich "" vorangestellt \_ , um Namenskollisionen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="7517a-116">Anonymous types are named after the enclosing element name but prefixed with underscore "\_" to avoid name collision.</span></span> <span data-ttu-id="7517a-117">Globale Typnamen bleiben erhalten, nachdem ungültige Zeichen normalisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="7517a-117">Global type names are preserved as it is after invalid characters are normalized.</span></span> <span data-ttu-id="7517a-118">Den Namen der in der Tabelle anonymen Typen wird der Name des übergeordneten Typs vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="7517a-118">Nested anonymous types are prefixed with the parent type name.</span></span>

<span data-ttu-id="7517a-119">Für jede globale Element Definition generiert wsutil.exe eine [**WS- \_ Element \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) in der globalen Beschreibungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="7517a-119">For every global element definition, wsutil.exe generates a [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) in the global description structure.</span></span> <span data-ttu-id="7517a-120">Für jede globale Typdefinition generiert wsutil.exe eine Typbeschreibung in der globalen Beschreibungs Struktur, auf die von der Anwendung verwiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7517a-120">For every global type definition, wsutil.exe generates a type description in the global description structure to be referenced by application.</span></span>

<span data-ttu-id="7517a-121">Für jedes Feld in der Struktur generiert wsutil.exe eine [**WS- \_ Feld \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description) , die als Teil der Gehäuse Struktur eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="7517a-121">For each field in the structure, wsutil.exe generates a [**WS\_FIELD\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description) embedded as part of the enclosure structure.</span></span>

## <a name="simple-types"></a><span data-ttu-id="7517a-122">Einfache Typen</span><span class="sxs-lookup"><span data-stu-id="7517a-122">Simple Types</span></span>

<span data-ttu-id="7517a-123">Werttypen, wie im [**WS \_ - \_ Werttyp**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)aufgelistet, werden als einfache Typen behandelt.</span><span class="sxs-lookup"><span data-stu-id="7517a-123">Value types, as listed in [**WS\_VALUE\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type), are treated as simple types.</span></span> <span data-ttu-id="7517a-124">Beachten Sie, dass der WS- \_ \_ Werttyp wirklich eine Teilmenge des [**WS- \_ Typs**](/windows/desktop/api/WebServices/ne-webservices-ws_type)ist.</span><span class="sxs-lookup"><span data-stu-id="7517a-124">Notice that WS\_VALUE\_TYPE is really a subset of [**WS\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span></span> <span data-ttu-id="7517a-125">Sie enthält die grundlegenden Datentypen "Integer" und "float" sowie "Decimal", "WS \_ DateTime" und "uuid".</span><span class="sxs-lookup"><span data-stu-id="7517a-125">It includes basic integral and float data types, as well as DECIMAL, WS\_DATETIME, and UUID.</span></span>

<span data-ttu-id="7517a-126">In-Dienst Modellen werden in einfachen Typen als Wert und Out-und in-Simple-Typen als Verweis übermittelt.</span><span class="sxs-lookup"><span data-stu-id="7517a-126">In service model, in simple types are passed by value, while out and in,out simple types are passed by reference.</span></span>

<span data-ttu-id="7517a-127">Wsutil erstellen Sie eine einfache Element Beschreibung wie unten für ein globales Element, das einfache Typen enthält.</span><span class="sxs-lookup"><span data-stu-id="7517a-127">Wsutil create simple element description like below for global element containing simple types.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="helloworld" type="xs:int"></xs:element>
</xs:schema>
```

<span data-ttu-id="7517a-128">Wsutil generiert die unten angegebene Element Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="7517a-128">Wsutil generates the element description below:</span></span>

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

<span data-ttu-id="7517a-129">Diese Struktur wird als Teil der globalen Beschreibungs Struktur generiert, die in der Header Datei generiert wird:</span><span class="sxs-lookup"><span data-stu-id="7517a-129">This structure is generated as part of the global description structure generated in header file:</span></span>

``` syntax
typedef struct _example_wsdl
{
WS_ELEMENT_DESCRIPTION helloworld;
} _example_wsdl;
```

## <a name="arrays"></a><span data-ttu-id="7517a-130">Arrays</span><span class="sxs-lookup"><span data-stu-id="7517a-130">Arrays</span></span>

<span data-ttu-id="7517a-131">Ein Element mit maxvorkommen, das größer als 1 ist, oder eine Sequenz mit nur einem Element, und für das untergeordnete Element ist maxvorkommen größer als 1, wird als Array behandelt.</span><span class="sxs-lookup"><span data-stu-id="7517a-131">Element with maxOccurs larger than 1, or sequence with only one item, and the child element has maxOccurs larger than 1, is treated as array.</span></span> <span data-ttu-id="7517a-132">Für ein Array Element im Schema generiert wsutil.exe zwei Felder: ein count-Feld, das nicht an das Netzwerk gesendet wird, und ein Zeiger Feld, das den Arraytyp enthält.</span><span class="sxs-lookup"><span data-stu-id="7517a-132">For an array element in schema, wsutil.exe generates two fields: one count field that does not go on wire, and one pointer field containing the array type.</span></span>

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

<span data-ttu-id="7517a-133">Die Header Datei enthält die C-Struktur Definition für das Array, wobei das Feld die Anzahl der Arrays angibt.</span><span class="sxs-lookup"><span data-stu-id="7517a-133">Header file contains the C structure definition for the array, with field aCount specifying the count of the array.</span></span>

``` syntax
typedef struct SimpleArray
{
  unsigned int  aCount ;
  int  * a;
} SimpleArray;
```

<span data-ttu-id="7517a-134">Im folgenden finden Sie einen Teil des localdefinition-Prototyps, der das Array beschreibt:</span><span class="sxs-lookup"><span data-stu-id="7517a-134">Following is part of the LocalDefinition prototype describing the array:</span></span>

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

<span data-ttu-id="7517a-135">Im folgenden sind die generierten Definitionen der obigen Beschreibungen aufgeführt. Beachten Sie, dass sich die Feld Zuordnung für das wiederholte Element von WS-Elementen befindet, \_ \_ \_ \_ das das Feld als Array</span><span class="sxs-lookup"><span data-stu-id="7517a-135">Following is the generated definitions of the above descriptions, notice the WS\_REPEATING\_ELEMENT\_FIELD\_MAPPING which indicates the field as an array field.</span></span>

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

<span data-ttu-id="7517a-136">Wenn das Array ein Parameterfeld in der Eingabe-/Ausgabenachricht ist, werden zwei tatsächliche Parameter für die Methode generiert.</span><span class="sxs-lookup"><span data-stu-id="7517a-136">If the array is a parameter field in input/output message, there would be two actual parameters generated for the method.</span></span> <span data-ttu-id="7517a-137">Wenn das Array ein out-oder in-, out-Parameter ist, gibt es eine zusätzliche Dereferenzierungsebene für beide Felder in paramstruct.</span><span class="sxs-lookup"><span data-stu-id="7517a-137">If the array is an out or in,out parameter, there would be one additional level of indirection for both fields in paramStruct.</span></span>

## <a name="range-on-array"></a><span data-ttu-id="7517a-138">Bereich im Array</span><span class="sxs-lookup"><span data-stu-id="7517a-138">Range on Array</span></span>

<span data-ttu-id="7517a-139">Es wird empfohlen, maxvorkommen = "ungebunden" für Arrays nicht anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7517a-139">We recommend the best practice of not specifying maxOccur="unbounded" for arrays.</span></span> <span data-ttu-id="7517a-140">Stattdessen sollte eine ganzzahlige Ganzzahl angegeben werden, um eine obere Grenze der zulässigen Array Anzahl festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7517a-140">Instead, a fixed integer number should be specified to set a upper bound of array counts allowed.</span></span> <span data-ttu-id="7517a-141">Range wird für ganzzahlige Typen sowie für Zeichen folgen, Byte Arrays und generische Arrays unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7517a-141">range is supported for integral types, as well as strings, byte arrays, and generic arrays.</span></span>

## <a name="heuristic-for-wrapped-as-opposed-to-unwrapped-array"></a><span data-ttu-id="7517a-142">Die Heuristik für die umschließende und nicht das entpackte Array</span><span class="sxs-lookup"><span data-stu-id="7517a-142">Heuristic for Wrapped as Opposed to Unwrapped array</span></span>

<span data-ttu-id="7517a-143">Manchmal sind Arrays in eine andere Struktur integriert, sodass Sie in eine Struktur auf oberster Ebene eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="7517a-143">Sometimes arrays are wrapped inside another structure to be embedded in a top level structure.</span></span> <span data-ttu-id="7517a-144">In diesem Fall sollte die zwischen Wrapper Ebene entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7517a-144">In that case, we should remove the intermediate wrapper layer.</span></span> <span data-ttu-id="7517a-145">WsUtil.exe generiert denselben Prototyp und Beschreibungen wie oben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7517a-145">WsUtil.exe generates the same prototype and descriptions as SimpleArray described above.</span></span>

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

<span data-ttu-id="7517a-146">Wsutil erkennt, dass simplearraywrapper ein Wrapper um simplearray ist, und generiert nur die folgenden Strukturen mit separater Struktur für simplearray.</span><span class="sxs-lookup"><span data-stu-id="7517a-146">Wsutil detects that SimpleArrayWrapper is a wrapper around SimpleArray, and generates following structures only, with separate structure for SimpleArray</span></span>

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

<span data-ttu-id="7517a-147">wsutil.exe generiert die folgenden Definitionen für den oben stehenden Prototyp, gibt an, dass in der Feld Beschreibung die Felder Wrapper Name und Wrapper Namespace ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="7517a-147">wsutil.exe generates the following definitions for the matching prototype above, notices that in the field description, the wrapper name and wrapper namespace fields are filled in</span></span>

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

## <a name="structures"></a><span data-ttu-id="7517a-148">Strukturen</span><span class="sxs-lookup"><span data-stu-id="7517a-148">Structures</span></span>

<span data-ttu-id="7517a-149">Ein complexType-Element mit mehreren Elementen in einer Sequenz ist eine-Struktur.</span><span class="sxs-lookup"><span data-stu-id="7517a-149">A complexType with multiple elements in a sequence is a structure.</span></span> <span data-ttu-id="7517a-150">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7517a-150">For example,</span></span>

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

<span data-ttu-id="7517a-151">Wsutil.exe generiert einen Struktur Prototyp wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7517a-151">Wsutil.exe generates a structure prototype as:</span></span>

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

<span data-ttu-id="7517a-152">wsutil generiert den folgenden Prototyp für localdefinition:</span><span class="sxs-lookup"><span data-stu-id="7517a-152">wsutil generates the following prototype for LocalDefinition:</span></span>

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

<span data-ttu-id="7517a-153">Die Definition für die-Struktur sieht wie folgt aus, wobei in der-Struktur zwei Feldbeschreibungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7517a-153">The definition for the structure looks like below, with two field descriptions in the structure.</span></span>

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

<span data-ttu-id="7517a-154">Um die Erweiterbarkeit zu unterstützen, werden eingebettete Strukturen immer als Verweis definiert.</span><span class="sxs-lookup"><span data-stu-id="7517a-154">To support extensibility, embedded structures are always defined passed by reference.</span></span> <span data-ttu-id="7517a-155">In Service werden alle out-oder in-out-Strukturen durch einen doppelten Zeiger übermittelt, um eine zukünftige Erweiterung der Struktur zuzulassen und eine nillable-Struktur zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="7517a-155">In service, all out or in,out structures are passed by double pointer to allow future extension of the structure, as well as allowing nillable structure.</span></span>

## <a name="recursive-structures"></a><span data-ttu-id="7517a-156">Rekursive Strukturen</span><span class="sxs-lookup"><span data-stu-id="7517a-156">Recursive Structures</span></span>

<span data-ttu-id="7517a-157">Rekursive Strukturen werden unterstützt, und die eingebetteten Typen werden als Verweis übermittelt.</span><span class="sxs-lookup"><span data-stu-id="7517a-157">Recursive structures are supported, and the embedded types is passed by reference.</span></span> <span data-ttu-id="7517a-158">Für die folgenden WSDL:</span><span class="sxs-lookup"><span data-stu-id="7517a-158">For the following wsdl:</span></span>

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

<span data-ttu-id="7517a-159">Wsutil generiert die folgenden Typdefinitionen sowie die Typbeschreibungen:</span><span class="sxs-lookup"><span data-stu-id="7517a-159">Wsutil generates the follow type definitions, as well as the type descriptions:</span></span>

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

<span data-ttu-id="7517a-160">Die Definition wird wie folgt generiert:</span><span class="sxs-lookup"><span data-stu-id="7517a-160">The definition is generated as below:</span></span>

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

## <a name="structure-inheritence"></a><span data-ttu-id="7517a-161">Struktur ererben</span><span class="sxs-lookup"><span data-stu-id="7517a-161">Structure inheritence</span></span>

<span data-ttu-id="7517a-162">wsutil unterstützt komplexe Typerweiterungen, bei denen ein komplexer Typ eine Erweiterung eines anderen komplexen Typs ist.</span><span class="sxs-lookup"><span data-stu-id="7517a-162">wsutil supports complex type extension where one complex type is an extension to another complex type.</span></span>

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

<span data-ttu-id="7517a-163">Das obige XSD-Fragment gibt an, dass derivedlinklist von Linklist abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="7517a-163">The above xsd fragment indicates that DerivedLinkList derives from LinkList.</span></span>

<span data-ttu-id="7517a-164">Wsutil.exe generiert Hilfsroutinen für C und C++, damit die Anwendung die Typinformationen des Basistyps und der abgeleiteten Typen leichter einrichten kann.</span><span class="sxs-lookup"><span data-stu-id="7517a-164">Wsutil.exe generates helper routines for both C and C++ to make it easier for application to set up the type information of base type and derived types.</span></span> <span data-ttu-id="7517a-165">Im folgenden Code wird das \_ WS \_ CPlusPlus-Makro verwendet, um die Definition für die C-und C++-Sprache zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="7517a-165">In the following code, \_WS\_CPLUSPLUS macro is used to differentiate definition for C and C++ language:</span></span>

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

<span data-ttu-id="7517a-166">Im Hilfsprogramm für das C-Format Ruft die Anwendung vor der Serialisierung die von wsutil generierte Routine Linklist \_ Init auf, um die Struktur zu initialisieren und die Typbeschreibung auf die Beschreibung des Linklist-Typs festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7517a-166">In C style helper, before serialiation, application calls wsutil generated routine LinkList\_Init to initialize the structure and set the type description to LinkList type description.</span></span> <span data-ttu-id="7517a-167">Nach der Deserialisierung kann die Anwendung Linklist \_ als \_ derivedlinklist abrufen, um den abgeleiteten Typ abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7517a-167">After deserialization, application can call LinkList\_As\_DerivedLinkList to get the derived type.</span></span>

<span data-ttu-id="7517a-168">Zum Abrufen von Typinformationen in der Laufzeit generiert wsutil das erste Feld des Basistyps mit dem Typ " [**WS \_ struct \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description) \* Type" und " [**WS \_ Type \_ Attribute \_ Field \_ Mapping**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping) Field Mapping", um die xsi: Type-Informationen zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7517a-168">To retrieve type information in runtime, wsutil generates the first field of base type with [**WS\_STRUCT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)\* type and [**WS\_TYPE\_ATTRIBUTE\_FIELD\_MAPPING**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping) field mapping to describe the xsi:type information.</span></span> <span data-ttu-id="7517a-169">Die Anwendung kann das Feld direkt festlegen oder überprüfen, um den tatsächlichen Typ der Strukturen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="7517a-169">Application can directly set or check the field to determine the actual type of structures.</span></span> <span data-ttu-id="7517a-170">Mit dem folgenden Code wird z. b. der Typ der Struktur auf drivedlinklist festgelegt:</span><span class="sxs-lookup"><span data-stu-id="7517a-170">For example, the following code set the type of the structure to be DrivedLinkList:</span></span>

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

<span data-ttu-id="7517a-171">Nachdem die Struktur deserialisiert wurde, kann die Anwendung die Typbeschreibung direkt vergleichen, um den deserialisierten Typ zu bestimmen:</span><span class="sxs-lookup"><span data-stu-id="7517a-171">After the structure is deserialized, application can directly compares the type description to determine the deserialized type:</span></span>

``` syntax
if (derviedLinkList._base._type == (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription)
{
    // the deserialized type is of type _DerivedLinkList
    ...
}
```

<span data-ttu-id="7517a-172">wsutil generieren Sie eine Klasse für die Basis Struktur und die abgeleitete Struktur.</span><span class="sxs-lookup"><span data-stu-id="7517a-172">wsutil generate class for both base structure and derived structure.</span></span> <span data-ttu-id="7517a-173">Der Standardkonstruktor initialisiert den Typ und die übereinstimmende Typbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="7517a-173">The default constructor initialize the type and matching type description.</span></span> <span data-ttu-id="7517a-174">Die asderivedtype-Routine unterstützt die sichere Typumwandlung zwischen Typen.</span><span class="sxs-lookup"><span data-stu-id="7517a-174">The AsDerivedType routine helps to do safe type casting between types.</span></span>

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

## <a name="nillable"></a><span data-ttu-id="7517a-175">nillable</span><span class="sxs-lookup"><span data-stu-id="7517a-175">nillable</span></span>

<span data-ttu-id="7517a-176">das nillable-Attribut wird für Zeichen folgen, Strukturen und Byte Arrays unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7517a-176">nillable attribute is supported for strings, structs, and byte arrays.</span></span> <span data-ttu-id="7517a-177">Das WS \_ Field \_ NILLABLE-Attribut wird Feldern mit einem NILLABLE-Attribut hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7517a-177">WS\_FIELD\_NILLABLE attribute will be added to fields with nillable attribute.</span></span> <span data-ttu-id="7517a-178">Der Zeiger wird auf **null** festgelegt, wenn ein Element nillable ist.</span><span class="sxs-lookup"><span data-stu-id="7517a-178">The pointer will be set to **NULL** if an element is nillable.</span></span> <span data-ttu-id="7517a-179">Ein nillable-Feld in einer Struktur wird als Zeiger behandelt.</span><span class="sxs-lookup"><span data-stu-id="7517a-179">A nillable field in a structure is treated as a pointer.</span></span> <span data-ttu-id="7517a-180">Eine Parameter Struktur mit einem nillable-Attribut wird als Verweis übergeben.</span><span class="sxs-lookup"><span data-stu-id="7517a-180">A parameter structure with nillable attribute will be passed by reference.</span></span>

## <a name="pointers"></a><span data-ttu-id="7517a-181">Zeiger</span><span class="sxs-lookup"><span data-stu-id="7517a-181">pointers</span></span>

<span data-ttu-id="7517a-182">Der Werttyp muss als Wert oder als Verweis für Out-Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7517a-182">Value type must be passed by value or by reference for out parameters.</span></span> <span data-ttu-id="7517a-183">Ein doppelter Zeiger ist nicht zulässig, außer nur für out-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="7517a-183">Double pointer is not allowed except for out only structures.</span></span>

## <a name="parameterless"></a><span data-ttu-id="7517a-184">Parameterlos</span><span class="sxs-lookup"><span data-stu-id="7517a-184">Parameterless</span></span>

<span data-ttu-id="7517a-185">Erinnern Sie sich an unsere vorherige Erörterung des Namens "Parameters" für den Nachrichten Teil.</span><span class="sxs-lookup"><span data-stu-id="7517a-185">Recall our prior discussion for the "parameters" name for the message part.</span></span> <span data-ttu-id="7517a-186">Wenn dies angegeben ist, wird versucht, einen kombinierten Frame für die Eingabe-und Ausgabe Meldung für den resultierenden Dienst Vorgang zu generieren.</span><span class="sxs-lookup"><span data-stu-id="7517a-186">If this is specified we will attempt to generate a combined frame for input and output message for the resulting service operation.</span></span> <span data-ttu-id="7517a-187">Wenn dies nicht angegeben ist, würde der resultierende Dienst Vorgang Eingabe-und Ausgabe Nachrichten als Strukturen als Parameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="7517a-187">If this is not specified the resulting service operation would then contain input and output messages as structs as parameters.</span></span>

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

<span data-ttu-id="7517a-188">Daher sieht die Signatur für den Dienst und den Client für den simplemethod-Vorgang wie folgt aus:.</span><span class="sxs-lookup"><span data-stu-id="7517a-188">Thus for our SimpleMethod operation the signature for the service and the client will look like.</span></span>

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

## <a name="security"></a><span data-ttu-id="7517a-189">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="7517a-189">Security</span></span>

<span data-ttu-id="7517a-190">Siehe Abschnitt "Sicherheit" im [wsutil-Compilertool](wsutil-compiler-tool.md) und [Serialisierung](serialization.md)</span><span class="sxs-lookup"><span data-stu-id="7517a-190">See security section in [Wsutil Compiler tool](wsutil-compiler-tool.md) as well as [Serialization](serialization.md)</span></span>

 

 




