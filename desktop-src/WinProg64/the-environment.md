---
title: Die Umgebung
description: Entwickler, die an Anwendungen für 64-Bit-Windows arbeiten, finden die Entwicklungsumgebung praktisch identisch mit der Entwicklungsumgebung für 32-Bit-Windows.
ms.assetid: 49b2b952-f771-4721-a9b0-01eb67a98007
keywords:
- Entwicklungsumgebung 64-Bit-Windows-Programmierung
- Umgebung 64-Bit-Windows-Programmierung
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung, Entwicklungsumgebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104ea1bdacbb478eaa0abcf46d04c3d772540f26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036631"
---
# <a name="the-environment"></a><span data-ttu-id="eb21b-106">Die Umgebung</span><span class="sxs-lookup"><span data-stu-id="eb21b-106">The Environment</span></span>

<span data-ttu-id="eb21b-107">Entwickler, die an Anwendungen für 64-Bit-Windows arbeiten, finden die Entwicklungsumgebung praktisch identisch mit der Entwicklungsumgebung für 32-Bit-Windows.</span><span class="sxs-lookup"><span data-stu-id="eb21b-107">Developers working on applications for 64-bit Windows will find the development environment virtually identical to the development environment for 32-bit Windows.</span></span> <span data-ttu-id="eb21b-108">Die vorhandenen APIs wurden bei Bedarf geändert, damit Sie die Genauigkeit der Plattform widerspiegeln können, auf der Sie ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="eb21b-108">The existing APIs have been modified where necessary to allow them to reflect the precision of the platform on which they are running.</span></span> <span data-ttu-id="eb21b-109">Das Ergebnis ist Einfachheit und eine kurze Lernkurve für den Entwickler – das Schreiben von Code für 64-Bit-Windows ist genauso wie das Schreiben von Code für 32-Bit-Windows.</span><span class="sxs-lookup"><span data-stu-id="eb21b-109">The result is simplicity and a short learning curve for the developer—writing code for 64-bit Windows is just like writing code for 32-bit Windows.</span></span>

<span data-ttu-id="eb21b-110">Die Windows-Header Dateien unterstützen neue Datentypen, mit denen Zeiger und Zeiger zugeordnete Variablen die Genauigkeit der Plattform widerspiegeln können.</span><span class="sxs-lookup"><span data-stu-id="eb21b-110">The Windows header files support new data types that allow pointers and pointer-associated variables to reflect the precision of the platform.</span></span> <span data-ttu-id="eb21b-111">Dies bedeutet, dass Entwickler eine einzelne quellbasis kompilieren können, um nativ 32 auf Windows-oder 64-Bit-Windows-Fenstern auszuführen.</span><span class="sxs-lookup"><span data-stu-id="eb21b-111">This means that developers can compile a single source base to run natively on either 32-bit Windows or 64-bit Windows.</span></span> <span data-ttu-id="eb21b-112">Diese Strategie reduziert die Kosten für die Entwicklung von Anwendungen, die 64-Bit-Hardware nutzen, wie z. b. AMD Opteron oder Athlon64-Prozessoren oder Intel Itanium-Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="eb21b-112">This strategy reduces the cost of developing applications that leverage 64-bit hardware such as AMD Opteron or Athlon64 processors or Intel Itanium processors.</span></span>

<span data-ttu-id="eb21b-113">Wenn Sie die neuen Datentyp Konventionen so schnell wie möglich übernehmen, müssen Sie mehr Zeit für die Bereitstellung Ihrer 64 Anwendungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="eb21b-113">You will have more time to make your applications 64-bit ready if you adopt the new data-type conventions as soon as possible.</span></span> <span data-ttu-id="eb21b-114">Wenn Sie den Code ändern, sollten Sie die Daten Definitionen gleichzeitig ändern.</span><span class="sxs-lookup"><span data-stu-id="eb21b-114">If you are changing your code, you should change the data definitions at the same time.</span></span> <span data-ttu-id="eb21b-115">Testen Sie die Anwendung auf 32-Bit-Fenstern, führen Sie Sie über den 64-Bit-Compiler aus (beschrieben in [den Tools](the-tools.md)), und die Anwendung kann getestet werden, wenn Sie über die entsprechende 64-Bit-Hardware verfügen.</span><span class="sxs-lookup"><span data-stu-id="eb21b-115">Test the application on 32-bit Windows, run it through the 64-bit compiler (described in [The Tools](the-tools.md)), and the application will be ready to test when you have the appropriate 64-bit hardware.</span></span>

 

 




