---
description: Die isearchjob-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 9e1675e9-fe40-4209-aba9-1cabb4f3ea4c
title: Isearchjob-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5c49a5af7435819750451c89ca68f976d76f13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129637"
---
# <a name="isearchjob-properties"></a><span data-ttu-id="a1f4e-103">Isearchjob-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1f4e-103">ISearchJob Properties</span></span>

<span data-ttu-id="a1f4e-104">Die [**isearchjob**](/windows/desktop/api/Wuapi/nn-wuapi-isearchjob) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a1f4e-104">The [**ISearchJob**](/windows/desktop/api/Wuapi/nn-wuapi-isearchjob) interface defines the following properties.</span></span>



| <span data-ttu-id="a1f4e-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a1f4e-105">Property</span></span>                                      | <span data-ttu-id="a1f4e-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1f4e-106">Description</span></span>                                                                                                                                                 |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1f4e-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="a1f4e-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-get_asyncstate)   | <span data-ttu-id="a1f4e-108">Ruft das aufruferspezifische Zustands Objekt ab, das an die [**iupdatesearch. beginsearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) -Methode übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a1f4e-108">Gets the caller-specific state object that is passed to the [**IUpdateSearch.BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) method.</span></span>                         |
| [<span data-ttu-id="a1f4e-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="a1f4e-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-get_iscompleted) | <span data-ttu-id="a1f4e-110">Ruft einen booleschen Wert ab, der angibt, ob der Aufrufen der [**iupdatesearch. beginsearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) -Methode vollständig verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="a1f4e-110">Gets a Boolean value that indicates whether the call to the [**IUpdateSearch.BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) method is completely processed.</span></span> |



 

 

 



