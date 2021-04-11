---
description: 'Nachdem Sie die Vorschau eines Videodaten Stroms gestartet haben, können Sie die iwiavideo:: takepicture-Methode der iwiavideo-Schnittstelle aufzurufen, um ein Image aus dem Streamingvideo zu erfassen.'
ms.assetid: 2b8c465b-0dbf-4741-a701-200862cc3de3
title: Erfassen eines Images aus einem Videostream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be475405f4aa9719514a531a6af0105d7a786f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216056"
---
# <a name="capturing-a-still-image-from-a-video-stream"></a><span data-ttu-id="bc58f-103">Erfassen eines Images aus einem Videostream</span><span class="sxs-lookup"><span data-stu-id="bc58f-103">Capturing a Still Image from a Video Stream</span></span>

<span data-ttu-id="bc58f-104">Nachdem Sie die Vorschau eines Videodaten Stroms gestartet haben, können Sie die [**iwiavideo:: takepicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) -Methode der [**iwiavideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) -Schnittstelle aufzurufen, um ein Image aus dem Streamingvideo zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="bc58f-104">After beginning preview of a video stream, call the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method of the [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface to capture a still image from the streaming video.</span></span> <span data-ttu-id="bc58f-105">Anweisungen dazu, wie Sie einen **iwiavideo** -Zeiger abrufen und mit der Vorschau von Streaming-Videos beginnen, finden Sie unter [Preview Video](-wia-previewing-video.md).</span><span class="sxs-lookup"><span data-stu-id="bc58f-105">For instructions on how to get an **IWiaVideo** pointer and begin previewing streaming video, see [Previewing Video](-wia-previewing-video.md).</span></span>

<span data-ttu-id="bc58f-106">Wenn die [**iwiavideo:: takepicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) -Methode zurückgibt, enthält der *pbstraunetwimagefilename* -Parameter den vollständigen Pfad und den Dateinamen der resultierenden Bilddatei.</span><span class="sxs-lookup"><span data-stu-id="bc58f-106">When the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method returns, the *pbstrNewImageFilename* parameter contains the full path and filename of the resulting image file.</span></span> <span data-ttu-id="bc58f-107">Die Datei weist das JPEG-Format auf.</span><span class="sxs-lookup"><span data-stu-id="bc58f-107">The file is in JPEG format.</span></span> <span data-ttu-id="bc58f-108">Das Verzeichnis, in dem die Datei erstellt wird, wird durch den Wert der [**iwiavideo:: imagesdirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) -Eigenschaft der [**iwiavideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) -Schnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="bc58f-108">The directory in which the file is created is specified by the value of the [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) property of the [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface.</span></span>

> [!Note]  
> <span data-ttu-id="bc58f-109">Windows-Abbild Beschaffung (WIA) unterstützt keine Videogeräte in Windows Server 2003, Windows Vista oder höher.</span><span class="sxs-lookup"><span data-stu-id="bc58f-109">Windows Image Acquisition (WIA) does not support video devices in Windows Server 2003, Windows Vista, or later.</span></span> <span data-ttu-id="bc58f-110">Verwenden Sie für diese Versionen von Windows [DirectShow](/previous-versions//ms783323(v=vs.85)) zum Abrufen von Bildern aus Videos.</span><span class="sxs-lookup"><span data-stu-id="bc58f-110">For those versions of the Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) to acquire images from video.</span></span>

 

 

 
