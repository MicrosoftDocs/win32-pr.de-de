---
description: Pulse Width Wave (PWM) ist das Verfahren zum Generieren einer rechteckigen Pulse Wave mit einer Pulsbreite, die moduliert wird, um die Variation des Durchschnittswerts der Wellenform zu erzeugen.
ms.assetid: 16B1E46F-2C42-4D94-949E-BE8F53EB1E1E
title: PWM-API
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ff257007180cf3da2b78c14415c8fa350b4bb395e0202f49d2d7ae056f025bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405194"
---
# <a name="pwm-api"></a>PWM-API

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Pulse Width Wave (PWM) ist das Verfahren zum Generieren einer rechteckigen Pulse Wave mit einer Pulsbreite, die moduliert wird, um die Variation des Durchschnittswerts der Wellenform zu erzeugen. Zu den gängigsten Verwendungsmöglichkeiten zählen das Fahren mit 35000Erfahren, das Abblenden von LEDs oder andere verwandte Funktionen. PWM ist für die Verwendung in erster Linie für Internet der Dinge vorgesehen.

## <a name="about-pulse-width-modulation"></a>Informationen zu Pulse Width Pulse

Eine PWM-Wellenform kann nach zwei Parametern kategorisiert werden:

-   Ein Wellenformzeitraum (T)

-   Der Pflichtzyklus, bei dem die Wellenformfrequenz (f) der Reziprok des Zeitraums f=1/T ist.

Der Pflichtzyklus beschreibt den Anteil der **zur** aktiven Zeit in Bezug auf das reguläre Intervall /  oder **den Zeitraum.** Ein Zyklus mit niedriger Leistung entspricht einem Durchschnitt einer niedrigen Ausgangsleistung, da die Stromversorgung in den meisten Jahren ausgeschaltet ist. Der Steuerzyklus wird als Prozentsatz ausgedrückt. Vollständig ein ist 100 %. Vollständig deaktiviert ist 0 %. **Die** aktive Hälfte der Zeit beträgt 50 %.

Entwickler, die PWM in ihre IoT-Anwendungen implementieren möchten, sollten die [WinRT PWM-Dokumentation untersuchen.](/uwp/api/windows.devices.pwm)

## <a name="pulse-width-modulation-types"></a>Pulse Width Pulse-Typen

PWM verwendet [diese E/A-Steuerungscodes,](pwm-control-codes.md) [-Strukturen](pwm-structures.md)und [-Enumerationen.](pwm-enumeration-types.md)

PWM verwendet auch die folgende Funktion: [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).

 

 
