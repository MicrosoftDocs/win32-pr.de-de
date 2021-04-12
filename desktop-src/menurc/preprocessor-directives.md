---
title: Präprozessordirektiven (Menüs und andere Ressourcen)
description: Sie können die in der folgenden Tabelle beschriebenen Anweisungen nach Bedarf in Ihrem Ressourcen Skript verwenden. Sie weisen RC an, Aktionen auszuführen oder den Namen Werte zuzuweisen.
ms.assetid: 162f946e-54d8-4e23-9aa7-8e91eda4ee68
keywords:
- Ressourcen Compiler, Präprozessordirektiven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e8c32f1d32dab784d5d947fdf64b7018451a5a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340238"
---
# <a name="preprocessor-directives-menus-and-other-resources"></a><span data-ttu-id="a3c2e-105">Präprozessordirektiven (Menüs und andere Ressourcen)</span><span class="sxs-lookup"><span data-stu-id="a3c2e-105">Preprocessor Directives (Menus and Other Resources)</span></span>

<span data-ttu-id="a3c2e-106">Sie können die in der folgenden Tabelle beschriebenen Anweisungen nach Bedarf in Ihrem Ressourcen Skript verwenden.</span><span class="sxs-lookup"><span data-stu-id="a3c2e-106">You can use the directives described in the following table as needed in your resource script.</span></span> <span data-ttu-id="a3c2e-107">Sie weisen RC an, Aktionen auszuführen oder den Namen Werte zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a3c2e-107">They instruct RC to perform actions or to assign values to names.</span></span>



| <span data-ttu-id="a3c2e-108">Anweisung</span><span class="sxs-lookup"><span data-stu-id="a3c2e-108">Directive</span></span>                     | <span data-ttu-id="a3c2e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3c2e-109">Description</span></span>                                                           |
|-------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="a3c2e-110">**\#definieren**</span><span class="sxs-lookup"><span data-stu-id="a3c2e-110">**\#define**</span></span>](-define.md)   | <span data-ttu-id="a3c2e-111">Definiert einen angegebenen Namen, indem ihm ein angegebener Wert zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a3c2e-111">Defines a specified name by assigning it a given value.</span></span>               |
| [<span data-ttu-id="a3c2e-112">**\#elif**</span><span class="sxs-lookup"><span data-stu-id="a3c2e-112">**\#elif**</span></span>](-elif.md)       | <span data-ttu-id="a3c2e-113">Markiert eine optionale Klausel eines Blocks für die bedingte Kompilierung.</span><span class="sxs-lookup"><span data-stu-id="a3c2e-113">Marks an optional clause of a conditional-compilation block.</span></span>          |
| [<span data-ttu-id="a3c2e-114">**\#else**</span><span class="sxs-lookup"><span data-stu-id="a3c2e-114">**\#else**</span></span>](-else.md)       | <span data-ttu-id="a3c2e-115">Markiert die letzte optionale Klausel eines Blocks für die bedingte Kompilierung.</span><span class="sxs-lookup"><span data-stu-id="a3c2e-115">Marks the last optional clause of a conditional-compilation block.</span></span>    |
| [<span data-ttu-id="a3c2e-116">**\#endif**</span><span class="sxs-lookup"><span data-stu-id="a3c2e-116">**\#endif**</span></span>](-endif.md)     | <span data-ttu-id="a3c2e-117">Markiert das Ende eines Blocks für die bedingte Kompilierung.</span><span class="sxs-lookup"><span data-stu-id="a3c2e-117">Marks the end of a conditional-compilation block.</span></span>                     |
| [<span data-ttu-id="a3c2e-118">**\#sei**</span><span class="sxs-lookup"><span data-stu-id="a3c2e-118">**\#if**</span></span>](-if.md)           | <span data-ttu-id="a3c2e-119">Kompiliert das Skript bedingt, wenn ein angegebener Ausdruck true ist.</span><span class="sxs-lookup"><span data-stu-id="a3c2e-119">Conditionally compiles the script if a specified expression is true.</span></span>  |
| [<span data-ttu-id="a3c2e-120">**\#ifdef**</span><span class="sxs-lookup"><span data-stu-id="a3c2e-120">**\#ifdef**</span></span>](-ifdef.md)     | <span data-ttu-id="a3c2e-121">Kompiliert das Skript bedingt, wenn ein angegebener Name definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a3c2e-121">Conditionally compiles the script if a specified name is defined.</span></span>     |
| [<span data-ttu-id="a3c2e-122">**\#ifndef**</span><span class="sxs-lookup"><span data-stu-id="a3c2e-122">**\#ifndef**</span></span>](-ifndef.md)   | <span data-ttu-id="a3c2e-123">Kompiliert das Skript bedingt, wenn ein angegebener Name nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a3c2e-123">Conditionally compiles the script if a specified name is not defined.</span></span> |
| [<span data-ttu-id="a3c2e-124">**\#darunter**</span><span class="sxs-lookup"><span data-stu-id="a3c2e-124">**\#include**</span></span>](-include.md) | <span data-ttu-id="a3c2e-125">Kopiert den Inhalt einer Datei in die Ressourcen Definitionsdatei.</span><span class="sxs-lookup"><span data-stu-id="a3c2e-125">Copies the contents of a file into the resource-definition file.</span></span>      |
| [<span data-ttu-id="a3c2e-126">**\#undef**</span><span class="sxs-lookup"><span data-stu-id="a3c2e-126">**\#undef**</span></span>](-undef.md)     | <span data-ttu-id="a3c2e-127">Entfernt die Definition des angegebenen Namens.</span><span class="sxs-lookup"><span data-stu-id="a3c2e-127">Removes the definition of the specified name.</span></span>                         |



 

<span data-ttu-id="a3c2e-128">Zum Definieren von Symbolen für Ihre Ressourcen Bezeichner verwenden Sie die **\# define** -Direktive, um Sie in einer Header Datei zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a3c2e-128">To define symbols for your resource identifiers, use the **\#define** directive to define them in a header file.</span></span> <span data-ttu-id="a3c2e-129">Fügen Sie diesen Header sowohl im Ressourcen Skript als auch in den Quellcode der Anwendung ein.</span><span class="sxs-lookup"><span data-stu-id="a3c2e-129">Include this header both in the resource script and your application source code.</span></span> <span data-ttu-id="a3c2e-130">Entsprechend definieren Sie die Werte für Ressourcen Attribute und-Stile durch Einschließen von Windows. h in das Ressourcen Skript.</span><span class="sxs-lookup"><span data-stu-id="a3c2e-130">Similarly, you define the values for resource attributes and styles by including Windows.h in the resource script.</span></span>

<span data-ttu-id="a3c2e-131">RC behandelt Dateien mit den Erweiterungen ". c" und ". h" auf besondere Weise.</span><span class="sxs-lookup"><span data-stu-id="a3c2e-131">RC treats files with the .c and .h extensions in a special manner.</span></span> <span data-ttu-id="a3c2e-132">Dabei wird davon ausgegangen, dass eine Datei mit einer dieser Erweiterungen keine Ressourcen enthält.</span><span class="sxs-lookup"><span data-stu-id="a3c2e-132">It assumes that a file with one of these extensions does not contain resources.</span></span> <span data-ttu-id="a3c2e-133">Wenn eine Datei die Dateinamenerweiterung ". c" oder ". h" enthält, ignoriert RC alle Zeilen in der Datei mit Ausnahme der Präprozessordirektiven.</span><span class="sxs-lookup"><span data-stu-id="a3c2e-133">If a file has the .c or .h file name extension, RC ignores all lines in the file except the preprocessor directives.</span></span> <span data-ttu-id="a3c2e-134">Wenn Sie also eine Datei einschließen möchten, die Ressourcen in einem anderen Ressourcen Skript enthält, geben Sie die Datei an, die eine andere Erweiterung als ". c" oder ". h" enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="a3c2e-134">Therefore, to include a file that contains resources in another resource script, give the file to be included an extension other than .c or .h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3c2e-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a3c2e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3c2e-136">Pragma-Direktiven</span><span class="sxs-lookup"><span data-stu-id="a3c2e-136">Pragma Directives</span></span>](pragma-directives.md)
</dt> </dl>

 

 




