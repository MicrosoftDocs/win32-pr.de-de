---
description: Die "Select"-Funktion in der ursprünglichen "Berkeley Software Distribution (BSD)"-Socketschnittstelle war das standardmäßige (und einzige) Mittel zum Abrufen von Netzwerk Ereignis hinweisen.
ms.assetid: f7f42b03-1f89-4801-abf0-396ff8b61cae
title: Wählt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e50339f298c18c75ad6451590f191fc1bd8afba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356626"
---
# <a name="selects"></a><span data-ttu-id="2e916-103">Wählt</span><span class="sxs-lookup"><span data-stu-id="2e916-103">Selects</span></span>

<span data-ttu-id="2e916-104">Die " [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) "-Funktion in der ursprünglichen "Berkeley Software Distribution (BSD)"-Socketschnittstelle war das standardmäßige (und einzige) Mittel zum Abrufen von Netzwerk Ereignis hinweisen.</span><span class="sxs-lookup"><span data-stu-id="2e916-104">In the original Berkeley Software Distribution (BSD) socket interface the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) function was the standard (and only) means to obtain network event indications.</span></span> <span data-ttu-id="2e916-105">Für jeden Socket können Informationen zu Lese-, Schreib-oder Fehlerstatus abgerufen oder gewartet werden.</span><span class="sxs-lookup"><span data-stu-id="2e916-105">For each socket, information on read, write, or error status can be polled or waited on.</span></span> <span data-ttu-id="2e916-106">Weitere Informationen finden [**Sie unter wspselect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2e916-106">See [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) for more information.</span></span> <span data-ttu-id="2e916-107">Beachten Sie, dass das Netzwerk Ereignis FD- \_ QoS von diesem Ansatz nicht abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="2e916-107">Note that network event FD\_QOS cannot be obtained by this approach.</span></span>

 

 
