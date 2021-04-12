---
description: In diesem Thema wird der IOCTLs-Code für die Pulse Width-Modulation aufgeführt.
ms.assetid: 2ED7A06A-A7EC-4C44-AB22-4A52CF2DF2C5
title: PWM-Steuerungs Codes
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: de7de81b26a1970bbecde76729be2f1c84e6c067
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958192"
---
# <a name="pwm-control-codes"></a>PWM-Steuerungs Codes

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

In diesem Thema wird der IOCTLs-Code für die Pulse Width-Modulation aufgeführt.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IOCTL \_ PWM- \_ Controller \_ get \_ tatsächlicher \_ Zeitraum**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_get_actual_period)<br/>                   | Ruft den effektiven Ausgabesignal Zeitraum des PWM-Controllers (Pulse Width Modulation) ab, wie er auf seine Ausgabekanäle gemessen würde.<br/>                                                                                                                                                                                  |
| [**IOCTL \_ PWM \_ Controller \_ get \_ Info**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_get_info)<br/>                                      | Ruft Informationen zu einem PWM-Controller (Pulse Width Modulation) ab. Diese Informationen werden nicht geändert, nachdem der Controller initialisiert wurde. <br/>                                                                                                                                                                                |
| [**IOCTL \_ PWM-Controller hat den \_ \_ \_ gewünschten Zeitraum festgelegt \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_set_desired_period)<br/>                 | Legt den Ausgabesignal Zeitraum eines PWM-Controllers (Pulse Width Modulation) auf einen empfohlenen Wert fest. <br/>                                                                                                                                                                                                                            |
| [**IOCTL \_ PWM- \_ Pin \_ get \_ Active \_ Duty \_ Cycle \_ Prozent**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_get_active_duty_cycle_percentage)<br/> | Ruft den aktuellen Duty-Cycle-Prozentsatz für eine PIN oder einen Kanal ab. Der Code des Steuer Elements gibt den Prozentsatz als [**PWM- \_ Pin \_ get \_ Active \_ Duty \_ Cycle \_ Prozent der \_ Ausgabe**](pwm-pin-get-active-duty-cycle-percentage-output.md) Struktur zurück.<br/>                                                                                  |
| [**IOCTL \_ PWM \_ Pin \_ Set \_ Active \_ Duty \_ Cycle \_ Prozentsatz**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_set_active_duty_cycle_percentage)<br/> | Legen Sie einen Prozentwert für den gewünschten Duty-Cycle-Wert für die Controller-Pin oder den Der Code des Steuer Elements gibt den Prozentsatz als PWM-Pin-Satz- [**\_ \_ \_ \_ \_ \_ \_ Eingabe**](pwm-pin-set-active-duty-cycle-percentage-input.md) Struktur in Prozent an. <br/>                                                                      |
| [**IOCTL \_ PWM- \_ Pin \_ get \_ Polarität**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_get_polarity)<br/>                                            | Ruft die aktuelle Signalpolarität der PIN oder des Kanals ab. Der Steuercode Ruft die Signalpolarität als [**PWM- \_ Pin \_ get \_ Polarität- \_ Ausgabe**](pwm-pin-get-polarity-output.md) Struktur ab. Die Signalpolarität ist entweder "hoch" oder "aktiv", wie in der [**PWM- \_ Polarität**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) -Enumeration definiert. <br/> |
| [**IOCTL \_ PWM- \_ Pin \_ Satz- \_ Polarität**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_set_polarity)<br/>                                            | Legt die Signalpolarität der PIN oder des Kanals fest. Der Steuercode legt die Signalpolarität basierend auf einer [**\_ polwm-Pin- \_ Satz-Polarität- \_ \_ Eingabe Struktur fest**](/windows/desktop/api/Pwm/ns-pwm-pwm_pin_set_polarity_input) . Die Signalpolarität ist entweder "hoch" oder "aktiv", wie in der [**PWM- \_ Polarität**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) -Enumeration definiert.<br/>           |
| [**IOCTL \_ PWM- \_ Pin \_ starten**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_start)<br/>                                                           | Startet die Generierung des Pulse Width Modulation-Signals (PWM) für eine PIN oder einen Kanal. Um zu überprüfen, ob eine PIN gestartet wurde, [**wird die IOCTL \_ PWM- \_ Pin \_ \_ gestartet**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**).<br/>                                                                                                                                |
| [**IOCTL \_ PWM- \_ Pin- \_ Pause**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_stop)<br/>                                                             | Beendet die Generierung des Pulse Width Modulation-Signals (PWM) auf einer PIN oder einem Kanal. Um zu überprüfen, ob eine PIN gestartet wurde, [**wird die IOCTL \_ PWM- \_ Pin \_ \_ gestartet**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**).<br/>                                                                                                                                 |
| [**IOCTL \_ PWM- \_ PIN wurde \_ \_ gestartet.**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_is_started)<br/>                                                | Ruft den Status der Signalgenerierung für eine PIN oder einen Kanal ab. Jede Pin weist den Status "gestartet" oder "beendet" auf, weil eine [**PWM- \_ Pin \_ \_ gestartet \_**](pwm-pin-is-started-output.md) wurde.<br/>                                                                                                                                 |



 

 

 




