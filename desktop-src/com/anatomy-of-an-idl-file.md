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
# <a name="anatomy-of-an-idl-file"></a>Anatomie einer IDL-Datei

Diese Beispiel-IDL-Dateien veranschaulichen die grundlegenden Konstrukte der Schnittstellen Definition. Die Speicher Belegung, das benutzerdefinierte Marshalling und das asynchrone Messaging sind nur einige der Features, die Sie in einer benutzerdefinierten COM-Schnittstelle implementieren können. Mit den-Mittelpunkt Attributen werden COM-Schnittstellen definiert. Weitere Informationen zum Implementieren von Schnittstellen und Typbibliotheken, einschließlich einer Zusammenfassung der Mittel l-Attribute, finden Sie unter [Schnittstellendefinitionen und Typbibliotheken](/windows/desktop/Midl/interface-definitions-and-type-libraries) im Programmier Handbuch zu Programmier-und Referenzinformationen. Einen vollständigen Verweis auf alle Mittel l-Attribute, Schlüsselwörter und Direktiven finden Sie in der [Referenz zur Mittel l-Sprache](/windows/desktop/Midl/midl-language-reference).

## <a name="exampleidl"></a>Beispiel. idl

Die folgende Beispiel-IDL-Datei definiert zwei COM-Schnittstellen. Aus dieser IDL-Datei generiert Midl.exe Proxy/Stub-und Marshallingcode und Header Dateien. Im Beispiel wird ein Zeilen-für-Zeile-Analyse befolgt.

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

Die IDL- [**Import**](/windows/desktop/Midl/import) -Anweisung wird hier verwendet, um eine Header Datei, mydefs. h, die benutzerdefinierte Typen enthält, und unknwn. idl zu verwenden, die die Definition von [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)enthält, von der IFace1 und IFace2 abgeleitet werden.

Das [**Object**](/windows/desktop/Midl/object) -Attribut identifiziert die-Schnittstelle als Objektschnittstelle und weist den Mittelwert Compiler an, Proxy-/Stubcode anstelle von RPC-Client-und Serverstubs zu generieren. Objekt Schnittstellen Methoden müssen einen Rückgabetyp von [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)aufweisen, damit der zugrunde liegende RPC-Mechanismus Fehler für Aufrufe meldet, die aufgrund von Netzwerkproblemen nicht ausgeführt werden können.

Das [**UUID**](/windows/desktop/Midl/uuid) -Attribut gibt den Schnittstellen Bezeichner (IID) an. Jede Schnittstelle, Klasse und Typbibliothek muss mit einem eigenen eindeutigen Bezeichner identifiziert werden. Verwenden Sie das Hilfsprogramm Uuidgen.exe, um einen Satz eindeutiger IDs für ihre Schnittstellen und andere Komponenten zu generieren.

Das [**Interface**](/windows/desktop/Midl/interface) -Schlüsselwort definiert den Namen der Schnittstelle. Alle Objekt Schnittstellen müssen direkt oder indirekt von [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)abgeleitet werden.

Der [**in**](/windows/desktop/Midl/in) direktionale Parameter gibt einen Parameter an, der nur vom Aufrufer festgelegt wird. Der [**out**](/windows/desktop/Midl/out-idl) -Parameter gibt Daten an, die an den Aufrufer zurückgegeben werden. Die Verwendung beider direktionaler Attribute für einen Parameter gibt an, dass der-Parameter verwendet wird, um Daten an die-Methode zu senden und Daten an den Aufrufer zurückzugeben.

Das [**\_ default**](/windows/desktop/Midl/pointer-default) -Attribut Attribut gibt den Standard Zeigertyp ([**Unique**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref)oder [**ptr**](/windows/desktop/Midl/ptr)) für alle Zeiger an, mit Ausnahme derjenigen, die in Parameterlisten enthalten sind. Wenn kein Standardtyp angegeben wird, wird von der Mittell ausgegangen, dass einzelne Zeiger **eindeutig** sind. Wenn Sie jedoch über mehrere Zeiger Ebenen verfügen, müssen Sie einen Standard Zeigertyp explizit angeben, auch wenn der Standardtyp **eindeutig** sein soll.

Im vorherigen Beispiel ist das Array bkfststuff \[ \] ein *konformes Array*, dessen Größe zur Laufzeit bestimmt wird. Das [**Maximum \_ is**](/windows/desktop/Midl/max-is) -Attribut gibt die Variable an, die den maximalen Wert für den Array Index enthält.

Die [**Größe \_**](/windows/desktop/Midl/size-is) "Attribute" wird auch verwendet, um die Größe eines Arrays anzugeben, oder, wie im vorherigen Beispiel, mehrere Ebenen von Zeigern. Im Beispiel kann der-Befehl durchgeführt werden, ohne im Voraus zu wissen, wie viele Daten zurückgegeben werden.

## <a name="example2idl"></a>"Example2". idl

Das folgende IDL-Beispiel (das die im vorherigen IDL-Beispiel beschriebenen Schnittstellen wieder verwendet) zeigt die verschiedenen Möglichkeiten zum Generieren von Typbibliotheks Informationen für Schnittstellen.

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

Das [**HelpString**](/windows/desktop/Midl/helpstring) -Attribut ist optional. Sie verwenden Sie, um das Objekt kurz zu beschreiben oder eine Statuszeile bereitzustellen. Diese Hilfe Zeichenfolgen sind mit einem Objektkatalog lesbar, z. b. dem, der in Microsoft Visual Basic enthalten ist.

Das [**Dual**](/windows/desktop/Midl/dual) -Attribut auf IFace3 erstellt eine Schnittstelle, die sowohl eine Dispatchschnittstelle als auch eine COM-Schnittstelle ist. Da es von **IDispatch** abgeleitet ist, unterstützt eine duale Schnittstelle die Automatisierung, was das [**oleautomation**](/windows/desktop/Midl/oleautomation) -Attribut angibt. IFace3 importiert oaidl. idl, um die Definition von **IDispatch** zu erhalten.

Die [**Library**](/windows/desktop/Midl/library) -Anweisung definiert die examplelib-Typbibliothek, die über eigene [**UUID**](/windows/desktop/Midl/uuid)-, [**HelpString**](/windows/desktop/Midl/helpstring)-und [**Versions**](/windows/desktop/Midl/version) Attribute verfügt.

In der Typbibliotheks Definition führt die [**importlib**](/windows/desktop/Midl/importlib) -Direktive eine kompilierte Typbibliothek ein. Alle Typbibliotheks Definitionen sollten die in Stdole32. tlb definierte basistypbibliothek in die Basisklasse bringen.

Diese Typbibliotheks Definition veranschaulicht drei verschiedene Möglichkeiten, Schnittstellen in der Typbibliothek einzuschließen. IFace3 wird nur durch Verweisen in der Library-Anweisung eingeschlossen.

Die [**Co-Klasse**](/windows/desktop/Midl/coclass) -Anweisung definiert eine vollständig neue Komponenten Klasse, bkfstcomponent, die zwei zuvor definierte Schnittstellen enthält, IFace1 und IFace2. Das Standard Attribut bezeichnet IFace1 als Standardschnittstelle.

IFace4 wird in der Library-Anweisung beschrieben. Das [**PROPPUT**](/windows/desktop/Midl/propput) -Attribut in methodd gibt an, dass die Methode eine Set-Aktion für eine Eigenschaft mit demselben Namen ausführt. Das [**propget**](/windows/desktop/Midl/propget) -Attribut gibt an, dass die-Methode Informationen aus einer Eigenschaft mit dem gleichen Namen wie die-Methode abruft. Das [**retval**](/windows/desktop/Midl/retval) -Attribut in methodd bezeichnet einen Output-Parameter, der den Rückgabewert der Funktion enthält.

 

 
