---
title: Erfassungs Rate
description: Erfassungs Rate
ms.assetid: 70cac7ac-0f7e-431e-a099-b075ba5fb039
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
- Captuprojektms-Struktur
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capcapturesetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93be9e94f5f9085d25c6ad85a30b115d13349169
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036963"
---
# <a name="capture-rate"></a><span data-ttu-id="91034-108">Erfassungs Rate</span><span class="sxs-lookup"><span data-stu-id="91034-108">Capture Rate</span></span>

<span data-ttu-id="91034-109">Die Erfassungs Rate ist die Anzahl der Frames, die pro Sekunde einer Aufzeichnungs Sitzung aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="91034-109">The capture rate is the number of frames that are captured each second of a capture session.</span></span> <span data-ttu-id="91034-110">Sie können die aktuelle Aufzeichnungsrate mithilfe der " [**WM \_ Cap \_ get \_ Sequence \_**](wm-cap-get-sequence-setup.md) "-Setup Nachricht (oder des " [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) "-Makros) abrufen.</span><span class="sxs-lookup"><span data-stu-id="91034-110">You can retrieve the current capture rate by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="91034-111">Die aktuelle Aufzeichnungsrate wird im **dwrequestmikro secperframe** -Member der [**captuprojektstruktur**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="91034-111">The current capture rate is stored in the **dwRequestMicroSecPerFrame** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="91034-112">Sie können die Erfassungs Rate festlegen, indem Sie die Anzahl der Mikrosekunden zwischen aufeinander folgenden Frames als Wert dieses Members angeben und dann die aktualisierte **captuprojektstruktur** an das Aufzeichnungs Fenster senden, indem Sie die Setup-Nachricht der [**WM-Cap-Set- \_ \_ \_ Sequenz \_**](wm-cap-set-sequence-setup.md) (oder das [**capcapturesetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) -Makro) verwenden.</span><span class="sxs-lookup"><span data-stu-id="91034-112">You can set the capture rate by specifying the number of microseconds between successive frames as the value of this member, then sending the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="91034-113">Der Standardwert von **dwrequestmikro secperframe** ist 66667, was 15 Frames pro Sekunde entspricht.</span><span class="sxs-lookup"><span data-stu-id="91034-113">The default value of **dwRequestMicroSecPerFrame** is 66667, which corresponds to 15 frames per second.</span></span>

 

 




