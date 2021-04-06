---
title: Video Puffer
description: Video Puffer
ms.assetid: 0dfe01ec-f997-4e5e-a73d-e6b712d0e19e
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capcapturesetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e2f3e5b56f995e6a09792260ac2fd6e1ba5cd7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712582"
---
# <a name="video-buffers"></a><span data-ttu-id="baabe-107">Video Puffer</span><span class="sxs-lookup"><span data-stu-id="baabe-107">Video Buffers</span></span>

<span data-ttu-id="baabe-108">Die mit der Video Erfassung verwendeten Puffer befinden sich im Arbeitsspeicher Heap.</span><span class="sxs-lookup"><span data-stu-id="baabe-108">The buffers used with video capture reside in the memory heap.</span></span> <span data-ttu-id="baabe-109">Die Anzahl von Puffern, die bei einem Aufzeichnungs Vorgang verwendet werden, kann variieren und hängt vom Wert des **wnumvideorequused** -Members der [**captuprojektmappenstruktur**](/windows/win32/api/vfw/ns-vfw-captureparms) und des verfügbaren System Speichers ab.</span><span class="sxs-lookup"><span data-stu-id="baabe-109">The number of buffers used in a capture operation can vary and depend on the value of the **wNumVideoRequested** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure and available system memory.</span></span>

<span data-ttu-id="baabe-110">Sie können den aktuellen Wert der angeforderten Video Puffer abrufen, indem Sie die " [**WM \_ Cap \_ get \_ Sequence \_**](wm-cap-get-sequence-setup.md) "-Setup Nachricht (oder das " [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) "-Makro) verwenden.</span><span class="sxs-lookup"><span data-stu-id="baabe-110">You can retrieve the current value of requested video buffers by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="baabe-111">Die aktuell angeforderte Anzahl von Video Puffern wird im **wnumvideorequtzig** -Member der **captuprojektstruktur** -Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="baabe-111">The current requested number of video buffers is stored in the **wNumVideoRequested** member of the **CAPTUREPARMS** structure.</span></span> <span data-ttu-id="baabe-112">Sie können die Platzierung und die Anzahl der Puffer anfordern, indem Sie dieses Element aktualisieren, und dann die aktualisierte **captuprojektmappenstruktur** [**mithilfe der**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) Setup-Nachricht der [**WM-Cap-Set- \_ \_ \_ Sequenz \_**](wm-cap-set-sequence-setup.md) an das Aufzeichnungs Fenster senden.</span><span class="sxs-lookup"><span data-stu-id="baabe-112">You can request the placement and number of buffers by updating this member, and then sending the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span>

 

 




