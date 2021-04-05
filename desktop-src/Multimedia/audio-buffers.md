---
title: Audiopuffer
description: Audiopuffer
ms.assetid: e18e9ff4-e8e9-4013-a800-1a30335026ff
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capcapturesetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a67f120dc2d2ff956148e5dd4e3992a960641d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709179"
---
# <a name="audio-buffers"></a><span data-ttu-id="9d8c5-107">Audiopuffer</span><span class="sxs-lookup"><span data-stu-id="9d8c5-107">Audio Buffers</span></span>

<span data-ttu-id="9d8c5-108">Sie können den Audioteil eines Aufzeichnungs Vorgangs auf drei Arten steuern:</span><span class="sxs-lookup"><span data-stu-id="9d8c5-108">You can control the audio portion of a capture operation in three ways:</span></span>

-   <span data-ttu-id="9d8c5-109">Einschließen oder Ausschließen von Audiodaten aus dem Aufzeichnungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9d8c5-109">Include or exclude audio from the capture operation.</span></span>
-   <span data-ttu-id="9d8c5-110">Fordern Sie eine bestimmte Anzahl von audiopuffern an.</span><span class="sxs-lookup"><span data-stu-id="9d8c5-110">Request a specific number of audio buffers.</span></span>
-   <span data-ttu-id="9d8c5-111">Fordern Sie an, dass Audiopuffer eine bestimmte Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9d8c5-111">Request that audio buffers be a specific size.</span></span>

<span data-ttu-id="9d8c5-112">Sie können die Einstellungen für Audiopuffer abrufen, indem Sie [**die \_ \_ get \_ Sequence- \_ Setup**](wm-cap-get-sequence-setup.md) Nachricht (oder das [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) -Makro) der WM-Obergrenze verwenden.</span><span class="sxs-lookup"><span data-stu-id="9d8c5-112">You can retrieve the settings for audio buffers by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="9d8c5-113">Der **fcaptureaudiomember** der [**captumams**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur gibt an, ob Audiodaten in den Aufzeichnungs Vorgang eingeschlossen oder davon ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="9d8c5-113">The **fCaptureAudio** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure specifies whether audio is included or excluded from the capture operation.</span></span> <span data-ttu-id="9d8c5-114">Die aktuell angeforderte Anzahl der Audiopuffer wird im **wnumaudiorequtzig** -Element gespeichert, und die aktuelle audiopuffergröße wird im **dwaudiobuffersize** -Element gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9d8c5-114">The current requested number of audio buffers is stored in the **wNumAudioRequested** member, and the current audio buffer size is stored in the **dwAudioBufferSize** member.</span></span> <span data-ttu-id="9d8c5-115">Sie können angeben, ob Audioerfassung eingeschlossen werden soll, wie die Größe und Anzahl der Audiopuffer durch Aktualisieren dieser Member angegeben werden soll, und die aktualisierte **captuadapms** -Struktur wird mithilfe der " [**WM \_ Cap \_ Set \_ Sequence \_**](wm-cap-set-sequence-setup.md) "-Setup Nachricht (oder dem [**capcapturesetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) -Makro) an das Aufzeichnungs Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="9d8c5-115">You can specify whether to include audio capture, specify the size and number of audio buffers by updating these members, and send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span>

<span data-ttu-id="9d8c5-116">Standardmäßig ist das Audioformat im Aufzeichnungs Vorgang enthalten, und es werden vier Audiopuffer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="9d8c5-116">By default, audio is included in the capture operation, and four audio buffers are allocated.</span></span> <span data-ttu-id="9d8c5-117">Der Standardwert von " **f** " ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="9d8c5-117">The default value of **fCaptureAudio** is **TRUE**.</span></span> <span data-ttu-id="9d8c5-118">Die Standardpuffergröße (der Wert von **dwaudiobuffersize**) kann 0,5 Sekunden Audiodaten oder 10K enthalten, je nachdem, welcher Wert größer ist.</span><span class="sxs-lookup"><span data-stu-id="9d8c5-118">The default buffer size (the value of **dwAudioBufferSize**) can contain 0.5 seconds of audio data or 10K, whichever is greater.</span></span>

 

 




