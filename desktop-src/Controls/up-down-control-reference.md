---
title: Up-Down-Steuerelement
description: Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit Auf-Ab-Steuerelementen verwendet werden.
ms.assetid: 48c6b4bd-65b4-4388-959e-efffa7658274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2979ac08889761cb7f226b58a9d951d407bc82420957ed9327de1a880d0d9bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018588"
---
# <a name="up-down-control"></a>Up-Down-Steuerelement

Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit Auf-Ab-Steuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                    | Inhalte                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Auf-Ab-Steuerelemente](up-down-controls.md) | Ein Nach-unten-Steuerelement ist ein Pfeilschaltflächenpaar, auf das der Benutzer klicken kann, um einen Wert zu erhöhen oder zu dekrementiert, z. B. eine Bildlaufposition oder eine Zahl, die in einem Begleitsteuerfeld (als Fenster "Fenster" bezeichnet) angezeigt wird.<br/> |



 

### <a name="functions"></a>Funktionen



| Thema                                              | Inhalte                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateUpDownControl**](/windows/desktop/api/Commctrl/nf-commctrl-createupdowncontrol) | Erstellt ein Auf-Ab-Steuerelement. Hinweis: Diese Funktion ist veraltet. Es handelt sich um eine 16-Bit-Funktion, die keine 32-Bit-Werte für Bereich und Position verarbeiten kann.<br/> |



 

### <a name="messages"></a>Meldungen



| Thema                                                 | Inhalte                                                                                                                                                                                                                               |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UDM \_ GETACCEL**](udm-getaccel.md)                 | Ruft Beschleunigungsinformationen für ein Auf-Ab-Steuerelement ab. <br/>                                                                                                                                                                 |
| [**UDM \_ GETBASE**](udm-getbase.md)                   | Ruft die aktuelle Radixbasis (d. h. Basis 10 oder 16) für ein Auf-Ab-Steuerelement ab. <br/>                                                                                                                                   |
| [**UDM \_ GETBUDDY**](udm-getbuddy.md)                 | Ruft das Handle für das aktuelle Fenster ab. <br/>                                                                                                                                                                          |
| [**UDM \_ GETPOS**](udm-getpos.md)                     | Ruft die aktuelle Position eines Auf-Ab-Steuerelements mit 16-Bit-Genauigkeit ab. <br/>                                                                                                                                                |
| [**UDM \_ GETPOS32**](udm-getpos32.md)                 | Gibt die 32-Bit-Position eines Auf-Ab-Steuerelements zurück.<br/>                                                                                                                                                                          |
| [**UDM \_ GETRANGE**](udm-getrange.md)                 | Ruft die minimalen und maximalen Positionen (Bereich) für ein Auf-Ab-Steuerelement ab. <br/>                                                                                                                                                |
| [**UDM \_ GETRANGE32**](udm-getrange32.md)             | Ruft den 32-Bit-Bereich eines Auf-Ab-Steuerelements ab. <br/>                                                                                                                                                                          |
| [**UDM \_ GETUNICODEFORMAT**](udm-getunicodeformat.md) | Ruft das Unicode-Zeichenformatflag für das Steuerelement ab. <br/>                                                                                                                                                               |
| [**UDM \_ SETACCEL**](udm-setaccel.md)                 | Legt die Beschleunigung für ein Auf-Ab-Steuerelement fest. <br/>                                                                                                                                                                              |
| [**UDM \_ SETBASE**](udm-setbase.md)                   | Legt die Radixbasis für ein Auf-Ab-Steuerelement fest. Der Basiswert bestimmt, ob im Fenster "Fenster" Zahlen in Dezimal- oder Hexadezimalziffern angezeigt werden. Hexadezimalzahlen sind immer ohne Vorzeichen, und Dezimalzahlen werden signiert. <br/> |
| [**UDM \_ SETBUDDY**](udm-setbuddy.md)                 | Legt das Fenster für ein Auf-Ab-Steuerelement fest. <br/>                                                                                                                                                                              |
| [**UDM \_ SETPOS**](udm-setpos.md)                     | Legt die aktuelle Position für ein Auf-Ab-Steuerelement mit 16-Bit-Genauigkeit fest. <br/>                                                                                                                                                    |
| [**UDM \_ SETPOS32**](udm-setpos32.md)                 | Legt die Position eines Auf-Ab-Steuerelements mit 32-Bit-Genauigkeit fest.<br/>                                                                                                                                                              |
| [**UDM \_ SETRANGE**](udm-setrange.md)                 | Legt die minimalen und maximalen Positionen (Bereich) für ein Auf-Ab-Steuerelement fest.<br/>                                                                                                                                                      |
| [**UDM \_ SETRANGE32**](udm-setrange32.md)             | Legt den 32-Bit-Bereich eines Auf-Ab-Steuerelements fest. <br/>                                                                                                                                                                               |
| [**UDM \_ SETUNICODEFORMAT**](udm-setunicodeformat.md) | Legt das Unicode-Zeichenformatflag für das Steuerelement fest. Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen. <br/>                                   |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                            | Inhalte                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ RELEASEDCAPTURE (nach oben)](nm-releasedcapture-up-down-.md) | Benachrichtigt das übergeordnete Fenster eines Auf-Ab-Steuerelements, dass das Steuerelement die Mauserfassung frei gibt. Diese Benachrichtigung wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                                                                                       |
| [UDN \_ DELTAPOS](udn-deltapos.md)                                | Wird vom Betriebssystem an das übergeordnete Fenster eines Auf-Ab-Steuerelements gesendet, wenn sich die Position des Steuerelements ändert. Dies geschieht, wenn der Benutzer eine Änderung des Werts an fordert, indem er den Nach-oben- oder Nach-unten-Pfeil des Steuerelements drückt. Die [ \_ UDN-DELTAPOS-Nachricht](udn-deltapos.md) wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/> |



 

### <a name="structures"></a>Strukturen



| Thema                        | Inhalte                                                                                                                                          |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) | Enthält Informationen, die für Benachrichtigungsmeldungen des Up-Down-Steuerelements spezifisch sind. Sie ist identisch mit und ersetzt die **NM \_ UPDOWN-Struktur.** <br/> |
| [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)   | Enthält Beschleunigungsinformationen für ein Auf-Ab-Steuerelement. <br/>                                                                             |



 

### <a name="constants"></a>Konstanten



| Thema                                                | Inhalte                                                                      |
|------------------------------------------------------|-------------------------------------------------------------------------------|
| [Auf-Ab-Steuerelementstile](up-down-control-styles.md) | In diesem Abschnitt werden die Stile aufgeführt, die beim Erstellen von Auf-Ab-Steuerelementen verwendet werden.<br/> |



 

 

 





