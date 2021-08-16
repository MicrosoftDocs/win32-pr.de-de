---
description: In diesem Thema werden die IOCTLs für Pulse Width Pulse aufgeführt.
ms.assetid: 2ED7A06A-A7EC-4C44-AB22-4A52CF2DF2C5
title: PWM-Steuerungscodes
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d9118d51721165860d6132cb7f0fc91a0ac95e7a9d92446df27076a625c83b68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405204"
---
# <a name="pwm-control-codes"></a>PWM-Steuerungscodes

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

In diesem Thema werden die IOCTLs für Pulse Width Pulse aufgeführt.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                      | Beschreibung                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IOCTL \_ PWM \_ CONTROLLER \_ GET \_ ACTUAL \_ PERIOD**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_get_actual_period)<br/>                   | Ruft den effektiven Ausgabesignalzeitraum des PWM-Controllers (Pulse Width PwM) ab, wie er an seinen Ausgabekanälen gemessen wird.<br/>                                                                                                                                                                                  |
| [**IOCTL \_ PWM \_ CONTROLLER \_ GET \_ INFO**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_get_info)<br/>                                      | Ruft Informationen zu einem PWM-Controller (Pulse Width Pulse) ab. Diese Informationen ändern sich nicht, nachdem der Controller initialisiert wurde. <br/>                                                                                                                                                                                |
| [**IOCTL \_ PWM \_ CONTROLLER \_ SET \_ DESIRED \_ PERIOD**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_set_desired_period)<br/>                 | Legt den Ausgabesignalzeitraum eines PWM-Controllers (Pulse Width Pulse) auf einen vorgeschlagenen Wert fest. <br/>                                                                                                                                                                                                                            |
| [**IOCTL \_ PWM \_ PIN \_ GET \_ ACTIVE \_ DUTY \_ CYCLE \_ PERCENTAGE**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_get_active_duty_cycle_percentage)<br/> | Ruft den aktuellen Prozentsatz des Steuerzyklus für eine Stecknadel oder einen Kanal ab. Der Steuerungscode gibt den Prozentsatz als [**\_ PWM-PIN \_ GET ACTIVE DUTY CYCLE PERCENTAGE \_ \_ \_ \_ \_ OUTPUT-Struktur**](pwm-pin-get-active-duty-cycle-percentage-output.md) zurück.<br/>                                                                                  |
| [**IOCTL \_ PWM \_ PIN \_ SET \_ ACTIVE \_ DUTY \_ CYCLE \_ PERCENTAGE**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_set_active_duty_cycle_percentage)<br/> | Legen Sie einen gewünschten Prozentwert für den Steuerpunkt oder Kanal fest. Der Steuerungscode gibt den Prozentsatz als [**PWM \_ PIN SET ACTIVE DUTY CYCLE PERCENTAGE \_ \_ \_ \_ \_ \_ INPUT-Struktur**](pwm-pin-set-active-duty-cycle-percentage-input.md) an. <br/>                                                                      |
| [**IOCTL \_ PWM \_ PIN \_ GET \_ POLARITY**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_get_polarity)<br/>                                            | Ruft die aktuelle Signalpolität des Pins oder Kanals ab. Der Steuerungscode ruft die Signalpolität als [**PWM \_ PIN GET \_ \_ POLARITY \_ OUTPUT-Struktur**](pwm-pin-get-polarity-output.md) ab. Die Signalpolität ist entweder Aktiv hoch oder Aktiv niedrig, wie in der [**PWM \_ POLARITY-Enumeration**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) definiert. <br/> |
| [**IOCTL \_ PWM \_ PIN \_ SET \_ POLARITY**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_set_polarity)<br/>                                            | Legt die Signalpolität des Pins oder Kanals fest. Der Steuerungscode legt die Signalpolität basierend auf einer [**PWM \_ PIN SET \_ \_ POLARITY \_ INPUT-Struktur**](/windows/desktop/api/Pwm/ns-pwm-pwm_pin_set_polarity_input) fest. Die Signalpolität ist entweder Aktiv hoch oder Aktiv niedrig, wie in der [**PWM \_ POLARITY-Enumeration**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) definiert.<br/>           |
| [**IOCTL \_ PWM \_ PIN \_ START**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_start)<br/>                                                           | Startet die Generierung des PWM-Signals (Pulse Width Pw) auf einem Pin oder Kanal. Um zu überprüfen, ob eine Stecknadel gestartet wird, verwenden Sie [**IOCTL \_ PWM \_ PIN IS \_ \_ STARTED**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**).<br/>                                                                                                                                |
| [**IOCTL \_ PWM \_ PIN \_ STOP**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_stop)<br/>                                                             | Beendet die Generierung des PWM-Signals (Pulse Width Pw) auf einem Pin oder Kanal. Um zu überprüfen, ob eine Stecknadel gestartet wird, verwenden Sie [**IOCTL \_ PWM \_ PIN IS \_ \_ STARTED**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**).<br/>                                                                                                                                 |
| [**IOCTL \_ PWM \_ PIN WIRD \_ \_ GESTARTET**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_is_started)<br/>                                                | Ruft den Status der Signalgenerierung für einen Pin oder Kanal ab. Jeder Pin hat den Status Gestartet oder Beendet als [**PWM \_ PIN IS \_ STARTED \_ \_ OUTPUT-Struktur.**](pwm-pin-is-started-output.md)<br/>                                                                                                                                 |



 

 

 




