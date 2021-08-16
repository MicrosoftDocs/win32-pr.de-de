---
title: Aufbau einer IDL-Datei
description: Diese IDL-Beispieldateien veranschaulichen die grundlegenden Konstrukte der Schnittstellendefinition.
ms.assetid: 9c276b8a-5342-4c09-91a7-c9a9f0f83c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531d46bfcfa0ef4e4eee075ae65b64dd0c80a8f6a51543a1762a0ddcd8a03888
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311334"
---
# <a name="anatomy-of-an-idl-file"></a>Aufbau einer IDL-Datei

Diese IDL-Beispieldateien veranschaulichen die grundlegenden Konstrukte der Schnittstellendefinition. Speicherbelegung, benutzerdefiniertes Marshalling und asynchrones Messaging sind nur einige der Features, die Sie in einer benutzerdefinierten COM-Schnittstelle implementieren können. MIDL-Attribute werden verwendet, um COM-Schnittstellen zu definieren. Weitere Informationen zum Implementieren von Schnittstellen und Typbibliotheken, einschließlich einer Zusammenfassung der MIDL-Attribute, finden Sie unter [Schnittstellendefinitionen und Typbibliotheken](/windows/desktop/Midl/interface-definitions-and-type-libraries) im MIDL-Programmierhandbuch und -Referenz. Eine vollständige Referenz aller MIDL-Attribute, -Schlüsselwörter und -Anweisungen finden Sie in der [MIDL-Sprachreferenz.](/windows/desktop/Midl/midl-language-reference)

## <a name="exampleidl"></a>Example.idl

Die folgende IDL-Beispieldatei definiert zwei COM-Schnittstellen. Aus dieser IDL-Datei generiert Midl.exe Proxy-/Stub- und Marshallingcode- und Headerdateien. Eine Zeilen-für-Zeile-Dissection folgt dem Beispiel.

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

Die [**IDL-Import-Anweisung**](/windows/desktop/Midl/import) wird hier verwendet, um die Headerdatei Mydefs.h einzubringen, die benutzerdefinierte Typen enthält, und Unknwn.idl, die die Definition von [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)enthält, von der IFace1 und IFace2 abgeleitet werden.

Das [](/windows/desktop/Midl/object) Objektattribut identifiziert die Schnittstelle als Objektschnittstelle und weist den MIDL-Compiler an, Proxy-/Stubcode anstelle von RPC-Client- und -Serverstubs zu generieren. Objektschnittstellenmethoden müssen den Rückgabetyp [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)aufweisen, damit der zugrunde liegende RPC-Mechanismus Fehler für Aufrufe melden kann, die aufgrund von Netzwerkproblemen nicht abgeschlossen werden können.

Das [**uuid-Attribut**](/windows/desktop/Midl/uuid) gibt den Schnittstellenbezeichner (INTERFACE Identifier, IID) an. Jede Schnittstelle, Klasse und Typbibliothek muss mit einem eigenen eindeutigen Bezeichner identifiziert werden. Verwenden Sie das Hilfsprogramm Uuidgen.exe, um einen Satz eindeutiger IDs für Ihre Schnittstellen und andere Komponenten zu generieren.

Das [**Schnittstellenschlüsselwort**](/windows/desktop/Midl/interface) definiert den Schnittstellennamen. Alle Objektschnittstellen müssen direkt oder indirekt von [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)abgeleitet werden.

Der [**indirektionale**](/windows/desktop/Midl/in) Parameter gibt einen Parameter an, der nur vom Aufrufer festgelegt wird. Der [**out-Parameter**](/windows/desktop/Midl/out-idl) gibt Daten an, die an den Aufrufer übergeben werden. Die Verwendung beider richtungsweisen Attribute für einen Parameter gibt an, dass der -Parameter sowohl zum Senden von Daten an die -Methode als auch zum Zurückgeben von Daten an den Aufrufer verwendet wird.

Das [**\_ Zeigerstandardattribut**](/windows/desktop/Midl/pointer-default) gibt den Standardzeigertyp ([**eindeutig,**](/windows/desktop/Midl/unique) [**ref**](/windows/desktop/Midl/ref)oder [**ptr**](/windows/desktop/Midl/ptr)) für alle Zeiger an, mit Ausnahme der in Parameterlisten enthaltenen Zeiger. Wenn kein Standardtyp angegeben wird, geht MIDL davon aus, dass einzelne Zeiger **eindeutig** sind. Wenn Sie jedoch über mehrere Zeigerebenen verfügen, müssen Sie explizit einen Standardzeigertyp angeben, auch wenn der Standardtyp **eindeutig** sein soll.

Im vorherigen Beispiel ist das Array BkfstStuff \[ \] ein *konformes Array,* dessen Größe zur Laufzeit bestimmt wird. Das [**Attribut max \_ is**](/windows/desktop/Midl/max-is) gibt die Variable an, die den Maximalen Wert für den Arrayindex enthält.

Das Size [**\_ is-Attribut**](/windows/desktop/Midl/size-is) wird auch verwendet, um die Größe eines Arrays oder, wie im vorherigen Beispiel, mehrere Zeigerebenen anzugeben. In diesem Beispiel kann der Aufruf erfolgen, ohne im Voraus zu wissen, wie viele Daten zurückgegeben werden.

## <a name="example2idl"></a>Example2.idl

Das folgende IDL-Beispiel (das die im vorherigen IDL-Beispiel beschriebenen Schnittstellen wiederverwendet) zeigt die verschiedenen Möglichkeiten zum Generieren von Typbibliotheksinformationen für Schnittstellen.

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

Das [**helpstring-Attribut**](/windows/desktop/Midl/helpstring) ist optional. Sie verwenden es, um das Objekt kurz zu beschreiben oder um eine Statuszeile bereitzustellen. Diese Hilfezeichenfolgen sind mit einem Objektbrowser lesbar, z. B. dem mit Microsoft Visual Basic bereitgestellten.

Das [**duale**](/windows/desktop/Midl/dual) Attribut in IFace3 erstellt eine Schnittstelle, die sowohl eine Dispatchschnittstelle als auch eine COM-Schnittstelle ist. Da sie von **IDispatch** abgeleitet ist, unterstützt eine duale Schnittstelle Automation, was vom [**oleautomation-Attribut**](/windows/desktop/Midl/oleautomation) angegeben wird. IFace3 importiert Oaidl.idl, um die Definition von **IDispatch** abzurufen.

Die [**Library-Anweisung**](/windows/desktop/Midl/library) definiert die ExampleLib-Typbibliothek, die über eigene [**uuid-,**](/windows/desktop/Midl/uuid) [**helpstring-**](/windows/desktop/Midl/helpstring)und [**versionsattribute**](/windows/desktop/Midl/version) verfügt.

Innerhalb der Definition der Typbibliothek wird mit der [**importlib-Direktive**](/windows/desktop/Midl/importlib) eine kompilierte Typbibliothek hinzugefügt. Alle Typbibliotheksdefinitionen sollten die in Stdole32.tlb definierte Basistypbibliothek verwenden.

Diese Typbibliotheksdefinition veranschaulicht drei verschiedene Möglichkeiten zum Einschließen von Schnittstellen in die Typbibliothek. IFace3 ist nur enthalten, indem in der Bibliotheks-Anweisung darauf verwiesen wird.

Die [**coclass-Anweisung**](/windows/desktop/Midl/coclass) definiert eine völlig neue Komponentenklasse, BkfstComponent, die zwei zuvor definierte Schnittstellen enthält: IFace1 und IFace2. Das Standardattribut kennzeichnet IFace1 als Standardschnittstelle.

IFace4 wird in der Library-Anweisung beschrieben. Das [**Propput-Attribut**](/windows/desktop/Midl/propput) für MethodD gibt an, dass die Methode eine festgelegte Aktion für eine Eigenschaft mit dem gleichen Namen ausführt. Das [**propget-Attribut**](/windows/desktop/Midl/propget) gibt an, dass die Methode Informationen aus einer Eigenschaft mit dem gleichen Namen wie die Methode abruft. Das [**Attribut retval**](/windows/desktop/Midl/retval) in MethodD legt einen Ausgabeparameter fest, der den Rückgabewert der Funktion enthält.

 

 
