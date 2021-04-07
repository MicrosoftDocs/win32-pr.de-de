---
title: Eingabe Datentypen Waveform-Audio
description: Eingabe Datentypen Waveform-Audio
ms.assetid: dfedcb93-edfb-4a25-8445-95d4aee55734
keywords:
- Wellenform-Audiodaten, Eingabe Datentypen
- Waveform-Audioschnittstelle, Eingabe Datentypen
- Aufzeichnen von Wellenform-Audiodaten, Eingabe Datentypen
- Hwavein-handle
- WaveFormatEx-Struktur
- Wavehdr-Struktur
- Wavin Caps-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8d37869224fe2ce677e2b8b952030ca6e021f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038921"
---
# <a name="waveform-audio-input-data-types"></a><span data-ttu-id="78148-110">Eingabe Datentypen Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="78148-110">Waveform-Audio Input Data Types</span></span>

<span data-ttu-id="78148-111">Die folgenden Datentypen werden für die Eingabefunktionen von Waveform-Audiodaten definiert.</span><span class="sxs-lookup"><span data-stu-id="78148-111">The following data types are defined for waveform-audio input functions.</span></span>



| <span data-ttu-id="78148-112">type</span><span class="sxs-lookup"><span data-stu-id="78148-112">Type</span></span>                                 | <span data-ttu-id="78148-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78148-113">Description</span></span>                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78148-114">**Hwavein**</span><span class="sxs-lookup"><span data-stu-id="78148-114">**HWAVEIN**</span></span>                          | <span data-ttu-id="78148-115">Handle eines geöffneten Waveform-Audioeingabegeräts.</span><span class="sxs-lookup"><span data-stu-id="78148-115">Handle of an open waveform-audio input device.</span></span>                                                                                                                  |
| [<span data-ttu-id="78148-116">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="78148-116">**WAVEFORMATEX**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | <span data-ttu-id="78148-117">-Struktur, die die von einem bestimmten Waveform-Audioeingabegerät unterstützten Datenformate angibt.</span><span class="sxs-lookup"><span data-stu-id="78148-117">Structure that specifies the data formats supported by a particular waveform-audio input device.</span></span> <span data-ttu-id="78148-118">Diese Struktur wird auch für Waveform-Audioausgabegeräte verwendet.</span><span class="sxs-lookup"><span data-stu-id="78148-118">This structure is also used for waveform-audio output devices.</span></span> |
| [<span data-ttu-id="78148-119">**Wavehdr**</span><span class="sxs-lookup"><span data-stu-id="78148-119">**WAVEHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | <span data-ttu-id="78148-120">Struktur, die als Header für einen Block von Waveform-audioeingabedaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="78148-120">Structure used as a header for a block of waveform-audio input data.</span></span> <span data-ttu-id="78148-121">Diese Struktur wird auch für Waveform-Audioausgabegeräte verwendet.</span><span class="sxs-lookup"><span data-stu-id="78148-121">This structure is also used for waveform-audio output devices.</span></span>                             |
| [<span data-ttu-id="78148-122">**Wavin Caps**</span><span class="sxs-lookup"><span data-stu-id="78148-122">**WAVEINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)     | <span data-ttu-id="78148-123">Struktur, die verwendet wird, um die Funktionen eines bestimmten Waveform-Audioeingabegeräts zu Fragen.</span><span class="sxs-lookup"><span data-stu-id="78148-123">Structure used to inquire about the capabilities of a particular waveform-audio input device.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="78148-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="78148-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78148-125">Aufzeichnen von Waveform-Audiodaten</span><span class="sxs-lookup"><span data-stu-id="78148-125">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 