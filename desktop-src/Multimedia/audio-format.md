---
title: Audioformat
description: Audioformat
ms.assetid: a65dbd3f-1539-4f02-8573-c527c4e3c58d
keywords:
- WM_CAP_GET_AUDIOFORMAT-Nachricht
- capGetAudioFormat-Makro
- capGetAudioFormatSize-Makro
- WM_CAP_SET_AUDIOFORMAT Nachricht
- capSetAudioFormat-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5891e8c244487895c51d68dd92fc4935f8981a36cf67d81437ff45f58950527b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375699"
---
# <a name="audio-format"></a>Audioformat

Sie können das aktuelle Erfassungsformat für Audiodaten oder die Größe der Audioformatstruktur abrufen, indem Sie die [**WM \_ CAP GET \_ \_ AUDIOFORMAT-Nachricht**](wm-cap-get-audioformat.md) (oder die Makros [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) und [**capGetAudioFormatSize)**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) an ein Aufnahmefenster senden. Das Standardformat für audio capture ist mono, 8-Bit, 11 kHz PCM (Pulse Code Codes). Wenn Sie das Format mit WM \_ CAP \_ GET \_ AUDIOFORMAT abrufen, verwenden Sie immer die [**WAVEFORMATEX-Struktur.**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)

Sie können das Erfassungsformat für Audiodaten festlegen, indem Sie die [**WM \_ CAP SET \_ \_ AUDIOFORMAT-Nachricht**](wm-cap-set-audioformat.md) (oder das [**Makro capSetAudioFormat)**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) an ein Erfassungsfenster senden. Beim Festlegen des Audioformats können Sie je nach angegebenem Audioformat einen Zeiger auf eine [**WAVEFORMAT-,**](/windows/win32/api/mmreg/ns-mmreg-waveformat) **WAVEFORMATEX-** oder [**PCMWAVEFORMAT-Struktur**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) übergeben.

 

 