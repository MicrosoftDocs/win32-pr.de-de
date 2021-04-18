---
title: Abfragen von MIDI-Eingabegeräten
description: Abfragen von MIDI-Eingabegeräten
ms.assetid: 2da88418-f9cf-49da-b17f-8a26d357b5ab
keywords:
- Digital Instrumentation Digital Interface (MIDI), Eingabegeräte
- MIDI (Digital Instrumentation Digital Interface), Eingabegeräte
- Aufzeichnen von MIDI-Audiodaten, Eingabegeräte
- MIDI-Eingabegeräte
- Digital Instrumentation Digital Interface (MIDI), Abfragen von Eingabegeräten
- MIDI (Digital Instrumentation Digital Interface), Abfragen von Eingabegeräten
- Aufzeichnen von MIDI-Audiodaten, Abfragen von Eingabegeräten
- Abfragen von MIDI-Eingabegeräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a92bec8733887e20c25f37d1de3dd493e555c8a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337221"
---
# <a name="querying-midi-input-devices"></a><span data-ttu-id="d315b-111">Abfragen von MIDI-Eingabegeräten</span><span class="sxs-lookup"><span data-stu-id="d315b-111">Querying MIDI Input Devices</span></span>

<span data-ttu-id="d315b-112">Vor dem Aufzeichnen von MIDI-Audiodaten sollten Sie die Funktion " [**midiingetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) " verwenden, um die Funktionen des im System vorhandenen MIDI-Eingabe Geräts zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="d315b-112">Before recording MIDI audio, you should use the [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) function to determine the capabilities of the MIDI input device that is present in the system.</span></span> <span data-ttu-id="d315b-113">Diese Funktion verwendet eine Adresse einer [**midiincaps**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) -Struktur, die Informationen zu den Funktionen des jeweiligen Geräts füllt.</span><span class="sxs-lookup"><span data-stu-id="d315b-113">This function takes an address of a [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) structure, which it fills with information about the capabilities of the given device.</span></span> <span data-ttu-id="d315b-114">Diese Informationen umfassen die Hersteller-und Produkt-IDs, einen Produktnamen für das Gerät und die Versionsnummer des Gerätetreibers.</span><span class="sxs-lookup"><span data-stu-id="d315b-114">This information includes the manufacturer and product identifiers, a product name for the device, and the version number of the device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d315b-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d315b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d315b-116">Aufzeichnen von MIDI-Audiodateien</span><span class="sxs-lookup"><span data-stu-id="d315b-116">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 