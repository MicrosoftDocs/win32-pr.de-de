---
title: IAgentNotifySinkEx ListeningState
description: IAgentNotifySinkEx ListeningState
ms.assetid: e303b299-0dd0-419a-87a9-1490fe6cf54a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21d3926741f83f66ab6133874ec47783976c0ddb6d3fbd2ee91c6e584813147a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692606"
---
# <a name="iagentnotifysinkexlisteningstate"></a>IAgentNotifySinkEx::ListeningState

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT ListeningState(
   long dwCharacterID,  // character ID
   long bListening,     // listening mode state
   long dwCause         // cause  
);
```

Benachrichtigt eine Clientanwendung, wenn sich der Abhörmodus ändert.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*
</dt> <dd>

Das Zeichen, für das sich der Lauschenzustand geändert hat.

</dd> <dt>

<span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*
</dt> <dd>

Der Status des Lauschenmodus. **True gibt** an, dass der Lauschenmodus gestartet wurde. **False**, dass der Abhörmodus beendet wurde.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

Die Ursache für das Ereignis. Dies kann einer der folgenden Werte sein.



| Wert                                                                             | BESCHREIBUNG                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ PROGRAMDISABLED = 1;**<br/>    | Der Lauschenmodus wurde durch Programmcode deaktiviert.                                 |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ PROGRAMTIMEDOUT = 2;**<br/>    | Time out des Lauschenmodus (durch Programmcode aktiviert).                          |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ USERTIMEDOUT = 3;**<br/>       | Beim Lauschenmodus (aktiviert durch die Abhörtaste) ist ein Time out erfolgt.                     |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ USERRELEASEDKEY = 4;**<br/>    | Der Lauschenmodus wurde deaktiviert, da der Benutzer die Abhörtaste losgelassen hat.     |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ USERUTTERANCEENDED = 5;**<br/> | Der Lauschenmodus wurde deaktiviert, weil der Benutzer das Sprechen beendet hat.              |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ CLIENTDEACTIVATED = 6;**<br/>  | Der Lauschenmodus wurde deaktiviert, weil der aktive Eingabeclient deaktiviert wurde. |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ DEFAULTCHARCHANGE = 7**<br/>   | Der Lauschenmodus wurde deaktiviert, weil das Standardzeichen geändert wurde.       |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ USERDISABLED = 8**<br/>        | Der Lauschenmodus wurde deaktiviert, da der Benutzer die Spracheingabe deaktiviert hat.          |



 

</dd> </dl>

Dieses Ereignis wird an alle Clients gesendet, wenn der Lauschmodus beginnt, nachdem der Benutzer die Abhörtaste drückt oder das Time out endet, oder wenn der eingabeaktive Client die [**IAgentCharacterEx::Listen-Methode**](iagentcharacterex--listen.md) mit **True** oder **False aufruft.**

Das Ereignis gibt Werte an die Clients zurück, auf denen dieses Zeichen derzeit geladen ist. Alle anderen Clients erhalten ein NULL-Zeichen (leere Zeichenfolge).

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md)


 

 





