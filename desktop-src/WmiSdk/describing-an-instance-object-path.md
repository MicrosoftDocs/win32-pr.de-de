---
description: Ein instanzobjektpfad beschreibt den Speicherort einer Instanz einer bestimmten Klasse in einem bestimmten Namespace.
ms.assetid: 78a194f0-cd21-4622-9242-be7e430b96c0
ms.tgt_platform: multiple
title: Beschreiben eines instanzobjektpfads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f977359ea9c3c4346052f1edd076c0cce5544441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347048"
---
# <a name="describing-an-instance-object-path"></a><span data-ttu-id="f919d-103">Beschreiben eines instanzobjektpfads</span><span class="sxs-lookup"><span data-stu-id="f919d-103">Describing an Instance Object Path</span></span>

<span data-ttu-id="f919d-104">Ein instanzobjektpfad beschreibt den Speicherort einer Instanz einer bestimmten Klasse in einem bestimmten Namespace.</span><span class="sxs-lookup"><span data-stu-id="f919d-104">An instance object path describes the location of an instance of a given class within a specific namespace.</span></span>

<span data-ttu-id="f919d-105">Sie können verschiedene Arten von instanzobjektpfaden haben:</span><span class="sxs-lookup"><span data-stu-id="f919d-105">You can have several different kinds of instance object paths:</span></span>

-   <span data-ttu-id="f919d-106">Vollständig</span><span class="sxs-lookup"><span data-stu-id="f919d-106">Full</span></span>

    <span data-ttu-id="f919d-107">Ein vollständiger instanzobjektpfad fügt den Namen und den Wert der Schlüsseleigenschaft für die Klasse an einen vollständigen Klassenobjekt Pfad an.</span><span class="sxs-lookup"><span data-stu-id="f919d-107">A full instance object path appends the name and value of the key property for the class to a full class object path.</span></span>

    <span data-ttu-id="f919d-108">Das folgende Beispiel zeigt die Definition des vollständigen instanzobjektpfads.</span><span class="sxs-lookup"><span data-stu-id="f919d-108">The following example shows the definition of the full instance object path.</span></span>

    ``` syntax
    \\Server\Namespace:Class.KeyName="KeyValue"
    ```

-   <span data-ttu-id="f919d-109">Relativ</span><span class="sxs-lookup"><span data-stu-id="f919d-109">Relative</span></span>

    <span data-ttu-id="f919d-110">Ein relativer Objekt Pfad verweist auf eine Instanz, die sich im aktuellen Namespace auf dem aktuellen Server befindet.</span><span class="sxs-lookup"><span data-stu-id="f919d-110">A relative object path refers to an instance located in the current namespace on the current server.</span></span> <span data-ttu-id="f919d-111">Der relative Pfad besteht aus dem Klassennamen, gefolgt von den Namen und Werten der Schlüsseleigenschaften dieser Instanz.</span><span class="sxs-lookup"><span data-stu-id="f919d-111">The relative path consists of the class name followed by the names and values of the key properties of this instance.</span></span>

    <span data-ttu-id="f919d-112">Das folgende Beispiel zeigt die Definition des relativen instanzobjektpfads.</span><span class="sxs-lookup"><span data-stu-id="f919d-112">The following example shows the definition of the relative instance object path.</span></span>

    ``` syntax
    MyClass.MyProp="e:"
    ```

-   <span data-ttu-id="f919d-113">Relativ zu einem einzelnen Schlüssel</span><span class="sxs-lookup"><span data-stu-id="f919d-113">Relative with a single key</span></span>

    <span data-ttu-id="f919d-114">Für Klassen, die nur eine Eigenschaft als Schlüssel festgelegt haben, können Sie den Namen der Schlüsseleigenschaft weglassen.</span><span class="sxs-lookup"><span data-stu-id="f919d-114">For classes with only one property designated as the key, you can omit the name of the key property.</span></span>

    <span data-ttu-id="f919d-115">Das folgende Beispiel zeigt die Definition des relativen instanzobjektpfads mit einem einzelnen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="f919d-115">The following example shows the definition of the relative instance object path with a single key.</span></span>

    ``` syntax
    MyClass="e:"
    ```

-   <span data-ttu-id="f919d-116">Relativ zu mehreren Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="f919d-116">Relative with multiple keys</span></span>

    <span data-ttu-id="f919d-117">Verwenden Sie ein Komma, um zwischen den Schlüsseln einer Instanz mit mehreren Schlüsseln zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="f919d-117">Use a comma to distinguish between the keys of an instance with multiple keys.</span></span>

    <span data-ttu-id="f919d-118">Das folgende Beispiel zeigt die Definitionen des relativen instanzobjektpfades mit mehreren Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="f919d-118">The following example shows the definitions of the relative instance object path with multiple keys.</span></span>

    ``` syntax
    MyOtherClass.FirstKey=1,SecondKey=2
    ```

-   <span data-ttu-id="f919d-119">Relativ für eine Singleton-Klasse</span><span class="sxs-lookup"><span data-stu-id="f919d-119">Relative for a singleton class</span></span>

    <span data-ttu-id="f919d-120">Der relative Objekt Pfad für eine Singleton-Klasse besteht aus dem Klassennamen, gefolgt von der Notation "= @".</span><span class="sxs-lookup"><span data-stu-id="f919d-120">The relative object path for a singleton class consists of the class name followed by the "=@" notation.</span></span>

    <span data-ttu-id="f919d-121">Das folgende Beispiel zeigt die Definition des relativen instanzobjektpfads für eine Singleton-Klasse.</span><span class="sxs-lookup"><span data-stu-id="f919d-121">The following example shows the definition of the relative instance object path for a singleton class.</span></span>

    ``` syntax
    MySingletonClass=@
    ```

<span data-ttu-id="f919d-122">Im folgenden Verfahren wird beschrieben, wie eine Klasseninstanz abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f919d-122">The following procedure describes how to retrieve a class instance.</span></span>

<span data-ttu-id="f919d-123">**So rufen Sie eine Klasseninstanz ab**</span><span class="sxs-lookup"><span data-stu-id="f919d-123">**To retrieve a class instance**</span></span>

1.  <span data-ttu-id="f919d-124">Initialisieren Sie eine Zeichenfolge, die den Objekt Pfad mit einem Rückruf der [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) -Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="f919d-124">Initialize a string that contains the object path with a call to the [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) function.</span></span>
2.  <span data-ttu-id="f919d-125">Initialisieren Sie ein Objekt, das die-Instanz empfängt.</span><span class="sxs-lookup"><span data-stu-id="f919d-125">Initialize an object that will receive the instance.</span></span>
3.  <span data-ttu-id="f919d-126">Rufen Sie das-Objekt mit einem Befehl von [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)ab.</span><span class="sxs-lookup"><span data-stu-id="f919d-126">Retrieve the object with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

    <span data-ttu-id="f919d-127">Um [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)zu verwenden, müssen Sie die [**iwbemsink**](swbemsink.md) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="f919d-127">To use [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), you must implement the [**IWbemSink**](swbemsink.md) interface.</span></span>

<span data-ttu-id="f919d-128">Die folgende \# include-Anweisung ist erforderlich, damit der Code, der weiter unten in diesem Thema aufgelistet ist, ordnungsgemäß kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="f919d-128">The following \#include statement is required for the code that is listed later in this topic to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="f919d-129">Im folgenden Codebeispiel wird beschrieben, wie eine-Klasseninstanz mit einem Objekt Pfad abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f919d-129">The following code example describes how to retrieve a class instance using an object path.</span></span>


```C++
IWbemServices* pWbemSvcs = 0;

BSTR Path = SysAllocString(L"ComPort=2");    
IWbemClassObject *pComPort = 0;
pWbemSvcs->GetObject(Path, 0, 0, &pComPort, 0);
```



<span data-ttu-id="f919d-130">Für Instanzen von Klassen, die mehrere Eigenschaften als Schlüssel angeben, erfordert WMI keine bestimmte Reihenfolge von Schlüsseleigenschaften in Objekt Pfaden.</span><span class="sxs-lookup"><span data-stu-id="f919d-130">For instances of classes that specify multiple properties as the key, WMI requires no specific ordering of key properties in object paths.</span></span> <span data-ttu-id="f919d-131">Sie müssen nur den Wert der einzelnen Eigenschaften im Objekt Pfad angeben.</span><span class="sxs-lookup"><span data-stu-id="f919d-131">You need only specify the value of each of the properties in the object path.</span></span>

<span data-ttu-id="f919d-132">Im folgenden Codebeispiel werden zwei äquivalente Schlüssel Beschreibungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f919d-132">The following code example describes two equivalent key descriptions.</span></span>

``` syntax
MyClass.IntVal=33,StrVal="AAA"
MyClass.StrVal="AAA",IntVal=33
```

 

 
