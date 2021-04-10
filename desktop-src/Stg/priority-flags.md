---
title: Prioritätsflags
description: Das Prioritäts Kennzeichen öffnet ein Speicher Objekt im Prioritäts Modus.
ms.assetid: 85f2df6f-9219-4752-8c17-f219c37a4037
keywords:
- Prioritätsflags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f4af04174ddb6c0ac459a6f7e6841e061b03c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037645"
---
# <a name="priority-flags"></a><span data-ttu-id="21c61-104">Prioritätsflags</span><span class="sxs-lookup"><span data-stu-id="21c61-104">Priority Flags</span></span>

<span data-ttu-id="21c61-105">Das Prioritäts Kennzeichen öffnet ein Speicher Objekt im Prioritäts Modus.</span><span class="sxs-lookup"><span data-stu-id="21c61-105">The priority flag opens a storage object in priority mode.</span></span> <span data-ttu-id="21c61-106">Wenn ein Objekt geöffnet wird, kann eine Anwendung in der Regel mit einer Momentaufnahme Kopie verwendet werden, da andere Anwendungen möglicherweise auch das Objekt gleichzeitig verwenden.</span><span class="sxs-lookup"><span data-stu-id="21c61-106">When it opens an object, an application usually works from a snapshot copy because other applications may also be using the object at the same time.</span></span> <span data-ttu-id="21c61-107">Wenn Sie ein Speicher Objekt im Prioritäts Modus öffnen, verfügt die Anwendung jedoch über exklusive Rechte, um Änderungen am Objekt zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="21c61-107">When opening a storage object in priority mode, however, the application has exclusive rights to commit changes to the object.</span></span>

<span data-ttu-id="21c61-108">Der Prioritäts Modus ermöglicht einer Anwendung, einige Datenströme aus dem Speicher zu lesen, bevor das Objekt in einem Modus geöffnet wird, in dem das System eine Momentaufnahme Kopie erstellen muss.</span><span class="sxs-lookup"><span data-stu-id="21c61-108">Priority mode enables an application to read some streams from storage before opening the object in a mode that would require the system to make a snapshot copy.</span></span> <span data-ttu-id="21c61-109">Da die Anwendung exklusiven Zugriff hat, muss Sie keine Momentaufnahme Kopie des-Objekts erstellen.</span><span class="sxs-lookup"><span data-stu-id="21c61-109">Because the application has exclusive access, it does not have to make a snapshot copy of the object.</span></span> <span data-ttu-id="21c61-110">Wenn die Anwendung das Objekt anschließend in einem Modus öffnet, in dem eine Momentaufnahme Kopie erforderlich ist, kann die Anwendung die Datenströme ausschließen, die Sie bereits aus der Momentaufnahme gelesen hat, wodurch der Aufwand für das Öffnen des Objekts reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="21c61-110">When the application subsequently opens the object in a mode where a snapshot copy is required, the application can exclude the streams it has already read from the snapshot, thereby reducing the overhead of opening the object.</span></span>

<span data-ttu-id="21c61-111">Da andere Anwendungen keine Änderungen an einem Objekt ausführen können, während es im Prioritäts Modus geöffnet ist, sollten Anwendungen das Objekt so kurz wie möglich in diesem Modus belassen.</span><span class="sxs-lookup"><span data-stu-id="21c61-111">Because other applications cannot commit changes to an object while it is open in priority mode, applications should keep the object in that mode for as short a time as possible.</span></span>

 

 




