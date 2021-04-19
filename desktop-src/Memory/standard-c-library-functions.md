---
description: Anwendungen können die Speicherverwaltungsfunktionen der C-Lauf Zeit Bibliothek (malloc, Free usw.) und C++ (neu, löschen usw.) sicher verwenden.
ms.assetid: c58ed263-577d-47c5-93cb-5a7c83604171
title: Standard-C-Bibliotheksfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303333b32f5645f19d8d22a072d25692cea4607f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349057"
---
# <a name="standard-c-library-functions"></a><span data-ttu-id="df178-103">Standard-C-Bibliotheksfunktionen</span><span class="sxs-lookup"><span data-stu-id="df178-103">Standard C Library Functions</span></span>

<span data-ttu-id="df178-104">Anwendungen können die Speicherverwaltungsfunktionen der C-Lauf Zeit Bibliothek (**malloc**, **Free** usw.) und C++ (**neu**, **Löschen** usw.) sicher verwenden.</span><span class="sxs-lookup"><span data-stu-id="df178-104">Applications can safely use the memory management features of the C run-time library (**malloc**, **free**, and so on) and C++ (**new**, **delete**, and so on).</span></span> <span data-ttu-id="df178-105">Die Funktionen der C-Lauf Zeit Bibliothek haben nicht die potenziellen Probleme, die Sie unter 16-Bit-Fenstern haben.</span><span class="sxs-lookup"><span data-stu-id="df178-105">The C run-time library functions do not have the potential problems they have under 16-bit Windows.</span></span> <span data-ttu-id="df178-106">Die Speicherverwaltung ist kein Problem mehr, da das System Arbeitsspeicher freigeben kann, indem Seiten des physischen Speichers verschoben werden, ohne dass sich dies auf die virtuellen Adressen auswirkt.</span><span class="sxs-lookup"><span data-stu-id="df178-106">Memory management is no longer a problem because the system is free to manage memory by moving pages of physical memory without affecting the virtual addresses.</span></span> <span data-ttu-id="df178-107">Ebenso ist der Unterschied zwischen Near-und Far-Zeigern nicht mehr relevant.</span><span class="sxs-lookup"><span data-stu-id="df178-107">Similarly, the distinction between near and far pointers is no longer relevant.</span></span> <span data-ttu-id="df178-108">Daher können Sie die Standard-C-Bibliotheksfunktionen für die Speicherverwaltung verwenden.</span><span class="sxs-lookup"><span data-stu-id="df178-108">Therefore, you can use the standard C library functions for memory management.</span></span> <span data-ttu-id="df178-109">Die Speicherverwaltungsfunktionen bieten jedoch Funktionen, die in der C-Lauf Zeit Bibliothek nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="df178-109">However, the memory management functions do provide functionality that is unavailable in the C run-time library.</span></span>

 

 



