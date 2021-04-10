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
# <a name="audio-format"></a>Audioformat

Sie können das aktuelle Erfassungs Format für Audiodaten oder die Größe der audioformatstruktur abrufen, indem Sie die WM-Abdeckung [**\_ \_ get \_ Audioformat**](wm-cap-get-audioformat.md) -Nachricht (oder die Makros [**capgetaudioformat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) und [**capgetaudioformatsize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) ) an ein Erfassungsfenster senden. Das Standardformat für die Audioerfassung ist Mono, 8-Bit, 11 kHz PCM (Pulse Code-Modulation). Wenn Sie das Format mit WM \_ Cap \_ get \_ Audioformat abrufen, verwenden Sie immer die [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -Struktur.

Sie können das Erfassungs Format für Audiodaten festlegen, indem Sie die " [**WM \_ Cap \_ Set \_ Audioformat**](wm-cap-set-audioformat.md) "-Nachricht (oder das " [**capsetaudioformat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) "-Makro) an ein Erfassungsfenster senden. Beim Festlegen des Audioformats können Sie je nach angegebenem Audioformat einen Zeiger an eine [**wellenformat**](/windows/win32/api/mmreg/ns-mmreg-waveformat)-, **Wellen FORMATEX**-oder [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) -Struktur übergeben.

 

 