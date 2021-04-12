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
# <a name="example-for-resolving-function-name-conflicts"></a><span data-ttu-id="57f89-105">Beispiel für das Auflösen von Funktionsnamens Konflikten</span><span class="sxs-lookup"><span data-stu-id="57f89-105">Example for Resolving Function Name Conflicts</span></span>

<span data-ttu-id="57f89-106">Beachten Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="57f89-106">Consider the following:</span></span>

-   <span data-ttu-id="57f89-107">IADs0 unterstützt Func0 nicht.</span><span class="sxs-lookup"><span data-stu-id="57f89-107">IADs0 does not support Func0.</span></span>
-   <span data-ttu-id="57f89-108">IADs1 unterstützt func1 und Func0.</span><span class="sxs-lookup"><span data-stu-id="57f89-108">IADs1 supports Func1 and Func0.</span></span>
-   <span data-ttu-id="57f89-109">IADs2 unterstützt func2 und Func0.</span><span class="sxs-lookup"><span data-stu-id="57f89-109">IADs2 supports Func2 and Func0.</span></span>

<span data-ttu-id="57f89-110">Alle drei Schnittstellen sind duale Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="57f89-110">All three interfaces are dual interfaces.</span></span>


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



<span data-ttu-id="57f89-111">Obwohl IADs1 func2 nicht unterstützt, erkennt ein ADSI-Client eine [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , die alle Dual-und Dispatch-Schnittstellen im Modell unterstützt.</span><span class="sxs-lookup"><span data-stu-id="57f89-111">Be aware that even though IADs1 does not support Func2, an ADSI client recognizes one [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that supports all the dual and dispatch interfaces in the model.</span></span> <span data-ttu-id="57f89-112">Daher kann der ADSI-Client func2 direkt mithilfe von myInf1. func2 aufzurufen, ohne aufzulösen, welche Schnittstelle func2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="57f89-112">Thus, the ADSI client can directly call Func2 using myInf1.Func2 without resolving which interface supports Func2.</span></span>


```VB
myInf1.Func2
```



<span data-ttu-id="57f89-113">Sowohl IADs1 als auch IADs2 verfügen über eine Funktion mit dem Namen Func0, IADs1:: Func0 wird jedoch direkt mithilfe des Vtable-Zugriffs aufgerufen, da für den Client beide folgenden Bedingungen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="57f89-113">Both IADs1 and IADs2 have a function called Func0, but IADs1::Func0 is invoked directly using vtable access, because both of following apply to the client:</span></span>

-   <span data-ttu-id="57f89-114">Der Client verfügt über einen Zeiger auf das Dual Interface IADs1 Object, das eine Funktion mit dem Namen "Func0" aufweist.</span><span class="sxs-lookup"><span data-stu-id="57f89-114">The client has a pointer to dual interface IADs1 object, which has a function called Func0.</span></span>
-   <span data-ttu-id="57f89-115">Visual Basic unterstützt den direkten Vtable-Zugriff, wobei angenommen wird, dass der Datentyp über die Typbibliothek verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="57f89-115">Visual Basic supports direct vtable access, assuming that type of data is available through the type library.</span></span>

<span data-ttu-id="57f89-116">Im nächsten Codebeispiel verfügt der Client über einen Dual-Interface-Zeiger auf IADs2 anstelle von IADs1.</span><span class="sxs-lookup"><span data-stu-id="57f89-116">In the next code example, the client has a dual interface pointer to IADs2 instead of IADs1.</span></span> <span data-ttu-id="57f89-117">Daher wird IADs2:: Func0 mit direktem Vtable-Zugriff aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="57f89-117">Therefore, IADs2::Func0 is invoked using direct vtable access.</span></span>


```VB
Dim myInf2 as IADs2
Set myInf2 = myInf1 ' Query for pointer to IADs2 
myInf2.Func0
```



<span data-ttu-id="57f89-118">Im nächsten Codebeispiel verfügen sowohl IADs1 als auch IADs2 über eine Funktion mit dem Namen Func0, aber hier hat der Client einen Zeiger auf eine duale Schnittstelle, IADs0, die keine Funktion mit dem Namen Func0 hat.</span><span class="sxs-lookup"><span data-stu-id="57f89-118">Again, in the next code example, both IADs1 and IADs2 have a function called Func0, but, here, the client has a pointer to a dual interface, IADs0, which does not have a function called Func0.</span></span> <span data-ttu-id="57f89-119">Daher kann kein direkter Vtable-Zugriff ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="57f89-119">Therefore, no direct vtable access can be performed.</span></span> <span data-ttu-id="57f89-120">Stattdessen werden [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) und [**Aufruf**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) aufgerufen, um Func0 aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="57f89-120">Instead, [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) are called to invoke Func0.</span></span>


```VB
Dim myInfNone as IADs0
Set myInfNone = myInf1    ' The aggregated object that 
   ' supports IADs1 and IADs2.
myInfNone.Func0
```



<span data-ttu-id="57f89-121">Beachten Sie die folgenden beiden Fälle:</span><span class="sxs-lookup"><span data-stu-id="57f89-121">Consider these two cases:</span></span>

-   <span data-ttu-id="57f89-122">IADs1 und IADs2 werden von den beiden com-Komponenten EXT1 bzw. ext2 implementiert.</span><span class="sxs-lookup"><span data-stu-id="57f89-122">IADs1 and IADs2 are implemented by two COM components, Ext1 and Ext2, respectively.</span></span> <span data-ttu-id="57f89-123">Wenn EXT1 in der Registrierung vor EXT2 steht, wird IADs1:: Func0 aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="57f89-123">If Ext1 comes before Ext2 in the registry, IADs1::Func0 is invoked.</span></span> <span data-ttu-id="57f89-124">Wenn der Wert für "ext2" in der Registrierung jedoch an erster Stelle steht, wird IADs2:: Func0 aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="57f89-124">However, if Ext2 comes first in the registry, IADs2::Func0 is invoked.</span></span>
-   <span data-ttu-id="57f89-125">Wenn IADs1 und ADs2 durch das gleiche Erweiterungs Objekt implementiert werden, wird Func0 immer von der [**iadsextension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) -und [**privateinvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) -Methode der Erweiterung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="57f89-125">If IADs1 and ADs2 are implemented by the same extension object, Func0 is always invoked by the extension's [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) and [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) methods.</span></span>

<span data-ttu-id="57f89-126">Der Erweiterungs Entwickler muss bestimmen, wie Konflikte von Funktionen oder Eigenschaften von unterschiedlichen Dual- [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstellen, die in einer Erweiterung denselben Namen haben, gelöst werden können.</span><span class="sxs-lookup"><span data-stu-id="57f89-126">The extension developer must determine how to resolve conflicts of functions, or properties, of different dual [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces that have the same name in an extension.</span></span> <span data-ttu-id="57f89-127">Die Implementierung von [**iadsextension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) -und [**privateinvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) -Methoden sollten diesen Konflikt lösen.</span><span class="sxs-lookup"><span data-stu-id="57f89-127">The implementation of [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) and [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) methods should resolve this conflict.</span></span> <span data-ttu-id="57f89-128">Wenn Sie z. b. IMyInterface1:: func1 und IMyInterface2:: func1 verwenden, sind IMyInterface1 und IMyInterface2 duale **IDispatch** -Schnittstellen, die vom gleichen Erweiterungs Objekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="57f89-128">For example, if you use IMyInterface1::Func1 and IMyInterface2::Func1, where IMyInterface1 and IMyInterface2 are dual **IDispatch** interfaces supported by the same extension object.</span></span> <span data-ttu-id="57f89-129">Die Methoden **privategetidsofnames** und **privateinvoke** müssen bestimmen, welche func1 immer aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="57f89-129">The **PrivateGetIDsOfNames** and **PrivateInvoke** methods must determine which Func1 should always be called.</span></span>

<span data-ttu-id="57f89-130">Das gleiche gilt für widersprüchliche DispIds in unterschiedlichen Dual-oder [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="57f89-130">The same applies to conflicting DISPIDs in different dual or [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces.</span></span>

<span data-ttu-id="57f89-131">Beispielsweise ist die DispID von IMyInterface1:: Y in der Datei IMyInterface1. ODL oder IMyInterface1. idl 2.</span><span class="sxs-lookup"><span data-stu-id="57f89-131">For example, the DISPID of IMyInterface1::Y is 2 in the file imyinterface1.odl, or imyinterface1.idl.</span></span> <span data-ttu-id="57f89-132">Die DispID von IMyInterface2:: X ist in IMyInterface2. ODL ebenfalls 2.</span><span class="sxs-lookup"><span data-stu-id="57f89-132">The DISPID of IMyInterface2::X is also 2 in iMyInterface2.odl.</span></span> <span data-ttu-id="57f89-133">[**Iadsextension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) muss in der Erweiterung selbst eine eindeutige "DISPID" zurückgeben, anstatt die gleiche "DISPID" für beide zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="57f89-133">[**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) must return a unique DISPID, within the extension itself, for each, instead of returning the same DISPID for both.</span></span>

<span data-ttu-id="57f89-134">ADSI löst das erste Problem, indem mehrere Schnittstellen mit widersprüchlichen Funktions-oder Eigenschaftsnamen nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="57f89-134">ADSI resolves the first problem by not supporting multiple interfaces with conflicting function or property names.</span></span> <span data-ttu-id="57f89-135">Das zweite Problem wird durch das Hinzufügen eines eindeutigen, das innerhalb desselben Erweiterungs Objekts liegt, zu den nicht verwendeten Bits der DISPID aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="57f89-135">It resolves the second problem by adding a unique, that is within the same extension object, interface number to the unused bits of the DISPID.</span></span>

 

 