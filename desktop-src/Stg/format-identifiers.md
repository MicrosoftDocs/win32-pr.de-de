---
title: Format Bezeichner
description: Eigenschafts Satz Werte werden in einem Abschnitt gespeichert, der mit einer eindeutigen fmtid gekennzeichnet ist.
ms.assetid: 3ffb6c5e-72ce-4769-847a-72db6f145d61
keywords:
- Format Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0202cd1287c3b4fef6e9e2b56e272541a03425b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309812"
---
# <a name="format-identifiers"></a><span data-ttu-id="15841-104">Format Bezeichner</span><span class="sxs-lookup"><span data-stu-id="15841-104">Format Identifiers</span></span>

<span data-ttu-id="15841-105">Eigenschafts Satz Werte werden in einem Abschnitt gespeichert, der mit einer eindeutigen fmtid gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="15841-105">Property set values are stored in a section tagged with a unique FMTID.</span></span> <span data-ttu-id="15841-106">Beispielsweise ist die fmtid für den Eigenschaften Satz für com-Zusammenfassungs Informationen **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.</span><span class="sxs-lookup"><span data-stu-id="15841-106">For example, the FMTID for the COM Summary Information property set is **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.</span></span>

<span data-ttu-id="15841-107">Zum Definieren einer fmtid für den Eigenschaften Satz für Zusammenfassungs Informationen verwenden Sie das **\_ GUID** -Makro definieren in einer Includedatei für den Code, der den Eigenschaften Satz bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="15841-107">To define a FMTID for the Summary Information property set, use the **DEFINE\_GUID** macro in an include file for the code that manipulates the property set.</span></span>


```C++
DEFINE_GUID(FMTID_SummaryInformation, 0xF29F85E0, 0x4FF9, 0x1068, 
0xAB, 0x91, 0x08, 0x00, 0x2B, 0x27, 0xB3, 0xD9);
```



<span data-ttu-id="15841-108">Sämtlicher Code, der die fmtid für den Eigenschaften Satz für Zusammenfassungs Informationen erfordert, kann über die *fmtid \_ SummaryInformation* -Variable darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="15841-108">Any code that requires the FMTID for the Summary Information property set, can access it through the *FMTID\_SummaryInformation* variable.</span></span>

<span data-ttu-id="15841-109">Beim Speichern von Eigenschafts Sätzen in [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Instanzen wird die fmtid in einen Zeichen folgen Namen für das Speicher Objekt konvertiert.</span><span class="sxs-lookup"><span data-stu-id="15841-109">When storing property sets in [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) instances, convert the FMTID to a string name for the storage object.</span></span>

 

 




