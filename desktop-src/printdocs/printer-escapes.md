---
description: Die Drucker Escapezeichen werden von Windows-Geräten mit 16-Bit-Zugriff auf spezielle Geräte bereitgestellt.
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: Drucker Escapezeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59463c4201e97c5ac1ec689a772581fab28314b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216631"
---
# <a name="printer-escapes"></a><span data-ttu-id="e6656-103">Drucker Escapezeichen</span><span class="sxs-lookup"><span data-stu-id="e6656-103">Printer Escapes</span></span>

<span data-ttu-id="e6656-104">Die Drucker Escapezeichen werden von Windows-Geräten mit 16-Bit-Zugriff auf spezielle Geräte bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e6656-104">The printer escapes provided by 16-bit Windows allowed access special device features.</span></span> <span data-ttu-id="e6656-105">Die meisten dieser Escapezeichen sind veraltet, aber einige werden bereitgestellt, um das Portieren von Windows-basierten 16-Bit-Anwendungen zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="e6656-105">Most of these escapes are obsolete, but a few are provided to simplify the porting of 16-bit Windows-based applications.</span></span> <span data-ttu-id="e6656-106">GDI unterstützt einen kompletten Satz von Pfad Funktionen, die von Anwendungen anstelle der Escapezeichen zum Zeichnen von Pfaden auf beliebigen Geräten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e6656-106">GDI supports a complete set of path functions that applications can use instead of the escapes to draw paths on any device.</span></span> <span data-ttu-id="e6656-107">Eine Liste der Funktionen, die einige der Escapezeichen ersetzen, finden Sie in der [**Escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e6656-107">For a list of functions that replace some of the escapes, see the [**Escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) function.</span></span>

<span data-ttu-id="e6656-108">Von den 64 ursprünglichen Drucker Escapezeichen können nur **queryescsupport** und **Passthrough** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6656-108">Of the 64 original printer escapes, only **QUERYESCSUPPORT** and **PASSTHROUGH** can be used.</span></span>

<span data-ttu-id="e6656-109">Es ist auch eine erweiterte escapefunktion mit dem Namen " [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)" vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e6656-109">There is also an extended escape function called [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span> <span data-ttu-id="e6656-110">Diese Funktion ermöglicht Anwendungen den Zugriff auf Funktionen eines bestimmten Geräts, das nicht direkt über GDI verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e6656-110">This function allows applications to access capabilities of a particular device not directly available through GDI.</span></span>

 

 



