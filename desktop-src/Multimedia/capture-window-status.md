---
title: Status des Aufzeichnungs Fensters
description: Status des Aufzeichnungs Fensters
ms.assetid: c3f80cac-30b2-42f0-8a9c-4053728c558b
keywords:
- WM_CAP_GET_STATUS Meldung
- capgetstatus-Makro
- Capstatus-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6019009c8510abe3429c1043527156c55f0c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037356"
---
# <a name="capture-window-status"></a><span data-ttu-id="29464-106">Status des Aufzeichnungs Fensters</span><span class="sxs-lookup"><span data-stu-id="29464-106">Capture Window Status</span></span>

<span data-ttu-id="29464-107">Sie können den aktuellen Status eines Aufzeichnungs Fensters abrufen, indem Sie die [**\_ \_ \_ Status**](wm-cap-get-status.md) Meldung "WM-Abdeckung abrufen" (oder das " [**capgetstatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) "-Makro) verwenden.</span><span class="sxs-lookup"><span data-stu-id="29464-107">You can retrieve the current status of a capture window by using the [**WM\_CAP\_GET\_STATUS**](wm-cap-get-status.md) message (or the [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) macro).</span></span> <span data-ttu-id="29464-108">Diese Meldung Ruft eine Kopie der [**capstatus**](/windows/win32/api/vfw/ns-vfw-capstatus) -Struktur mit den aktuellen Werten der zugehörigen Member ab.</span><span class="sxs-lookup"><span data-stu-id="29464-108">This message retrieves a copy of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure with the current values of its members.</span></span> <span data-ttu-id="29464-109">Die **capstatus** -Struktur enthält Informationen über die Abmessungen des Bilds, die Scrollposition und ob die Überlagerung oder die Vorschau des Bilds aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="29464-109">The **CAPSTATUS** structure contains information regarding the dimensions of the image, scroll position, and whether overlay or preview of the image is enabled.</span></span> <span data-ttu-id="29464-110">Da die in **capstatus** dargestellten Informationen dynamisch sind, sollte Ihre Anwendung den Inhalt der Struktur immer dann aktualisieren, wenn sich die Größe oder das Format des aufgezeichneten Videostreams geändert hat (z. b. nach dem Anzeigen des Video Formats des Aufzeichnungs Treibers).</span><span class="sxs-lookup"><span data-stu-id="29464-110">Because the information represented in **CAPSTATUS** is dynamic, your application should refresh the contents of the structure whenever the size or format of the captured video stream might have changed (such as after displaying the video format of the capture driver).</span></span>

<span data-ttu-id="29464-111">Das Ändern der Abmessungen des Aufzeichnungs Fensters wirkt sich nicht auf die Dimensionen des tatsächlich aufgezeichneten Videostreams aus.</span><span class="sxs-lookup"><span data-stu-id="29464-111">Changing the dimensions of the capture window has no effect on the dimensions of the actual captured video stream.</span></span> <span data-ttu-id="29464-112">Im Dialogfeld Format, das vom Gerätetreiber für die Video Erfassung angezeigt wird, werden die Dimensionen des aufgezeichneten Videostreams gesteuert.</span><span class="sxs-lookup"><span data-stu-id="29464-112">The format dialog box displayed by the video capture device driver controls the dimensions of the captured video stream.</span></span>

 

 




