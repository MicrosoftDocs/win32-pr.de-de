---
title: HelpComplete-Ereignis
description: HelpComplete-Ereignis
ms.assetid: d805f089-154f-4b39-9d78-a02b732f87ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a41b4dc0b1b6767b113220f2a922d1a512132a2cd7754891acb9c99b92d0039
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478995"
---
# <a name="helpcomplete-event"></a>HelpComplete-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt an, dass der kontextbezogene Hilfemodus beendet wurde.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Sub-Agent.**(ByVal* *  *CharacterID!),* ByVal-Name**, *  *ByVal-Ursache))* *  *



| Teil          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Gibt die ID des geklickten Zeichens als Zeichenfolge zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *Name*        | Gibt einen Zeichenfolgenwert zurück, der den Namen (ID) des Befehls identifiziert.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| *Ursache*       | Gibt einen Wert zurück, der angibt, wodurch der Hilfemodus abgeschlossen wurde. 1 Der Benutzer hat einen von Ihrer Anwendung bereitgestellten Befehl ausgewählt.<br/> 2 Der Benutzer hat das [**Commands-Objekt**](/windows/desktop/lwef/the-commands-collection-object) eines anderen Clients ausgewählt.<br/> 3 Der Benutzer hat den Befehl "Open Voice Commands" ausgewählt.<br/> 4 Der Benutzer hat den Befehl Sprachbefehle schließen ausgewählt.<br/> 5 Der Benutzer hat den Befehl *Zeichenname* anzeigen ausgewählt.<br/> 6 Der Benutzer hat den Befehl *CharacterName* ausblenden ausgewählt.<br/> 7 Der Benutzer hat das Zeichen ausgewählt (geklickt).<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Hinweise

In der Regel wird der Hilfemodus abgeschlossen, wenn der Benutzer auf das Zeichen klickt oder es zieht oder einen Befehl aus dem Popupmenü des Zeichens auswählt. Wenn Sie auf ein anderes Zeichen oder an anderer Stelle auf dem Bildschirm klicken, wird der Hilfemodus nicht abgebrochen. Der Client, der den Hilfemodus für das Zeichen festlegt, kann den Hilfemodus abbrechen, indem [**HelpModeOn**](helpmodeon-property.md) auf **False** festgelegt wird. (Dadurch wird das **HelpComplete-Ereignis** nicht ausgelöst.)

Wenn der Benutzer im Hilfemodus im Popupmenü des Zeichens einen Befehl auswählt, entfernt der Server das Menü, ruft die Hilfe mit der angegebenen [**HelpContextID**](helpcontextid-property.md)des Befehls auf und sendet dieses Ereignis. Kontextabhängig (auch bekannt als What es This?) Das Hilfefenster wird an der Zeigerposition angezeigt. Wenn der Benutzer den Befehl per Spracheingabe auswählt, wird das Hilfefenster über dem Zeichen angezeigt. Wenn sich das Zeichen außerhalb des Bildschirms befindet, wird das Fenster auf dem Bildschirm angezeigt, der der aktuellen Position des Zeichens am nächsten ist.

Wenn der Server Name als leere Zeichenfolge ("") zurückgibt, gibt er an, dass der Benutzer einen vom Server bereitgestellten Befehl ausgewählt hat.

Dieses Ereignis wird nur an die Clientanwendung gesendet, die das Zeichen im Hilfemodus platziert.

### <a name="see-also"></a>Weitere Informationen

[**HelpModeOn-Eigenschaft,**](helpmodeon-property.md) [ **HelpContextID-Eigenschaft**](helpcontextid-property.md)


 

