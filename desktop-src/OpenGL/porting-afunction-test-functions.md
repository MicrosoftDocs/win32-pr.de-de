---
title: Portieren von Test Funktionen
description: In der folgenden Tabelle sind die verfügbaren IRIS GL-Alpha Testfunktionen und ihre entsprechenden OpenGL-Funktionen aufgelistet.
ms.assetid: cd4082fe-2fd6-43d8-a9a7-37fd448c084b
keywords:
- IRIS GL portieren, afunction-Testfunktionen
- Portieren von IRIS GL, afunction-Testfunktionen
- Portieren auf OpenGL von IRIS GL, afunction Test Functions
- OpenGL-Portierung von IRIS GL, afunction-Testfunktionen
- afunction-Testfunktionen
- Alpha-Testfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3abfd3ba46d99f8b70ecfb97c0160efea944ccd2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856880"
---
# <a name="porting-afunction-test-functions"></a><span data-ttu-id="ef252-109">Portieren von Test Funktionen</span><span class="sxs-lookup"><span data-stu-id="ef252-109">Porting afunction Test Functions</span></span>

<span data-ttu-id="ef252-110">In der folgenden Tabelle sind die verfügbaren IRIS GL-Alpha Testfunktionen und ihre entsprechenden OpenGL-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ef252-110">The following table lists the available IRIS GL alpha test functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="ef252-111">Aufheben der Bindung</span><span class="sxs-lookup"><span data-stu-id="ef252-111">afunction</span></span>    | <span data-ttu-id="ef252-112">glalphafunc</span><span class="sxs-lookup"><span data-stu-id="ef252-112">glAlphaFunc</span></span>  |
|--------------|--------------|
| <span data-ttu-id="ef252-113">AF- \_ NotEqual</span><span class="sxs-lookup"><span data-stu-id="ef252-113">AF\_NOTEQUAL</span></span> | <span data-ttu-id="ef252-114">GL- \_ NotEqual</span><span class="sxs-lookup"><span data-stu-id="ef252-114">GL\_NOTEQUAL</span></span> |
| <span data-ttu-id="ef252-115">\_immer AF</span><span class="sxs-lookup"><span data-stu-id="ef252-115">AF\_ALWAYS</span></span>   | <span data-ttu-id="ef252-116">immer GL. \_</span><span class="sxs-lookup"><span data-stu-id="ef252-116">GL\_ALWAYS</span></span>   |
| <span data-ttu-id="ef252-117">AF \_ nie</span><span class="sxs-lookup"><span data-stu-id="ef252-117">AF\_NEVER</span></span>    | <span data-ttu-id="ef252-118">GL \_ nie</span><span class="sxs-lookup"><span data-stu-id="ef252-118">GL\_NEVER</span></span>    |
| <span data-ttu-id="ef252-119">weniger als AF \_</span><span class="sxs-lookup"><span data-stu-id="ef252-119">AF\_LESS</span></span>     | <span data-ttu-id="ef252-120">GL \_ weniger</span><span class="sxs-lookup"><span data-stu-id="ef252-120">GL\_LESS</span></span>     |
| <span data-ttu-id="ef252-121">AF \_ gleich</span><span class="sxs-lookup"><span data-stu-id="ef252-121">AF\_EQUAL</span></span>    | <span data-ttu-id="ef252-122">GL \_ gleich</span><span class="sxs-lookup"><span data-stu-id="ef252-122">GL\_EQUAL</span></span>    |
| <span data-ttu-id="ef252-123">AF- \_ lequal</span><span class="sxs-lookup"><span data-stu-id="ef252-123">AF\_LEQUAL</span></span>   | <span data-ttu-id="ef252-124">GL \_ lequal</span><span class="sxs-lookup"><span data-stu-id="ef252-124">GL\_LEQUAL</span></span>   |
| <span data-ttu-id="ef252-125">AF \_ größer</span><span class="sxs-lookup"><span data-stu-id="ef252-125">AF\_GREATER</span></span>  | <span data-ttu-id="ef252-126">GL \_ größer</span><span class="sxs-lookup"><span data-stu-id="ef252-126">GL\_GREATER</span></span>  |
| <span data-ttu-id="ef252-127">AF- \_ gequal</span><span class="sxs-lookup"><span data-stu-id="ef252-127">AF\_GEQUAL</span></span>   | <span data-ttu-id="ef252-128">GL \_ gequal</span><span class="sxs-lookup"><span data-stu-id="ef252-128">GL\_GEQUAL</span></span>   |



 

 

 




