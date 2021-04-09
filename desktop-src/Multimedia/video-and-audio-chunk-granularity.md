---
title: Granularität von Video-und audiosegmenten
description: Granularität von Video-und audiosegmenten
ms.assetid: 02c94de7-c7cb-4150-8b3e-0542d317c19b
keywords:
- AVI-Dateien, Segment Granularität
- Avicap-Klasse, Füll Blöcke
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capcapturesetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2245b133fbf14bfd6403fa2f3d7e02ed328de6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947831"
---
# <a name="video-and-audio-chunk-granularity"></a><span data-ttu-id="1dad4-109">Granularität von Video-und audiosegmenten</span><span class="sxs-lookup"><span data-stu-id="1dad4-109">Video and Audio Chunk Granularity</span></span>

<span data-ttu-id="1dad4-110">Die Segment Granularität ist eine logische Blockgröße für eine AVI-Datei, die zum Schreiben und Abrufen von Audiodaten und Videodaten Segmenten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1dad4-110">The chunk granularity is a logical block size for an AVI file that is used for writing and retrieving audio and video data chunks.</span></span> <span data-ttu-id="1dad4-111">Beim Schreiben von Audiodaten und Video Blöcken auf den Datenträger fügt avicap bei Bedarf Füll Blöcke (Riff "Junk"-Blöcke) hinzu, um jeden logischen Datenblock auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="1dad4-111">When writing audio and video chunks to disk, AVICap adds filler chunks (RIFF "JUNK" chunks) as necessary to fill each logical block of data.</span></span>

<span data-ttu-id="1dad4-112">Sie können die aktuelle Segment granularitätseinstellung mithilfe der " [**WM \_ Cap \_ get \_ Sequence \_**](wm-cap-get-sequence-setup.md) "-Setup Nachricht (oder des " [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) "-Makros) abrufen.</span><span class="sxs-lookup"><span data-stu-id="1dad4-112">You can retrieve the current chunk granularity setting by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="1dad4-113">Die aktuelle Segment Granularität wird im **wchunkgranularity** -Member der [**captuprojektstruktur**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1dad4-113">The current chunk granularity is stored in the **wChunkGranularity** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="1dad4-114">Sie können eine neue Segment Granularität als Wert von **wchunkgranularität** angeben und dann die aktualisierte **captuadapms** -Struktur [**mithilfe der**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) Setup-Nachricht der [**WM-Cap- \_ \_ Set- \_ Sequenz \_**](wm-cap-set-sequence-setup.md) an das Aufzeichnungs Fenster senden.</span><span class="sxs-lookup"><span data-stu-id="1dad4-114">You can specify a new chunk granularity as the value of **wChunkGranularity** and then send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="1dad4-115">Sie können auch NULL für diesen Member angeben, um die Segment Granularität auf die Sektorgröße des Datenträgers festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1dad4-115">You can also specify zero for this member to set the chunk granularity to the sector size of the disk.</span></span>

 

 




