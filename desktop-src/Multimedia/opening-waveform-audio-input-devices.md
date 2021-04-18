---
title: Öffnen Waveform-Audio Eingabegeräte
description: Öffnen Waveform-Audio Eingabegeräte
ms.assetid: 46cdbce6-2433-433a-abd2-39e4146aa2e9
keywords:
- Wellenform-Audiodatei, Öffnen von Eingabegeräten
- Waveform-Audioschnittstelle, Öffnen von Eingabegeräten
- Aufzeichnen von Wellenform-Audiodaten, Öffnen von Eingabegeräten
- Öffnen von Waveform-audioeingabegeräten
- Wavin Open-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92b7f49b9d170ceb8ebce287025ce0e0c1c5530
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337647"
---
# <a name="opening-waveform-audio-input-devices"></a><span data-ttu-id="c56bf-108">Öffnen Waveform-Audio Eingabegeräte</span><span class="sxs-lookup"><span data-stu-id="c56bf-108">Opening Waveform-Audio Input Devices</span></span>

<span data-ttu-id="c56bf-109">Verwenden Sie die [**waveinopen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) -Funktion, um ein Waveform-Audioeingabegerät für die Aufzeichnung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c56bf-109">Use the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function to open a waveform-audio input device for recording.</span></span> <span data-ttu-id="c56bf-110">Diese Funktion öffnet das Gerät, das dem angegebenen Geräte Bezeichner zugeordnet ist, und gibt ein Handle des geöffneten Geräts zurück, indem das Handle eines angegebenen Speicher Orts geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c56bf-110">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle of a specified memory location.</span></span>

<span data-ttu-id="c56bf-111">Einige Multimedia-Computer verfügen über mehrere Waveform-Audioeingabegeräte.</span><span class="sxs-lookup"><span data-stu-id="c56bf-111">Some multimedia computers have multiple waveform-audio input devices.</span></span> <span data-ttu-id="c56bf-112">Wenn Sie nicht wissen, dass Sie ein bestimmtes Waveform-Audioeingabegerät in einem System öffnen möchten, sollten Sie die Wave- \_ Mapper-Konstante für den Geräte Bezeichner verwenden, wenn Sie ein Gerät öffnen.</span><span class="sxs-lookup"><span data-stu-id="c56bf-112">Unless you know you want to open a specific waveform-audio input device in a system, you should use the WAVE\_MAPPER constant for the device identifier when you open a device.</span></span> <span data-ttu-id="c56bf-113">Die [**Wavin Open**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) -Funktion wählt das Gerät im System aus, das im angegebenen Datenformat am besten aufgezeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c56bf-113">The [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function will choose the device in the system best able to record in the specified data format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c56bf-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c56bf-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c56bf-115">Aufzeichnen von Waveform-Audiodaten</span><span class="sxs-lookup"><span data-stu-id="c56bf-115">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 