---
description: Rufen Sie nach Beginn der Vorschau eines Videostreams die IWiaVideo::TakePicture-Methode der IWiaVideo-Schnittstelle auf, um ein Stillbild aus dem Streamingvideo zu erfassen.
ms.assetid: 2b8c465b-0dbf-4741-a701-200862cc3de3
title: Erfassen eines Still-Bilds aus einem Videostream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af98dc313ddde7f2da160515ab53d31357a6d9cc96e1737ed01767b40fb0e7c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814280"
---
# <a name="capturing-a-still-image-from-a-video-stream"></a>Erfassen eines Still-Bilds aus einem Videostream

Rufen Sie nach Beginn der Vorschau eines Videostreams die [**IWiaVideo::TakePicture-Methode**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) der [**IWiaVideo-Schnittstelle**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) auf, um ein Stillbild aus dem Streamingvideo zu erfassen. Anweisungen dazu, wie Sie einen **IWiaVideo-Zeiger** erhalten und mit der Vorschau des Streamingvideos beginnen, finden Sie unter [Vorschau von Video](-wia-previewing-video.md).

Wenn die [**IWiaVideo::TakePicture-Methode**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) zurückgegeben wird, enthält der *Parameter pbstrNewImageFilename* den vollständigen Pfad und Dateinamen der resultierenden Bilddatei. Die Datei hat das JPEG-Format. Das Verzeichnis, in dem die Datei erstellt wird, wird durch den Wert der [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) -Eigenschaft der [**IWiaVideo-Schnittstelle**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) angegeben.

> [!Note]  
> Windows Die Bilderfassung (WIA) unterstützt keine Videogeräte in Windows Server 2003, Windows Vista oder höher. Verwenden Sie für diese Versionen Windows [DirectShow,](/previous-versions//ms783323(v=vs.85)) um Bilder aus Videos zu erhalten.

 

 

 
