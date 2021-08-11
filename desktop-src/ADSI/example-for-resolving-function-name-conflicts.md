---
title: Beispiel für das Auflösen von Funktionsnamenskonflikten
description: In diesem Thema wird beschrieben, wie Funktionsnamenkonflikte beim Erstellen einer Erweiterung für ADSI gelöst werden.
ms.assetid: 8121f037-3845-44ba-a2cd-8d7f15e0beb2
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, Beispielcode Visual Basic , Auflösen von Funktionsnamenskonflikten
- Auflösen von Funktionsnamenskonflikten bei ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e6ce09251ba61b31768d973e258c568694067aff0420f0512a13913bb6fce90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179980"
---
# <a name="example-for-resolving-function-name-conflicts"></a>Beispiel für das Auflösen von Funktionsnamenskonflikten

Beachten Sie Folgendes:

-   IADs0 unterstützt Func0 nicht.
-   IADs1 unterstützt Func1 und Func0.
-   IADs2 unterstützt Func2 und Func0.

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



Beachten Sie, dass ein ADSI-Client einen [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) erkennt, der alle Dual- und Dispatchschnittstellen im Modell unterstützt, obwohl IADs1 Func2 nicht unterstützt. Daher kann der ADSI-Client Func2 mithilfe von myInf1.Func2 direkt aufrufen, ohne aufzulösen, welche Schnittstelle Func2 unterstützt.


```VB
myInf1.Func2
```



Sowohl IADs1 als auch IADs2 verfügen über eine Funktion namens Func0, aber IADs1::Func0 wird direkt mithilfe des vtable-Zugriffs aufgerufen, da beide der folgenden Funktionen für den Client gelten:

-   Der Client verfügt über einen Zeiger auf das IADs1-Objekt mit dualer Schnittstelle, das über eine Funktion namens Func0 verfügt.
-   Visual Basic unterstützt direkten vtable-Zugriff, vorausgesetzt, dass der Datentyp über die Typbibliothek verfügbar ist.

Im nächsten Codebeispiel verfügt der Client über einen Dual Interface-Zeiger auf IADs2 anstelle von IADs1. Daher wird IADs2::Func0 mithilfe des direkten vtable-Zugriffs aufgerufen.


```VB
Dim myInf2 as IADs2
Set myInf2 = myInf1 ' Query for pointer to IADs2 
myInf2.Func0
```



Auch im nächsten Codebeispiel verfügen sowohl IADs1 als auch IADs2 über eine Funktion namens Func0, aber hier hat der Client einen Zeiger auf eine duale Schnittstelle, IADs0, die keine Funktion namens Func0 hat. Daher kann kein direkter vtable-Zugriff ausgeführt werden. Stattdessen werden [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) und [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) aufgerufen, um Func0 aufzurufen.


```VB
Dim myInfNone as IADs0
Set myInfNone = myInf1    ' The aggregated object that 
   ' supports IADs1 and IADs2.
myInfNone.Func0
```



Betrachten Sie diese beiden Fälle:

-   IADs1 und IADs2 werden von zwei COM-Komponenten implementiert: Ext1 bzw. Ext2. Wenn Ext1 in der Registrierung vor Ext2 steht, wird IADs1::Func0 aufgerufen. Wenn Ext2 jedoch an erster Stelle in der Registrierung steht, wird IADs2::Func0 aufgerufen.
-   Wenn IADs1 und ADs2 vom gleichen Erweiterungsobjekt implementiert werden, wird Func0 immer von den [**IADsExtension::P rivateGetIDsOfNames-**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) und [**PrivateInvoke-Methoden**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) der Erweiterung aufgerufen.

Der Erweiterungsentwickler muss bestimmen, wie Konflikte von Funktionen oder Eigenschaften verschiedener dualer [**IDispatch-Schnittstellen**](/windows/win32/api/oaidl/nn-oaidl-idispatch) gelöst werden, die in einer Erweiterung den gleichen Namen aufweisen. Die Implementierung der [**Methoden IADsExtension::P rivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) und [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) sollte diesen Konflikt lösen. Wenn Sie beispielsweise IMyInterface1::Func1 und IMyInterface2::Func1 verwenden, wobei IMyInterface1 und IMyInterface2 duale **IDispatch-Schnittstellen** sind, die vom gleichen Erweiterungsobjekt unterstützt werden. Die **Methoden PrivateGetIDsOfNames** und **PrivateInvoke** müssen bestimmen, welche Func1 immer aufgerufen werden soll.

Dasselbe gilt für in Konflikt geratene DISPIDs in verschiedenen Dual- oder [**IDispatch-Schnittstellen.**](/windows/win32/api/oaidl/nn-oaidl-idispatch)

Beispielsweise ist die DISPID von IMyInterface1::Y in der Datei imyinterface1.odl oder imyinterface1.idl 2. Die DISPID von IMyInterface2::X ist auch 2 in iMyInterface2.odl. [**IADsExtension::P rivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) muss eine eindeutige DISPID innerhalb der Erweiterung selbst zurückgeben, anstatt für beide dieselbe DISPID zurückzugeben.

ADSI löst das erste Problem, indem nicht mehrere Schnittstellen mit in Konfliktstehenden Funktions- oder Eigenschaftsnamen unterstützt werden. Das zweite Problem wird behoben, indem den nicht verwendeten Bits der DISPID eine eindeutige Schnittstellennummer hinzugefügt wird, die sich innerhalb desselben Erweiterungsobjekts befindet.

 

 