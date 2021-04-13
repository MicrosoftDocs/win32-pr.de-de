---
title: Abrufen der aktuellen Wiedergabe Position
description: Abrufen der aktuellen Wiedergabe Position
ms.assetid: a08fe5da-8945-486f-9413-877c7d13d5de
keywords:
- Wellenform-Audiodatei, aktuelle Wiedergabe Position
- Waveform-Audioschnittstelle, aktuelle Wiedergabe Position
- Wiedergeben von Waveform-Audiodateien, aktuelle Wiedergabe Position
- waveoutgetposition-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28737cfc292dc8779b21756f38813642b82e452
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314673"
---
# <a name="retrieving-the-current-playback-position"></a><span data-ttu-id="6aa5b-107">Abrufen der aktuellen Wiedergabe Position</span><span class="sxs-lookup"><span data-stu-id="6aa5b-107">Retrieving the Current Playback Position</span></span>

<span data-ttu-id="6aa5b-108">Sie können die aktuelle Wiedergabe Position innerhalb der Datei überwachen, während das Wellenform-Audioformat mithilfe der [**waveoutgetposition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) -Funktion wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6aa5b-108">You can monitor the current playback position within the file while waveform audio is playing by using the [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) function.</span></span>

<span data-ttu-id="6aa5b-109">Bei Waveform-Audiogeräten sind Beispiele das bevorzugte Zeitformat, in dem die aktuelle Position dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6aa5b-109">For waveform-audio devices, samples are the preferred time format in which to represent the current position.</span></span> <span data-ttu-id="6aa5b-110">Folglich wird die aktuelle Position eines Waveform-Audiogeräts als Anzahl von Stichproben für einen Kanal vom Anfang der Waveform-Audiodatei angegeben.</span><span class="sxs-lookup"><span data-stu-id="6aa5b-110">Thus, the current position of a waveform-audio device is specified as the number of samples for one channel from the beginning of the waveform-audio file.</span></span> <span data-ttu-id="6aa5b-111">Um die aktuelle Position eines Waveform-Audiogeräts abzufragen, legen Sie den **wType** -Member der [**mmtime**](/previous-versions//dd757347(v=vs.85)) -Struktur auf Zeit Beispiele fest, \_ und übergeben Sie diese Struktur an **waveoutgetposition**.</span><span class="sxs-lookup"><span data-stu-id="6aa5b-111">To query the current position of a waveform-audio device, set the **wType** member of the [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure to TIME\_SAMPLES and pass this structure to **waveOutGetPosition**.</span></span>

<span data-ttu-id="6aa5b-112">Die **mmtime** -Struktur kann Zeit in einem oder mehreren unterschiedlichen Formaten darstellen, einschließlich Millisekunden, Samplings, SMPTE (Society of Motion Picture and TV Engineers) und Formatvorlagen-Formatvorlagen.</span><span class="sxs-lookup"><span data-stu-id="6aa5b-112">The **MMTIME** structure can represent time in one or more different formats, including milliseconds, samples, SMPTE (Society of Motion Picture and Television Engineers), and MIDI song pointer formats.</span></span> <span data-ttu-id="6aa5b-113">Der **wType** -Member gibt das Format an, das zum Darstellen der Zeit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6aa5b-113">The **wType** member specifies the format used to represent time.</span></span> <span data-ttu-id="6aa5b-114">Bevor Sie eine Funktion aufrufen, die die **mmtime** -Struktur verwendet, müssen Sie **wType** festlegen, um das angeforderte Zeitformat anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6aa5b-114">Before calling a function that uses the **MMTIME** structure, you must set **wType** to indicate your requested time format.</span></span> <span data-ttu-id="6aa5b-115">Überprüfen Sie nach dem Aufruf von **wType** , ob das angeforderte Zeitformat unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="6aa5b-115">Be sure to check **wType** after the call to see whether the requested time format is supported.</span></span> <span data-ttu-id="6aa5b-116">Wenn das angeforderte Zeitformat nicht unterstützt wird, gibt der Gerätetreiber die Uhrzeit in einem alternativen Zeitformat an und ändert das **wType** -Element in das ausgewählte Uhrzeit Format.</span><span class="sxs-lookup"><span data-stu-id="6aa5b-116">If the requested time format is not supported, the device driver specifies the time in an alternate time format and changes the **wType** member to the selected time format.</span></span>

<span data-ttu-id="6aa5b-117">Weitere Informationen zur **mmtime** -Struktur finden Sie unter [Multimedia-Timer](multimedia-timers.md).</span><span class="sxs-lookup"><span data-stu-id="6aa5b-117">For more information about the **MMTIME** structure, see [Multimedia Timers](multimedia-timers.md).</span></span>

 

 