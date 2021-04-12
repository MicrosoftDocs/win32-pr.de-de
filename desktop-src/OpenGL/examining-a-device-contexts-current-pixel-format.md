---
title: Untersuchen eines Geräte Kontexten Aktuelles Pixel Format
description: Verwenden Sie die Funktionen GetPixelFormat und describepixelformat, um das aktuelle Pixel Format eines Geräte Kontexts zu untersuchen, wie im folgenden Code Fragment dargestellt.
ms.assetid: 1da8c8e0-9444-421a-9c2e-c196b5a9db36
keywords:
- OpenGL unter Windows, Pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea36f0f25b2cf76a6fb2ffb3159a4f2763a95af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206519"
---
# <a name="examining-a-device-contexts-current-pixel-format"></a>Untersuchen eines Geräte Kontexten Aktuelles Pixel Format

Verwenden Sie die Funktionen [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) und [**describepixelformat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) , um das aktuelle Pixel Format eines Geräte Kontexts zu untersuchen, wie im folgenden Code Fragment dargestellt.


```C++
PIXELFORMATDESCRIPTOR  pfd;
HDC    hdc;
int    iPixelFormat;
 
// if the device context has a current pixel format ...  
if (iPixelFormat = GetPixelFormat(hdc)) { 
 
    // obtain a detailed description of that pixel format  
    DescribePixelFormat(hdc, iPixelFormat, 
                             sizeof(PIXELFORMATDESCRIPTOR), &pfd); 
    }
```



 

 




