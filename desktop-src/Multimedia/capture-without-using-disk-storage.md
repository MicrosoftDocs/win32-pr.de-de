---
title: Erfassung ohne Verwendung Disk Storage
description: Erfassung ohne Verwendung Disk Storage
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- WM_CAP_SEQUENCE_NOFILE Meldung
- capcapturesequencenofile-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76fa69fa8a827117dbc110a410cb40084614559
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337358"
---
# <a name="capture-without-using-disk-storage"></a><span data-ttu-id="e697c-105">Erfassung ohne Verwendung Disk Storage</span><span class="sxs-lookup"><span data-stu-id="e697c-105">Capture Without Using Disk Storage</span></span>

<span data-ttu-id="e697c-106">Sie können Aufzeichnungs Dienste verwenden, ohne die Daten in eine Datenträger Datei zu schreiben, indem Sie die " [**WM \_ Cap \_ Sequence \_ NoFile**](wm-cap-sequence-nofile.md) "-Nachricht (oder das [**capcapturesequencenofile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) -Makro) verwenden.</span><span class="sxs-lookup"><span data-stu-id="e697c-106">You can use capture services without writing the data to a disk file by using the [**WM\_CAP\_SEQUENCE\_NOFILE**](wm-cap-sequence-nofile.md) message (or the [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) macro).</span></span> <span data-ttu-id="e697c-107">Diese Meldung ist nur in Verbindung mit Rückruf Funktionen hilfreich, mit denen Ihre Anwendung die Video-und Audiodaten direkt verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="e697c-107">This message is useful only in conjunction with callback functions that allow your application to use the video and audio data directly.</span></span> <span data-ttu-id="e697c-108">Beispielsweise können Videokonferenz-Anwendungen diese Nachricht zum Abrufen von streamingvideoframes verwenden.</span><span class="sxs-lookup"><span data-stu-id="e697c-108">For example, videoconferencing applications might use this message to obtain streaming video frames.</span></span> <span data-ttu-id="e697c-109">Die Rückruf Funktionen würden die erfassten Images auf den Remote Computer übertragen.</span><span class="sxs-lookup"><span data-stu-id="e697c-109">The callback functions would transfer the captured images to the remote computer.</span></span>

 

 




