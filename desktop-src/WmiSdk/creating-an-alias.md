---
description: Ein Alias in WMI ist ein symbolischer Verweis in einer Klasse oder einer Klasseninstanz an einer anderen Stelle in einer Managed Object Format Datei (MOF).
ms.assetid: bf4981dc-3aab-46c5-bf02-48132ccec8c2
ms.tgt_platform: multiple
title: Erstellen eines WMI-Alias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fdd538e113f227eac4980855ea0035e839b92fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343819"
---
# <a name="creating-a-wmi-alias"></a><span data-ttu-id="fd109-103">Erstellen eines WMI-Alias</span><span class="sxs-lookup"><span data-stu-id="fd109-103">Creating a WMI Alias</span></span>

<span data-ttu-id="fd109-104">Ein [*Alias*](gloss-a.md) in WMI ist ein symbolischer Verweis in einer Klasse oder einer Klasseninstanz an einer anderen Stelle in einer Managed Object Format Datei (MOF).</span><span class="sxs-lookup"><span data-stu-id="fd109-104">An [*alias*](gloss-a.md) in WMI is a symbolic reference in either a class or a class instance located elsewhere in a Managed Object Format (MOF) file.</span></span> <span data-ttu-id="fd109-105">Der MOF-Compiler verwendet Aliase, um Verweise zwischen Klassen und Instanzen herzustellen.</span><span class="sxs-lookup"><span data-stu-id="fd109-105">The MOF compiler uses aliases to establish references between classes and instances.</span></span> <span data-ttu-id="fd109-106">Der Compiler löst Aliase zu den Klassen auf, auf die Sie verweisen, sodass Aliasnamen im kompilierten Code nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="fd109-106">The compiler resolves aliases to the classes to which they refer, so alias names are not available in compiled code.</span></span> <span data-ttu-id="fd109-107">Daher können Client Anwendungen nicht auf Klassen verweisen, die Aliase verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd109-107">As a result, client applications cannot refer to classes using aliases.</span></span>

> [!Note]  
> <span data-ttu-id="fd109-108">WMI unterstützt Forward-Verweise, aber keine zirkulären Aliase.</span><span class="sxs-lookup"><span data-stu-id="fd109-108">WMI supports forward referencing but not circular aliases.</span></span>

 

<span data-ttu-id="fd109-109">Ein Alias weist nur den Gültigkeitsbereich innerhalb der MOF-Datei auf, in der Sie den Alias deklarieren.</span><span class="sxs-lookup"><span data-stu-id="fd109-109">An alias has scope only within the MOF file in which you declare the alias.</span></span> <span data-ttu-id="fd109-110">Daher verwenden Sie in der Regel einen Alias als Verknüpfung zu einem langen Objekt Pfad.</span><span class="sxs-lookup"><span data-stu-id="fd109-110">Therefore, you typically use an alias as a shortcut to a lengthy object path.</span></span>

<span data-ttu-id="fd109-111">**So definieren Sie einen Alias**</span><span class="sxs-lookup"><span data-stu-id="fd109-111">**To define an alias**</span></span>

1.  <span data-ttu-id="fd109-112">Fügen Sie der-Instanz oder-Klassen Deklaration den Ausdruck "as $*Aliasname*" hinzu.</span><span class="sxs-lookup"><span data-stu-id="fd109-112">Add the phrase "as $*aliasname*" to the instance or class declaration.</span></span>
2.  <span data-ttu-id="fd109-113">Aliasnamen folgen denselben Regeln wie Instanznamen und Klassennamen, mit dem Unterschied, dass Aliasnamen mit einem Dollarzeichen ($) beginnen müssen.</span><span class="sxs-lookup"><span data-stu-id="fd109-113">Alias names follow the same rules as instance and class names, except that alias names must begin with a dollar sign ($).</span></span> <span data-ttu-id="fd109-114">Unterstriche können in einem Aliasnamen nach dem ersten Zeichen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fd109-114">Underscores can appear in an alias name following the initial character.</span></span>

<span data-ttu-id="fd109-115">Im folgenden Codebeispiel wird beschrieben, wie ein Alias in einer Klassendefinition verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd109-115">The following code example describes how to use an alias in a class definition.</span></span>

``` syntax
class MyClass as $MyClassAlias
{
};
instance of MyClass as $MyInstanceAlias
{
};
```

<span data-ttu-id="fd109-116">In den folgenden Codebeispielen wird beschrieben, wie ein Alias als symbolischer Verweis auf einen Objekt Pfad verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd109-116">The following code examples describe how to use an alias as a symbolic reference to an object path.</span></span> <span data-ttu-id="fd109-117">In diesen Beispielen werden zwei Klassen deklariert, um einen Datenträger zu beschreiben: die Disk-Klasse zum Angeben des Laufwerk Buchstabens und die DiskRef-Klasse, um den Datenträger Pfad anzugeben.</span><span class="sxs-lookup"><span data-stu-id="fd109-117">These examples declare two classes to describe a disk: the Disk class to indicate the drive letter and the DiskRef class to indicate the disk path.</span></span> <span data-ttu-id="fd109-118">Ein Alias ist für die Datenträger Klasseninstanz definiert.</span><span class="sxs-lookup"><span data-stu-id="fd109-118">An alias is defined for the Disk class instance.</span></span> <span data-ttu-id="fd109-119">Dieser Alias wird als Wert für die Eigenschaft pathto Disk in der DiskRef-Instanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd109-119">This alias is used as the value for the PathToDisk property in the DiskRef instance.</span></span>

``` syntax
class Disk {
    [key]  string    DriveLetter;
};

class DiskRef 
{
    [key]  string    MyKey;
    Disk   ref       PathToDisk;
};

instance of Disk as $DiskAlias 
{
    DriveLetter = "c";
};

instance of DiskRef
{
    MyKey      =  "hello";
    PathToDisk = $DiskAlias;
};
```

## <a name="related-topics"></a><span data-ttu-id="fd109-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd109-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd109-121">Erstellen einer Klasse</span><span class="sxs-lookup"><span data-stu-id="fd109-121">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



