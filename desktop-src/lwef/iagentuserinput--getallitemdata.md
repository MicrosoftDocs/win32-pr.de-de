---
title: Iagentuserinput getallitemdata
description: Iagentuserinput getallitemdata
ms.assetid: d1857b28-c745-4ed2-b49e-774f247e7348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced6a618d4fbbc093bf54c19fc393b7e195f2069
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470741"
---
# <a name="iagentuserinputgetallitemdata"></a>Iagentuserinput:: getallitemdata

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetAllItemData(
   VARIANT * pdwItemIndices,  // address of variable for alternative IDs
   VARIANT * plConfidences,   // address of variable for confidence scores
   VARIANT * pbszText         // address of variable for voice text
);
```

Ruft die Daten für alle [**Befehls**](command-event.md) Alternativen ab, die an einen [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt werden.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwitemindices*
</dt> <dd>

Adresse einer Variablen, die die IDs der [**Befehle**](command-event.md) empfängt, die an den [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt werden.

</dd> <dt>

<span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plconfidential*
</dt> <dd>

Adresse einer Variablen, die die Vertrauens Ergebnisse für [**Befehls**](command-event.md) Alternativen empfängt, die an den [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt werden.

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbsztext*
</dt> <dd>

Adresse einer Variablen, die den sprach Text für [**Befehls**](command-event.md) Alternativen empfängt, die an den [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt werden.

</dd> </dl>

Wenn die Spracheingabe [**iagentnotifysink:: Command**](iagentnotifysink--command.md)auslöst, gibt der Server die beste Entsprechung zurück, die zweitbeste Entsprechung und die beste Entsprechung, wenn diese von der Sprach-Engine bereitgestellt werden. Sie stellt die relativen Vertrauens Ergebnisse im Bereich von-100 bis 100 und den tatsächlichen Text "Heard" der Sprach-Engine bereit. Wenn die beste Entsprechung ein vom Server bereitgestellter Befehl war, sendet der Server eine NULL-ID, sendet jedoch dennoch eine Vertrauenswürdigkeit und den [**Stimm**](voice-property.md) Text.

, Wenn die Spracheingabe nicht die Quelle für das Ereignis war. Wenn der Benutzer z. b. den Befehl aus dem Popupmenü des Zeichens ausgewählt hat, gibt der Microsoft-Agent-Server die ID des ausgewählten [**Befehls**](command-event.md) mit einem Vertrauens Ergebnis von 100 und einem sprach Text als NULL zurück. Die anderen Alternativen geben als NULL zurück, wenn die Vertrauenswürdigkeit NULL (0) und der sprach Text NULL ist.

> [!Note]  
> Nicht alle Spracherkennungs-Engines geben möglicherweise alle Werte für alle Parameter dieses Ereignisses zurück. Wenden Sie sich an den Hersteller Ihrer Hersteller, um zu ermitteln, ob die Engine die Microsoft Speech API-Schnittstelle für das Zurückgeben von Alternativen und Vertrauens Bewertungen

 

## <a name="see-also"></a>Weitere Informationen

[**Iagentuserinput:: getitemconfidence**](iagentuserinput--getitemconfidence.md), [**iagentuserinput:: GetItemText**](iagentuserinput--getitemtext.md), [**iagentuserinput:: getItemID**](iagentuserinput--getitemid.md)


 

 




