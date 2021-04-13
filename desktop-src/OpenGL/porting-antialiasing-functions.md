---
title: Portieren von Antialiasing-Funktionen
description: Portieren von Antialiasing-Funktionen
ms.assetid: 7f79f0fa-4a08-4678-bc73-8611e8d9e91a
keywords:
- IRIS GL portieren, Antialiasing
- Portieren von IRIS GL, Antialiasing
- Portieren auf OpenGL von IRIS GL, Antialiasing
- OpenGL-Portierung von IRIS GL, Antialiasing
- Antialiasing (antialiasing)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec2fcae4fe7b6909e00efb0fb892821a5c12765
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388731"
---
# <a name="porting-antialiasing-functions"></a><span data-ttu-id="7dd85-108">Portieren von Antialiasing-Funktionen</span><span class="sxs-lookup"><span data-stu-id="7dd85-108">Porting Antialiasing Functions</span></span>

<span data-ttu-id="7dd85-109">In OpenGL ist der subpixelmodus immer eingeschaltet. Folglich ist das IRIS GL- **funktionssubpixel**(**true**) nicht erforderlich und hat keine OpenGL-Entsprechung.</span><span class="sxs-lookup"><span data-stu-id="7dd85-109">In OpenGL the subpixel mode is always on, consequently the IRIS GL function **subpixel**(**TRUE**) is not necessary and has no OpenGL equivalent.</span></span> <span data-ttu-id="7dd85-110">In den folgenden Themen werden Aspekte der Portierung von IRIS GL-Antialiasing-Code beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7dd85-110">The following topics describe aspects of porting IRIS GL antialiasing code.</span></span>

-   [<span data-ttu-id="7dd85-111">Portieren von Mischungs Code</span><span class="sxs-lookup"><span data-stu-id="7dd85-111">Porting Blending Code</span></span>](porting-blending-code.md)
-   [<span data-ttu-id="7dd85-112">Portieren von Test Funktionen</span><span class="sxs-lookup"><span data-stu-id="7dd85-112">Porting afunction Test Functions</span></span>](porting-afunction-test-functions.md)
-   [<span data-ttu-id="7dd85-113">Verwenden von Antialiasing-Funktionen</span><span class="sxs-lookup"><span data-stu-id="7dd85-113">Using Antialiasing Functions</span></span>](using-antialiasing-functions.md)

 

 




