---
description: Ein Array ist eine indizierte Liste mit Datenwerten desselben Datentyps, auf die Sie verweisen können. Zusätzlich zu Zeichen folgen-und numerischen Arrays unterstützt MOF auch Arrays von eingebetteten Objekten und verweisen.
ms.assetid: f63c222f-499d-4776-8901-65cb8b142d2b
ms.tgt_platform: multiple
title: MOF-Arrays
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0443f2ef3b3fe8fca398e281de71b0927a4f06f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214982"
---
# <a name="mof-arrays"></a><span data-ttu-id="f547e-104">MOF-Arrays</span><span class="sxs-lookup"><span data-stu-id="f547e-104">MOF Arrays</span></span>

<span data-ttu-id="f547e-105">Ein Array ist eine indizierte Liste mit Datenwerten desselben Datentyps, auf die Sie verweisen können.</span><span class="sxs-lookup"><span data-stu-id="f547e-105">An array is an indexed list of data values that are of the same data type, which you can reference.</span></span> <span data-ttu-id="f547e-106">Zusätzlich zu Zeichen folgen-und numerischen Arrays unterstützt MOF auch Arrays von eingebetteten Objekten und verweisen.</span><span class="sxs-lookup"><span data-stu-id="f547e-106">In addition to string and numeric arrays, MOF supports arrays of embedded objects and references.</span></span>

<span data-ttu-id="f547e-107">Die folgenden Regeln definieren ein MOF-Array:</span><span class="sxs-lookup"><span data-stu-id="f547e-107">The following rules define a MOF array:</span></span>

-   <span data-ttu-id="f547e-108">Die nach dem Eigenschaften Bezeichner verwendeten Klammern geben ein Array in einer Klassendefinition an.</span><span class="sxs-lookup"><span data-stu-id="f547e-108">Brackets used after the property identifier specify an array in a class definition.</span></span>

    ``` syntax
    Class ArrayDataSample1
    {
        string strArray1[];
    };
    ```

-   <span data-ttu-id="f547e-109">Alle Arrays müssen eindimensional sein.</span><span class="sxs-lookup"><span data-stu-id="f547e-109">All arrays must be one-dimensional.</span></span>
-   <span data-ttu-id="f547e-110">Arrays können unbegrenzt sein oder eine explizite Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f547e-110">Arrays can be unbounded or have an explicit size.</span></span>

    ``` syntax
    Class MyClass
    {
        sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskArray1[]);
        sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskArray2[32]);
    };
    ```

    <span data-ttu-id="f547e-111">WMI implementiert begrenzte und ungebundene Arrays als **SAFEARRAY** -Strukturen, sodass WMI die Array Dimensionen zur Laufzeit variieren kann.</span><span class="sxs-lookup"><span data-stu-id="f547e-111">WMI implements bounded and unbounded arrays as **SAFEARRAY** structures, which allows WMI to vary array dimensions at run time.</span></span> <span data-ttu-id="f547e-112">Wenn Sie ein Array mit einer expliziten Größe deklarieren, wird die Größe von WMI als Qualifizierer gespeichert, und die Größe wird als vorgeschlagene maximale Größe behandelt.</span><span class="sxs-lookup"><span data-stu-id="f547e-112">When you declare an array with an explicit size, WMI stores the size as a qualifier, and treats the size as the suggested maximum size.</span></span> <span data-ttu-id="f547e-113">Allerdings kann WMI die Größe ggf. erweitern.</span><span class="sxs-lookup"><span data-stu-id="f547e-113">However, WMI can expand the size if necessary.</span></span> <span data-ttu-id="f547e-114">Das Ändern der expliziten Größe hat keine Auswirkung auf die eigentlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="f547e-114">Changing the explicit size has no effect on the actual data.</span></span>

-   <span data-ttu-id="f547e-115">Arrays werden initialisiert, indem Werte des entsprechenden Typs in einer durch Trennzeichen getrennten Liste angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f547e-115">Arrays are initialized by specifying values of the appropriate type in a comma-separated list.</span></span>

    ``` syntax
    Class ArrayDataSample2
    {
        [key] string s;
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
    };
    ```

-   <span data-ttu-id="f547e-116">Ein Array von verweisen wird als Array von Objekt Pfad Zeichenfolgen deklariert.</span><span class="sxs-lookup"><span data-stu-id="f547e-116">An array of references is declared as an array of object path strings.</span></span>

    <span data-ttu-id="f547e-117">Wenn Sie eine Objekt Pfad Zeichenfolge deklarieren, dürfen Sie keinen Leerraum zwischen den Elementen des Objekt Pfads platzieren.</span><span class="sxs-lookup"><span data-stu-id="f547e-117">When declaring an object path string, do not place white space between the elements of the object path.</span></span> <span data-ttu-id="f547e-118">Im folgenden Beispiel wird beschrieben, wie Sie einen Objekt Pfad Verweis deklarieren.</span><span class="sxs-lookup"><span data-stu-id="f547e-118">The following example describes how to declare an object path reference.</span></span>

    ``` syntax
    Class ClassWithRefArray
        { 
        [key] string s; 
        object ref refArray[]; 
        };

    instance of ClassWithRefArray
        {
        s = 23;
        refArray = {"Disk.Name=\"C:\"", "Disk.Name=\"E:\""};
        };
    ```

-   <span data-ttu-id="f547e-119">Sie können ein Array als Parameter für eine Methode verwenden, aber nicht als Rückgabewert für einen Eingabe-oder Eingabe-/Ausgabeparameter.</span><span class="sxs-lookup"><span data-stu-id="f547e-119">You can use an array as a parameter for a method, but not as a return value for an input or input-output parameter.</span></span>
-   <span data-ttu-id="f547e-120">Alle Elemente in einem Array werden als Werte desselben Typs erstellt.</span><span class="sxs-lookup"><span data-stu-id="f547e-120">All elements in an array are created as values of the same type.</span></span>

    <span data-ttu-id="f547e-121">Wenn die Elemente eines Arrays den **Objekttyp** haben, können Sie alle Arten von Objekten im Array platzieren.</span><span class="sxs-lookup"><span data-stu-id="f547e-121">If the elements of an array are of the **object** type, then you can place any kind of object in the array.</span></span> <span data-ttu-id="f547e-122">Wenn Sie dagegen einen bestimmten Objekttyp deklarieren, lässt WMI nur Objekte dieser Klasse oder Unterklasse im Array zu.</span><span class="sxs-lookup"><span data-stu-id="f547e-122">On the other hand, if you declare a specific type of object, then WMI allows only objects of that class or subclass in the array.</span></span> <span data-ttu-id="f547e-123">In den folgenden Beispielen werden Array Deklarationen veranschaulicht,  die den-Objekttyp verwenden.</span><span class="sxs-lookup"><span data-stu-id="f547e-123">The following examples show array declarations that includes using the **object** type.</span></span>

    ``` syntax
    Class EmbedClass
    {
        [key] sint32 PropOfClass;
    };

    Class ArrayDataClass
    {
        [key] string s;
        string strArray1[];
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
        EmbedClass objArray[];
    };

    instance of ArrayDataClass
    { 
        s = "keyStuff";
        strArray1 = { "1.2.3.4", "1.2.3.5", "1.2.3.7"};
        strArray2 = 
            {
                "SELECT * FROM RegistryKeyChangeEvent",
                "SELECT * FROM RegistryValueChangeEvent",
                "SELECT * FROM RegistryTreeChangeEvent"
            };
        dwArray  = { 1,2,3,5,6 };
        objArray = {
                       instance of EmbedClass{PropOfClass=3;},
                       instance of EmbedClass{PropOfClass=4;}
                   };
    };
    ```

 

 



