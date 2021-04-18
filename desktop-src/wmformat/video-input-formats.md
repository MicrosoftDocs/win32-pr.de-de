---
title: Video Eingabeformate
description: Video Eingabeformate
ms.assetid: 0f1ec15d-328e-4c07-bf58-fd4ecb483549
keywords:
- Windows Media-Format-SDK, Videoeingabe Formate
- Advanced Systems Format (ASF), Videoeingabe Formate
- ASF (Advanced Systems Format), Videoeingabe Formate
- Videoeingabe Formate
- Windows Media-Format-SDK, Videoformate
- Advanced Systems Format (ASF), Videoformate
- ASF (Advanced Systems Format), Videoformate
- Videoformate
- Windows Media Video 9-Codec, Video Eingabeformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5113ee3cbd9c9235104f858968db20ebc29e3a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "106339052"
---
# <a name="video-input-formats"></a>Video Eingabeformate

Der Writer akzeptiert die folgenden Videoformate als Eingabe, die mit dem Windows Media Video 9-Codec komprimiert werden sollen:

-   wmmediasubtype \_ IYUV
-   Wmmediasubtype \_ I420
-   Wmmediasubtype \_ YV12
-   Wmmediasubtype \_ im YUY2
-   wmmediasubtype \_ UYVY
-   wmmediasubtype \_ yvyu
-   Wmmediasubtype \_ YVU9
-   Wmmediasubtype \_ RGB32
-   Wmmediasubtype \_ RGB24
-   Wmmediasubtype \_ RGB565
-   Wmmediasubtype \_ RGB555
-   Wmmediasubtype \_ RGB8

Sie sollten immer [**iwmwriter:: getinputformatcount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) und [**iwmwriter:: getinputformat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) verwenden, um die verfügbaren Eingabeformate aufzulisten und das Eingabemedien-Eigenschaften Objekt für das gewünschte Format zu erhalten. Die Eigenschaften der Video Eingabemedien-Eigenschaften müssen so geändert werden, dass Sie die Frame Größe und die Framerate der Eingabemedien widerspiegeln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Medientyp-IDs**](media-type-identifiers.md)
</dt> <dt>

[**Medientypen**](media-types.md)
</dt> </dl>

 

 




