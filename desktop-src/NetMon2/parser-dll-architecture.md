---
description: Die Architektur der Parser-DLL muss die in der folgenden Abbildung gezeigten Features bereitstellen.
ms.assetid: 2da5d4bc-a219-47b5-8522-1237f7bcac16
title: Architektur der Parser-DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7852029a892d8b74c954cbc2d7341fcaf29032fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485854"
---
# <a name="parser-dll-architecture"></a><span data-ttu-id="b286c-103">Architektur der Parser-DLL</span><span class="sxs-lookup"><span data-stu-id="b286c-103">Parser DLL Architecture</span></span>

<span data-ttu-id="b286c-104">Die Architektur der Parser-DLL muss die in der folgenden Abbildung gezeigten Features bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b286c-104">The architecture of the parser DLL must provide the features shown in the following illustration.</span></span> <span data-ttu-id="b286c-105">Beachten Sie, dass für einige Features nur ein Einstiegspunkt implementiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="b286c-105">Be aware that some features require the implementation of only one entry point.</span></span> <span data-ttu-id="b286c-106">Wenn Ihre Parser-DLL jedoch mehrere Protokolle unterstützt, erfordert die Funktion die Implementierung mehrerer Einstiegspunkte.</span><span class="sxs-lookup"><span data-stu-id="b286c-106">However, if your parser DLL supports multiple protocols, then the feature requires the implementation of multiple entry points.</span></span>

![Parser-DLL-Features](images/parserarchitecture1.png)



| <span data-ttu-id="b286c-108">Informationen über</span><span class="sxs-lookup"><span data-stu-id="b286c-108">For information about</span></span>                                                  | <span data-ttu-id="b286c-109">Finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="b286c-109">See</span></span>                                                                    |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="b286c-110">Gewusst wie: Implementieren von parserdll-Exportfunktionen</span><span class="sxs-lookup"><span data-stu-id="b286c-110">How to implement parser DLL export functions.</span></span>                          | [<span data-ttu-id="b286c-111">Schreiben eines Protokoll Parsers</span><span class="sxs-lookup"><span data-stu-id="b286c-111">Writing a Protocol Parser</span></span>](writing-a-protocol-parser.md)             |
| <span data-ttu-id="b286c-112">Bestimmte Funktionen und Strukturen, die von den Parser verwendet werden – Referenz Themen.</span><span class="sxs-lookup"><span data-stu-id="b286c-112">Specific functions and structures that parsers use — reference topics.</span></span> | [<span data-ttu-id="b286c-113">Parser-Funktionen und-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b286c-113">Parser Functions and Structures</span></span>](parser-functions-and-structures.md) |



 

 

 



