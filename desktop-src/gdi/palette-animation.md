---
description: Die Palette-Animation ist eine Technik zum Simulieren von Bewegung, indem die Farben ausgewählter Einträge in einer Farbpalette schnell geändert werden.
ms.assetid: fc5b8061-fd4f-4751-883d-877fa32cdfcc
title: Palette-Animation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9761e99033e7a01fa875fce7c41e5a35cf40ab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754337"
---
# <a name="palette-animation"></a><span data-ttu-id="106a4-103">Palette-Animation</span><span class="sxs-lookup"><span data-stu-id="106a4-103">Palette Animation</span></span>

<span data-ttu-id="106a4-104">Die Palette-Animation ist eine Technik zum Simulieren von Bewegung, indem die Farben ausgewählter Einträge in einer Farbpalette schnell geändert werden.</span><span class="sxs-lookup"><span data-stu-id="106a4-104">Palette animation is a technique to simulate motion by rapidly changing the colors of selected entries in a color palette.</span></span> <span data-ttu-id="106a4-105">Eine Anwendung kann eine palettenanimation durchführen, indem Sie eine logische Palette erstellt, die "reservierte" Einträge enthält, und dann die [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) -Funktion verwenden, um die Farben in diesen reservierten Einträgen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="106a4-105">An application can carry out palette animation by creating a logical palette that contains "reserved" entries and then using the [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) function to change colors in those reserved entries.</span></span>

<span data-ttu-id="106a4-106">Eine Anwendung erstellt einen reservierten Eintrag in einer logischen Palette durch Festlegen des **pfflags** -Members der [**PaletteEntry**](/previous-versions//dd162769(v=vs.85)) -Struktur auf das \_ reservierte PC-Flag.</span><span class="sxs-lookup"><span data-stu-id="106a4-106">An application creates a reserved entry in a logical palette by setting the **peFlags** member of the [**PALETTEENTRY**](/previous-versions//dd162769(v=vs.85)) structure to the PC\_RESERVED flag.</span></span> <span data-ttu-id="106a4-107">Nachdem diese logische Palette ausgewählt und erkannt wurde, kann die Anwendung die [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) -Funktion zum Ändern von mindestens einem reservierten Eintrag aufruft.</span><span class="sxs-lookup"><span data-stu-id="106a4-107">Once this logical palette is selected and realized, the application can call the [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) function to change one or more reserved entries.</span></span> <span data-ttu-id="106a4-108">Wenn die angegebene Palette dem aktiven Fenster zugeordnet ist, aktualisiert das System die Farben auf dem Bildschirm sofort.</span><span class="sxs-lookup"><span data-stu-id="106a4-108">If the given palette is associated with the active window, the system updates the colors on the screen immediately.</span></span>

 

 
