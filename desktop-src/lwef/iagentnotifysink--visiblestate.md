---
title: Iagentnotifysink visiblestate
description: Iagentnotifysink visiblestate
ms.assetid: b0346296-74e9-448f-aa6d-a9fb1e645f05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3525c079ecd1b566ac2230f06e3effa1ceb7a694
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337389"
---
# <a name="iagentnotifysinkvisiblestate"></a>Iagentnotifysink:: visiblestate

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT VisibleState(
   long dwCharID,  // character ID
   long bVisible,  // visibility flag
   long dwCause,   // cause of visible state
);                          
```

Benachrichtigt eine Client Anwendung, wenn sich der Sichtbarkeits Zustand des Zeichens ändert.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*
</dt> <dd>

Der Bezeichner des Zeichens, dessen Sichtbarkeits Zustand geändert wird.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bvisible*
</dt> <dd>

Sichtbarkeits Kennzeichen. Dieser boolesche Wert ist **true** , wenn das Zeichen sichtbar wird, und **false** , wenn das Zeichen ausgeblendet wird.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwcause*
</dt> <dd>

Ursache der letzten Änderung des Sichtbarkeits Zustands des Zeichens. Der Parameter kann eines der folgenden sein:



| Wert                                                                   | BESCHREIBUNG                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| Konstante ohne Vorzeichen, **nicht signiert** **= 0;**<br/>                 | Das Zeichen wurde nicht angezeigt.                                                               |
| " **Ganzzahl ohne Vorzeichen Short** **userhid = 1;".**<br/>                    | Der Benutzer hat das Zeichen mit dem Popup Menü des Task leisten Symbols oder mit der Spracheingabe ausgeblendet. |
| "Konstante **Ganzzahl ohne Vorzeichen Short** **userhat = 2;** "<br/>                 | Der Benutzer hat das Zeichen angezeigt.                                                                  |
| Konstante " **Ganzzahl ohne Vorzeichen Short** **Program HID = 3;** "<br/>                 | Die Anwendung hat das Zeichen verborgen.                                                         |
| "Konstante **Ganzzahl ohne Vorzeichen Short** **Program" = 4;**<br/>              | Die Anwendung hat das Zeichen angezeigt.                                                      |
| Konstante **Ganzzahl ohne Vorzeichen Short** **otherprogramhid = 5;**<br/>            | Eine andere Anwendung hat das Zeichen verborgen.                                                      |
| " **Ganzzahl ohne Vorzeichen Short** otherprogram" in "Ganzzahl ohne Vorzeichen" **= 6;**<br/>         | Das Zeichen wurde in einer anderen Anwendung angezeigt.                                                   |
| " **Ganzzahl ohne Vorzeichen Short" für "Ganzzahl ohne Vorzeichen Short** **userhidviacharactermenu = 7** "<br/>     | Der Benutzer hat das Zeichen mit dem Popupmenü des Zeichens verborgen.                                    |
| Konstante **Ganzzahl ohne Vorzeichen Short** **userhidviataskbaricon = userhid**<br/> | Der Benutzer hat das Zeichen mit dem Popup Menü des Task leisten Symbols oder mithilfe von Spracheingaben versteckt. |



 

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: getVisible**](iagentcharacter--getvisible.md), [ **iagentcharacter:: getvisibilitycause**](iagentcharacter--getvisibilitycause.md)


 

 





