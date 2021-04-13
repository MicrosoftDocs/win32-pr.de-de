---
title: Anatomie einer IDL-Datei
description: Diese Beispiel-IDL-Dateien veranschaulichen die grundlegenden Konstrukte der Schnittstellen Definition.
ms.assetid: 9c276b8a-5342-4c09-91a7-c9a9f0f83c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acbcfbf5c145a1fb389cc26543cf75d8cc75a107
ms.sourcegitcommit: 5ebaf3a456bc68cd0c6bd46c8135b67b1bf6fa54
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "104351009"
---
# <a name="anatomy-of-an-idl-file"></a><span data-ttu-id="3a479-103">Anatomie einer IDL-Datei</span><span class="sxs-lookup"><span data-stu-id="3a479-103">Anatomy of an IDL File</span></span>

<span data-ttu-id="3a479-104">Diese Beispiel-IDL-Dateien veranschaulichen die grundlegenden Konstrukte der Schnittstellen Definition.</span><span class="sxs-lookup"><span data-stu-id="3a479-104">These example IDL files demonstrate the fundamental constructs of interface definition.</span></span> <span data-ttu-id="3a479-105">Die Speicher Belegung, das benutzerdefinierte Marshalling und das asynchrone Messaging sind nur einige der Features, die Sie in einer benutzerdefinierten COM-Schnittstelle implementieren können.</span><span class="sxs-lookup"><span data-stu-id="3a479-105">Memory allocation, custom marshaling, and asynchronous messaging are just a few of the features you can implement in a custom COM interface.</span></span> <span data-ttu-id="3a479-106">Mit den-Mittelpunkt Attributen werden COM-Schnittstellen definiert.</span><span class="sxs-lookup"><span data-stu-id="3a479-106">MIDL attributes are used to define COM interfaces.</span></span> <span data-ttu-id="3a479-107">Weitere Informationen zum Implementieren von Schnittstellen und Typbibliotheken, einschließlich einer Zusammenfassung der Mittel l-Attribute, finden Sie unter [Schnittstellendefinitionen und Typbibliotheken](/windows/desktop/Midl/interface-definitions-and-type-libraries) im Programmier Handbuch zu Programmier-und Referenzinformationen.</span><span class="sxs-lookup"><span data-stu-id="3a479-107">For more information about implementing interfaces and type libraries, including a summary of MIDL attributes, see [Interface Definitions and Type Libraries](/windows/desktop/Midl/interface-definitions-and-type-libraries) in the MIDL Programmer's Guide and Reference.</span></span> <span data-ttu-id="3a479-108">Einen vollständigen Verweis auf alle Mittel l-Attribute, Schlüsselwörter und Direktiven finden Sie in der [Referenz zur Mittel l-Sprache](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="3a479-108">For a complete reference of all MIDL attributes, keywords, and directives, see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

## <a name="exampleidl"></a><span data-ttu-id="3a479-109">Beispiel. idl</span><span class="sxs-lookup"><span data-stu-id="3a479-109">Example.idl</span></span>

<span data-ttu-id="3a479-110">Die folgende Beispiel-IDL-Datei definiert zwei COM-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="3a479-110">The following example IDL file defines two COM interfaces.</span></span> <span data-ttu-id="3a479-111">Aus dieser IDL-Datei generiert Midl.exe Proxy/Stub-und Marshallingcode und Header Dateien.</span><span class="sxs-lookup"><span data-stu-id="3a479-111">From this IDL file, Midl.exe will generate proxy/stub and marshaling code and header files.</span></span> <span data-ttu-id="3a479-112">Im Beispiel wird ein Zeilen-für-Zeile-Analyse befolgt.</span><span class="sxs-lookup"><span data-stu-id="3a479-112">A line-by-line dissection follows the example.</span></span>

``` syntax
//
// Example.idl 
//
import "mydefs.h","unknwn.idl"; 
[
object,
uuid(a03d1420-b1ec-11d0-8c3a-00c04fc31d2f),
] interface IFace1 : IUnknown
{
HRESULT MethodA([in] short Bread, [out] BKFST * pBToast);
HRESULT MethodB([in, out] BKFST * pBPoptart);
};
 
[
object,
uuid(a03d1421-b1ec-11d0-8c3a-00c04fc31d2f),
pointer_default(unique)
] interface IFace2 : IUnknown
{
HRESULT MethodC([in] long Max,
                [in, max_is(Max)] BkfstStuff[ ],
                [out] long * pSize,
                [out, size_is( , *pSize)] BKFST ** ppBKFST);
}; 
 
```

<span data-ttu-id="3a479-113">Die IDL- [**Import**](/windows/desktop/Midl/import) -Anweisung wird hier verwendet, um eine Header Datei, mydefs. h, die benutzerdefinierte Typen enthält, und unknwn. idl zu verwenden, die die Definition von [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)enthält, von der IFace1 und IFace2 abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="3a479-113">The IDL [**import**](/windows/desktop/Midl/import) statement is used here to bring in a header file, Mydefs.h, which contains user-defined types, and Unknwn.idl, which contains the definition of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), from which IFace1 and IFace2 derive.</span></span>

<span data-ttu-id="3a479-114">Das [**Object**](/windows/desktop/Midl/object) -Attribut identifiziert die-Schnittstelle als Objektschnittstelle und weist den Mittelwert Compiler an, Proxy-/Stubcode anstelle von RPC-Client-und Serverstubs zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3a479-114">The [**object**](/windows/desktop/Midl/object) attribute identifies the interface as an object interface and tells the MIDL compiler to generate proxy/stub code instead of RPC client and server stubs.</span></span> <span data-ttu-id="3a479-115">Objekt Schnittstellen Methoden müssen einen Rückgabetyp von [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)aufweisen, damit der zugrunde liegende RPC-Mechanismus Fehler für Aufrufe meldet, die aufgrund von Netzwerkproblemen nicht ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="3a479-115">Object interface methods must have a return type of [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a), to allow the underlying RPC mechanism to report errors for calls that fail to complete due to network problems.</span></span>

<span data-ttu-id="3a479-116">Das [**UUID**](/windows/desktop/Midl/uuid) -Attribut gibt den Schnittstellen Bezeichner (IID) an.</span><span class="sxs-lookup"><span data-stu-id="3a479-116">The [**uuid**](/windows/desktop/Midl/uuid) attribute specifies the interface identifier (IID).</span></span> <span data-ttu-id="3a479-117">Jede Schnittstelle, Klasse und Typbibliothek muss mit einem eigenen eindeutigen Bezeichner identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="3a479-117">Each interface, class, and type library must be identified with its own unique identifier.</span></span> <span data-ttu-id="3a479-118">Verwenden Sie das Hilfsprogramm Uuidgen.exe, um einen Satz eindeutiger IDs für ihre Schnittstellen und andere Komponenten zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3a479-118">Use the utility Uuidgen.exe to generate a set of unique IDs for your interfaces and other components.</span></span>

<span data-ttu-id="3a479-119">Das [**Interface**](/windows/desktop/Midl/interface) -Schlüsselwort definiert den Namen der Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3a479-119">The [**interface**](/windows/desktop/Midl/interface) keyword defines the interface name.</span></span> <span data-ttu-id="3a479-120">Alle Objekt Schnittstellen müssen direkt oder indirekt von [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="3a479-120">All object interfaces must derive, directly or indirectly, from [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span></span>

<span data-ttu-id="3a479-121">Der [**in**](/windows/desktop/Midl/in) direktionale Parameter gibt einen Parameter an, der nur vom Aufrufer festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3a479-121">The [**in**](/windows/desktop/Midl/in) directional parameter specifies a parameter that is set only by the caller.</span></span> <span data-ttu-id="3a479-122">Der [**out**](/windows/desktop/Midl/out-idl) -Parameter gibt Daten an, die an den Aufrufer zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3a479-122">The [**out**](/windows/desktop/Midl/out-idl) parameter specifies data that is passed back to the caller.</span></span> <span data-ttu-id="3a479-123">Die Verwendung beider direktionaler Attribute für einen Parameter gibt an, dass der-Parameter verwendet wird, um Daten an die-Methode zu senden und Daten an den Aufrufer zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="3a479-123">Using both directional attributes on one parameter specifies that the parameter is used both to send data to the method and to pass data back to the caller.</span></span>

<span data-ttu-id="3a479-124">Das [**\_ default**](/windows/desktop/Midl/pointer-default) -Attribut Attribut gibt den Standard Zeigertyp ([**Unique**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref)oder [**ptr**](/windows/desktop/Midl/ptr)) für alle Zeiger an, mit Ausnahme derjenigen, die in Parameterlisten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="3a479-124">The [**pointer\_default**](/windows/desktop/Midl/pointer-default) attribute specifies the default pointer type ([**unique**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref), or [**ptr**](/windows/desktop/Midl/ptr)) for all pointers except for those included in parameter lists.</span></span> <span data-ttu-id="3a479-125">Wenn kein Standardtyp angegeben wird, wird von der Mittell ausgegangen, dass einzelne Zeiger **eindeutig** sind.</span><span class="sxs-lookup"><span data-stu-id="3a479-125">If no default type is specified, MIDL assumes that single pointers are **unique**.</span></span> <span data-ttu-id="3a479-126">Wenn Sie jedoch über mehrere Zeiger Ebenen verfügen, müssen Sie einen Standard Zeigertyp explizit angeben, auch wenn der Standardtyp **eindeutig** sein soll.</span><span class="sxs-lookup"><span data-stu-id="3a479-126">However, when you have multiple levels of pointers, you must explicitly specify a default pointer type, even if you want the default type to be **unique**.</span></span>

<span data-ttu-id="3a479-127">Im vorherigen Beispiel ist das Array bkfststuff \[ \] ein *konformes Array*, dessen Größe zur Laufzeit bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="3a479-127">In the preceding example, the array BkfstStuff\[ \] is a *conformant array*, the size of which is determined at run time.</span></span> <span data-ttu-id="3a479-128">Das [**Maximum \_ is**](/windows/desktop/Midl/max-is) -Attribut gibt die Variable an, die den maximalen Wert für den Array Index enthält.</span><span class="sxs-lookup"><span data-stu-id="3a479-128">The [**max\_is**](/windows/desktop/Midl/max-is) attribute specifies the variable that contains the maximum value for the array index.</span></span>

<span data-ttu-id="3a479-129">Die [**Größe \_**](/windows/desktop/Midl/size-is) "Attribute" wird auch verwendet, um die Größe eines Arrays anzugeben, oder, wie im vorherigen Beispiel, mehrere Ebenen von Zeigern.</span><span class="sxs-lookup"><span data-stu-id="3a479-129">The [**size\_is**](/windows/desktop/Midl/size-is) attribute is also used to specify the size of an array or, as in the preceding example, multiple levels of pointers.</span></span> <span data-ttu-id="3a479-130">Im Beispiel kann der-Befehl durchgeführt werden, ohne im Voraus zu wissen, wie viele Daten zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3a479-130">In the example, the call can be made without knowing in advance how much data will be returned.</span></span>

## <a name="example2idl"></a><span data-ttu-id="3a479-131">"Example2". idl</span><span class="sxs-lookup"><span data-stu-id="3a479-131">Example2.idl</span></span>

<span data-ttu-id="3a479-132">Das folgende IDL-Beispiel (das die im vorherigen IDL-Beispiel beschriebenen Schnittstellen wieder verwendet) zeigt die verschiedenen Möglichkeiten zum Generieren von Typbibliotheks Informationen für Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="3a479-132">The following IDL example (which reuses the interfaces described in the previous IDL example) shows the various ways to generate type library information for interfaces.</span></span>

``` syntax
//
// Example2.idl
//

import "example.idl","oaidl.idl"; 

[
uuid(a03d1422-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace3 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace3 : IDispatch
{
   HRESULT MethodD([in] BSTR OrderIn,
                   [out, retval] * pTakeOut);
}; //end IFace3 def

[
uuid(a03d1423-b1ec-11d0-8c3a-00c04fc31d2f),
version(1.0),
helpstring("Example Type Library"),
] library ExampleLib
{
  importlib("stdole32.tlb");
  interface IFace3;
  [
  uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
  helpstring("Breakfast Component Class")
  ] coclass BkfstComponent
    {
    [default]interface IFace1;
    interfaceIFace2
    }; //end coclass def

[
uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace4 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace4 : IDispatch
{
[propput] HRESULT MethodD([in] BSTR OrderIn);
[propget] HRESULT MethodE([out, retval] * pTakeOut);
}; //end IFace4 def
 
}; //end library def
 
```

<span data-ttu-id="3a479-133">Das [**HelpString**](/windows/desktop/Midl/helpstring) -Attribut ist optional. Sie verwenden Sie, um das Objekt kurz zu beschreiben oder eine Statuszeile bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3a479-133">The [**helpstring**](/windows/desktop/Midl/helpstring) attribute is optional; you use it to briefly describe the object or to provide a status line.</span></span> <span data-ttu-id="3a479-134">Diese Hilfe Zeichenfolgen sind mit einem Objektkatalog lesbar, z. b. dem, der in Microsoft Visual Basic enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="3a479-134">These help strings are readable with an object browser such as the one provided with Microsoft Visual Basic.</span></span>

<span data-ttu-id="3a479-135">Das [**Dual**](/windows/desktop/Midl/dual) -Attribut auf IFace3 erstellt eine Schnittstelle, die sowohl eine Dispatchschnittstelle als auch eine COM-Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="3a479-135">The [**dual**](/windows/desktop/Midl/dual) attribute on IFace3 creates an interface that is both a dispatch interface and a COM interface.</span></span> <span data-ttu-id="3a479-136">Da es von **IDispatch** abgeleitet ist, unterstützt eine duale Schnittstelle die Automatisierung, was das [**oleautomation**](/windows/desktop/Midl/oleautomation) -Attribut angibt.</span><span class="sxs-lookup"><span data-stu-id="3a479-136">Because it is derived from **IDispatch**, a dual interface supports Automation, which is what the [**oleautomation**](/windows/desktop/Midl/oleautomation) attribute specifies.</span></span> <span data-ttu-id="3a479-137">IFace3 importiert oaidl. idl, um die Definition von **IDispatch** zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3a479-137">IFace3 imports Oaidl.idl to get the definition of **IDispatch**.</span></span>

<span data-ttu-id="3a479-138">Die [**Library**](/windows/desktop/Midl/library) -Anweisung definiert die examplelib-Typbibliothek, die über eigene [**UUID**](/windows/desktop/Midl/uuid)-, [**HelpString**](/windows/desktop/Midl/helpstring)-und [**Versions**](/windows/desktop/Midl/version) Attribute verfügt.</span><span class="sxs-lookup"><span data-stu-id="3a479-138">The [**library**](/windows/desktop/Midl/library) statement defines the ExampleLib type library, which has its own [**uuid**](/windows/desktop/Midl/uuid), [**helpstring**](/windows/desktop/Midl/helpstring), and [**version**](/windows/desktop/Midl/version) attributes.</span></span>

<span data-ttu-id="3a479-139">In der Typbibliotheks Definition führt die [**importlib**](/windows/desktop/Midl/importlib) -Direktive eine kompilierte Typbibliothek ein.</span><span class="sxs-lookup"><span data-stu-id="3a479-139">Within the type library definition, the [**importlib**](/windows/desktop/Midl/importlib) directive brings in a compiled type library.</span></span> <span data-ttu-id="3a479-140">Alle Typbibliotheks Definitionen sollten die in Stdole32. tlb definierte basistypbibliothek in die Basisklasse bringen.</span><span class="sxs-lookup"><span data-stu-id="3a479-140">All type library definitions should bring in the base type library defined in Stdole32.tlb.</span></span>

<span data-ttu-id="3a479-141">Diese Typbibliotheks Definition veranschaulicht drei verschiedene Möglichkeiten, Schnittstellen in der Typbibliothek einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="3a479-141">This type library definition demonstrates three different ways to include interfaces in the type library.</span></span> <span data-ttu-id="3a479-142">IFace3 wird nur durch Verweisen in der Library-Anweisung eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="3a479-142">IFace3 is included merely by referencing it within the library statement.</span></span>

<span data-ttu-id="3a479-143">Die [**Co-Klasse**](/windows/desktop/Midl/coclass) -Anweisung definiert eine vollständig neue Komponenten Klasse, bkfstcomponent, die zwei zuvor definierte Schnittstellen enthält, IFace1 und IFace2.</span><span class="sxs-lookup"><span data-stu-id="3a479-143">The [**coclass**](/windows/desktop/Midl/coclass) statement defines an entirely new component class, BkfstComponent, that includes two previously defined interfaces, IFace1 and IFace2.</span></span> <span data-ttu-id="3a479-144">Das Standard Attribut bezeichnet IFace1 als Standardschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3a479-144">The default attribute designates IFace1 as the default interface.</span></span>

<span data-ttu-id="3a479-145">IFace4 wird in der Library-Anweisung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3a479-145">IFace4 is described within the library statement.</span></span> <span data-ttu-id="3a479-146">Das [**PROPPUT**](/windows/desktop/Midl/propput) -Attribut in methodd gibt an, dass die Methode eine Set-Aktion für eine Eigenschaft mit demselben Namen ausführt.</span><span class="sxs-lookup"><span data-stu-id="3a479-146">The [**propput**](/windows/desktop/Midl/propput) attribute on MethodD indicates that the method performs a set action on a property of the same name.</span></span> <span data-ttu-id="3a479-147">Das [**propget**](/windows/desktop/Midl/propget) -Attribut gibt an, dass die-Methode Informationen aus einer Eigenschaft mit dem gleichen Namen wie die-Methode abruft.</span><span class="sxs-lookup"><span data-stu-id="3a479-147">The [**propget**](/windows/desktop/Midl/propget) attribute indicates that the method retrieves information from a property of the same name as the method.</span></span> <span data-ttu-id="3a479-148">Das [**retval**](/windows/desktop/Midl/retval) -Attribut in methodd bezeichnet einen Output-Parameter, der den Rückgabewert der Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="3a479-148">The [**retval**](/windows/desktop/Midl/retval) attribute in MethodD designates an output parameter that contains the return value of the function.</span></span>

 

 
