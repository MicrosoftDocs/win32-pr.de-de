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
# <a name="obtaining-and-setting-the-video-format"></a><span data-ttu-id="61ab4-105">Abrufen und Festlegen des Video Formats</span><span class="sxs-lookup"><span data-stu-id="61ab4-105">Obtaining and Setting the Video Format</span></span>

<span data-ttu-id="61ab4-106">Die [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur hat eine Variable Länge, um Standard-und komprimierte Datenformate zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="61ab4-106">The [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure is of variable length to accommodate standard and compressed data formats.</span></span> <span data-ttu-id="61ab4-107">Da diese Struktur eine Variable Länge hat, müssen Anwendungen die Größe der Struktur immer Abfragen und Arbeitsspeicher zuweisen, bevor das aktuelle Videoformat abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="61ab4-107">Because this structure is of variable length, applications must always query the size of the structure and allocate memory before retrieving the current video format.</span></span> <span data-ttu-id="61ab4-108">Im folgenden Beispiel wird das [**capgetvideoformatsize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) -Makro zum Abrufen der Puffergröße verwendet, und anschließend wird das [**capgetvideoformat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) -Makro aufgerufen, um das aktuelle Videoformat abzurufen.</span><span class="sxs-lookup"><span data-stu-id="61ab4-108">The following example uses the [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) macro to retrieve the buffer size and then calls the [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) macro to retrieve the current video format.</span></span>


```C++
LPBITMAPINFO lpbi;
DWORD dwSize;

dwSize = capGetVideoFormatSize(hWndC);
lpbi = GlobalAllocPtr (GHND, dwSize);
capGetVideoFormat(hWndC, lpbi, dwSize); 

// Access the video format and then free the allocated memory.
 
```



<span data-ttu-id="61ab4-109">Anwendungen können das [**capsetvideoformat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) -Makro (oder die [**WM-Cap-Nachricht \_ \_ Set \_ Videoformat**](wm-cap-set-videoformat.md) ) verwenden, um eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Header Struktur an das Aufzeichnungs Fenster zu senden.</span><span class="sxs-lookup"><span data-stu-id="61ab4-109">Applications can use the [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) macro (or the [**WM\_CAP\_SET\_VIDEOFORMAT**](wm-cap-set-videoformat.md) message) to send a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) header structure to the capture window.</span></span> <span data-ttu-id="61ab4-110">Da Videoformate gerätespezifisch sind, sollte die Anwendung den Rückgabewert überprüfen, um festzustellen, ob das Format akzeptiert wurde.</span><span class="sxs-lookup"><span data-stu-id="61ab4-110">Because video formats are device specific, your application should check the return value to determine if the format was accepted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61ab4-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="61ab4-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61ab4-112">Verwenden der Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="61ab4-112">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 