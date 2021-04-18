---
description: WIA stellt eine TWAIN-Kompatibilitäts Ebene bereit, die es TWAIN-fähigen Anwendungen ermöglicht, mit Windows-Abbild Erfassungs Geräten (WIA) zu kommunizieren.
ms.assetid: 8e5673b9-c234-4722-b244-41aae015ac0c
title: TWAIN-Kompatibilität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afc7d0beb9a6001a0cbb4dc0bc032cf4df781736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347192"
---
# <a name="twain-compatibility"></a><span data-ttu-id="e961c-103">TWAIN-Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="e961c-103">TWAIN Compatibility</span></span>

<span data-ttu-id="e961c-104">WIA stellt eine TWAIN-Kompatibilitäts Ebene bereit, die es TWAIN-fähigen Anwendungen ermöglicht, mit Windows-Abbild Erfassungs Geräten (WIA) zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="e961c-104">WIA provides a TWAIN compatibility layer that allows TWAIN-aware applications to communicate with Windows Image Acquisition (WIA) devices.</span></span> <span data-ttu-id="e961c-105">TWAIN-kompatible Anwendungen haben keinen vollständigen Zugriff auf die WIA-Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="e961c-105">TWAIN-aware applications do not have full access to WIA functionality.</span></span> <span data-ttu-id="e961c-106">Beispielsweise kann eine Anwendung die Benutzeroberfläche nicht mithilfe der TWAIN-Kompatibilitätsschicht unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="e961c-106">For example, an application cannot suppress the user interface using the TWAIN compatibility layer.</span></span>

<span data-ttu-id="e961c-107">WIA-Geräte werden zweimal für eine Anwendung angezeigt, die sowohl WIA als auch TWAIN kennt: einmal durch normale WIA-Kommunikation und einmal über die TWAIN-Kompatibilitätsschicht.</span><span class="sxs-lookup"><span data-stu-id="e961c-107">WIA devices appear twice to an application that is aware of both WIA and TWAIN: once through normal WIA communication, and once through the TWAIN compatibility layer.</span></span> <span data-ttu-id="e961c-108">Um das doppelte Auflisten eines WIA-Geräts zu vermeiden, muss eine Anwendung, die sowohl WIA als auch TWAIN kennt, die WIA-Geräte herausfiltern, die über die TWAIN-Kompatibilitätsschicht kommen.</span><span class="sxs-lookup"><span data-stu-id="e961c-108">To avoid listing a WIA device twice, an application that is aware of both WIA and TWAIN must filter out the WIA devices that come through the TWAIN compatibility layer.</span></span> <span data-ttu-id="e961c-109">Alle WIA-Geräte, die die TWAIN-Kompatibilitätsschicht durchlaufen, haben "WIA-" als Präfix, sodass Sie leicht gefiltert werden können.</span><span class="sxs-lookup"><span data-stu-id="e961c-109">All WIA devices that come through the TWAIN compatibility layer have "WIA-" as a prefix, so it is easy to filter them.</span></span>

 

 



