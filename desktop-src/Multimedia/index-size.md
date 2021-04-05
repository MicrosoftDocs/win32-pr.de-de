---
title: Indexgröße
description: Indexgröße
ms.assetid: 7902589d-5e08-4c0c-9a22-82d28ad2677e
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capcapturesetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cd9e59c23376a7aa201673ef71743c8a192b60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711585"
---
# <a name="index-size"></a><span data-ttu-id="ebab6-107">Indexgröße</span><span class="sxs-lookup"><span data-stu-id="ebab6-107">Index Size</span></span>

<span data-ttu-id="ebab6-108">Jede AVI-Datei verwendet einen Index einer angegebenen Größe, um Video-und Audiodatenblöcke innerhalb der Datei zu suchen.</span><span class="sxs-lookup"><span data-stu-id="ebab6-108">Each AVI file uses an index of a specified size to locate video and audio data chunks within the file.</span></span> <span data-ttu-id="ebab6-109">Ein Eintrag im Index gibt einen Video Frame oder einen Wellenform-Audiopuffer an.</span><span class="sxs-lookup"><span data-stu-id="ebab6-109">An entry in the index locates one video frame or waveform-audio buffer.</span></span> <span data-ttu-id="ebab6-110">Folglich legt der Wert der Indexgröße indirekt die Obergrenze für die Anzahl der Frames fest, die in einer Datei aufgezeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="ebab6-110">Consequently, the value of the index size indirectly sets the upper limit on the number of frames that can be captured in a file.</span></span>

<span data-ttu-id="ebab6-111">Sie können die aktuelle Indexgröße abrufen, indem Sie die " [**WM \_ Cap \_ get \_ Sequence \_**](wm-cap-get-sequence-setup.md) "-Setup Nachricht (oder das " [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) "-Makro) verwenden.</span><span class="sxs-lookup"><span data-stu-id="ebab6-111">You can retrieve the current index size by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="ebab6-112">Die aktuelle Indexgröße wird im **dwindexsize** -Member der [**captuindems**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ebab6-112">The current index size is stored in the **dwIndexSize** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="ebab6-113">Sie können eine neue Indexgröße als Wert von " **dwindexsize** " angeben und dann die aktualisierte **captuadapms** -Struktur mithilfe der [**\_ \_ \_ \_ Setup**](wm-cap-set-sequence-setup.md) -Nachricht für die WM-Abdeckung (oder dem [**capcapturesetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) -Makro) an das Aufzeichnungs Fenster senden.</span><span class="sxs-lookup"><span data-stu-id="ebab6-113">You can specify a new index size as the value of **dwIndexSize** and then send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="ebab6-114">Die Standard Indexgröße beträgt 34.952 Einträge (32-KB-Frames und eine proportionale Anzahl von audiopuffern).</span><span class="sxs-lookup"><span data-stu-id="ebab6-114">The default index size is 34,952 entries (allowing 32K frames and a proportional number of audio buffers).</span></span>

 

 




