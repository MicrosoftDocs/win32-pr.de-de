---
description: Sie müssen die setupopeninffile-Funktion verwenden, um die INF-Datei zu öffnen, bevor Sie Informationen aus ihr abrufen oder andere INF-Dateien an Sie anfügen können.
ms.assetid: ba4d511a-ad19-4619-a10a-cafef789821b
title: Öffnen der INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8493fda983f2942705b97ea243f6cb95e91c15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865719"
---
# <a name="opening-the-inf-file"></a><span data-ttu-id="11c45-103">Öffnen der INF-Datei</span><span class="sxs-lookup"><span data-stu-id="11c45-103">Opening the INF File</span></span>

<span data-ttu-id="11c45-104">Sie müssen die [**setupopeninffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) -Funktion verwenden, um die INF-Datei zu öffnen, bevor Sie Informationen aus ihr abrufen oder andere INF-Dateien an Sie anfügen können.</span><span class="sxs-lookup"><span data-stu-id="11c45-104">You must use the [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) function to open the INF file before you can retrieve information from it, or append other INF files to it.</span></span>

<span data-ttu-id="11c45-105">Im folgenden wird eine INF-Datei mithilfe von [**setupopeninffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) geöffnet, und es wird ein Handle, myinf, an die geöffnete INF-Datei zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="11c45-105">The following opens an INF file using [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) and returns a handle, MyInf, to the opened INF file.</span></span> <span data-ttu-id="11c45-106">Der *infclass* -Parameter von **setupopeininffile** ist als **null** angegeben, um anzugeben, dass die Klasse der INF-Datei ignoriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="11c45-106">The *InfClass* parameter of **SetupOpenInfFile** is specified as **NULL** to indicate that the Class of the INF file should be ignored.</span></span>


```C++
HINF MyInf;                //variable to hold the INF handle
UINT ErrorLine;            //variable to hold errors returned
BOOL test=0;                 //variable to receive function success
 
MyInf = SetupOpenInfFile (
      szInfFileName,       //the filename of the inf file to open
      NULL,                //optional class information
      INF_STYLE_WIN4,      //the inf style
      &ErrorLine           //line number of the syntax error
);
```



<span data-ttu-id="11c45-107">Nachdem eine INF-Datei geöffnet wurde, können Sie die Funktion [**setupopenappendinffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) aufrufen, um der geöffneten INF-Datei eine Datei anzufügen.</span><span class="sxs-lookup"><span data-stu-id="11c45-107">After an INF file is opened, you can call the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function to append a file to the open INF file.</span></span> <span data-ttu-id="11c45-108">Wiederholen Sie diesen Vorgang, um mehrere Dateien anzufügen.</span><span class="sxs-lookup"><span data-stu-id="11c45-108">To append several files, repeat this process.</span></span> <span data-ttu-id="11c45-109">Wenn Sie die Funktion **setupopenappendinffile** aufrufen und der an Sie weiter gegebene Dateiname **null** ist, durchsucht die Funktion den Abschnitt Version der geöffneten INF-Datei (und alle angefügten INF-Dateien) nach einem Layoutfile-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="11c45-109">If you call the **SetupOpenAppendInfFile** function and the filename passed to it is **NULL**, then the function will search the Version section of the open INF file (and any appended INF files) for a LayoutFile key.</span></span> <span data-ttu-id="11c45-110">Wenn die Funktion einen Schlüssel findet, wird die durch diesen Schlüssel angegebene Datei (normalerweise Layout) angefügt. Inf).</span><span class="sxs-lookup"><span data-stu-id="11c45-110">If the function finds a key, it will append the file specified by that key (usually LAYOUT.INF).</span></span> <span data-ttu-id="11c45-111">Wenn mehrere INF-Dateien kombiniert wurden, wird **setupopeinappendinffile** bei der Suche nach einem Versions Abschnitt mit der letzten angefügten INF-Datei gestartet.</span><span class="sxs-lookup"><span data-stu-id="11c45-111">When multiple INF files have been combined, **SetupOpenAppendInfFile** starts with the last appended INF file when it searches for a Version section.</span></span>

 

 



