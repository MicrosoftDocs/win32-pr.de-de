---
description: Microsoft Image Color Management (ICM) stellt sicher, dass ein Farbbild, ein Grafik Objekt oder Textobjekt so nah wie möglich an die ursprüngliche Absicht auf jedem Gerät gerendert wird, trotz der Unterschiede bei den Abbild Erstellungs Technologien und Farbfunktionen zwischen Geräten.
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: ICM-Enabled Bitmap-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b89dac569aafad1ef94b066bc97f588bac62c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863639"
---
# <a name="icm-enabled-bitmap-functions"></a><span data-ttu-id="e28b6-103">ICM-Enabled Bitmap-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e28b6-103">ICM-Enabled Bitmap Functions</span></span>

<span data-ttu-id="e28b6-104">Microsoft Image Color Management (ICM) stellt sicher, dass ein Farbbild, ein Grafik Objekt oder Textobjekt so nah wie möglich an die ursprüngliche Absicht auf jedem Gerät gerendert wird, trotz der Unterschiede bei den Abbild Erstellungs Technologien und Farbfunktionen zwischen Geräten.</span><span class="sxs-lookup"><span data-stu-id="e28b6-104">Microsoft Image Color Management (ICM) ensures that a color image, graphic object, or text object is rendered as closely as possible to its original intent on any device, despite differences in imaging technologies and color capabilities between devices.</span></span> <span data-ttu-id="e28b6-105">Unabhängig davon, ob Sie ein Bild oder eine andere Grafik auf einem Farbscanner Scannen, es über das Internet herunterladen, auf dem Bildschirm anzeigen oder bearbeiten oder es auf Papier-, Film-oder anderen Medien drucken, unterstützt Sie ICM 2,0 dabei, Farben konsistent und genau zu halten.</span><span class="sxs-lookup"><span data-stu-id="e28b6-105">Whether you are scanning an image or other graphic on a color scanner, downloading it over the Internet, viewing or editing it onscreen, or printing it on paper, film, or other media, ICM 2.0 helps you keep colors consistent and accurate.</span></span> <span data-ttu-id="e28b6-106">Weitere Informationen zu ICM finden Sie unter [Windows Color System](/previous-versions//dd372446(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e28b6-106">For more information about ICM, see [Windows Color System](/previous-versions//dd372446(v=vs.85)).</span></span>

<span data-ttu-id="e28b6-107">Es gibt verschiedene Funktionen in der Graphics Device Interface (GDI), die Farbdaten verwenden oder verwenden.</span><span class="sxs-lookup"><span data-stu-id="e28b6-107">There are various functions in the graphics device interface (GDI) that use or operate on color data.</span></span> <span data-ttu-id="e28b6-108">Die folgenden bitmapfunktionen sind für die Verwendung mit ICM aktiviert:</span><span class="sxs-lookup"><span data-stu-id="e28b6-108">The following bitmap functions are enabled for use with ICM:</span></span>

-   [<span data-ttu-id="e28b6-109">**BitBLT**</span><span class="sxs-lookup"><span data-stu-id="e28b6-109">**BitBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)
-   [<span data-ttu-id="e28b6-110">**"Kreatedibitmap"**</span><span class="sxs-lookup"><span data-stu-id="e28b6-110">**CreateDIBitmap**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)
-   [<span data-ttu-id="e28b6-111">**"Kreatedibsection"**</span><span class="sxs-lookup"><span data-stu-id="e28b6-111">**CreateDIBSection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)
-   [<span data-ttu-id="e28b6-112">**MaskBlt**</span><span class="sxs-lookup"><span data-stu-id="e28b6-112">**MaskBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)
-   [<span data-ttu-id="e28b6-113">**Setdibcolortable**</span><span class="sxs-lookup"><span data-stu-id="e28b6-113">**SetDIBColorTable**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)
-   [<span data-ttu-id="e28b6-114">**StretchBlt**</span><span class="sxs-lookup"><span data-stu-id="e28b6-114">**StretchBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)
-   [<span data-ttu-id="e28b6-115">**SetDIBits**</span><span class="sxs-lookup"><span data-stu-id="e28b6-115">**SetDIBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)
-   [<span data-ttu-id="e28b6-116">**SetDIBitsToDevice**</span><span class="sxs-lookup"><span data-stu-id="e28b6-116">**SetDIBitsToDevice**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)
-   [<span data-ttu-id="e28b6-117">**StretchDIBits**</span><span class="sxs-lookup"><span data-stu-id="e28b6-117">**StretchDIBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

 

 
