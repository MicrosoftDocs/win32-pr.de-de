---
title: Iagentnotifysinkex activeclientchange
description: Iagentnotifysinkex activeclientchange
ms.assetid: e953e803-c898-4c07-adc0-8b895b5e8473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96988f80d8a1799bf46f12bd38906e9357453f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341861"
---
# <a name="iagentnotifysinkexactiveclientchange"></a>Iagentnotifysinkex:: activeclientchange

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT ActiveClientChange(
...long dwCharID,  // character ID
   long lStatus    // active state flag
);
```

Benachrichtigt eine Client Anwendung, wenn der aktive Client nicht mehr der aktive Client eines Zeichens ist.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*
</dt> <dd>

Der Bezeichner des Zeichens, für das der Status des aktiven Clients geändert wurde.

</dd> <dt>

<span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lstatus*
</dt> <dd>

Aktive Zustandsänderung des Clients, bei der es sich um eine Kombination aus einem der folgenden Werte handeln kann:



| Wert                                                              | BESCHREIBUNG                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| Konstante " **Ganzzahl ohne Vorzeichen Short** " Aktivieren von " **\_ notactive" = 0;**<br/>   | Der Client ist nicht der aktive Client des Zeichens.                |
| Konstante " **Ganzzahl ohne Vorzeichen Short** **" \_ aktiviert = 1;**<br/>      | Der Client ist der aktive Client des Zeichens.                    |
| Konstante " **Ganzzahl ohne Vorzeichen Short** **" \_ inputactive = 2;**<br/> | Der Client ist Eingabe aktiv (aktiver Client des obersten Zeichens). |



 

</dd> </dl>

Wenn mehrere Client Anwendungen dasselbe Zeichen gemeinsam verwenden, empfängt der aktive Client des Zeichens Maus Eingaben (z. b. Click-oder Drag-Ereignisse der Microsoft-agentsteuerung). Wenn mehrere Zeichen angezeigt werden, empfängt der aktive Client des obersten Zeichens (auch als Input-Active Client bezeichnet) [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Ereignisse.

Wenn sich der aktive Client eines Zeichens ändert, übergibt dieses Ereignis die ID dieses Zeichens und **true** , wenn die Anwendung zum aktiven Client des Zeichens geworden ist, oder **false** , wenn es nicht mehr der aktive Client des Zeichens ist.

Eine Client Anwendung empfängt dieses Ereignis möglicherweise, wenn der Benutzer im Popupmenü des Zeichens oder über den Sprachbefehl den Eintrag einer anderen Client Anwendung auswählt, die Client Anwendung seinen aktiven Status ändert oder eine andere Client Anwendung die Verbindung mit dem Microsoft-Agent beendet. Der-Agent sendet dieses Ereignis nur an die Client Anwendungen, die direkt betroffen sind. diese Ereignisse werden entweder zum aktiven Client, oder der aktive Client wird beendet.

Mit der Methode " [**aktivieren**](iagentcharacter--activate.md) " können Sie festlegen, ob Ihre Anwendung der aktive Client des Zeichens ist, oder ob Sie die Anwendung als Eingabe-aktiv-Client festlegen möchten (wodurch das Zeichen auch am höchsten ist).

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: Aktivierung**](iagentcharacter--activate.md), [**iagentcharakteriex:: getactive**](iagentcharacterex--getactive.md), [**iagentnotifysink:: activateinputstate**](iagentnotifysink--activateinputstate.md)


 

 





