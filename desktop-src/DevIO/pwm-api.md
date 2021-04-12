---
description: Die Pulse Width-Modulation (Pulse Width Modulation, PWM) ist das Verfahren, mit dem eine rechteckige Pulse-Wave erzeugt wird, die eine Pulsbreite aufweist, die für die Variation des durchschnittlichen Werts des Waveforms-Werts zur Folge hat.
ms.assetid: 16B1E46F-2C42-4D94-949E-BE8F53EB1E1E
title: PWM-API
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 10b1951d9d96f49a9df9a51604767dbce360f9e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523643"
---
# <a name="pwm-api"></a>PWM-API

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die Pulse Width-Modulation (Pulse Width Modulation, PWM) ist das Verfahren, mit dem eine rechteckige Pulse-Wave erzeugt wird, die eine Pulsbreite aufweist, die für die Variation des durchschnittlichen Werts des Waveforms-Werts zur Folge hat. Zu den häufigsten Verwendungsmöglichkeiten gehören das Antreiben von Servomotoren, das Abdichten von LEDs oder andere verwandte Funktionen. PWM ist für die Verwendung in erster Linie für Internet der Dinge Szenarien vorgesehen.

## <a name="about-pulse-width-modulation"></a>Informationen zur Pulse Width-Modulation

Ein PWM-Wellenform kann nach zwei Parametern kategorisiert werden:

-   Ein Wellenform-Zeitraum (T)

-   Der Duty-Cycle, bei dem Wellenform Frequency (f) die gegenseitige des Zeitraums f = 1/T ist.

Der Duty Cycle beschreibt den Anteil der **auf** dem / **aktiven** Zeitpunkt in Bezug auf das reguläre Intervall oder den **Zeitraum** . Ein kostengünstiger Zeitraum entspricht dem Mittelwert einer geringen Ausgabe Leistung, da die Stromversorgung in den meisten Fällen deaktiviert ist. Der Duty Cycle wird als Prozentsatz ausgedrückt. Vollständig auf ist 100%. Vollständig deaktiviert ist 0%. Die **Hälfte der** Hälfte der Zeit beträgt 50%.

Entwickler, die PWM in ihren IOT-Anwendungen implementieren möchten, sollten die [WinRT PWM-Dokumentation](/uwp/api/windows.devices.pwm) untersuchen.

## <a name="pulse-width-modulation-types"></a>Pulse Width-Modultyp

PWM verwendet diese e/a- [Kontrollcodes](pwm-control-codes.md), [Strukturen](pwm-structures.md)und [Enumerationen.](pwm-enumeration-types.md)

PWM verwendet auch die folgende Funktion: [**pwmparamesepinpath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).

 

 
