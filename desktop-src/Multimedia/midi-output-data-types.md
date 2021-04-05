---
title: Datentypen der MIDI-Ausgabe
description: Datentypen der MIDI-Ausgabe
ms.assetid: d0cb0614-e979-4b9f-81ce-13457fdde906
keywords:
- Digital Instrumentation Digital Interface (MIDI), Ausgabe Datentypen
- MIDI (Digital Instrumentation Digital Interface), Ausgabe Datentypen
- Abspielen von MIDI-Dateien, Ausgabe Datentypen
- Datentypen der MIDI-Ausgabe
- Midihdr-Datentyp
- Midioutcaps-Datentyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57911800e0d45c1db515e5b57045aae3856732c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726328"
---
# <a name="midi-output-data-types"></a><span data-ttu-id="5c78c-109">Datentypen der MIDI-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5c78c-109">MIDI Output Data Types</span></span>

<span data-ttu-id="5c78c-110">Windows definiert die folgenden Datentypen für die Funktionen von MIDI-Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="5c78c-110">Windows defines the following data types for MIDI output functions.</span></span>



| <span data-ttu-id="5c78c-111">Wert</span><span class="sxs-lookup"><span data-stu-id="5c78c-111">Value</span></span>                              | <span data-ttu-id="5c78c-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5c78c-112">Meaning</span></span>                                                                              |
|------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5c78c-113">**Hmidiout**</span><span class="sxs-lookup"><span data-stu-id="5c78c-113">**HMIDIOUT**</span></span>                       | <span data-ttu-id="5c78c-114">Handle eines MIDI-Ausgabegeräts.</span><span class="sxs-lookup"><span data-stu-id="5c78c-114">Handle of a MIDI output device.</span></span>                                                      |
| [<span data-ttu-id="5c78c-115">**Midihdr**</span><span class="sxs-lookup"><span data-stu-id="5c78c-115">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)         | <span data-ttu-id="5c78c-116">-Header für einen Block von System exklusiven oder Streamingdaten des systemeigenen Systems.</span><span class="sxs-lookup"><span data-stu-id="5c78c-116">Header for a block of MIDI system-exclusive or stream data.</span></span>                          |
| [<span data-ttu-id="5c78c-117">**Midioutcaps**</span><span class="sxs-lookup"><span data-stu-id="5c78c-117">**MIDIOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) | <span data-ttu-id="5c78c-118">Struktur, die verwendet wird, um die Funktionen eines bestimmten MIDI-Ausgabegeräts zu Fragen.</span><span class="sxs-lookup"><span data-stu-id="5c78c-118">Structure used to inquire about the capabilities of a particular MIDI output device.</span></span> |



 

 

 