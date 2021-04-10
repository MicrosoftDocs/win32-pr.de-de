---
title: Audioformat
description: Audioformat
ms.assetid: a65dbd3f-1539-4f02-8573-c527c4e3c58d
keywords:
- WM_CAP_GET_AUDIOFORMAT Meldung
- capgetaudioformat-Makro
- capgetaudioformatsize-Makro
- WM_CAP_SET_AUDIOFORMAT Meldung
- capsetaudioformat-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e362abd393097ae8763b44b3ee3474685ffd5c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858181"
---
# <a name="audio-format"></a><span data-ttu-id="f9037-108">Audioformat</span><span class="sxs-lookup"><span data-stu-id="f9037-108">Audio Format</span></span>

<span data-ttu-id="f9037-109">Sie können das aktuelle Erfassungs Format für Audiodaten oder die Größe der audioformatstruktur abrufen, indem Sie die WM-Abdeckung [**\_ \_ get \_ Audioformat**](wm-cap-get-audioformat.md) -Nachricht (oder die Makros [**capgetaudioformat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) und [**capgetaudioformatsize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) ) an ein Erfassungsfenster senden.</span><span class="sxs-lookup"><span data-stu-id="f9037-109">You can retrieve the current capture format for audio data or the size of the audio format structure by sending the [**WM\_CAP\_GET\_AUDIOFORMAT**](wm-cap-get-audioformat.md) message (or the [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) and [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) macros) to a capture window.</span></span> <span data-ttu-id="f9037-110">Das Standardformat für die Audioerfassung ist Mono, 8-Bit, 11 kHz PCM (Pulse Code-Modulation).</span><span class="sxs-lookup"><span data-stu-id="f9037-110">The default audio capture format is mono, 8-bit, 11 kHz PCM (Pulse Code Modulation).</span></span> <span data-ttu-id="f9037-111">Wenn Sie das Format mit WM \_ Cap \_ get \_ Audioformat abrufen, verwenden Sie immer die [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f9037-111">When you retrieve the format by using WM\_CAP\_GET\_AUDIOFORMAT, always use the [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure.</span></span>

<span data-ttu-id="f9037-112">Sie können das Erfassungs Format für Audiodaten festlegen, indem Sie die " [**WM \_ Cap \_ Set \_ Audioformat**](wm-cap-set-audioformat.md) "-Nachricht (oder das " [**capsetaudioformat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) "-Makro) an ein Erfassungsfenster senden.</span><span class="sxs-lookup"><span data-stu-id="f9037-112">You can set the capture format for audio data by sending the [**WM\_CAP\_SET\_AUDIOFORMAT**](wm-cap-set-audioformat.md) message (or the [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) macro) to a capture window.</span></span> <span data-ttu-id="f9037-113">Beim Festlegen des Audioformats können Sie je nach angegebenem Audioformat einen Zeiger an eine [**wellenformat**](/windows/win32/api/mmreg/ns-mmreg-waveformat)-, **Wellen FORMATEX**-oder [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) -Struktur übergeben.</span><span class="sxs-lookup"><span data-stu-id="f9037-113">When setting the audio format, you can pass a pointer to a [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat), **WAVEFORMATEX**, or [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) structure, depending on the specified audio format.</span></span>

 

 