---
title: Verwenden von C/C++-Präprozessor mit mittlerer l
description: Der mittlerer l-Compiler führt keine Vorverarbeitung von Quelldateien aus.
ms.assetid: 0f62d2a4-cfc3-42a7-b3a6-4e5c67c7c849
keywords:
- Mittel l-compilermittell, C-Präprozessor
- C-präprozessormittell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5752bd64ee9a9b5fc26d586b5bc33c1a1fb96e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309823"
---
# <a name="using-cc-preprocessor-with-midl"></a><span data-ttu-id="0266a-105">Verwenden von C/C++-Präprozessor mit mittlerer l</span><span class="sxs-lookup"><span data-stu-id="0266a-105">Using C/C++-Preprocessor with MIDL</span></span>

<span data-ttu-id="0266a-106">Der mittlerer l-Compiler führt keine Vorverarbeitung von Quelldateien aus.</span><span class="sxs-lookup"><span data-stu-id="0266a-106">The MIDL compiler does not preprocess source files.</span></span> <span data-ttu-id="0266a-107">Stattdessen verwendet der mittlerer l-Compiler einen verfügbaren Präprozessor, um den Eingabestream für die Verarbeitung vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="0266a-107">Rather, the MIDL compiler uses an available preprocessor to prepare the input stream for parsing.</span></span> <span data-ttu-id="0266a-108">In der Standardeinstellung verwendet die Mittel l den Präprozessor für den Microsoft C/C++-Compiler aus derselben Gebäudeumgebung wie die Mitte.</span><span class="sxs-lookup"><span data-stu-id="0266a-108">By default, MIDL uses the preprocessor for the Microsoft C/C++ compiler from the same building environment as MIDL.</span></span> <span data-ttu-id="0266a-109">Der Benutzer kann bei Bedarf einen anderen Präprozessor angeben, der von der Mittell verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0266a-109">The user can indicate a different preprocessor to be used by MIDL, if needed.</span></span>

<span data-ttu-id="0266a-110">In mittlerer l-Datei werden separate präprozessorausführungen für IDL-und ACF-Dateien der obersten Ebene und für jede mit der Anweisung "Mittel l Import" importierte Datei ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0266a-110">MIDL spawns separate preprocessor runs for top-level IDL and ACF files, and for each file imported with the MIDL import directive.</span></span> <span data-ttu-id="0266a-111">Dateien, die in der **\# include** -Anweisung enthalten sind, werden vom Präprozessor direkt verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0266a-111">Files included with the **\#include** directive are handled by the preprocessor directly.</span></span>

<span data-ttu-id="0266a-112">In den folgenden Themen werden verschiedene Aspekte von mittlerer l-präprozessorinteraktionen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="0266a-112">The following topics describe various aspects of MIDL-preprocessor interactions:</span></span>

-   [<span data-ttu-id="0266a-113">C-präprozessoranforderungen für die Mittel l</span><span class="sxs-lookup"><span data-stu-id="0266a-113">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
-   [<span data-ttu-id="0266a-114">Überprüfen von Präprozessoroptionen</span><span class="sxs-lookup"><span data-stu-id="0266a-114">Verifying Preprocessor Options</span></span>](verifying-preprocessor-options.md)
-   [<span data-ttu-id="0266a-115">Speichern der Präprozessorausgabe</span><span class="sxs-lookup"><span data-stu-id="0266a-115">Saving Preprocessor Output</span></span>](saving-preprocessor-output.md)
-   [<span data-ttu-id="0266a-116">Umgang mit \# Definitionen in IDL-Dateien</span><span class="sxs-lookup"><span data-stu-id="0266a-116">Dealing with \#defines in IDL Files</span></span>](dealing-with-defines-in-idl-files-2.md)

 

 




