---
title: Dateiname erfassen
description: Dateiname erfassen
ms.assetid: b17ecdd4-899e-4e94-98f2-496f93491e06
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE Meldung
- capfilesetcapturefile-Makro
- WM_CAP_FILE_GET_CAPTURE_FILE Meldung
- capfilegetcapturefile-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4856649906e09f212d2f8992c9d4fb9b8f4c37d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342269"
---
# <a name="capture-filename"></a><span data-ttu-id="bc3ad-107">Dateiname erfassen</span><span class="sxs-lookup"><span data-stu-id="bc3ad-107">Capture Filename</span></span>

<span data-ttu-id="bc3ad-108">Avicap leitet standardmäßig Video-und audiostreamdaten aus einem Erfassungsfenster in eine Datei mit dem Namen CAPTURE.AVI im Stammverzeichnis des aktuellen Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-108">AVICap, by default, routes video and audio stream data from a capture window to a file named CAPTURE.AVI in the root directory of the current drive.</span></span> <span data-ttu-id="bc3ad-109">Sie können einen alternativen Dateinamen angeben, indem Sie die [**\_ \_ Datei \_ Set \_ Capture \_**](wm-cap-file-set-capture-file.md) -Datei für die WM-Abdeckung (oder das Makro [**capfilesetcapturefile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) ) an ein Aufzeichnungs Fenster senden.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-109">You can specify an alternate filename by sending the [**WM\_CAP\_FILE\_SET\_CAPTURE\_FILE**](wm-cap-file-set-capture-file.md) message (or the [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) macro) to a capture window.</span></span> <span data-ttu-id="bc3ad-110">Diese Meldung gibt den Dateinamen an. die Datei wird nicht erstellt, neu erstellt oder geöffnet.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-110">This message specifies the filename; it does not create, allocate, or open the file.</span></span> <span data-ttu-id="bc3ad-111">Sie können den aktuellen Aufzeichnungs Dateinamen abrufen, indem Sie die [**WM- \_ Cap-Datei " \_ \_ get \_ Capture \_ File**](wm-cap-file-get-capture-file.md) " (oder das Makro " [**capfilegetcapturefile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) ") an ein Erfassungsfenster senden.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-111">You can retrieve the current capture filename by sending the [**WM\_CAP\_FILE\_GET\_CAPTURE\_FILE**](wm-cap-file-get-capture-file.md) message (or the [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) macro) to a capture window.</span></span>

 

 




