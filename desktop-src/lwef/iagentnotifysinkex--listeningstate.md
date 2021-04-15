---
title: Iagentnotifysinkex listeningstate
description: Iagentnotifysinkex listeningstate
ms.assetid: e303b299-0dd0-419a-87a9-1490fe6cf54a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fee8f931030cbd68cd148fc57360d8b0ccf7624
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515830"
---
# <a name="iagentnotifysinkexlisteningstate"></a>Iagentnotifysinkex:: listeningstate

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT ListeningState(
   long dwCharacterID,  // character ID
   long bListening,     // listening mode state
   long dwCause         // cause  
);
```

Benachrichtigt eine Client Anwendung, wenn der überwachungmodus geändert wird.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwcharakteriid*
</dt> <dd>

Das Zeichen, für das sich der Überwachungszustand geändert hat.

</dd> <dt>

<span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*blistening*
</dt> <dd>

Der Status des Überwachungsmodus. **True** gibt an, dass der Empfangsmodus gestartet wurde. **False** gibt an, dass der Empfangsmodus beendet wurde.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwcause*
</dt> <dd>

Die Ursache für das Ereignis, bei der es sich möglicherweise um einen der folgenden Werte handelt.



| Wert                                                                             | BESCHREIBUNG                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| die Konstante " **Ganzzahl ohne Vorzeichen long** **lscomplete" \_ verursacht \_ Programm deaktiviert = 1;**<br/>    | Der Empfangsmodus wurde durch Programmcode ausgeschaltet.                                 |
| die Konstante " **Ganzzahl ohne Vorzeichen long** **lscomplete" \_ bewirkt \_ , dass Program TimedOut = 2;**<br/>    | Timeout beim lauschen-Modus (durch Programmcode aktiviert).                          |
| Konstante **Länge ohne** Vorzeichen **lscomplete \_ bewirkt \_ usertimedout = 3;**<br/>       | Timeout beim überwachenden Modus (aktiviert durch den abhörenden Schlüssel).                     |
| Konstante **Länge ohne** Vorzeichen **lscomplete \_ bewirkt \_ userreleasedkey = 4;**<br/>    | Der Empfangsmodus wurde deaktiviert, da der Benutzer die Abhör Taste losgelassen hat.     |
| Konstante **Länge ohne** Vorzeichen **lscomplete \_ bewirkt, dass \_ userutterancebeendeten = 5;**<br/> | Der Empfangsmodus wurde deaktiviert, da der Benutzer die sprachbearbeitung beendet hat.              |
| Konstante " **Ganzzahl ohne Vorzeichen long** **lscomplete \_ " \_ CLIENTDEACTIVATED = 6;**<br/>  | Der Abhör Modus wurde deaktiviert, da der aktive Client für die Eingabe deaktiviert wurde. |
| Konstante " **Ganzzahl ohne Vorzeichen long** **lscomplete": \_ \_ defaultcharchange = 7**<br/>   | Der Abhör Modus wurde deaktiviert, da das Standard Zeichen geändert wurde.       |
| Konstante " **Ganzzahl ohne Vorzeichen long** **lscomplete": \_ \_ userdeaktiviert = 8**<br/>        | Der Abhör Modus wurde deaktiviert, da der Benutzer die Spracheingabe deaktiviert hat.          |



 

</dd> </dl>

Dieses Ereignis wird an alle Clients gesendet, wenn der Empfangsmodus beginnt, nachdem der Benutzer die Abhör Taste gedrückt hat oder wenn das Timeout abgelaufen ist, oder wenn der Eingabe aktive Client die Methode [**iagentcharakteriex::**](iagentcharacterex--listen.md) Listening mit **true** oder **false** aufruft.

Das Ereignis gibt Werte an die Clients zurück, für die dieses Zeichen zurzeit geladen ist. Alle anderen Clients erhalten ein NULL-Zeichen (leere Zeichenfolge).

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharakteriex:: lauschen**](iagentcharacterex--listen.md)


 

 





