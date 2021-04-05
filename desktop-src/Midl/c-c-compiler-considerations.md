---
title: C/C++-compilerüberlegungen
description: Der mittlerer l-Compiler muss mit dem c-Compiler und dem c-Präprozessor zusammenarbeiten.
ms.assetid: 3d91d0e4-3a47-4aa2-82d6-c3af11df3a78
keywords:
- Mittel l-compilermittell, C-Compiler
- C-compilermittell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf6968951bbcbb423896f5609092054dfa65f4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037359"
---
# <a name="cc-compiler-considerations"></a><span data-ttu-id="a27a0-105">C/C++-compilerüberlegungen</span><span class="sxs-lookup"><span data-stu-id="a27a0-105">C/C++-Compiler Considerations</span></span>

<span data-ttu-id="a27a0-106">Der mittlerer l-Compiler muss mit dem c-Compiler und dem c-Präprozessor zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a27a0-106">The MIDL compiler must interoperate with the C compiler and C preprocessor.</span></span> <span data-ttu-id="a27a0-107">Die C++-Syntax für die Eingabe wird von der mittleren l nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="a27a0-107">MIDL does not accept C++ syntax on input.</span></span> <span data-ttu-id="a27a0-108">Die generierte h-Datei verfügt sowohl über C-als auch C++-Definitionen für Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="a27a0-108">The generated .h file has both C-style and C++-style definitions for interfaces.</span></span> <span data-ttu-id="a27a0-109">In den folgenden Themen werden die Anforderungen für den C-Compiler beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a27a0-109">The following topics describe the requirements for the C compiler.</span></span>

-   [<span data-ttu-id="a27a0-110">C-Compilerprobleme beim Packen</span><span class="sxs-lookup"><span data-stu-id="a27a0-110">C-Compiler Packing Issues</span></span>](c-compiler-packing-issues.md)
-   [<span data-ttu-id="a27a0-111">C-compilerdefinitionen für Proxy/Stub</span><span class="sxs-lookup"><span data-stu-id="a27a0-111">C-Compiler Definitions for Proxy/Stubs</span></span>](c-compiler-definitions-for-proxy-stubs.md)

 

 




