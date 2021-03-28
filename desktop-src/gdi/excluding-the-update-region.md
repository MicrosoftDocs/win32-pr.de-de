---
description: Die excludeupdatergn-Funktion schließt den Aktualisierungs Bereich aus dem Clippingbereich für den Anzeigegeräte Kontext aus.
ms.assetid: e652122b-a3b7-4d1b-8afd-9648d5ee3d42
title: Ausschließen der Update Region
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7be39b948e61fc06c7f7005d15c1163cef0068f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041970"
---
# <a name="excluding-the-update-region"></a><span data-ttu-id="f55dd-103">Ausschließen der Update Region</span><span class="sxs-lookup"><span data-stu-id="f55dd-103">Excluding the Update Region</span></span>

<span data-ttu-id="f55dd-104">Die [**excludeupdatergn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn) -Funktion schließt den Aktualisierungs Bereich aus dem Clippingbereich für den Anzeigegeräte Kontext aus.</span><span class="sxs-lookup"><span data-stu-id="f55dd-104">The [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn) function excludes the update region from the clipping region for the display device context.</span></span> <span data-ttu-id="f55dd-105">Diese Funktion ist nützlich, wenn in einem anderen Fenster gezeichnet wird, als wenn eine WM-Zeichnungs \_ Nachricht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="f55dd-105">This function is useful when drawing in a window other than when a WM\_PAINT message is processing.</span></span> <span data-ttu-id="f55dd-106">Es verhindert das Zeichnen in den Bereichen, die während der nächsten WM Paint-Meldung aktualisiert werden \_ .</span><span class="sxs-lookup"><span data-stu-id="f55dd-106">It prevents drawing in the areas that will be updated during the next WM\_PAINT message.</span></span>

 

 



