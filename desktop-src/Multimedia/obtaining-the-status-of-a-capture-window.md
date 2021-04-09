---
title: Abrufen des Status eines Aufzeichnungs Fensters
description: Abrufen des Status eines Aufzeichnungs Fensters
ms.assetid: 5095dbd2-7cd4-48b6-bbb4-1f0bddfcfd06
keywords:
- capgetstatus-Makro
- Capstatus-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f848898247ad8ea2ddbb0dde7a13c08b6a7274
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948652"
---
# <a name="obtaining-the-status-of-a-capture-window"></a>Abrufen des Status eines Aufzeichnungs Fensters

Im folgenden Beispiel wird die [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) -Funktion verwendet, um die Größe des Aufzeichnungs Fensters auf die Gesamtabmessungen des eingehenden Videostreams basierend auf Informationen festzulegen, die vom [**capgetstatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) -Makro in der [**capstatus**](/windows/win32/api/vfw/ns-vfw-capstatus) -Struktur zurückgegeben werden.


```C++
CAPSTATUS CapStatus;

capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS)); 

SetWindowPos(hWndC, NULL, 0, 0, CapStatus.uiImageWidth, 
    CapStatus.uiImageHeight, SWP_NOZORDER | SWP_NOMOVE); 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Video Erfassung](using-video-capture.md)
</dt> </dl>

 

 