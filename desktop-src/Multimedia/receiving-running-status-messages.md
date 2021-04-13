---
title: Empfangen von Running-Status Nachrichten
description: Empfangen von Running-Status Nachrichten
ms.assetid: 4f2e8e41-89f6-45e3-ae16-47b856f0e63e
keywords:
- Digital Instrumentation Digital Interface (MIDI), Running Status
- MIDI (Digital Interface Digital Interface), Running Status
- Aufzeichnen von MIDI-Audiodaten, Ausführen des Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4d12a19f525a6fa673747063774bf4507d65b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388008"
---
# <a name="receiving-running-status-messages"></a><span data-ttu-id="f79a5-106">Empfangen von Running-Status Nachrichten</span><span class="sxs-lookup"><span data-stu-id="f79a5-106">Receiving Running-Status Messages</span></span>

<span data-ttu-id="f79a5-107">Die *Standard mäßige* Version der Version von MIDI-Dateien 1,0 ermöglicht die Verwendung des *Status wird ausgeführt* , wenn eine Nachricht das gleiche Status Byte wie die vorherige Meldung aufweist.</span><span class="sxs-lookup"><span data-stu-id="f79a5-107">The *Standard MIDI Files 1.0* specification allows the use of *running status* when a message has the same status byte as the previous message.</span></span> <span data-ttu-id="f79a5-108">Wenn Running Status verwendet wird, kann das Status Byte der nachfolgenden Nachrichten ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="f79a5-108">When running status is used, the status byte of subsequent messages can be omitted.</span></span> <span data-ttu-id="f79a5-109">Alle Treiber der MIDI-Eingabegeräte sind erforderlich, um Nachrichten mit dem Status "wird ausgeführt" in vollständige Nachrichten zu erweitern, damit Sie immer vollständige MIDI-Nachrichten von einem Eingabegeräte Treiber von</span><span class="sxs-lookup"><span data-stu-id="f79a5-109">All MIDI input device drivers are required to expand messages using running status into complete messages, so that you always receive complete MIDI messages from a MIDI input device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f79a5-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f79a5-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f79a5-111">Aufzeichnen von MIDI-Audiodateien</span><span class="sxs-lookup"><span data-stu-id="f79a5-111">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 




