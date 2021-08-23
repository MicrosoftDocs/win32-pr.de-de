---
description: Pulse Width Generator (PWM) ist die Technik zum Generieren einer rechteckigen Pulse-Welle, die eine Pulsebreite aufweist, die moduliert wird, um die Variation des Durchschnittswerts der Wellenform zu erzielen.
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

Pulse Width Generator (PWM) ist die Technik zum Generieren einer rechteckigen Pulse-Welle, die eine Pulsebreite aufweist, die moduliert wird, um die Variation des Durchschnittswerts der Wellenform zu erzielen. Die gängigsten Verwendungsmöglichkeiten sind fahrbare Fahrten, abgeblendbare LEDs oder andere verwandte Funktionen. PWM ist in erster Linie für Internet der Dinge Szenarien vorgesehen.

## <a name="about-pulse-width-modulation"></a>Informationen zu Pulse Width Pulse

Eine PWM-Wellenform kann nach zwei Parametern kategorisiert werden:

-   Ein Wellenformzeitraum (T)

-   Der Arbeitszyklus, wobei die Wellenfrequenz (f) der Reziprok des Zeitraums f=1/T ist.

Der Arbeitszyklus beschreibt den Anteil der aktiven Zeit in /  Bezug auf das reguläre Intervall oder den **Zeitraum.** Ein niedriger Leistungszyklus entspricht dem Durchschnitt einer niedrigen Ausgabeleistung, da der Strom meistens ausgeschaltet ist. Der Arbeitszyklus wird als Prozentsatz ausgedrückt. Vollständig aktiviert ist 100 %. "Vollständig deaktiviert" beträgt 0 %. **Die** Aktive Hälfte der Zeit beträgt 50 %.

Entwickler, die PWM in ihre IoT-Anwendungen implementieren möchten, sollten die [WinRT PWM-Dokumentation untersuchen.](/uwp/api/windows.devices.pwm)

## <a name="pulse-width-modulation-types"></a>Pulse Width Pulse-Typen

PWM verwendet [diese E/A-Steuerungscodes,](pwm-control-codes.md) [Strukturen](pwm-structures.md)und [Enumerationen.](pwm-enumeration-types.md)

PWM verwendet auch die folgende Funktion: [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).

 

 
