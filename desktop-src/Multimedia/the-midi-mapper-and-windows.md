---
title: Der MIDI-Mapper und Windows
description: Der MIDI-Mapper und Windows
ms.assetid: a077f935-e085-4148-9975-7926ac018f0c
keywords:
- Digital Instrumentation Digital Interface (MIDI), MIDI-Mapper
- MIDI (Digital Instrumentation Digital Interface), MIDI-Mapper
- MIDI-Mapper, Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad3cee4fb37de6ecbfdc4f81860afcb9f589d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038923"
---
# <a name="the-midi-mapper-and-windows"></a><span data-ttu-id="866c1-106">Der MIDI-Mapper und Windows</span><span class="sxs-lookup"><span data-stu-id="866c1-106">The MIDI Mapper and Windows</span></span>

<span data-ttu-id="866c1-107">Der MIDI-Mapper ist Teil der Systemsoftware.</span><span class="sxs-lookup"><span data-stu-id="866c1-107">The MIDI Mapper is part of the system software.</span></span> <span data-ttu-id="866c1-108">In der folgenden Abbildung wird gezeigt, wie sich der MIDI-Mapper auf andere Elemente der Audiodienste bezieht.</span><span class="sxs-lookup"><span data-stu-id="866c1-108">The following illustration shows how the MIDI Mapper relates to other elements of the audio services.</span></span>

![Beziehung des MIDI-Mappers mit anderen Elementen des audiodienstebilds](images/mmap-a01.gif)

<span data-ttu-id="866c1-110">Vom Standpunkt einer Anwendung aus sieht der MIDI-Mapper wie ein anderes MIDI-Ausgabegerät aus.</span><span class="sxs-lookup"><span data-stu-id="866c1-110">From the viewpoint of an application, the MIDI Mapper looks like another MIDI output device.</span></span> <span data-ttu-id="866c1-111">Der MIDI-Mapper empfängt die an ihn gesendeten Nachrichten von den " [**midioutshortmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) " und " [**midioutlongmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)" auf niedriger Ebene.</span><span class="sxs-lookup"><span data-stu-id="866c1-111">The MIDI Mapper receives messages sent to it by the low-level MIDI output functions [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) and [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg).</span></span> <span data-ttu-id="866c1-112">Der MIDI-Mapper ändert diese Nachrichten und leitet Sie entsprechend der aktuellen Registerkarte für das MIDI-Setup an ein MIDI-Ausgabegerät weiter.</span><span class="sxs-lookup"><span data-stu-id="866c1-112">The MIDI Mapper modifies these messages and redirects them to a MIDI output device according to the current MIDI setup map.</span></span> <span data-ttu-id="866c1-113">Die aktuelle Zuordnung von "MIDI-Setup" wird vom Benutzer mithilfe der System Steuerungs Option "MIDI" ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="866c1-113">The current MIDI setup map is selected by the user by means of the MIDI Control Panel option.</span></span> <span data-ttu-id="866c1-114">Nur der Benutzer kann die aktuelle Setup Zuordnung auswählen. die aktuelle Setup Zuordnung kann von Anwendungen nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="866c1-114">Only the user can select the current setup map; applications cannot change the current setup map.</span></span>

 

 