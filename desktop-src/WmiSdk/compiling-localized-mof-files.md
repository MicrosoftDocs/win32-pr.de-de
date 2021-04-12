---
description: Sie müssen ihre Master-MOF-Datei kompilieren, um die sprach neutralen und sprachspezifischen MOF-Dateien zu erstellen.
ms.assetid: ae2fa320-8294-4991-be30-403088c34b7a
ms.tgt_platform: multiple
title: Kompilieren lokalisierter MOF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ab1341a37269ba98fdbbdecaa64b5e5a119703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346768"
---
# <a name="compiling-localized-mof-files"></a><span data-ttu-id="34c4a-103">Kompilieren lokalisierter MOF-Dateien</span><span class="sxs-lookup"><span data-stu-id="34c4a-103">Compiling Localized MOF Files</span></span>

<span data-ttu-id="34c4a-104">Sie müssen ihre Master-MOF-Datei kompilieren, um die sprach neutralen und sprachspezifischen MOF-Dateien zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="34c4a-104">You must compile your master MOF file to create the language-neutral and language-specific MOF files.</span></span>

<span data-ttu-id="34c4a-105">Geben Sie den folgenden Befehl an einer Eingabeaufforderung ein, um eine Master-MOF-Datei zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="34c4a-105">Type the following command at a command prompt to compile a master MOF file.</span></span>

<span data-ttu-id="34c4a-106">**"MOF": "MOF-MFL: lsmof. MFL-Zusatz: ms \_ 409 mastermof. mof"**</span><span class="sxs-lookup"><span data-stu-id="34c4a-106">**mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS\_409 Mastermof.mof**</span></span>

<span data-ttu-id="34c4a-107">Wenn Sie diesen Befehl ausführen, erstellt der MOF-Compiler zwei MOF-Dateien aus der ursprünglichen Datei "mastermof. mof".</span><span class="sxs-lookup"><span data-stu-id="34c4a-107">When you run this command, the MOF compiler creates two MOF files from the original Mastermof.mof file.</span></span> <span data-ttu-id="34c4a-108">Der MOF-Compiler erzeugt eine sprachneutrale Version (lnmof. MOF), in der alle sprachspezifischen Elemente entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="34c4a-108">The MOF compiler produces a language-neutral version, Lnmof.mof, in which all language-specific items are removed.</span></span> <span data-ttu-id="34c4a-109">Außerdem wird eine zweite sprachspezifische Version (lsmof. MOF) erstellt. Diese Datei enthält nur Elemente, die mit der [**geänderten**](qualifier-flavors.md) qualifiziererkonfiguration in der Datei mastermof. MOF gekennzeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="34c4a-109">A second, language-specific version, Lsmof.mof, is also created; this file contains only items that were marked with the [**Amended**](qualifier-flavors.md) Qualifier Flavor in the Mastermof.mof file.</span></span>

<span data-ttu-id="34c4a-110">Im folgenden Codebeispiel wird der Inhalt der-sprach neutralen MOF-Datei (lnmof. MOF) gezeigt, die generiert wird.</span><span class="sxs-lookup"><span data-stu-id="34c4a-110">The following code example shows the contents of the language-neutral MOF file (Lnmof.mof) that is generated.</span></span>

``` syntax
#pragma namespace("\\\\.\\root")

Instance of __Namespace
{
  Name = "TEST";
};
#pragma namespace("\\\\.\\root\\TEST")

[LOCALE(1033)] 
class myclass
{
  [key] string Name;
  uint64 Value;
  uint64 Timestamp;
};
```

<span data-ttu-id="34c4a-111">Das folgende Codebeispiel zeigt den Inhalt der sprachspezifischen MOF-Datei (lsmof. MFL), die generiert wird.</span><span class="sxs-lookup"><span data-stu-id="34c4a-111">The following code example shows the contents of the language-specific MOF file (Lsmof.mfl) that is generated.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\TEST")
instance of __namespace{ name="ms_409";};
#pragma namespace("\\\\.\\root\\TEST\\ms_409")

[Description("Localized version of MyClass for American English") :
    Amended, LOCALE(0x409)] 

class myclass
{
    [DisplayName("User Name") : Amended,
    Description("The Name property contains the name of the user") : 
    Amended, key]
     string Name;

    [DisplayName("Time Stamp") : Amended,
    Description("This property shows when the object was created") : 
    Amended] 
     uint64 Timestamp;
};
```

<span data-ttu-id="34c4a-112">Beim Kompilieren einer MOF-Datei mit dem [**geänderten**](qualifier-flavors.md) Qualifizierer werden nur separate sprachneutrale und sprachspezifische MOF-Dateien generiert. das CIM-Repository wird nicht mit den neuen Klassen Informationen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="34c4a-112">Compiling a MOF file with the [**Amended**](qualifier-flavors.md) qualifier only generates separate language-neutral and language-specific MOF files; the CIM repository is not updated with the new class information.</span></span> <span data-ttu-id="34c4a-113">Sie müssen den MOF-Compiler verwenden, um die beiden MOF-Dateien zu kompilieren, die von der ersten Kompilierung erstellt wurden, bevor Klassen Informationen für WMI verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="34c4a-113">You must use the MOF compiler to compile the two MOF files that the first compilation produced before any class information is available to WMI.</span></span>

<span data-ttu-id="34c4a-114">Wenn Sie eine MOF-Master Datei kompilieren, werden nur Qualifizierer mit der [**geänderten**](qualifier-flavors.md) Konfiguration in die sprachspezifische MOF-Datei verschoben.</span><span class="sxs-lookup"><span data-stu-id="34c4a-114">When you compile a master MOF file, only qualifiers with the [**Amended**](qualifier-flavors.md) flavor are moved to the language-specific MOF file.</span></span> <span data-ttu-id="34c4a-115">Qualifizierer, die nicht die **geänderte** Art aufweisen, werden nicht lokalisiert und sind nur in der grundlegenden Klassendefinition in der sprach neutralen MOF-Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="34c4a-115">Qualifiers that do not have the **Amended** flavor are not localized and only exist in the basic class definition in the language-neutral MOF file.</span></span> <span data-ttu-id="34c4a-116">Nicht lokalisierte Qualifizierer können für Standard Beschreibungen verwendet werden, wenn keine lokalisierten Beschreibungen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="34c4a-116">Nonlocalized qualifiers can be used for default descriptions if localized descriptions are not available.</span></span>

<span data-ttu-id="34c4a-117">Sie können den [pragma-Zusatz](pragma-amendment.md) Befehl verwenden, anstatt ihn als Schalter für den MOF- [**Compiler anzugeben.**](qualifier-flavors.md)</span><span class="sxs-lookup"><span data-stu-id="34c4a-117">You can use the [pragma amendment](pragma-amendment.md) command instead of specifying [**Amended**](qualifier-flavors.md) as a switch to the MOF compiler.</span></span> <span data-ttu-id="34c4a-118">Jede dieser Optionen entspricht der Anforderung von sprachspezifischen und sprach neutralen Versionen einer MOF-Datei.</span><span class="sxs-lookup"><span data-stu-id="34c4a-118">Either of these options are equivalent to requesting language-specific and language-neutral versions of a MOF file.</span></span> <span data-ttu-id="34c4a-119">Wenn Sie entweder den Befehl "Pragma-Zusatz" oder die **geänderte** Befehlszeilenoption verwenden, müssen Sie den Namen der Ausgabedateien mithilfe der Optionen " **-MFL** " und " **-MOF** " an der Eingabeaufforderung angeben.</span><span class="sxs-lookup"><span data-stu-id="34c4a-119">If you use either the pragma amendment command or the **Amended** command-line option, you must specify the name of the output files using the **-MFL** and **-MOF** options at the command prompt.</span></span>

> [!Note]  
> <span data-ttu-id="34c4a-120">Die sprachneutrale MOF-Datei, die der MOF-Compiler generiert, enthält die dezimale Entsprechung der Gebiets Schema-ID, auch wenn dieser Wert in Hexadezimal eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="34c4a-120">The language-neutral MOF file that the MOF compiler generates contains the decimal equivalent of the locale ID, even if this value was entered in hexadecimal.</span></span> <span data-ttu-id="34c4a-121">Im obigen Beispiel hat der Compiler den Wert 0x409 in die Dezimalzahl 1033 für die Ausgabedatei "lnmof. mof" konvertiert.</span><span class="sxs-lookup"><span data-stu-id="34c4a-121">In the example above, the compiler has converted the value 0x409 to the decimal number 1033 for the Lnmof.mof output file.</span></span>

 

 

 



