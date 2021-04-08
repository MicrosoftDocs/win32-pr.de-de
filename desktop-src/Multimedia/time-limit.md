---
title: Zeitlimit
description: Zeitlimit
ms.assetid: 7c07755b-ba4d-4ec0-82ee-f76a533c6c5b
keywords:
- Captuprojektms-Struktur
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
- Captuprojektms-Struktur
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capcapturesetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878c76ab1e380fe878cd8c9493163bcb71e574cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714441"
---
# <a name="time-limit"></a><span data-ttu-id="77271-109">Zeitlimit</span><span class="sxs-lookup"><span data-stu-id="77271-109">Time Limit</span></span>

<span data-ttu-id="77271-110">Sie können die Dauer eines Aufzeichnungs Vorgangs beschränken, indem Sie die Elemente **flimitenabled** und **wtimelimit** der [**captuvertrams**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur verwenden.</span><span class="sxs-lookup"><span data-stu-id="77271-110">You can limit the duration of a capture operation by using the **fLimitEnabled** and **wTimeLimit** members of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="77271-111">Der **flimitenabled** -Member gibt an, ob der Aufzeichnungs Vorgang zeitgleich ist, während **wtimelimit** die maximale Dauer des Aufzeichnungs Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="77271-111">The **fLimitEnabled** member indicates whether the capture operation is to be timed, while **wTimeLimit** specifies the maximum duration of the capture operation.</span></span>

<span data-ttu-id="77271-112">Sie können die Werte für " **flimitenabled** " und " **wtimelimit** " mithilfe der " [**WM \_ Cap \_ get \_ Sequence \_**](wm-cap-get-sequence-setup.md) "-Setup Nachricht (oder des " [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) "-Makros) abrufen.</span><span class="sxs-lookup"><span data-stu-id="77271-112">You can retrieve the values for **fLimitEnabled** and **wTimeLimit** by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="77271-113">Sie können einen Timer für den Aufzeichnungs Vorgang aktivieren, indem Sie " **true** " als Wert von " **flimitenabled**" angeben, oder Sie können die Dauer des Aufzeichnungs Vorgangs festlegen, indem Sie einen Wert (in Sekunden) für " **wtimelimit**" angeben.</span><span class="sxs-lookup"><span data-stu-id="77271-113">You can enable a timer for the capture operation by specifying **TRUE** as the value of **fLimitEnabled**, or you can set the duration of the capture operation by specifying a value, in seconds, for **wTimeLimit**.</span></span> <span data-ttu-id="77271-114">Nachdem Sie diese Member festgelegt haben, senden Sie die aktualisierte [**captuadapms**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur mithilfe der " [**WM \_ Cap \_ Set \_ Sequence \_**](wm-cap-set-sequence-setup.md) "-Setup Nachricht (oder dem " [**capcapturesetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) "-Makro) an das Aufzeichnungs Fenster.</span><span class="sxs-lookup"><span data-stu-id="77271-114">After you set these members, send the updated [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="77271-115">Der Standardwert von **flimitenabled** ist **false**.</span><span class="sxs-lookup"><span data-stu-id="77271-115">The default value of **fLimitEnabled** is **FALSE**.</span></span>

 

 




