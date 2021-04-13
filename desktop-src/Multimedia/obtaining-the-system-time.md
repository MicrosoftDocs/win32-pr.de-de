---
title: Abrufen der System Zeit
description: Abrufen der System Zeit
ms.assetid: 33dfcd56-11d9-45b9-b983-8354526101a7
keywords:
- Multimedia-Timer, Systemzeit
- Timer, Systemzeit
- Systemuhrzeit
- timeGetTime-Funktion
- timegetsystemtime-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89fdcc905569a500afe689658676137c460d19d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472820"
---
# <a name="obtaining-the-system-time"></a><span data-ttu-id="2b977-108">Abrufen der System Zeit</span><span class="sxs-lookup"><span data-stu-id="2b977-108">Obtaining the System Time</span></span>

<span data-ttu-id="2b977-109">Bevor eine Anwendung mit der Verwendung der Multimediatimer-Dienste beginnt, wird in der Regel die aktuelle *Systemzeit* abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2b977-109">Typically, before an application begins using the multimedia timer services, it retrieves the current *system time*.</span></span> <span data-ttu-id="2b977-110">Die Systemzeit ist die Zeit (in Millisekunden), seit der das Microsoft Windows-Betriebssystem gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="2b977-110">The system time is the time, in milliseconds, since the Microsoft Windows operating system was started.</span></span> <span data-ttu-id="2b977-111">Sie können die [**timeGetTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) -Funktion oder die [**timegetsystemtime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) -Funktion verwenden, um die Systemzeit abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2b977-111">You can use the [**timeGetTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) or [**timeGetSystemTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) function to retrieve the system time.</span></span> <span data-ttu-id="2b977-112">Diese beiden Funktionen sind sehr ähnlich: **timeGetTime** gibt die Systemzeit zurück, und **timegetsystemtime** füllt eine [**mmtime**](/previous-versions//dd757347(v=vs.85)) -Struktur mit der Systemzeit.</span><span class="sxs-lookup"><span data-stu-id="2b977-112">These two functions are very similar: **timeGetTime** returns the system time, and **timeGetSystemTime** fills an [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure with the system time.</span></span>

 

 