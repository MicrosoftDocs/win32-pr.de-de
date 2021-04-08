---
description: Das MOF-ref-Schlüsselwort beschreibt einen Objekt Pfad und ist einem VT \_ BSTR-Automatisierungstyp zugeordnet.
ms.assetid: 9da25435-4ccc-4251-a4be-37239156e320
ms.tgt_platform: multiple
title: Verweise (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30722910de761f3d2111a3218cf364f49ccb3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866587"
---
# <a name="references-wmi"></a><span data-ttu-id="23ac2-103">Verweise (WMI)</span><span class="sxs-lookup"><span data-stu-id="23ac2-103">References (WMI)</span></span>

<span data-ttu-id="23ac2-104">Das MOF- **ref** -Schlüsselwort beschreibt einen Objekt Pfad und ist einem VT \_ BSTR-Automatisierungstyp zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="23ac2-104">The MOF **ref** key word describes an object path and maps to a VT\_BSTR Automation type.</span></span> <span data-ttu-id="23ac2-105">Der Objekt Pfad kann entweder ein vollständiger Pfad zu einem Server und Namespace oder ein relativer Pfad zu einem anderen Objekt im gleichen Namespace sein.</span><span class="sxs-lookup"><span data-stu-id="23ac2-105">The object path can be either a full path to a server and namespace, or a relative path to another object in the same namespace.</span></span> <span data-ttu-id="23ac2-106">Sie können ein **ref** -Schlüsselwort verwenden, um zwei oder mehr Klassen zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="23ac2-106">You can use a **ref** key word to link two or more classes together.</span></span> <span data-ttu-id="23ac2-107">WMI unterstützt zwei Typen von Objekt Pfaden, die verwenden, um allgemeine oder bestimmte Pfade innerhalb von WMI zu definieren.</span><span class="sxs-lookup"><span data-stu-id="23ac2-107">WMI supports two types of object paths, which use to define general or specific paths within WMI.</span></span>

<span data-ttu-id="23ac2-108">Der Hauptzweck des **ref** -Schlüssel Worts besteht darin, die Transportzeit und die Codierung zwischen Objekten zu reduzieren, die vollständig im WMI-Repository vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="23ac2-108">The main purpose of the **ref** key word is to reduce transport time and encoding between objects that exist entirely within the WMI repository.</span></span> <span data-ttu-id="23ac2-109">Sie können auch das **ref** -Schlüsselwort verwenden, um eine Zuordnung zwischen zwei Klassen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="23ac2-109">You can also use the **ref** key word to create an association between two classes.</span></span> <span data-ttu-id="23ac2-110">Weitere Informationen finden Sie unter [Deklarieren einer Association-Klasse](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="23ac2-110">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span> <span data-ttu-id="23ac2-111">Wenn sich das Element, auf das verwiesen wird, innerhalb derselben MOF-Datei befindet, verwenden Sie einen Alias, um den **ref** -Wert zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="23ac2-111">If the referenced item is located within the same MOF file, use an alias to initialize the **ref** value.</span></span> <span data-ttu-id="23ac2-112">Weitere Informationen finden Sie unter [Erstellen eines Alias](creating-an-alias.md).</span><span class="sxs-lookup"><span data-stu-id="23ac2-112">For more information, see [Creating an Alias](creating-an-alias.md).</span></span>

> [!Note]  
> <span data-ttu-id="23ac2-113">Wenn ein **ref** -Schlüsselwort auf eine Schlüsseleigenschaft angewendet wird, können Sie Objekt Verweise durch den Objekt Zeichen folgen Wert anstelle des dereferenzierten Werts unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="23ac2-113">When a **ref** key word is applied to a key property, you can distinguish object references by the object string value instead of by the dereferenced value.</span></span>

 

<span data-ttu-id="23ac2-114">MOF unterstützt das Konzept eines schwach typisierten und stark typisierten Objekt Pfads.</span><span class="sxs-lookup"><span data-stu-id="23ac2-114">MOF supports the concept of a weakly typed and strongly typed object path.</span></span> <span data-ttu-id="23ac2-115">Ein schwach typisierter Objekt Pfad zeigt auf ein Objekt einer nicht angegebenen Klasse und verwendet das **ref** -Schlüsselwort mit dem [Object](object.md) -Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="23ac2-115">A weakly typed object path points to an object of an unspecified class and uses the **ref** key word with the [OBJECT](object.md) keyword.</span></span> <span data-ttu-id="23ac2-116">Ein stark typisiertes Objekt verweist auf ein Objekt einer bestimmten Klasse und verwendet **ref** mit dem Klassennamen.</span><span class="sxs-lookup"><span data-stu-id="23ac2-116">A strongly typed object points to an object of a specific class and uses **ref** with the class name.</span></span> <span data-ttu-id="23ac2-117">Das folgende Beispiel beschreibt einen schwach typisierten **reftoanyclass** -Verweis, der auf eine beliebige Klassen-oder Klasseninstanz verweisen kann, sowie einen **reftoclassx** -Verweis, der nur auf eine **ClassX** -Klasse oder-Instanz verweisen kann:</span><span class="sxs-lookup"><span data-stu-id="23ac2-117">The following example describes a weakly typed **RefToAnyClass** reference that can point to any class or class instance, and a **RefToClassX** reference that can point only to a **ClassX** class or instance:</span></span>

``` syntax
class MyClass
{
    object ref RefToAnyClass;       // Weakly typed
    ClassX ref RefToClassX;         // Strongly typed
};
```

<span data-ttu-id="23ac2-118">Im folgenden Beispiel werden zwei-Instanzen und ein Association-Objekt beschrieben, das auf die vorherigen-Instanzen verweist:</span><span class="sxs-lookup"><span data-stu-id="23ac2-118">The following example describes two instances and an association object that references the previous instances:</span></span>

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

Class A{
    [key] string aKey;
};

Class C{
    [key] string cKey;
};

// The following class creates an association 
// between the "A" class and the "C" class
    [Association] Class B{
    [key] A ref aRef;
    [Key, Min(1)] C ref cRef;
};

instance of a
{
    aKey = "This is the key for the A class";
};

instance of c
{
    cKey = "This is the key for the c class";
};
```

 

 



