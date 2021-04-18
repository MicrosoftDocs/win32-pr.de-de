---
title: Datentypen der MIDI-Eingabe
description: Datentypen der MIDI-Eingabe
ms.assetid: c67f149e-60b8-4f9e-8e3c-a88cd579d29f
keywords:
- Digital Instrumentation Digital Interface (MIDI), Eingabe Datentypen
- MIDI (Digital Instrumentation Digital Interface), Eingabe Datentypen
- Aufzeichnen von MIDI-Audiodaten, Eingabe Datentypen
- Datentypen der MIDI-Eingabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f0738827cce4cfd8cb4a237dcd2031c2fe71a7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340264"
---
# <a name="midi-input-data-types"></a><span data-ttu-id="a681b-107">Datentypen der MIDI-Eingabe</span><span class="sxs-lookup"><span data-stu-id="a681b-107">MIDI Input Data Types</span></span>

<span data-ttu-id="a681b-108">Windows definiert die folgenden Datentypen für die MIDI-Eingabefunktionen.</span><span class="sxs-lookup"><span data-stu-id="a681b-108">Windows defines the following data types for the MIDI input functions.</span></span>



| <span data-ttu-id="a681b-109">Wert</span><span class="sxs-lookup"><span data-stu-id="a681b-109">Value</span></span>                            | <span data-ttu-id="a681b-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a681b-110">Meaning</span></span>                                                                                                                                                                                     |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a681b-111">**Hmidiin**</span><span class="sxs-lookup"><span data-stu-id="a681b-111">**HMIDIIN**</span></span>                      | <span data-ttu-id="a681b-112">Handle eines MIDI-Eingabe Geräts.</span><span class="sxs-lookup"><span data-stu-id="a681b-112">Handle of a MIDI input device.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="a681b-113">**Midihdr**</span><span class="sxs-lookup"><span data-stu-id="a681b-113">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)       | <span data-ttu-id="a681b-114">Header für einen Streampuffer oder einen Block von System exklusiven systemeigenen Systemdaten.</span><span class="sxs-lookup"><span data-stu-id="a681b-114">Header for a stream buffer or a block of MIDI system-exclusive data.</span></span> <span data-ttu-id="a681b-115">Bei Eingabe Anwendungen zeichnet diese Struktur nur System exklusive Daten auf (das Streaming wird für eine MIDI-Eingabe nicht unterstützt).</span><span class="sxs-lookup"><span data-stu-id="a681b-115">For input applications, this structure records only system-exclusive data (streaming is not supported for MIDI input).</span></span> |
| [<span data-ttu-id="a681b-116">**Midiincaps**</span><span class="sxs-lookup"><span data-stu-id="a681b-116">**MIDIINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) | <span data-ttu-id="a681b-117">Struktur, die verwendet wird, um die Funktionen eines MIDI-Eingabe Geräts zu Fragen.</span><span class="sxs-lookup"><span data-stu-id="a681b-117">Structure used to inquire about the capabilities of a MIDI input device.</span></span>                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="a681b-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a681b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a681b-119">Aufzeichnen von MIDI-Audiodateien</span><span class="sxs-lookup"><span data-stu-id="a681b-119">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 