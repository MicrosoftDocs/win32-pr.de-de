---
title: IAgentNotifySinkEx ActiveClientChange
description: IAgentNotifySinkEx ActiveClientChange
ms.assetid: e953e803-c898-4c07-adc0-8b895b5e8473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50549c4b091a39614fd7ff6b15af0bc1436113dfd2e9b3d31ca86e6995a0e94d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961500"
---
# <a name="iagentnotifysinkexactiveclientchange"></a>IAgentNotifySinkEx::ActiveClientChange

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT ActiveClientChange(
...long dwCharID,  // character ID
   long lStatus    // active state flag
);
```

Benachrichtigt eine Clientanwendung, wenn ihr aktiver Client nicht mehr der aktive Client eines Zeichens ist.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Bezeichner des Zeichens, für das sich der aktive Clientstatus geändert hat.

</dd> <dt>

<span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*
</dt> <dd>

Aktive Statusänderung des Clients, die eine Kombination aus einem der folgenden Werte sein kann:



| Wert                                                              | BESCHREIBUNG                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| **const unsigned short** **ACTIVATE \_ NOTACTIVE = 0;**<br/>   | Ihr Client ist nicht der aktive Client des Zeichens.                |
| **const unsigned short** **ACTIVATE ACTIVE = \_ 1;**<br/>      | Ihr Client ist der aktive Client des Zeichens.                    |
| **const unsigned short** **ACTIVATE \_ INPUTACTIVE = 2;**<br/> | Ihr Client ist eingabeaktiv (aktiver Client des obersten Zeichens). |



 

</dd> </dl>

Wenn mehrere Clientanwendungen das gleiche Zeichen verwenden, empfängt der aktive Client des Zeichens Mauseingaben (z. B. Klick- oder Ziehereignisse des Microsoft-Agent-Steuerelements). Wenn mehrere Zeichen angezeigt werden, empfängt der aktive Client des obersten Zeichens (auch als eingabeaktiver Client bezeichnet) [**IAgentNotifySink::Command-Ereignisse.**](iagentnotifysink--command.md)

Wenn sich der aktive Client eines Zeichens ändert, übergibt dieses Ereignis die ID dieses Zeichens und **True,** wenn Ihre Anwendung zum aktiven Client des Zeichens geworden ist, oder **False,** wenn es sich nicht mehr um den aktiven Client des Zeichens handelt.

Eine Clientanwendung kann dieses Ereignis empfangen, wenn der Benutzer den Eintrag einer anderen Clientanwendung im Popupmenü des Zeichens oder per Sprachbefehl auswählt, die Clientanwendung ihren aktiven Status ändert oder eine andere Clientanwendung ihre Verbindung mit dem Microsoft-Agent beendet. Der Agent sendet dieses Ereignis nur an die Clientanwendungen, die direkt betroffen sind– also diejenigen, die entweder zum aktiven Client werden oder nicht mehr der aktive Client sind.

Sie können die [**Activate-Methode**](iagentcharacter--activate.md) verwenden, um festzulegen, ob Ihre Anwendung der aktive Client des Zeichens ist, oder um Ihre Anwendung zum eingabeaktiven Client zu machen (wodurch das Zeichen auch ganz oben steht).

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [**IAgentCharacterEx::GetActive**](iagentcharacterex--getactive.md), [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md)


 

 





