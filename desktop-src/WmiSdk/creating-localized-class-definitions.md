---
description: Das Erstellen lokalisierter Klassendefinitionen ist ein dreistufiger Prozess.
ms.assetid: e303b894-07c4-44e3-9c57-58b1db16ae9a
ms.tgt_platform: multiple
title: Erstellen von lokalisierten Klassendefinitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41a183c1478c259b0428cd827088a769e680425
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106351854"
---
# <a name="creating-localized-class-definitions"></a><span data-ttu-id="c9a81-103">Erstellen von lokalisierten Klassendefinitionen</span><span class="sxs-lookup"><span data-stu-id="c9a81-103">Creating Localized Class Definitions</span></span>

<span data-ttu-id="c9a81-104">Das Erstellen lokalisierter Klassendefinitionen ist ein dreistufiger Prozess.</span><span class="sxs-lookup"><span data-stu-id="c9a81-104">Creating localized class definitions is a three-step process.</span></span> <span data-ttu-id="c9a81-105">Sie beginnen mit dem Schreiben von MOF-Code, der die Klassen definiert, einschließlich aller Qualifizierer, die lokalisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c9a81-105">You start by writing MOF code that defines the classes, including all qualifiers that must be localized.</span></span> <span data-ttu-id="c9a81-106">Diese ursprüngliche Datei wird als "Master MOF"-Datei bezeichnet, da Sie alle Qualifizierer und Eigenschaften enthält, die die Klasse definieren.</span><span class="sxs-lookup"><span data-stu-id="c9a81-106">This original file is called the "master MOF" file because it contains all of the qualifiers and properties that define the class.</span></span>

<span data-ttu-id="c9a81-107">Verwenden Sie als nächstes den [MOF-Compiler](mofcomp.md) , um die sprach neutralen und sprachspezifischen Versionen der MOF-Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c9a81-107">Next, use the [MOF compiler](mofcomp.md) to create the language-neutral and language-specific versions of the MOF file.</span></span> <span data-ttu-id="c9a81-108">Der MOF-Compiler platziert die grundlegende Klassen Beschreibung in einer neuen MOF-Datei und erstellt eine lokalisierte Version der MOF-Datei, die nur die Eigenschaften und Qualifizierer enthält, die lokalisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c9a81-108">The MOF compiler places the basic class description in a new MOF file and creates a localized version of the MOF file that contains only the properties and qualifiers that must be localized.</span></span> <span data-ttu-id="c9a81-109">Obwohl die sprachspezifischen und sprach neutralen Versionen der MOF-Datei den gleichen Dateinamen haben können, sollten Sie eine MFL-Dateinamenerweiterung verwenden, um anzugeben, dass die Datei lokalisierte Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="c9a81-109">Although the language-specific and language-neutral versions of the MOF file can have the same file name, you should use a .mfl file name extension to indicate that the file contains localized information.</span></span> <span data-ttu-id="c9a81-110">Sie können die MFL-Datei ggf. mit anderen Gebiets Schemata lokalisieren.</span><span class="sxs-lookup"><span data-stu-id="c9a81-110">You can localize the .mfl file to other locales, if necessary.</span></span> <span data-ttu-id="c9a81-111">Zum Speichern der Klassendefinitionen im CIM-Repository ist ein zusätzlicher Schritt erforderlich, um den MOF-Compiler zum Kompilieren der sprach neutralen und sprachspezifischen MOF-Dateien zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9a81-111">Storing the class definitions in the CIM repository requires an additional step of using the MOF compiler to compile both the language-neutral and the language-specific MOF files.</span></span>

<span data-ttu-id="c9a81-112">In den folgenden Schritten wird beschrieben, wie eine lokalisierte Klassendefinition erstellt und gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="c9a81-112">The following steps describe how to create and store a localized class definition.</span></span>

<span data-ttu-id="c9a81-113">**So erstellen und speichern Sie eine lokalisierte Klassendefinition**</span><span class="sxs-lookup"><span data-stu-id="c9a81-113">**To create and store a localized class definition**</span></span>

1.  <span data-ttu-id="c9a81-114">Erstellen Sie die MOF-Master Datei, mit der die Klassen definiert werden, die lokalisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c9a81-114">Create the master MOF file that defines the classes that you want localized.</span></span>

    <span data-ttu-id="c9a81-115">Speichern Sie diesen MOF-Code in einer Datei namens mastermof. mof.</span><span class="sxs-lookup"><span data-stu-id="c9a81-115">Save this MOF code in a file called Mastermof.mof.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root")

    instance of __Namespace
    {
        Name = "TEST" ;
    } ;

    #pragma namespace("\\\\.\\root\\TEST")

    [Description("Localized version of MyClass for American English") 
        : Amended, LOCALE(0x409)] 

    class myclass
    {
        [DisplayName("User Name") : Amended,
        Description("The Name property contains the name of the user") : 
        Amended, key]
         string Name;

        uint64 Value; // non-localized value field

          [DisplayName("Time Stamp") : Amended,
        Description("This property shows when the object was created") : 
        Amended] 
         uint64 Timestamp;
    };
    ```

2.  <span data-ttu-id="c9a81-116">Erstellen Sie sprachneutrale und sprachspezifische Versionen der MOF-Datei, indem Sie die mastermof. MOF-Datei kompilieren.</span><span class="sxs-lookup"><span data-stu-id="c9a81-116">Create language-neutral and language-specific versions of the MOF file by compiling the MasterMOF.mof file.</span></span>

    <span data-ttu-id="c9a81-117">Geben Sie den folgenden Befehl an einer Eingabeaufforderung ein, um die Datei mastermof. MOF zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="c9a81-117">Type the following command at a command prompt to compile the MasterMOF.mof file.</span></span>

    <span data-ttu-id="c9a81-118">**"MOF": "MOF-MFL: lsmof. MFL-Zusatz: ms \_ 409 mastermof. mof"**</span><span class="sxs-lookup"><span data-stu-id="c9a81-118">**mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS\_409 Mastermof.mof**</span></span>

3.  <span data-ttu-id="c9a81-119">Kompilieren Sie die sprach neutralen (lnmof. MOF) und sprachspezifischen Dateien (lsmof. MFL), und speichern Sie die Klassen Informationen im CIM-Repository.</span><span class="sxs-lookup"><span data-stu-id="c9a81-119">Compile the language-neutral (Lnmof.mof) and language-specific (Lsmof.mfl) files and store the class information in the CIM repository.</span></span>

    <span data-ttu-id="c9a81-120">Geben Sie die folgenden Befehle an einer Eingabeaufforderung ein, um die Klassen Informationen im CIM-Repository zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c9a81-120">Type the following commands at a command prompt to store the class information in the CIM repository.</span></span>

    <span data-ttu-id="c9a81-121">**"Mamacomp lnmof. mof"**</span><span class="sxs-lookup"><span data-stu-id="c9a81-121">**Mofcomp Lnmof.mof**</span></span>

    <span data-ttu-id="c9a81-122">**"Mumacomp lsmof. MFL"**</span><span class="sxs-lookup"><span data-stu-id="c9a81-122">**Mofcomp Lsmof.mfl**</span></span>

    <span data-ttu-id="c9a81-123">Nachdem Sie diese Dateien kompiliert haben, verfügen Sie über eine sprachneutrale Klassendefinition im Stamm \\ Test Namespace und eine lokalisierte Klassendefinition im Stamm \\ Test \\ MS 409- \_ Namespace.</span><span class="sxs-lookup"><span data-stu-id="c9a81-123">After you compile these files, you will have a language-neutral class definition in the root\\test namespace and a localized class definition in the root\\test\\ms\_409 namespace.</span></span> <span data-ttu-id="c9a81-124">Weitere Informationen zum Kompilieren lokalisierter MOF-Dateien finden Sie unter [Kompilieren lokalisierter MOF-Dateien](compiling-localized-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="c9a81-124">For more information about compiling localized MOF files, see [Compiling Localized MOF files](compiling-localized-mof-files.md).</span></span>

 

 



