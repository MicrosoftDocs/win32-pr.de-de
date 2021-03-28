---
description: Das System behandelt Farben in Bitmaps anders als Farben in den Stiften, Pinseln und Text.
ms.assetid: c315dd6e-87ee-4905-b193-186ea580ac0a
title: Farbe in Bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 834744f35ccc8bd0c8714fa5bbb438b59c8b8db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130817"
---
# <a name="color-in-bitmaps"></a><span data-ttu-id="4fd4d-103">Farbe in Bitmaps</span><span class="sxs-lookup"><span data-stu-id="4fd4d-103">Color in Bitmaps</span></span>

<span data-ttu-id="4fd4d-104">Das System behandelt Farben in Bitmaps anders als Farben in den Stiften, Pinseln und Text.</span><span class="sxs-lookup"><span data-stu-id="4fd4d-104">The system handles colors in bitmaps differently than colors in pens, brushes, and text.</span></span> <span data-ttu-id="4fd4d-105">Kompatible Bitmaps, die mithilfe der Funktion "up- [**Bitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) " oder der Funktion " [**kreatecompatiblebitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) " erstellt wurden, sind gerätespezifisch und behalten Farbinformationen in einem geräteabhängigen Format bei.</span><span class="sxs-lookup"><span data-stu-id="4fd4d-105">Compatible bitmaps, created by using the [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) or [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) function, are device specific and retain color information in a device-dependent format.</span></span> <span data-ttu-id="4fd4d-106">Es werden keine Farbwerte verwendet, und die Farben unterliegen keinem Näherungs-und Dithering.</span><span class="sxs-lookup"><span data-stu-id="4fd4d-106">No color values are used, and the colors are not subject to approximations and dithering.</span></span>

<span data-ttu-id="4fd4d-107">Geräteunabhängige Bitmaps (Disb) behalten Farbinformationen entweder als Farbwerte oder Farb palettenindizes bei.</span><span class="sxs-lookup"><span data-stu-id="4fd4d-107">Device-independent bitmaps (DIBs) retain color information either as color values or color palette indexes.</span></span> <span data-ttu-id="4fd4d-108">Wenn Farbwerte verwendet werden, unterliegen die Farben Näherungs-, aber nicht Dithering.</span><span class="sxs-lookup"><span data-stu-id="4fd4d-108">If color values are used, the colors are subject to approximation, but not dithering.</span></span> <span data-ttu-id="4fd4d-109">Farbpalette-Indizes können nur mit Geräten verwendet werden, die Farbpaletten unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4fd4d-109">Color palette indexes can only be used with devices that support color palettes.</span></span> <span data-ttu-id="4fd4d-110">Obwohl das System keine Näherungs-oder Dithering Farben durch Indizes identifiziert, kann sich die resultierende Farbe von der vorgesehenen Farbe unterscheiden, da die Indizes gültige Ergebnisse nur im Kontext der Farbpalette ergeben, der zum Zeitpunkt der Erstellung der Bitmap aktuell war.</span><span class="sxs-lookup"><span data-stu-id="4fd4d-110">Although the system does not approximate or dither colors identified by indexes, the resulting color may be different than that intended, because the indexes yield valid results only in the context of the color palette that was current at the time the bitmap was created.</span></span> <span data-ttu-id="4fd4d-111">Wenn die Palette geändert wird, ändern Sie die Farben in der Bitmap.</span><span class="sxs-lookup"><span data-stu-id="4fd4d-111">If the palette changes, so do the colors in the bitmap.</span></span> <span data-ttu-id="4fd4d-112">Weitere Informationen zu palettenindizes finden Sie unter " [Standardpalette](default-palette.md) " und " [**paletteindex**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex)".</span><span class="sxs-lookup"><span data-stu-id="4fd4d-112">For more information on palette indexes, see [Default Palette](default-palette.md) and [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex).</span></span>

<span data-ttu-id="4fd4d-113">Zusätzlich zum Verweisen auf die logische Palette kann eine Anwendung auch auf einen Wert in einer DIB-Farbtabelle verweisen.</span><span class="sxs-lookup"><span data-stu-id="4fd4d-113">In addition to referencing the logical palette, an application can also reference a value in a DIB color table.</span></span> <span data-ttu-id="4fd4d-114">Um eine Farbe in einer DIB-Farbtabelle auszuwählen, nennen Sie [**dibindex**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex).</span><span class="sxs-lookup"><span data-stu-id="4fd4d-114">To select a color in a DIB color table, call [**DIBINDEX**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex).</span></span> <span data-ttu-id="4fd4d-115">Beachten Sie, dass dies nur für einen Gerätekontext möglich ist, für den ein DIB ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="4fd4d-115">Note that this is only possible for a device context that has a DIB selected into it.</span></span>

 

 



