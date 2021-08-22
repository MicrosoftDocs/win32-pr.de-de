---
title: Abrufen der aktuellen Wiedergabeposition
description: Abrufen der aktuellen Wiedergabeposition
ms.assetid: a08fe5da-8945-486f-9413-877c7d13d5de
keywords:
- Waveformaudio, aktuelle Wiedergabeposition
- Waveform-Audioschnittstelle, aktuelle Wiedergabeposition
- Wiedergabe von Waveform-Audiodateien, aktuelle Wiedergabeposition
- waveOutGetPosition-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85bc46e476786625ccae51802e0b720379a935110eb37d941c4c76d69d94783
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689050"
---
# <a name="retrieving-the-current-playback-position"></a>Abrufen der aktuellen Wiedergabeposition

Sie können die aktuelle Wiedergabeposition innerhalb der Datei überwachen, während Waveformaudio mithilfe der [**waveOutGetPosition-Funktion abspielt.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition)

Bei Waveform-Audiogeräten sind Beispiele das bevorzugte Zeitformat, in dem die aktuelle Position angezeigt werden soll. Daher wird die aktuelle Position eines Waveform-Audiogeräts als Anzahl von Stichproben für einen Kanal ab dem Anfang der Waveform-Audiodatei angegeben. Legen Sie zum Abfragen der aktuellen Position eines Waveform-Audio-Geräts den **wType-Member** der [**MMTIME-Struktur**](/previous-versions//dd757347(v=vs.85)) auf TIME SAMPLES fest, und übergeben Sie diese Struktur \_ an **waveOutGetPosition**.

Die **MMTIME-Struktur** kann die Zeit in einem oder in verschiedenen Formaten darstellen, einschließlich Millisekunden, Stichproben, SMPTE (Society of Motion Picture and Tv Engineers) und DANN-Titelzeigerformaten. Der **wType-Member** gibt das Format an, das zum Darstellen der Zeit verwendet wird. Bevor Sie eine Funktion aufrufen, die die **MMTIME-Struktur** verwendet, müssen Sie **wType** festlegen, um das angeforderte Zeitformat anzugeben. Überprüfen Sie nach dem Aufruf **wType,** um festzustellen, ob das angeforderte Zeitformat unterstützt wird. Wenn das angeforderte Zeitformat nicht unterstützt wird, gibt der Gerätetreiber die Uhrzeit in einem alternativen Zeitformat an und ändert den **wType-Member** in das ausgewählte Zeitformat.

Weitere Informationen zur **MMTIME-Struktur** finden Sie unter [Multimedia-Timer.](multimedia-timers.md)

 

 