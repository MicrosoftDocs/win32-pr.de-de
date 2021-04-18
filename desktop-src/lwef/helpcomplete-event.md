---
title: Helpcomplete-Ereignis
description: Helpcomplete-Ereignis
ms.assetid: d805f089-154f-4b39-9d78-a02b732f87ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3984f4b67eaed6bc9226685e927c35e151c11e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337220"
---
# <a name="helpcomplete-event"></a>Helpcomplete-Ereignis

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt an, dass der kontextbezogene Hilfe Modus beendet wurde.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**Sub** - *Agent. * * * (ByVal*- *  *Merkmal-ID * * *, ByVal*- *  *Name * * *, ByVal*- *  *Ursache * * *)**



| Teil          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Merkmal-ID* | Gibt die ID des angeklickten Zeichens als Zeichenfolge zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *Name*        | Gibt einen Zeichen folgen Wert zurück, der den Namen (ID) des Befehls identifiziert.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| *Ursache*       | Gibt einen Wert zurück, der angibt, wodurch der Hilfe Modus beendet wurde. 1 der Benutzer hat einen von der Anwendung bereitgestellten Befehl ausgewählt.<br/> 2 der Benutzer hat das Objekt " [**Befehle**](/windows/desktop/lwef/the-commands-collection-object) " eines anderen Clients ausgewählt.<br/> 3 der Benutzer hat den Befehl "Sprachbefehle öffnen" ausgewählt.<br/> 4 der Benutzer hat den Befehl "Sprachbefehle schließen" ausgewählt.<br/> 5 der Benutzer hat den Befehl " *Merkmal Name* anzeigen" ausgewählt.<br/> 6 der Benutzer hat den Befehl " *Merkmal Name* ausblenden" ausgewählt.<br/> 7 der Benutzer hat das Zeichen ausgewählt (geklickt).<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

In der Regel wird der Hilfe Modus beendet, wenn der Benutzer auf das Zeichen klickt oder zieht oder einen Befehl aus dem Popupmenü des Zeichens auswählt. Durch Klicken auf ein anderes Zeichen oder an anderer Stelle auf dem Bildschirm wird der Hilfe Modus nicht abgebrochen. Der Client, der den Hilfe Modus für das Zeichen festlegt, kann den Hilfe Modus abbrechen, indem [**helpmudeon**](helpmodeon-property.md) auf **false** festgelegt wird. (Dies löst nicht das **helpcomplete** -Ereignis aus.)

Wenn der Benutzer im Hilfe Modus aus dem Popupmenü des Zeichens einen Befehl auswählt, entfernt der Server das Menü, ruft die Hilfe mit der angegebenen [**HelpContextID**](helpcontextid-property.md)des Befehls auf und sendet dieses Ereignis. Die kontextabhängige (auch bekannt als was ist das?) Das Hilfefenster wird an der Zeigerposition angezeigt. Wenn der Benutzer den Befehl per Spracheingabe auswählt, wird das Hilfefenster für das Zeichen angezeigt. Wenn das Zeichen außerhalb des Bildschirms ist, wird das Fenster auf dem Bildschirm angezeigt, das der aktuellen Position des Zeichens am nächsten ist.

Wenn der Server den Namen als leere Zeichenfolge ("") zurückgibt, bedeutet dies, dass der Benutzer einen vom Server bereitgestellten Befehl ausgewählt hat.

Dieses Ereignis wird nur an die Client Anwendung gesendet, die das Zeichen im Hilfe Modus platziert.

### <a name="see-also"></a>Weitere Informationen

[**Helpmudeon-Eigenschaft**](helpmodeon-property.md), [ **HelpContextID-Eigenschaft**](helpcontextid-property.md)


 

