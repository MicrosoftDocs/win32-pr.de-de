---
title: Iagentcharacter getvisibilitycause
description: Iagentcharacter getvisibilitycause
ms.assetid: 46f681de-1c99-4f90-a3fe-aae04bb75339
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6013385144b82b79a0f17ae6443b094a9d9c8a4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388809"
---
# <a name="iagentcharactergetvisibilitycause"></a>Iagentcharacter:: getvisibilitycause

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetVisibilityCause(
   long * pdwCause  // address of variable for cause of character visible state
);
```

Ruft die Ursache für den sichtbaren Zustand des Zeichens ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwcause*
</dt> <dd>

Adresse einer Variablen, die die Ursache der letzten Änderung des Status der Sichtbarkeit des Zeichens empfängt und eine der folgenden ist:



| Wert                                                                   | BESCHREIBUNG                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| Konstante ohne Vorzeichen, **nicht signiert** **= 0;**<br/>                 | Das Zeichen wurde nicht angezeigt.                                                               |
| " **Ganzzahl ohne Vorzeichen Short** **userhid = 1;".**<br/>                    | Der Benutzer hat das Zeichen mit dem Popup Menü des Task leisten Symbols oder mithilfe von Spracheingaben versteckt. |
| "Konstante **Ganzzahl ohne Vorzeichen Short** **userhat = 2;** "<br/>                 | Der Benutzer hat das Zeichen angezeigt.                                                                  |
| Konstante " **Ganzzahl ohne Vorzeichen Short** **Program HID = 3;** "<br/>                 | Die Anwendung hat das Zeichen verborgen.                                                         |
| "Konstante **Ganzzahl ohne Vorzeichen Short** **Program" = 4;**<br/>              | Die Anwendung hat das Zeichen angezeigt.                                                      |
| Konstante **Ganzzahl ohne Vorzeichen Short** **otherprogramhid = 5;**<br/>            | Eine andere Anwendung hat das Zeichen verborgen.                                                      |
| " **Ganzzahl ohne Vorzeichen Short** otherprogram" in "Ganzzahl ohne Vorzeichen" **= 6;**<br/>         | Das Zeichen wurde in einer anderen Anwendung angezeigt.                                                   |
| " **Ganzzahl ohne Vorzeichen Short" für "Ganzzahl ohne Vorzeichen Short** **userhidviacharactermenu = 7** "<br/>     | Der Benutzer hat das Zeichen mit dem Popupmenü des Zeichens verborgen.                                    |
| Konstante **Ganzzahl ohne Vorzeichen Short** **userhidviataskbaricon = userhid**<br/> | Der Benutzer hat das Zeichen mit dem Popup Menü des Task leisten Symbols oder mithilfe von Spracheingaben versteckt. |



 

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentnotifysink:: visiblestate**](iagentnotifysink--visiblestate.md)


 

 





