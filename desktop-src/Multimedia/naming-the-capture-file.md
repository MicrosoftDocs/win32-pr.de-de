---
title: Benennen der Erfassungsdatei
description: Benennen der Erfassungsdatei
ms.assetid: fae2fd6a-4c2f-432f-a714-9faae6daeafe
keywords:
- capFileSetCaptureFile-Makro
- capFileAlloc-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c07653b854b4af476c22566aac5e9ecf27cb78b3dac5b317aab4b8f3f23a19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373315"
---
# <a name="naming-the-capture-file"></a>Benennen der Erfassungsdatei

Im folgenden Beispiel wird das [**Makro capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) verwendet, um einen alternativen Dateinamen (MYCAP.AVI) für die Erfassungsdatei anzugeben, und das [**Makro capFileAlloc,**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) um eine Datei mit 5 MB vorab zu bestimmen.


```C++
char szCaptureFile[] = "MYCAP.AVI";

capFileSetCaptureFile( hWndC, szCaptureFile); 
capFileAlloc( hWndC, (1024L * 1024L * 5)); 
 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Video Capture](using-video-capture.md)
</dt> </dl>

 

 




