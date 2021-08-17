---
title: IAgentNotifySinkEx HelpComplete
description: IAgentNotifySinkEx HelpComplete
ms.assetid: f8285d05-3b96-4046-a058-0e001e47b54b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6ad0cc7212a7e7bedbcb968f9b9d2a658f520f1a3593595ff03091b03ba32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749562"
---
# <a name="iagentnotifysinkexhelpcomplete"></a>IAgentNotifySinkEx::HelpComplete

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT HelpComplete(
   long dwCharID,     // character ID
   long dwCommandID,  // command ID
   long dwCause       // cause 
);
```

Benachrichtigt eine Clientanwendung, wenn der Benutzer einen Befehl oder ein Zeichen auswählt, um den Hilfemodus zu vervollständigen.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Bezeichner des Zeichens, für das der Hilfemodus abgeschlossen wurde.

</dd> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

Bezeichner des befehls, den der Benutzer ausgewählt hat.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

Die Ursache für das Ereignis kann die folgenden Werte sein:



| Wert                                                                         | BESCHREIBUNG                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **CSHELPCAUSE \_ COMMAND = 1;**<br/>             | Der Benutzer hat einen von Ihrer Anwendung bereitgestellten Befehl ausgewählt.                            |
| **const unsigned short** **CSHELPCAUSE \_ OTHERPROGRAM = 2;**<br/>        | Der Benutzer hat das [**Commands-Objekt**](/windows/desktop/lwef/the-commands-collection-object) eines anderen Clients ausgewählt. |
| **const unsigned short** **CSHELPCAUSE \_ OPENCOMMANDSWINDOW = 3;**<br/>  | Der Benutzer hat den Befehl Open Voice Commands (Sprachbefehle öffnen) ausgewählt.                                   |
| **const unsigned short** **CSHELPCAUSE \_ CLOSECOMMANDSWINDOW = 4;**<br/> | Der Benutzer hat den Befehl Sprachbefehle schließen ausgewählt.                                  |
| **const unsigned short** **CSHELPCAUSE \_ SHOWCHARACTER = 5;**<br/>       | Der Benutzer hat den Befehl *Zeichenname anzeigen* ausgewählt.                                  |
| **const unsigned short** **CSHELPCAUSE \_ HIDECHARACTER = 6;**<br/>       | Der Benutzer hat den Befehl *CharacterName ausblenden* ausgewählt.                                  |
| **const unsigned short** **CSHELPCAUSE \_ CHARACTER = 7;**<br/>           | Der Benutzer hat das Zeichen ausgewählt (geklickt).                                           |



 

</dd> </dl>

In der Regel wird der Hilfemodus abgeschlossen, wenn der Benutzer auf das Zeichen klickt oder es zieht oder einen Befehl aus dem Popupmenü des Zeichens auswählt. Wenn Sie auf ein anderes Zeichen oder an anderer Stelle auf dem Bildschirm klicken, wird der Hilfemodus nicht abgebrochen. Der Client, der den Hilfemodus für das Zeichen festgelegt hat, kann den Hilfemodus abbrechen, indem [**er IAgentCharacter::HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) auf **False festgelegt.** (Dadurch wird das **IAgentNotifySinkEx::HelpComplete-Ereignis nicht** ausgelöst.)

Wenn der Benutzer einen Befehl aus dem Popupmenü des Zeichens im Hilfemodus auswählt, entfernt der Server das Menü, ruft Hilfe mit der angegebenen [**HelpContextID**](helpcontextid-property.md)des Befehls auf und sendet dieses Ereignis. Die kontextsensitive (auch bekannt als What es This?) Das Hilfefenster wird an der Position des Zeigers angezeigt. Wenn der Benutzer den Befehl per Spracheingabe auswählt, wird das Hilfefenster über dem Zeichen angezeigt. Wenn das Zeichen nicht auf dem Bildschirm angezeigt wird, wird das Fenster auf dem Bildschirm angezeigt, der der aktuellen Position des Zeichens am nächsten ist.

Wenn der Server *dwCommandID* als leere Zeichenfolge ("") zurückgibt, gibt dies an, dass der Benutzer einen vom Server bereitgestellten Befehl ausgewählt hat.

Dieses Ereignis wird nur an die Clientanwendung gesendet, die das Zeichen in den Hilfemodus setzt.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md), [**IAgentCharacterEx::SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)


 

