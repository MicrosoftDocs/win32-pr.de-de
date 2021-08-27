---
title: Abrufen des Status eines Erfassungsfensters
description: Abrufen des Status eines Erfassungsfensters
ms.assetid: 5095dbd2-7cd4-48b6-bbb4-1f0bddfcfd06
keywords:
- capGetStatus-Makro
- CAPSTATUS-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8effedac3950f0f57aaa6e57ccd5a93fe3044982c3d6ec6d6bb69b56024a1255
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038370"
---
# <a name="obtaining-the-status-of-a-capture-window"></a>Abrufen des Status eines Erfassungsfensters

Im folgenden Beispiel wird die [SetWindowPos-Funktion](/windows/win32/api/winuser/nf-winuser-setwindowpos) verwendet, um die Größe des Erfassungsfensters auf die Gesamtdimensionen des eingehenden Videodatenstroms basierend auf Informationen festzulegen, die vom [**capGetStatus-Makro**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) in der [**CAPSTATUS-Struktur**](/windows/win32/api/vfw/ns-vfw-capstatus) zurückgegeben werden.


```C++
CAPSTATUS CapStatus;

capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS)); 

SetWindowPos(hWndC, NULL, 0, 0, CapStatus.uiImageWidth, 
    CapStatus.uiImageHeight, SWP_NOZORDER | SWP_NOMOVE); 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Video capture](using-video-capture.md)
</dt> </dl>

 

 