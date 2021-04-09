---
title: Up-Down-Steuerelement
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit auf-ab-Steuerelementen verwendet werden.
ms.assetid: 48c6b4bd-65b4-4388-959e-efffa7658274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8364eb44ee01e27439c82d1d77e674bfb9e3165
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036799"
---
# <a name="up-down-control"></a>Up-Down-Steuerelement

Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit auf-ab-Steuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                    | Inhalte                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Auf-ab-Steuerelemente](up-down-controls.md) | Ein auf-ab-Steuerelement ist ein paar von Pfeil Schaltflächen, auf die der Benutzer klicken kann, um einen Wert zu erhöhen oder zu verringern, z. b. eine Bild Lauf Position oder eine Zahl, die in einem Begleit Steuerelement (einem Buddy-Fenster) angezeigt wird<br/> |



 

### <a name="functions"></a>Functions



| Thema                                              | Inhalte                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreateupdowncontrol"**](/windows/desktop/api/Commctrl/nf-commctrl-createupdowncontrol) | Erstellt ein auf-ab-Steuerelement. Hinweis: Diese Funktion ist veraltet. Es handelt sich um eine 16-Bit-Funktion und kann keine 32-Bit-Werte für Bereich und Position verarbeiten.<br/> |



 

### <a name="messages"></a>Meldungen



| Thema                                                 | Inhalte                                                                                                                                                                                                                               |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UDM \_ GetAccel**](udm-getaccel.md)                 | Ruft Beschleunigungs Informationen für ein auf-ab-Steuerelement ab. <br/>                                                                                                                                                                 |
| [**UDM \_ GetBase**](udm-getbase.md)                   | Ruft die aktuelle Basis 10 (d. h. entweder Basis 10 oder 16) für ein auf-ab-Steuerelement ab. <br/>                                                                                                                                   |
| [**UDM \_ GetBuddy**](udm-getbuddy.md)                 | Ruft das Handle für das aktuelle Buddy-Fenster ab. <br/>                                                                                                                                                                          |
| [**UDM- \_ GetPos**](udm-getpos.md)                     | Ruft die aktuelle Position eines auf-ab-Steuer Elements mit 16-Bit-Genauigkeit ab. <br/>                                                                                                                                                |
| [**UDM \_ GETPOS32**](udm-getpos32.md)                 | Gibt die 32-Bit-Position eines auf-ab-Steuer Elements zurück.<br/>                                                                                                                                                                          |
| [**UDM- \_ GetRange**](udm-getrange.md)                 | Ruft die minimalen und maximalen Positionen (Bereich) für ein auf-ab-Steuerelement ab. <br/>                                                                                                                                                |
| [**UDM \_ GETRANGE32**](udm-getrange32.md)             | Ruft den 32-Bit-Bereich eines auf-ab-Steuer Elements ab. <br/>                                                                                                                                                                          |
| [**UDM \_ getunicodeformat**](udm-getunicodeformat.md) | Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab. <br/>                                                                                                                                                               |
| [**UDM- \_ SetAccel**](udm-setaccel.md)                 | Legt die Beschleunigung für ein auf-ab-Steuerelement fest. <br/>                                                                                                                                                                              |
| [**UDM- \_ setbase**](udm-setbase.md)                   | Legt die Basis für ein auf-ab-Steuerelement fest. Der Basiswert bestimmt, ob das Buddy-Fenster Zahlen in Dezimal-oder hexadezimal Ziffern anzeigt. Hexadezimale Zahlen sind immer unsigniert, und Dezimalzahlen werden signiert. <br/> |
| [**UDM- \_ SetBuddy**](udm-setbuddy.md)                 | Legt das Buddy-Fenster für ein auf-ab-Steuerelement fest. <br/>                                                                                                                                                                              |
| [**UDM- \_ SetPos**](udm-setpos.md)                     | Legt die aktuelle Position für ein auf-ab-Steuerelement mit 16-Bit-Genauigkeit fest. <br/>                                                                                                                                                    |
| [**UDM \_ SETPOS32**](udm-setpos32.md)                 | Legt die Position eines auf-ab-Steuer Elements mit 32-Bit-Genauigkeit fest.<br/>                                                                                                                                                              |
| [**UDM-über \_ Tragung**](udm-setrange.md)                 | Legt die minimalen und maximalen Positionen (Bereich) für ein auf-ab-Steuerelement fest.<br/>                                                                                                                                                      |
| [**UDM \_ SETRANGE32**](udm-setrange32.md)             | Legt den 32-Bit-Bereich eines auf-ab-Steuer Elements fest. <br/>                                                                                                                                                                               |
| [**UDM- \_ Format-Code Format**](udm-setunicodeformat.md) | Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest. Mit dieser Meldung können Sie den Zeichensatz ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen. <br/>                                   |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                            | Inhalte                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ releasedcapture (auf-ab)](nm-releasedcapture-up-down-.md) | Benachrichtigt das übergeordnete Fenster eines auf-ab-Steuer Elements, dass das Steuerelement die Maus Aufzeichnung freigibt. Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md) <br/>                                                                                                                                                                       |
| [udn-Delta Torys \_](udn-deltapos.md)                                | Wird vom Betriebssystem an das übergeordnete Fenster eines auf-ab-Steuer Elements gesendet, wenn sich die Position des-Steuer Elements ändert. Dies geschieht, wenn der Benutzer eine Änderung des Werts anfordert, indem er den Pfeil nach oben oder nach unten drückt. Die [udn- \_ Delta](udn-deltapos.md) -Nachricht wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/> |



 

### <a name="structures"></a>Strukturen



| Thema                        | Inhalte                                                                                                                                          |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nmupdown**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) | Enthält Informationen, die spezifisch für die Benachrichtigungs Meldungen auf der auf-ab- Sie ist identisch mit und ersetzt die **- \_ UpDown** -Struktur von nm. <br/> |
| [**Udaccel**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)   | Enthält Beschleunigungs Informationen für ein auf-ab-Steuerelement. <br/>                                                                             |



 

### <a name="constants"></a>Konstanten



| Thema                                                | Inhalte                                                                      |
|------------------------------------------------------|-------------------------------------------------------------------------------|
| [Auf-ab-Steuerelement Stile](up-down-control-styles.md) | In diesem Abschnitt werden die Formate aufgelistet, die bei der Erstellung von auf-ab-Steuerelementen<br/> |



 

 

 





