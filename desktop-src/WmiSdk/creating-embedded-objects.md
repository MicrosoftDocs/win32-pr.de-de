---
description: 'Wenn Sie eine Instanz mit eingebetteten Objekten erstellen, führen Sie die folgenden Aufgaben aus:'
ms.assetid: 2abf6197-8b95-4c04-b154-508aa85fe12f
ms.tgt_platform: multiple
title: Erstellen von eingebetteten Objekten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a76a70fa0e01068622a4f4cdbbbfb6c992b67f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351016"
---
# <a name="creating-embedded-objects"></a><span data-ttu-id="b8cf4-103">Erstellen von eingebetteten Objekten</span><span class="sxs-lookup"><span data-stu-id="b8cf4-103">Creating Embedded Objects</span></span>

<span data-ttu-id="b8cf4-104">Wenn Sie eine Instanz mit eingebetteten Objekten erstellen, führen Sie die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="b8cf4-104">When creating an instance with embedded objects, perform the following tasks:</span></span>

-   <span data-ttu-id="b8cf4-105">Sie müssen ein eingebettetes Objekt als stark typisiert oder schwach typisiert deklarieren.</span><span class="sxs-lookup"><span data-stu-id="b8cf4-105">You must declare an embedded object as strongly typed or weakly typed.</span></span>

    <span data-ttu-id="b8cf4-106">Ein stark typisiertes Objekt verweist auf ein Objekt einer bestimmten Klasse und verwendet den Klassennamen.</span><span class="sxs-lookup"><span data-stu-id="b8cf4-106">A strongly typed object points to an object of a specific class and uses the class name.</span></span> <span data-ttu-id="b8cf4-107">Ein schwach typisiertes Objekt verweist auf ein Objekt einer nicht angegebenen Klasse und verwendet das **Object** -Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="b8cf4-107">A weakly typed object points to an object of an unspecified class and uses the **object** keyword.</span></span> <span data-ttu-id="b8cf4-108">Beide Objekte werden dem **\_ unbekannten VT** -Typ zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b8cf4-108">Both objects map to the **VT\_UNKNOWN** type.</span></span>

-   <span data-ttu-id="b8cf4-109">Sie können **null** als Standardwert für eingebettete Objekte und Pfade in Initialisierungen und Deklarationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8cf4-109">You can use **NULL** for the default value of embedded objects and paths in initializations and declarations.</span></span>
-   <span data-ttu-id="b8cf4-110">Wenn Sie einen Objekt Pfad einbetten, dürfen Sie keinen Leerraum zwischen den Elementen des eingebetteten Pfades platzieren.</span><span class="sxs-lookup"><span data-stu-id="b8cf4-110">When embedding an object path, do not place white space between the elements of the embedded path.</span></span> <span data-ttu-id="b8cf4-111">Der Objekt Pfad "Class1Index = 3;" enthält z. b. kein Leerzeichen zwischen dem Eigenschaftsnamen "Class1Index" und dem zugewiesenen Wert ("3").</span><span class="sxs-lookup"><span data-stu-id="b8cf4-111">For example, the object path "Class1Index=3;" contains no space between the property name "Class1index" and the value being assigned, which is "3".</span></span>

<span data-ttu-id="b8cf4-112">Die folgende Klassen Deklaration zeigt, wie stark typisierte und schwach typisierte eingebettete Objekte deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="b8cf4-112">The following class declaration shows you how to declare strongly typed and weakly typed embedded objects.</span></span>

``` syntax
Class MyClass
{
    EmbedClass    Object1;          // Strongly typed
    object        Object2;          // Weakly typed
};
```

<span data-ttu-id="b8cf4-113">In den folgenden Beispielen wird beschrieben, wie eingebettete Objekte innerhalb einer Klassen Deklaration deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="b8cf4-113">The following examples describe how to declare embedded objects within a class declaration.</span></span>

``` syntax
Class Class1 
{ 
     [key] sint32 Class1Index;
};

Class Class2 
{
    [key] sint32 Class2Index;
    Class1 EmbedObject1 = instance of Class1{Class1Index=3;};
};

Class Class3
{
    [key] sint32 Class3Index;
    Class2 EmbedObject2 = instance of Class2 {Class2Index=4;};
};
```

<span data-ttu-id="b8cf4-114">Im folgenden Beispiel wird die Initialisierung einer Eigenschaft beschrieben, bei der es sich um ein stark typisiertes Objekt handelt, und eine andere Eigenschaft, die ein Array von schwach typisierten Objekten ist.</span><span class="sxs-lookup"><span data-stu-id="b8cf4-114">The following example describes the initialization of one property that is a strongly typed object and another property that is an array of weakly typed objects.</span></span>

``` syntax
Class EmbedClass1
{
    [key] sint32 intval;
};

Class EmbedClass2
{
    [key] string sval;
};

Class ContainerClass
{
    [key] sint32 intval;
    EmbedClass1 SingleObject;
    Object ArrayObject[];
};

Instance of ContainerClass
{
    intval = 33;
    SingleObject = instance of EmbedClass1 {intval=99;};
    ArrayObject = {instance of EmbedClass2 {sval="something";},
                   instance of EmbedClass1 {intval=100;}};
};
```

 

 



