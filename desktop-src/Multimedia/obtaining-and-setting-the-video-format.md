---
title: Abrufen und Festlegen des Video Formats
description: Abrufen und Festlegen des Video Formats
ms.assetid: 0e6baf24-7a79-45ab-9fc7-69334419956d
keywords:
- capgetvideoformat-Makro
- capgetvideoformatsize-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6890c3a1d653d43d24c5baa0790cc0d26040685b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858237"
---
# <a name="obtaining-and-setting-the-video-format"></a>Abrufen und Festlegen des Video Formats

Die [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur hat eine Variable Länge, um Standard-und komprimierte Datenformate zu unterstützen. Da diese Struktur eine Variable Länge hat, müssen Anwendungen die Größe der Struktur immer Abfragen und Arbeitsspeicher zuweisen, bevor das aktuelle Videoformat abgerufen wird. Im folgenden Beispiel wird das [**capgetvideoformatsize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) -Makro zum Abrufen der Puffergröße verwendet, und anschließend wird das [**capgetvideoformat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) -Makro aufgerufen, um das aktuelle Videoformat abzurufen.


```C++
LPBITMAPINFO lpbi;
DWORD dwSize;

dwSize = capGetVideoFormatSize(hWndC);
lpbi = GlobalAllocPtr (GHND, dwSize);
capGetVideoFormat(hWndC, lpbi, dwSize); 

// Access the video format and then free the allocated memory.
 
```



Anwendungen können das [**capsetvideoformat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) -Makro (oder die [**WM-Cap-Nachricht \_ \_ Set \_ Videoformat**](wm-cap-set-videoformat.md) ) verwenden, um eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Header Struktur an das Aufzeichnungs Fenster zu senden. Da Videoformate gerätespezifisch sind, sollte die Anwendung den Rückgabewert überprüfen, um festzustellen, ob das Format akzeptiert wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Video Erfassung](using-video-capture.md)
</dt> </dl>

 

 