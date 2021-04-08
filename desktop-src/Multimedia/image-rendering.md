---
title: Bild Rendering
description: Bild Rendering
ms.assetid: de87f288-f1bd-471c-b594-e9dbde3cff0a
keywords:
- Drawdib, Bild Rendering
- Drawdib, Zeichnen von DIBs
- Drawdibdraw-Funktion
- Drawdibgetbuffer-Funktion
- Drawdibupdate-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e0d3f4d770a3acc290273b14ec14ff4b6efa30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037532"
---
# <a name="image-rendering"></a><span data-ttu-id="599de-108">Bild Rendering</span><span class="sxs-lookup"><span data-stu-id="599de-108">Image Rendering</span></span>

<span data-ttu-id="599de-109">Nachdem Sie [**drawdibopen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) aufgerufen haben, um einen drawdib-DC zu erstellen (siehe [drawdib-Vorgänge](drawdib-operations.md)), können Sie mithilfe der [**drawdibdraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) -Funktion ein DIB auf den Bildschirm ziehen.</span><span class="sxs-lookup"><span data-stu-id="599de-109">After you call [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) to create a DrawDib DC (see [DrawDib Operations](drawdib-operations.md)), you can draw a DIB to the screen by using the [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) function.</span></span> <span data-ttu-id="599de-110">**Drawdibdraw** Dithers True-Color-Bitmaps, wenn Sie mit 8-Bit-Anzeige Adaptern angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="599de-110">**DrawDibDraw** dithers true-color bitmaps when displaying them with 8-bit display adapters.</span></span>

<span data-ttu-id="599de-111">[**Drawdibdraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) unterstützt auch Video-Kompressoren transparent, wenn komprimierte Bitmaps angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="599de-111">[**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) also supports video compressors transparently when displaying compressed bitmaps.</span></span> <span data-ttu-id="599de-112">Mithilfe der [**drawdibgetbuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) -Funktion können Sie auf den Puffer zugreifen, der das entkomprimierte Image enthält.</span><span class="sxs-lookup"><span data-stu-id="599de-112">You can access the buffer that contains the decompressed image by using the [**DrawDibGetBuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) function.</span></span> <span data-ttu-id="599de-113">**Drawdibgetbuffer** gibt **null** zurück, wenn eine nicht komprimierte Bitmap gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="599de-113">**DrawDibGetBuffer** returns **NULL** when drawing an uncompressed bitmap.</span></span> <span data-ttu-id="599de-114">Sie sollten die Anwendung für die Verarbeitung von komprimierten und unkomprimierten Bitmaps vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="599de-114">You should prepare your application to handle compressed and uncompressed bitmaps.</span></span>

<span data-ttu-id="599de-115">Sie können ein Bild oder einen Teil eines Bilds aktualisieren, das von der Anwendung angezeigt wird, indem Sie das [**drawdibupdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="599de-115">You can refresh an image or a portion of an image displayed by your application by using the [**DrawDibUpdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) macro.</span></span>

## <a name="related-topics"></a><span data-ttu-id="599de-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="599de-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="599de-117">Informationen über die drawdib-Funktionen</span><span class="sxs-lookup"><span data-stu-id="599de-117">About the DrawDib Functions</span></span>](about-the-drawdib-functions.md)
</dt> </dl>

 

 




