---
title: Arbeiten mit komprimierten Video Daten in einem Stream
description: Arbeiten mit komprimierten Video Daten in einem Stream
ms.assetid: b701e072-f162-438f-b607-aea7491a02f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0587ee6c12a93eb014368642ba1605f546129e0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038884"
---
# <a name="working-with-compressed-video-data-in-a-stream"></a><span data-ttu-id="13794-103">Arbeiten mit komprimierten Video Daten in einem Stream</span><span class="sxs-lookup"><span data-stu-id="13794-103">Working with Compressed Video Data in a Stream</span></span>

<span data-ttu-id="13794-104">Avifile bietet mehrere Möglichkeiten für den Zugriff auf komprimierte Videostreams.</span><span class="sxs-lookup"><span data-stu-id="13794-104">AVIFile provides several ways for you to access compressed video streams.</span></span>

<span data-ttu-id="13794-105">Wenn Sie einen oder mehrere Frames eines komprimierten Videodaten Stroms anzeigen möchten, können Sie die Frames mithilfe der [**avistreamread**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) -Funktion abrufen und die komprimierten Frame Daten an drawdib-Funktionen weiterleiten, um Sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="13794-105">If you want to display one or more frames of a compressed video stream, you can retrieve the frames by using the [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) function and forwarding the compressed frame data to DrawDib functions to display them.</span></span> <span data-ttu-id="13794-106">Die drawdib-Funktionen können Bilder mehrerer Bild tiefen anzeigen und Bilder für Anzeige Dateien, die bestimmte Typen von geräteunabhängigen Bitmaps (DIBs) nicht verarbeiten können, automatisch unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="13794-106">DrawDib functions can display images of several image depths and automatically dither images for displays that cannot handle certain types of device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="13794-107">Diese Funktionen können mit nicht komprimierten und komprimierten Bildern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13794-107">These functions work with uncompressed and compressed images.</span></span> <span data-ttu-id="13794-108">Weitere Informationen zu drawdib-Funktionen finden Sie unter [drawdib Functions](drawdib-functions.md).</span><span class="sxs-lookup"><span data-stu-id="13794-108">For more information about DrawDib functions, see [DrawDib Functions](drawdib-functions.md).</span></span>

<span data-ttu-id="13794-109">Avifile bietet Funktionen zum Dekomprimieren eines einzelnen Video Frames.</span><span class="sxs-lookup"><span data-stu-id="13794-109">AVIFile provides functions for decompressing a single video frame.</span></span> <span data-ttu-id="13794-110">Verwenden Sie zum Zuordnen von Ressourcen die [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="13794-110">To allocate resources, use the [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) function.</span></span> <span data-ttu-id="13794-111">Mit dieser Funktion wird ein Puffer für die entkomprimierten Daten erstellt.</span><span class="sxs-lookup"><span data-stu-id="13794-111">This function creates a buffer for the decompressed data.</span></span>

<span data-ttu-id="13794-112">Sie können einen einzelnen Videoframe mithilfe der [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) -Funktion entkomprimieren.</span><span class="sxs-lookup"><span data-stu-id="13794-112">You can decompress a single video frame by using the [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) function.</span></span> <span data-ttu-id="13794-113">Diese Funktion zerlegt den Frame und Ruft einen kompletten Rahmen der Bilddaten ab, wobei die Adresse des DIB in der [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) -Struktur zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="13794-113">This function decompresses the frame and retrieves a complete frame of image data, returning the address of the DIB in the [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) structure.</span></span> <span data-ttu-id="13794-114">Die Anwendung kann das DIB mithilfe von Standard Zeichnungsfunktionen oder mithilfe der drawdib-Funktionen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="13794-114">Your application can display the DIB by using standard drawing functions or by using the DrawDib functions.</span></span>

<span data-ttu-id="13794-115">Wenn die Anwendung aufeinander folgende Aufrufe an **AVIStreamGetFrame** durchführt, überschreibt die Funktion den Puffer mit jedem abgerufenen Frame.</span><span class="sxs-lookup"><span data-stu-id="13794-115">If your application makes successive calls to **AVIStreamGetFrame**, the function overwrites its buffer with each retrieved frame.</span></span>

<span data-ttu-id="13794-116">Wenn Sie die Verwendung von **AVIStreamGetFrame** abgeschlossen haben und sich das entkomprimierte DIB in seinem Puffer befindet, können Sie die zugeordneten Ressourcen mithilfe der [**avistreamgetframeclose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="13794-116">When you finish using **AVIStreamGetFrame** and the decompressed DIB is in its buffer, you can release the allocated resources by using the [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) function.</span></span>

<span data-ttu-id="13794-117">Weitere Informationen zur Dekomprimierung von Bildern finden Sie unter [Video Compression Manager](video-compression-manager.md).</span><span class="sxs-lookup"><span data-stu-id="13794-117">For more information about decompressing images, see [Video Compression Manager](video-compression-manager.md).</span></span>

 

 