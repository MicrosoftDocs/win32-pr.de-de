---
title: IP-Adressensteuerelement
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit IP-Adress Steuerelementen verwendet werden.
ms.assetid: vs|controls|~\controls\ipaddress\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c80fc87a12ce49038f4c1836e684fa0f8895bd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471069"
---
# <a name="ip-address-control"></a>IP-Adressensteuerelement

Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit IP-Adress Steuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                          | Inhalte                                                                                                                    |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [IP-Adress Steuerelemente](ip-address-controls.md) | Ein IP-Adress Steuerelement (Internet Protocol) ermöglicht es dem Benutzer, eine IP-Adresse in einem leicht verständlichen Format einzugeben.<br/> |



 

### <a name="macros"></a>Makros



| Thema                                         | Inhalte                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**erste \_ IP-Adresse**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)   | Extrahiert den Wert von Feld 0 aus einer gepackten IP-Adresse, die mit der [**IPM \_ GetAddress**](ipm-getaddress.md) -Nachricht abgerufen wird. <br/> |
| [**vierte \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) | Extrahiert den Wert von Feld 3 aus einer gepackten IP-Adresse, die mit der [**IPM \_ GetAddress**](ipm-getaddress.md) -Nachricht abgerufen wird. <br/> |
| [**MakeIPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress)        | Packt vier Byte-Werte in einem einzelnen lParam-Element, das für die Verwendung mit der [**IPM- \_ setAddress**](ipm-setaddress.md) -Nachricht geeignet ist. <br/>  |
| [**Makeiprange**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange)            | Packt zwei Bytewerte in einem einzelnen lParam-Element, das für die Verwendung mit der [**IPM \_**](ipm-setrange.md) -Nachricht verwendet werden soll. <br/>       |
| [**zweite \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress) | Extrahiert den Wert für Feld 1 aus einer gepackten IP-Adresse, die mit der [**IPM \_ GetAddress**](ipm-getaddress.md) -Nachricht abgerufen wird. <br/> |
| [**Dritte \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)   | Extrahiert den Wert von Feld 2 aus einer gepackten IP-Adresse, die mit der [**IPM \_ GetAddress**](ipm-getaddress.md) -Nachricht abgerufen wird. <br/> |



 

### <a name="messages"></a>Meldungen



| Thema                                         | Inhalte                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**IPM- \_ clearaddress**](ipm-clearaddress.md) | Löscht den Inhalt des Steuer Elements für die IP-Adresse. <br/>                                                                            |
| [**IPM- \_ GetAddress**](ipm-getaddress.md)     | Ruft die Adress Werte für alle vier Felder im IP-Adress Steuerelement ab. <br/>                                                    |
| [**IPM \_ isblank**](ipm-isblank.md)           | Bestimmt, ob alle Felder im IP-Adress Steuerelement leer sind. <br/>                                                             |
| [**IPM- \_ setAddress**](ipm-setaddress.md)     | Legt die Adress Werte für alle vier Felder im IP-Adress Steuerelement fest. <br/>                                                    |
| [**IPM- \_ SetFocus**](ipm-setfocus.md)         | Legt den Tastaturfokus auf das angegebene Feld im IP-Adress Steuerelement fest. Der gesamte Text in diesem Feld wird ausgewählt. <br/> |
| [**IPM-über \_ Tragung**](ipm-setrange.md)         | Legt den gültigen Bereich für das angegebene Feld im IP-Adress Steuerelement fest. <br/>                                                   |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                     | Inhalte                                                                                                                                                                                   |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IPN- \_ FieldChanged](ipn-fieldchanged.md) | Wird gesendet, wenn der Benutzer ein Feld im Steuerelement ändert oder von einem Feld zu einem anderen verschoben wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/> |



 

### <a name="structures"></a>Strukturen



| Thema                              | Inhalte                                                                                              |
|------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**Nmipaddress**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) | Enthält Informationen für den [IPN \_ FieldChanged](ipn-fieldchanged.md) -Benachrichtigungs Code. <br/> |



 

 

 





