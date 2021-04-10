---
title: Iagentnotifysinkex helpcomplete
description: Iagentnotifysinkex helpcomplete
ms.assetid: f8285d05-3b96-4046-a058-0e001e47b54b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3b7dbbdf272844242943d49ed86b303d220185
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038862"
---
# <a name="iagentnotifysinkexhelpcomplete"></a>Iagentnotifysinkex:: helpcomplete

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT HelpComplete(
   long dwCharID,     // character ID
   long dwCommandID,  // command ID
   long dwCause       // cause 
);
```

Benachrichtigt eine Client Anwendung, wenn der Benutzer einen Befehl oder ein Zeichen zum Vervollständigen des Hilfe Modus auswählt.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*
</dt> <dd>

Der Bezeichner des Zeichens, für das der Hilfe Modus abgeschlossen wurde.

</dd> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwcommandid*
</dt> <dd>

Der Bezeichner des Befehls, den der Benutzer ausgewählt hat.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwcause*
</dt> <dd>

Die Ursache für das Ereignis, bei der es sich um die folgenden Werte handeln kann:



| Wert                                                                         | BESCHREIBUNG                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **Ganzzahl ohne Vorzeichen Short** **cshelpcause- \_ Befehl = 1;**<br/>             | Der Benutzer hat einen von der Anwendung bereitgestellten Befehl ausgewählt.                            |
| **Ganzzahl ohne Vorzeichen Short** **cshelpcause \_ otherprogram = 2;**<br/>        | Der Benutzer hat das Objekt " [**Befehle**](/windows/desktop/lwef/the-commands-collection-object) " eines anderen Clients ausgewählt. |
| " **Ganzzahl ohne Vorzeichen Short** **cshelpcause" für " \_ opencommandswindow = 3;** "<br/>  | Der Benutzer hat den Befehl "Sprachbefehle öffnen" ausgewählt.                                   |
| " **Ganzzahl ohne Vorzeichen Short** **cshelpcause" \_ , "closecommandswindow" = 4;**<br/> | Der Benutzer hat den Befehl "Sprachbefehle schließen" ausgewählt.                                  |
| **unsigniertes kurzes** **cshelpcause- \_ showcharacter = 5;**<br/>       | Der Benutzer hat den Befehl " *Merkmal Name* anzeigen" ausgewählt.                                  |
| **Ganzzahl ohne Vorzeichen Short** **cshelpcause- \_ hidecharacter = 6;**<br/>       | Der Benutzer hat den Befehl " *Merkmal Name* ausblenden" ausgewählt.                                  |
| **Ganzzahl ohne Vorzeichen Short** **cshelpcause- \_ Zeichen = 7;**<br/>           | Der Benutzer hat das Zeichen ausgewählt (geklickt).                                           |



 

</dd> </dl>

In der Regel wird der Hilfe Modus abgeschlossen, wenn der Benutzer auf das Zeichen klickt oder zieht oder einen Befehl aus dem Popupmenü des Zeichens auswählt. Durch Klicken auf ein anderes Zeichen oder an anderer Stelle auf dem Bildschirm wird der Hilfe Modus nicht abgebrochen. Der Client, der den Hilfe Modus für das Zeichen festlegt, kann den Hilfe Modus abbrechen, indem er [**iagentcharacter:: helpmudeon**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) auf **false** festlegt. (Hierdurch wird das Ereignis **iagentnotifysinkex:: helpcomplete** nicht auslöst.)

Wenn der Benutzer im Hilfe Modus aus dem Popupmenü des Zeichens einen Befehl auswählt, entfernt der Server das Menü, ruft die Hilfe mit der angegebenen [**HelpContextID**](helpcontextid-property.md)des Befehls auf und sendet dieses Ereignis. Die kontextabhängige (auch bekannt als was ist das?) Das Hilfefenster wird an der Zeigerposition angezeigt. Wenn der Benutzer den Befehl per Spracheingabe auswählt, wird das Hilfefenster für das Zeichen angezeigt. Wenn das Zeichen außerhalb des Bildschirms ist, wird das Fenster auf dem Bildschirm angezeigt, das der aktuellen Position des Zeichens am nächsten ist.

Wenn der Server *dwcommandid* als leere Zeichenfolge ("") zurückgibt, bedeutet dies, dass der Benutzer einen vom Server bereitgestellten Befehl ausgewählt hat.

Dieses Ereignis wird nur an die Client Anwendung gesendet, die das Zeichen in den Hilfe Modus versetzt.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharakteriex::**](iagentcharacterex--sethelpmodeon.md)Setup Element-ID, [**iagentcharakteriex:: Setup Element Dateiname**](iagentcharacterex--sethelpfilename.md), [**iagentcharakteriex::**](iagentcharacterex--sethelpcontextid.md)Setup Element-ID, [**iagentcommandsex::**](iagentcommandsex--sethelpcontextid.md) ab.


 

