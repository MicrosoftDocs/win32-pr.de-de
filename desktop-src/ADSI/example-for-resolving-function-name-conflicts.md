---
title: Beispiel für das Auflösen von Funktionsnamens Konflikten
description: In diesem Thema wird beschrieben, wie Konflikte bei Funktionsnamen beim Erstellen einer Erweiterung für ADSI gelöst werden.
ms.assetid: 8121f037-3845-44ba-a2cd-8d7f15e0beb2
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, Beispielcode Visual Basic, Auflösen von Funktionsnamen Konflikten
- Auflösen von Funktionsnamens Konflikten ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049f9ce6447bf6d6ead783db3e34f74374333f10
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316466"
---
# <a name="example-for-resolving-function-name-conflicts"></a>Beispiel für das Auflösen von Funktionsnamens Konflikten

Beachten Sie Folgendes:

-   IADs0 unterstützt Func0 nicht.
-   IADs1 unterstützt func1 und Func0.
-   IADs2 unterstützt func2 und Func0.

Alle drei Schnittstellen sind duale Schnittstellen.


```C++
IADs0 : IDispatch
{
    OtherFunc();
}

IADs1 : IDispatch
{
    Func0() 
    Func1();
}

IADs2 : IDispatch
{
    Func0()
    Func2();
}
```




```VB
Dim myInf1 as IADs1
 
myInf1.Func1  ' IADs1::Func1 is invoked using direct vtable access 
 
myInf1.Func2  ' IADs2::Func2 is invoked using GetIDsOfNames/Invoke
```



Obwohl IADs1 func2 nicht unterstützt, erkennt ein ADSI-Client eine [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , die alle Dual-und Dispatch-Schnittstellen im Modell unterstützt. Daher kann der ADSI-Client func2 direkt mithilfe von myInf1. func2 aufzurufen, ohne aufzulösen, welche Schnittstelle func2 unterstützt.


```VB
myInf1.Func2
```



Sowohl IADs1 als auch IADs2 verfügen über eine Funktion mit dem Namen Func0, IADs1:: Func0 wird jedoch direkt mithilfe des Vtable-Zugriffs aufgerufen, da für den Client beide folgenden Bedingungen zutreffen:

-   Der Client verfügt über einen Zeiger auf das Dual Interface IADs1 Object, das eine Funktion mit dem Namen "Func0" aufweist.
-   Visual Basic unterstützt den direkten Vtable-Zugriff, wobei angenommen wird, dass der Datentyp über die Typbibliothek verfügbar ist.

Im nächsten Codebeispiel verfügt der Client über einen Dual-Interface-Zeiger auf IADs2 anstelle von IADs1. Daher wird IADs2:: Func0 mit direktem Vtable-Zugriff aufgerufen.


```VB
Dim myInf2 as IADs2
Set myInf2 = myInf1 ' Query for pointer to IADs2 
myInf2.Func0
```



Im nächsten Codebeispiel verfügen sowohl IADs1 als auch IADs2 über eine Funktion mit dem Namen Func0, aber hier hat der Client einen Zeiger auf eine duale Schnittstelle, IADs0, die keine Funktion mit dem Namen Func0 hat. Daher kann kein direkter Vtable-Zugriff ausgeführt werden. Stattdessen werden [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) und [**Aufruf**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) aufgerufen, um Func0 aufzurufen.


```VB
Dim myInfNone as IADs0
Set myInfNone = myInf1    ' The aggregated object that 
   ' supports IADs1 and IADs2.
myInfNone.Func0
```



Beachten Sie die folgenden beiden Fälle:

-   IADs1 und IADs2 werden von den beiden com-Komponenten EXT1 bzw. ext2 implementiert. Wenn EXT1 in der Registrierung vor EXT2 steht, wird IADs1:: Func0 aufgerufen. Wenn der Wert für "ext2" in der Registrierung jedoch an erster Stelle steht, wird IADs2:: Func0 aufgerufen.
-   Wenn IADs1 und ADs2 durch das gleiche Erweiterungs Objekt implementiert werden, wird Func0 immer von der [**iadsextension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) -und [**privateinvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) -Methode der Erweiterung aufgerufen.

Der Erweiterungs Entwickler muss bestimmen, wie Konflikte von Funktionen oder Eigenschaften von unterschiedlichen Dual- [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstellen, die in einer Erweiterung denselben Namen haben, gelöst werden können. Die Implementierung von [**iadsextension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) -und [**privateinvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) -Methoden sollten diesen Konflikt lösen. Wenn Sie z. b. IMyInterface1:: func1 und IMyInterface2:: func1 verwenden, sind IMyInterface1 und IMyInterface2 duale **IDispatch** -Schnittstellen, die vom gleichen Erweiterungs Objekt unterstützt werden. Die Methoden **privategetidsofnames** und **privateinvoke** müssen bestimmen, welche func1 immer aufgerufen werden soll.

Das gleiche gilt für widersprüchliche DispIds in unterschiedlichen Dual-oder [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstellen.

Beispielsweise ist die DispID von IMyInterface1:: Y in der Datei IMyInterface1. ODL oder IMyInterface1. idl 2. Die DispID von IMyInterface2:: X ist in IMyInterface2. ODL ebenfalls 2. [**Iadsextension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) muss in der Erweiterung selbst eine eindeutige "DISPID" zurückgeben, anstatt die gleiche "DISPID" für beide zurückzugeben.

ADSI löst das erste Problem, indem mehrere Schnittstellen mit widersprüchlichen Funktions-oder Eigenschaftsnamen nicht unterstützt werden. Das zweite Problem wird durch das Hinzufügen eines eindeutigen, das innerhalb desselben Erweiterungs Objekts liegt, zu den nicht verwendeten Bits der DISPID aufgelöst.

 

 