---
description: Im Allgemeinen benötigen ältere Anwendungen keine Änderungen, die auf mehreren Überwachungssystemen funktionieren.
ms.assetid: 908cf88c-69ed-4855-817d-ba749e14ff85
title: Überlegungen zu mehreren überwachen für ältere Programme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feebb356cb2f9c5480c84f1718b51d6e866ef621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978521"
---
# <a name="multiple-monitor-considerations-for-older-programs"></a><span data-ttu-id="fa49d-103">Überlegungen zu mehreren überwachen für ältere Programme</span><span class="sxs-lookup"><span data-stu-id="fa49d-103">Multiple Monitor Considerations for Older Programs</span></span>

<span data-ttu-id="fa49d-104">Im Allgemeinen benötigen ältere Anwendungen keine Änderungen, die auf mehreren Überwachungssystemen funktionieren.</span><span class="sxs-lookup"><span data-stu-id="fa49d-104">Generally, older applications do not need changes to work on multiple monitor systems.</span></span> <span data-ttu-id="fa49d-105">In den meisten Fällen scheint das System nur eine Anzeige zu haben.</span><span class="sxs-lookup"><span data-stu-id="fa49d-105">For most, the system will appear to have only one display.</span></span> <span data-ttu-id="fa49d-106">Systemmetriken spiegeln die primäre Anzeige und Vollbild-Anwendungen auf dem primären Replikat wider.</span><span class="sxs-lookup"><span data-stu-id="fa49d-106">System metrics reflect the primary display and fullscreen applications show up on the primary.</span></span> <span data-ttu-id="fa49d-107">Das System verarbeitet Minimierung, Maximierung, Menüs und Dialogfelder.</span><span class="sxs-lookup"><span data-stu-id="fa49d-107">The system handles minimization, maximization, menus, and dialog boxes.</span></span>

<span data-ttu-id="fa49d-108">Bei einigen Programmen treten jedoch Probleme auf.</span><span class="sxs-lookup"><span data-stu-id="fa49d-108">However, some programs will have problems.</span></span> <span data-ttu-id="fa49d-109">Bei einigen, die Probleme haben können, handelt es sich um Remote Steuerungsanwendungen, die über direkten Hardware Zugriff verfügen, und um solche, die den GDI oder Anzeigetreiber gepatcht haben.</span><span class="sxs-lookup"><span data-stu-id="fa49d-109">Some that could have problems are remote control applications, those that have direct hardware access, and those that have patched the GDI or DISPLAY driver.</span></span> <span data-ttu-id="fa49d-110">In diesen Fällen muss der Benutzer möglicherweise einen Monitor über den primären Monitor hinaus deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="fa49d-110">In these cases, the user may be required to disable any monitor beyond the primary monitor.</span></span>

 

 



