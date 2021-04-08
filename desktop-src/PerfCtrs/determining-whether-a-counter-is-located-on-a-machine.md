---
description: Wenn Sie ermitteln möchten, ob ein-Wert auf einem bestimmten Computer installiert ist, nennen Sie pdhvalidatepath mit dem voll qualifizierten Counter-Pfad. Die Funktion gibt einen Fehler Erfolg zurück, \_ Wenn sich der gegen Computer auf dem angegebenen Computer befindet.
ms.assetid: 5533a8d8-3621-4ce7-984c-c3895adef531
title: Ermitteln, ob sich ein gegen Computer auf einem Computer befindet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795878e2f9c97989fe924737ec7f8e7f14bdc67c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959765"
---
# <a name="determining-whether-a-counter-is-located-on-a-computer"></a><span data-ttu-id="68fab-104">Ermitteln, ob sich ein gegen Computer auf einem Computer befindet</span><span class="sxs-lookup"><span data-stu-id="68fab-104">Determining Whether a Counter Is Located on a Computer</span></span>

<span data-ttu-id="68fab-105">Wenn Sie ermitteln möchten, ob ein-Wert auf einem bestimmten Computer installiert ist, nennen Sie [**pdhvalidatepath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) mit dem voll qualifizierten Counter-Pfad.</span><span class="sxs-lookup"><span data-stu-id="68fab-105">To determine if a counter is installed on a particular computer, call [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) with the fully qualified counter path.</span></span> <span data-ttu-id="68fab-106">Die Funktion gibt einen Fehler Erfolg zurück, \_ Wenn sich der gegen Computer auf dem angegebenen Computer befindet.</span><span class="sxs-lookup"><span data-stu-id="68fab-106">The function returns ERROR\_SUCCESS if the counter is located on the specified computer.</span></span>

<span data-ttu-id="68fab-107">[**Pdhvalidatepath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) überprüft den gesamten Pfad. Daher gibt der Rückgabewert an, wenn ein Objekt, eine Instanz oder ein Leistungs Bezeichner im Pfad nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="68fab-107">[**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) validates the entire path; therefore, if any object, instance, or counter in the path does not exist, the return value indicates so.</span></span> <span data-ttu-id="68fab-108">**Pdhvalidatepath** überprüft den angegebenen Leistungswert Pfad in dieser Reihenfolge: Computer, Leistungs Objekt, Instanz und Leistungsdaten.</span><span class="sxs-lookup"><span data-stu-id="68fab-108">**PdhValidatePath** verifies the specified counter path in this order: computer, performance object, instance, and counter.</span></span>

 

 



