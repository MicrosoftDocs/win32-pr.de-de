---
title: Abfragen von Waveform-Audio Eingabegeräten
description: Abfragen von Waveform-Audio Eingabegeräten
ms.assetid: 573b33bc-f445-496e-a0e6-0194d30bb668
keywords:
- Wellenform-Audiodaten, Abfragen von Eingabegeräten
- Waveform-Audioschnittstelle, Abfragen von Eingabegeräten
- Aufzeichnen von Wellenform-Audiodaten, Abfragen von Eingabegeräten
- Abfragen von Waveform-Audioeingabegeräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b915b3f39ad417a3d92396d887e5fb66092119
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948679"
---
# <a name="querying-waveform-audio-input-devices"></a><span data-ttu-id="be73a-107">Abfragen von Waveform-Audio Eingabegeräten</span><span class="sxs-lookup"><span data-stu-id="be73a-107">Querying Waveform-Audio Input Devices</span></span>

<span data-ttu-id="be73a-108">Vor dem Aufzeichnen von Wellenform-Audiodaten sollten Sie die [**waveingetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) -Funktion aufrufen, um die Wellenform-audioeingabefunktionen des Systems zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="be73a-108">Before recording waveform audio, you should call the [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) function to determine the waveform-audio input capabilities of the system.</span></span> <span data-ttu-id="be73a-109">Diese Funktion füllt eine [**waveincaps**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) -Struktur mit Informationen über die Funktionen eines angegebenen Geräts aus.</span><span class="sxs-lookup"><span data-stu-id="be73a-109">This function fills a [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) structure with information about the capabilities of a specified device.</span></span> <span data-ttu-id="be73a-110">Diese Informationen umfassen die Hersteller-und Produkt-IDs, einen Produktnamen für das Gerät und die Versionsnummer des Gerätetreibers.</span><span class="sxs-lookup"><span data-stu-id="be73a-110">This information includes the manufacturer and product identifiers, a product name for the device, and the version number of the device driver.</span></span> <span data-ttu-id="be73a-111">Außerdem bietet die **waveincaps** -Strukturinformationen zu den standardmäßigen Waveform-Audioformaten, die das Gerät unterstützt.</span><span class="sxs-lookup"><span data-stu-id="be73a-111">In addition, the **WAVEINCAPS** structure provides information about the standard waveform-audio formats that the device supports.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be73a-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="be73a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be73a-113">Aufzeichnen von Waveform-Audiodaten</span><span class="sxs-lookup"><span data-stu-id="be73a-113">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 