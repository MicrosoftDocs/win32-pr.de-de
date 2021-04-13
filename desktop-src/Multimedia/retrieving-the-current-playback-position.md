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
# <a name="retrieving-the-current-playback-position"></a>Abrufen der aktuellen Wiedergabe Position

Sie können die aktuelle Wiedergabe Position innerhalb der Datei überwachen, während das Wellenform-Audioformat mithilfe der [**waveoutgetposition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) -Funktion wiedergegeben wird.

Bei Waveform-Audiogeräten sind Beispiele das bevorzugte Zeitformat, in dem die aktuelle Position dargestellt werden soll. Folglich wird die aktuelle Position eines Waveform-Audiogeräts als Anzahl von Stichproben für einen Kanal vom Anfang der Waveform-Audiodatei angegeben. Um die aktuelle Position eines Waveform-Audiogeräts abzufragen, legen Sie den **wType** -Member der [**mmtime**](/previous-versions//dd757347(v=vs.85)) -Struktur auf Zeit Beispiele fest, \_ und übergeben Sie diese Struktur an **waveoutgetposition**.

Die **mmtime** -Struktur kann Zeit in einem oder mehreren unterschiedlichen Formaten darstellen, einschließlich Millisekunden, Samplings, SMPTE (Society of Motion Picture and TV Engineers) und Formatvorlagen-Formatvorlagen. Der **wType** -Member gibt das Format an, das zum Darstellen der Zeit verwendet wird. Bevor Sie eine Funktion aufrufen, die die **mmtime** -Struktur verwendet, müssen Sie **wType** festlegen, um das angeforderte Zeitformat anzugeben. Überprüfen Sie nach dem Aufruf von **wType** , ob das angeforderte Zeitformat unterstützt wird. Wenn das angeforderte Zeitformat nicht unterstützt wird, gibt der Gerätetreiber die Uhrzeit in einem alternativen Zeitformat an und ändert das **wType** -Element in das ausgewählte Uhrzeit Format.

Weitere Informationen zur **mmtime** -Struktur finden Sie unter [Multimedia-Timer](multimedia-timers.md).

 

 