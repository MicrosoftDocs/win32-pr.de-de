---
title: IAgentUserInput GetAllItemData
description: IAgentUserInput GetAllItemData
ms.assetid: d1857b28-c745-4ed2-b49e-774f247e7348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d74c59e05e021fdff05ee8991c4563a7a4be918f6ecb244c26402b5234b240b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105146"
---
# <a name="iagentuserinputgetallitemdata"></a>IAgentUserInput::GetAllItemData

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetAllItemData(
   VARIANT * pdwItemIndices,  // address of variable for alternative IDs
   VARIANT * plConfidences,   // address of variable for confidence scores
   VARIANT * pbszText         // address of variable for voice text
);
```

Ruft die Daten für alle [**Befehlsalternativen**](command-event.md) ab, die an einen [**IAgentNotifySink::Command-Rückruf**](iagentnotifysink--command.md) übergeben werden.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*
</dt> <dd>

Adresse einer Variablen, die die IDs von [**Befehlen**](command-event.md) empfängt, die an den [**IAgentNotifySink::Command-Rückruf**](iagentnotifysink--command.md) übergeben werden.

</dd> <dt>

<span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*
</dt> <dd>

Adresse einer Variablen, die die Zuverlässigkeitsbewertungen für [**Befehlsalternativen**](command-event.md) empfängt, die an den [**IAgentNotifySink::Command-Rückruf**](iagentnotifysink--command.md) übergeben werden.

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*
</dt> <dd>

Adresse einer Variablen, die den Sprachtext für [**Befehlsalternativen**](command-event.md) empfängt, die an den [**IAgentNotifySink::Command-Rückruf**](iagentnotifysink--command.md) übergeben werden.

</dd> </dl>

Wenn die Spracheingabe [**IAgentNotifySink::Command**](iagentnotifysink--command.md)auslöst, gibt der Server die beste Übereinstimmung, die zweitbeste Übereinstimmung und die dritte beste Übereinstimmung zurück, wenn diese von der Sprach-Engine bereitgestellt werden. Sie stellt die relativen Zuverlässigkeitsbewertungen im Bereich von -100 bis 100 und den tatsächlichen Text bereit, der von der Sprach-Engine "gehört" wird. Wenn die beste Übereinstimmung ein vom Server bereitgestellter Befehl war, sendet der Server eine NULL-ID, sendet aber trotzdem eine Zuverlässigkeitsbewertung und den [**Sprachtext.**](voice-property.md)

Wenn die Spracheingabe nicht die Quelle für das Ereignis war, Wenn der Benutzer beispielsweise den Befehl im Popupmenü des Zeichens ausgewählt hat, gibt der Microsoft-Agent-Server die ID des ausgewählten [**Befehls**](command-event.md) mit einer Zuverlässigkeitsbewertung von 100 und Sprachtext als NULL zurück. Die anderen Alternativen geben als NULL mit Konfidenzbewertungen von null (0) und Sprachtext als NULL zurück.

> [!Note]  
> Nicht alle Spracherkennungs-Engines geben möglicherweise alle Werte für alle Parameter dieses Ereignisses zurück. Wenden Sie sich an Ihren Engine-Anbieter, um zu ermitteln, ob die Engine die Microsoft Speech-API-Schnittstelle für die Rückgabe von Alternativen und Zuverlässigkeitsbewertungen unterstützt.

 

## <a name="see-also"></a>Weitere Informationen

[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md)


 

 




