---
title: Messen der Video Qualität
description: Messen der Video Qualität
ms.assetid: e1e76bed-a632-45e8-a8b3-13dd6969e85a
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capcapturesetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0ad32bd3983301687b0eb0bb01f0fd932a43944
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036888"
---
# <a name="measuring-video-quality"></a><span data-ttu-id="91042-107">Messen der Video Qualität</span><span class="sxs-lookup"><span data-stu-id="91042-107">Measuring Video Quality</span></span>

<span data-ttu-id="91042-108">Eine Möglichkeit zum Messen der Videoqualität besteht darin, die Anzahl der aufgezeichneten Frames einzuschränken, die während des Aufzeichnungs Vorgangs verworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="91042-108">One way to measure video quality is to limit the number of captured frames dropped during the capture operation.</span></span> <span data-ttu-id="91042-109">Wenn die streamingerfassung abgeschlossen ist, wird der Qualitäts Wert mit dem Verhältnis der verworfenen Frames zu den Gesamtrahmen verglichen.</span><span class="sxs-lookup"><span data-stu-id="91042-109">When streaming capture has finished, the quality value is compared with the ratio of dropped frames to total frames.</span></span> <span data-ttu-id="91042-110">Wenn der Prozentsatz der gelöschten Frames größer ist als der Wert des **wprozdropforerror** -Members der [**captuprojektstruktur**](/windows/win32/api/vfw/ns-vfw-captureparms) , sendet avicap bei der Installation eine Fehlermeldung an die Fehler Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="91042-110">If the percentage of dropped frames is greater than the value of the **wPercentDropForError** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure, AVICap sends an error message to the error callback function if it is installed.</span></span>

<span data-ttu-id="91042-111">Sie können das aktuelle Limit von gelöschten Frames (ausgedrückt als Prozentsatz) mithilfe der [**\_ \_ get \_ Sequence- \_ Setup**](wm-cap-get-sequence-setup.md) Nachricht der WM-Abdeckung abrufen (oder das-Makro [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="91042-111">You can retrieve the current limit of dropped frames (expressed as a percentage) by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="91042-112">Sie können eine neue Grenze festlegen, indem Sie einen Prozentwert als Wert des **wprozentudropforerror** -Members der **captuprojektstruktur** angeben und dann die aktualisierte Struktur mithilfe der [**\_ \_ \_ \_ Setup**](wm-cap-set-sequence-setup.md) -Nachricht für die WM-Abdeckung (oder das [**capcapturesetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) -Makro) an das Aufzeichnungs Fenster senden.</span><span class="sxs-lookup"><span data-stu-id="91042-112">You can set a new limit by specifying a percentage as the value of the **wPercentDropForError** member of the **CAPTUREPARMS** structure, and then sending the updated structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="91042-113">Der Standardwert von **wprozdropforerror** ist 10 Prozent.</span><span class="sxs-lookup"><span data-stu-id="91042-113">The default value of **wPercentDropForError** is 10 percent.</span></span>

 

 




