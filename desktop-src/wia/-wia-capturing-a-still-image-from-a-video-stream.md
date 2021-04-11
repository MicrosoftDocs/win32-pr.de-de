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
# <a name="capturing-a-still-image-from-a-video-stream"></a>Erfassen eines Images aus einem Videostream

Nachdem Sie die Vorschau eines Videodaten Stroms gestartet haben, können Sie die [**iwiavideo:: takepicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) -Methode der [**iwiavideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) -Schnittstelle aufzurufen, um ein Image aus dem Streamingvideo zu erfassen. Anweisungen dazu, wie Sie einen **iwiavideo** -Zeiger abrufen und mit der Vorschau von Streaming-Videos beginnen, finden Sie unter [Preview Video](-wia-previewing-video.md).

Wenn die [**iwiavideo:: takepicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) -Methode zurückgibt, enthält der *pbstraunetwimagefilename* -Parameter den vollständigen Pfad und den Dateinamen der resultierenden Bilddatei. Die Datei weist das JPEG-Format auf. Das Verzeichnis, in dem die Datei erstellt wird, wird durch den Wert der [**iwiavideo:: imagesdirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) -Eigenschaft der [**iwiavideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) -Schnittstelle angegeben.

> [!Note]  
> Windows-Abbild Beschaffung (WIA) unterstützt keine Videogeräte in Windows Server 2003, Windows Vista oder höher. Verwenden Sie für diese Versionen von Windows [DirectShow](/previous-versions//ms783323(v=vs.85)) zum Abrufen von Bildern aus Videos.

 

 

 
