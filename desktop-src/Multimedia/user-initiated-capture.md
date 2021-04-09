---
title: User-Initiated Erfassung
description: User-Initiated Erfassung
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db44049ff64f6e0187ed38ca78ca0d3e1f36d6ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856624"
---
# <a name="user-initiated-capture"></a><span data-ttu-id="7de22-105">User-Initiated Erfassung</span><span class="sxs-lookup"><span data-stu-id="7de22-105">User-Initiated Capture</span></span>

<span data-ttu-id="7de22-106">Sie können den aktuellen Wert des vom Benutzer initiierten Erfassungs Flags abrufen, indem Sie die " [**WM \_ Cap \_ get \_ Sequence \_**](wm-cap-get-sequence-setup.md) "-Setup Nachricht (oder das " [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) "-Makro) verwenden.</span><span class="sxs-lookup"><span data-stu-id="7de22-106">You can retrieve the current value of the user-initiated capture flag by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="7de22-107">Der Wert des Flags wird im **fmakeuserhitektocapture** -Member der [**captuprojektstruktur**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7de22-107">The value of the flag is stored in the **fMakeUserHitOKToCapture** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="7de22-108">Sie können dem Benutzer genau steuern, wann eine Aufzeichnungs Sitzung gestartet werden soll, indem Sie dieses Element auf " **true**" festlegen.</span><span class="sxs-lookup"><span data-stu-id="7de22-108">You can provide the user with precise control over when to start a capture session by setting this member to **TRUE**.</span></span> <span data-ttu-id="7de22-109">Avicap zeigt ein Dialogfeld an, nachdem alle Video-und Audiopuffer für eine Aufzeichnungs Sitzung zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="7de22-109">AVICap displays a dialog box after allocating all video and audio buffers for a capture session.</span></span> <span data-ttu-id="7de22-110">Dadurch kann der Benutzer aufgrund der Software Initialisierung Aufzeichnungs Verzögerungen vermeiden.</span><span class="sxs-lookup"><span data-stu-id="7de22-110">This lets the user eliminate capture delays because of software initialization.</span></span> <span data-ttu-id="7de22-111">Wenn Ihre Anwendung eine kleine Anzahl von Video Puffern verwendet, ist dieses Dialogfeld wahrscheinlich unnötig.</span><span class="sxs-lookup"><span data-stu-id="7de22-111">If your application uses a small number of video buffers, this dialog box is probably unnecessary.</span></span> <span data-ttu-id="7de22-112">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="7de22-112">The default value is **FALSE**.</span></span>

 

 




