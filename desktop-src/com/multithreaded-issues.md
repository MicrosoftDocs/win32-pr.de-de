---
title: Multithread-Probleme
description: Multithread-Probleme
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0910e1602d00d3429bb9e4c7a1667bf8113cd659
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388821"
---
# <a name="multi-threaded-issues"></a><span data-ttu-id="7f3c6-103">Multithread-Probleme</span><span class="sxs-lookup"><span data-stu-id="7f3c6-103">Multi-Threaded Issues</span></span>

<span data-ttu-id="7f3c6-104">OLE bietet Unterstützung für Multithreadanwendungen und ermöglicht Anwendungen das Erstellen von OLE-aufrufen aus mehreren Threads.</span><span class="sxs-lookup"><span data-stu-id="7f3c6-104">OLE provides support for multithreaded applications, allowing applications to make OLE calls from multiple threads.</span></span> <span data-ttu-id="7f3c6-105">Diese Multithreadunterstützung wird als Apartment Modell bezeichnet. es ist wichtig, dass alle OLE-Komponenten, die mehrere Threads verwenden, diesem Modell folgen.</span><span class="sxs-lookup"><span data-stu-id="7f3c6-105">This multithreaded support is called the apartment model, it is important that all OLE components using multiple threads follow this model.</span></span> <span data-ttu-id="7f3c6-106">Das Apartment Modell erfordert, dass Schnittstellen Zeiger gemarshallt werden (mithilfe von " [**comarshalinterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)" und " [**framarshalinterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)"), wenn Sie zwischen Threads übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="7f3c6-106">The apartment model requires that interface pointers are marshaled (using [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface), and [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) when passed between threads.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f3c6-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7f3c6-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f3c6-108">Prozesse, Threads und Apartments</span><span class="sxs-lookup"><span data-stu-id="7f3c6-108">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> </dl>

 

 




