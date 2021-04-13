---
title: Iagentcharakteriex-Überwachung
description: Iagentcharakteriex-Überwachung
ms.assetid: 8d4cdb6c-04e1-498c-867f-fddbe6e2791a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12c479936a8d2dc43e2f2da5a680a51705af2885
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310388"
---
# <a name="iagentcharacterexlisten"></a>Iagentcharakteriex:: lauschen

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Listen(
   long bListen  // listening mode flag
);
```

Schaltet den Lesemodus (sprach Erkennungs Eingabe) ein oder aus.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*blisten*
</dt> <dd>

Flag zum lauschen des Modus. Wenn dieser Parameter **true** ist, wird der Empfangsmodus aktiviert. der Wert **false** gibt an, dass der Überwachungsmodus deaktiviert ist.

</dd> </dl>

Wenn diese Methode auf **true** festgelegt wird, wird der Empfangsmodus (aktiviert die Spracherkennung) für einen festgelegten Zeitraum aktiviert. Obwohl Sie den Wert für das Timeout nicht festlegen können, können Sie den Empfangsmodus deaktivieren, bevor das Timeout abläuft. Wenn der Überwachungsmodus bereits aktiviert ist, weil Sie (oder ein anderer Client) die-Methode erfolgreich auf **true** festgelegt haben, bevor das Timeout abläuft, wird die-Methode erfolgreich ausgeführt, und das Timeout wird zurückgesetzt. Wenn der Überwachungsmodus jedoch bereits auf ON eingestellt ist, da der Benutzer die Abhör Taste drückt, wird die Methode erfolgreich ausgeführt, aber das Timeout wird ignoriert, und der Empfangsmodus wird basierend auf der Interaktion des Benutzers mit dem lauschenden Schlüssel beendet.

Diese Methode ist nur erfolgreich, wenn Sie vom Eingabe aktiven Client aufgerufen wird. Daher schlägt die Methode fehl, wenn der Client nicht der aktive Client des obersten Zeichens ist. Die-Methode schlägt auch fehl, wenn Sie versuchen, die-Methode auf **false** festzulegen, und der Benutzer die Abhör Taste drückt. Dies kann auch fehlschlagen, wenn keine kompatible Sprach-Engine verfügbar ist, die mit der Sprach-ID-Einstellung des Zeichens übereinstimmt, oder der Benutzer die Spracheingabe mithilfe der Eigenschaften Seite des Microsoft-Agents deaktiviert hat. Die Methode schlägt jedoch nicht fehl, wenn das Audiogerät ausgelastet ist.

Wenn Sie diese Methode erfolgreich auf **true** festgelegt haben, löst der Server das [**iagentnotifysinkex:: listeningstate**](iagentnotifysinkex--listeningstate.md) -Ereignis aus. Der Server sendet auch **iagentnotifysinkex:: listeningstate** , wenn der Timeout für das Ansichtsmodus abgeschlossen ist oder wenn Sie [**iagentcharakteriex::**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) Listening auf **false** festlegen.

Diese Methode ruft nicht automatisch [**iagentcharacter:: stopAll**](iagentcharacter--stopall.md) auf und wiederholt eine Animation zum lauschen des Zeichens, wenn der Benutzer die Abhör Taste drückt. Dies ermöglicht es Ihnen, das [**iagentnotifysinkex:: listeningstate**](iagentnotifysinkex--listeningstate.md) -Ereignis zu verwenden, um zu bestimmen, ob Sie die aktuelle Animation abbrechen und ihre eigene passende Animation wiedergeben möchten. Nachdem jedoch eine Benutzer Äußerung erkannt wurde, ruft der Server automatisch **iagentcharacter:: stopAll** auf und spielt eine Animation für den hörzustand.

## <a name="see-also"></a>Weitere Informationen

[**Iagentnotifysinkex:: listeningstate**](iagentnotifysinkex--listeningstate.md), [ **iagentspeechinputproperties:: GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




