---
description: Um eine Bitmap zu erstellen, verwenden Sie die Funktionen "up", "kreatebitmap", "up" oder "kreatecompatiblebitmap", "kreatedibitmap" und "kreateverwerdablebitmap".
ms.assetid: 313072fc-68c9-4ece-95bb-2748ccbd7f57
title: Bitmap-Erstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00a0bc5a39d1b5e6053a34a87c28d6792a42b0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215219"
---
# <a name="bitmap-creation"></a><span data-ttu-id="c28b2-103">Bitmap-Erstellung</span><span class="sxs-lookup"><span data-stu-id="c28b2-103">Bitmap Creation</span></span>

<span data-ttu-id="c28b2-104">Um eine Bitmap zu erstellen, verwenden [**Sie die Funktionen**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)"up", "kreatebitmap", "up" oder [](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)" [**kreatecompatiblebitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) ", " [**kreatedibitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)" und " [**kreateverwerdablebitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap)".</span><span class="sxs-lookup"><span data-stu-id="c28b2-104">To create a bitmap, use the [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect), or [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) function, [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap), and [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).</span></span>

<span data-ttu-id="c28b2-105">Mit diesen Funktionen können Sie die Breite und Höhe der Bitmap in Pixel angeben.</span><span class="sxs-lookup"><span data-stu-id="c28b2-105">These functions allow you to specify the width and height, in pixels, of the bitmap.</span></span> <span data-ttu-id="c28b2-106">Mit der Funktion "up- [**Bitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) " und der Funktion " [**kreatebitmapindirekte**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) " können Sie auch die Anzahl von Farbebenen und die Anzahl der Bits angeben, die zum Identifizieren der Farbe erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c28b2-106">The [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) and [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) function also allow you to specify the number of color planes and the number of bits required to identify the color.</span></span> <span data-ttu-id="c28b2-107">Andererseits verwenden die Funktionen " [**kreatecompatiblebitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) " und " [**deateverwerdablebitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) " einen angegebenen Gerätekontext, um die Anzahl von Farbebenen und die Anzahl der Bits, die zum Identifizieren der Farbe erforderlich sind, abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c28b2-107">On the other hand, the [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) and [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) functions use a specified device context to obtain the number of color planes and the number of bits required to identify the color.</span></span>

<span data-ttu-id="c28b2-108">Die Funktion " [**kreatedibitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) " erstellt eine Geräte abhängige Bitmap aus einer geräteunabhängigen Bitmap.</span><span class="sxs-lookup"><span data-stu-id="c28b2-108">The [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) function creates a device-dependent bitmap from a device-independent bitmap.</span></span> <span data-ttu-id="c28b2-109">Sie enthält eine Farbtabelle, in der beschrieben wird, wie Pixelwerte RGB-Farbwerten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c28b2-109">It contains a color table that describes how pixel values correspond to RGB color values.</span></span> <span data-ttu-id="c28b2-110">Weitere Informationen finden Sie unter [Geräte abhängige Bitmaps](device-dependent-bitmaps.md) und [geräteunabhängige Bitmaps](device-independent-bitmaps.md).</span><span class="sxs-lookup"><span data-stu-id="c28b2-110">For more information, see [Device-Dependent Bitmaps](device-dependent-bitmaps.md) and [Device-Independent Bitmaps](device-independent-bitmaps.md).</span></span>

<span data-ttu-id="c28b2-111">Nachdem die Bitmap erstellt wurde, können Sie die Größe, die Anzahl von Farbebenen oder die Anzahl der Bits, die zum Identifizieren der Farbe erforderlich sind, nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="c28b2-111">After the bitmap has been created, you cannot change its size, number of color planes, or number of bits required to identify the color.</span></span>

<span data-ttu-id="c28b2-112">Wenn Sie keine Bitmap mehr benötigen, können Sie die [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) -Funktion aufrufen, um Sie zu löschen.</span><span class="sxs-lookup"><span data-stu-id="c28b2-112">When you no longer need a bitmap, call the [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) function to delete it.</span></span>

 

 



