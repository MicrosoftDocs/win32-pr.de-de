---
description: Schließt den Inhalt einer MOF-Datei in eine andere MOF-Datei ein.
ms.assetid: 06765956-e4ee-467b-9b3b-d5da17b9cd82
ms.tgt_platform: multiple
title: '#include'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5eb3d203cff5bca7e5096082cca7ba531580ae27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362679"
---
# <a name="include"></a><span data-ttu-id="3ceb6-103">"#include"</span><span class="sxs-lookup"><span data-stu-id="3ceb6-103">'#include'</span></span>
<span data-ttu-id="3ceb6-104">/\* Title: mymof. MOF                           *//*   Title: MyMof2. MOF \*/</span><span class="sxs-lookup"><span data-stu-id="3ceb6-104">/\*   Title: MyMof.Mof                           */ /*   Title: MyMof2.Mof                               \*/</span></span>

<span data-ttu-id="3ceb6-105">Der \# Befehl include Präprozessor enthält den Inhalt einer MOF-Datei in eine andere MOF-Datei.</span><span class="sxs-lookup"><span data-stu-id="3ceb6-105">The \#include preprocessor command includes the contents of one MOF file into another MOF file.</span></span> <span data-ttu-id="3ceb6-106">Im folgenden Codebeispiel wird die Syntax für den \# include-Befehl beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3ceb6-106">The following code example describes the syntax for the \#include command.</span></span>

``` syntax
#include ("Moffile.mof")
```

<span data-ttu-id="3ceb6-107">Im vorherigen Beispiel ist "muffile. mof" der Name der MOF-Datei, die eingeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ceb6-107">In the previous example, Moffile.mof is the name of the MOF file to include.</span></span>

<span data-ttu-id="3ceb6-108">Das folgende Beispiel zeigt zwei MOF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="3ceb6-108">The following example shows two MOF files.</span></span> <span data-ttu-id="3ceb6-109">Wenn Sie die erste MOF-Datei kompilieren, kompiliert der Compiler automatisch die zweite MOF-Datei (Mymof2. MOF) an dem Speicherort, an dem Sie die \# include-Anweisung platzieren.</span><span class="sxs-lookup"><span data-stu-id="3ceb6-109">When you compile the first MOF file, the compiler automatically compiles the second MOF file (Mymof2.mof) in the location you place the \#include statement.</span></span>

``` syntax
/*   Title: MyMof.Mof                           */
/*                                              */ 
/*   This MOF file shows how to include  */
/*   an MOF file in another MOF file             */

#pragma namespace("\\\\.\\root")            

#include ("mymof2.mof")

class myclass1 
{
    [key] string Description;
};


instance of myclass1
{
    Description = "Description of myclass1";
};
/*   End of MyMof.Mof                           */
```

<span data-ttu-id="3ceb6-110">Das vorherige Beispiel enthält die folgende MOF-Datei:</span><span class="sxs-lookup"><span data-stu-id="3ceb6-110">The following MOF file is included in the previous example:</span></span>

``` syntax
/*   Title: MyMof2.Mof                               */
/*                                                   */
/*   This MOF is included when MyMof.MOF is compiled */

class myclass2 
{
    [key] string Description;
};


instance of myclass2
{
    Description = "Description of myclass2";
    
};
```

## <a name="related-topics"></a><span data-ttu-id="3ceb6-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3ceb6-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ceb6-112">Präprozessorbefehle</span><span class="sxs-lookup"><span data-stu-id="3ceb6-112">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



