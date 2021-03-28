---
description: Jeder Monitor kann über eine eigene Farbtiefe verfügen.
ms.assetid: 8d1ba8d2-b43d-498d-be5a-100fe9fc0f61
title: Farben auf mehreren Anzeige Monitoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50410631cf0ea3ac0a1b9967f1116809be0a4851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959312"
---
# <a name="colors-on-multiple-display-monitors"></a><span data-ttu-id="121ff-103">Farben auf mehreren Anzeige Monitoren</span><span class="sxs-lookup"><span data-stu-id="121ff-103">Colors on Multiple Display Monitors</span></span>

<span data-ttu-id="121ff-104">Jeder Monitor kann über eine eigene Farbtiefe verfügen.</span><span class="sxs-lookup"><span data-stu-id="121ff-104">Each monitor can have its own color depth.</span></span> <span data-ttu-id="121ff-105">Das System passt Farben automatisch an, wenn Fenster über Monitore mit unterschiedlicher Farbtiefe bewegt werden.</span><span class="sxs-lookup"><span data-stu-id="121ff-105">The system automatically adjusts colors as windows move across monitors with different color depths.</span></span> <span data-ttu-id="121ff-106">Im allgemeinen ergibt dies gute Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="121ff-106">In general, this produces good results.</span></span> <span data-ttu-id="121ff-107">Dies ist jedoch nicht immer optimal.</span><span class="sxs-lookup"><span data-stu-id="121ff-107">However, this is not always optimal.</span></span> <span data-ttu-id="121ff-108">Wenn Sie die Farbfunktionen verschiedener Monitore nutzen möchten, finden Sie entsprechende Informationen im folgenden Abschnitt zeichnen [auf mehreren Anzeige Monitoren](painting-on-multiple-display-monitors.md) .</span><span class="sxs-lookup"><span data-stu-id="121ff-108">To take advantage of the color capabilities of different monitors, see the [Painting on Multiple Display Monitors](painting-on-multiple-display-monitors.md) section that follows.</span></span>

<span data-ttu-id="121ff-109">Um zu ermitteln, ob alle Monitore das gleiche Farb Format aufweisen, müssen Sie [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) mit SM \_ samedisplayformat aufrufen.</span><span class="sxs-lookup"><span data-stu-id="121ff-109">To determine if all monitors have the same color format, call [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_SAMEDISPLAYFORMAT.</span></span>

<span data-ttu-id="121ff-110">Wenn der primäre Monitor palettisiert ist, funktionieren [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) und [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) genauso wie zuvor, aber über alle Monitore hinweg.</span><span class="sxs-lookup"><span data-stu-id="121ff-110">If the primary monitor is palettized, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) and [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) work the same as before, but across all monitors.</span></span> <span data-ttu-id="121ff-111">Außerdem werden die Paletten aller palettengeräte synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="121ff-111">In addition, the palettes of all palettized devices are synchronized.</span></span> <span data-ttu-id="121ff-112">Wenn der primäre Monitor nicht palettisiert ist, wählen **SelectPalette** und **RealizePalette** die Palette im Hintergrund aus, und die Geräte werden nicht synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="121ff-112">If the primary monitor is not palettized, **SelectPalette** and **RealizePalette** will select the palette into the background and palettized devices will not be synchronized.</span></span>

 

 
