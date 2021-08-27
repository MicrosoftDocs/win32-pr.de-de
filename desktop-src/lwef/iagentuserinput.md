---
title: IAgentUserInput
description: IAgentUserInput
ms.assetid: 59ce7337-6031-4449-8b29-fd0c6737c3e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58ed14c9097a4bd5d3d743a5c026f3e13d6d5ed29a73edb619dd0b2e8bdae17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114650"
---
# <a name="iagentuserinput"></a>IAgentUserInput

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Wenn der Server den eingabeaktiven Client mit [**IAgentNotifySink::Command**](iagentnotifysink--command.md)benachrichtigt, gibt er Informationen über das [**IAgentUserInput-Objekt**](/windows/desktop/lwef/iagentuserinput) zurück. **IAgentUserInput** definiert eine Schnittstelle, mit der Anwendungen diese Werte abfragen können.

**Methoden in Vtable-Reihenfolge**



| IAgentUserInput-Methoden                                         | Beschreibung                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCount**](iagentuserinput--getcount.md)                   | Gibt die Anzahl von Befehlsalternativen zurück, die in einem [**Command-Ereignis**](command-event.md) zurückgegeben werden.                                         |
| [**GetItemID**](iagentuserinput--getitemid.md)                 | Gibt die ID für eine bestimmte [**Befehlsalternative**](command-event.md) zurück.                                                              |
| [**GetItemConfidence**](iagentuserinput--getitemconfidence.md) | Gibt den Wert der [**Confidence-Eigenschaft**](confidence-property.md) für eine bestimmte [**Command-Alternative**](command-event.md) zurück. |
| [**GetItemText**](iagentuserinput--getitemtext.md)             | Gibt den Wert von [**Sprachtext**](voice-property.md) für eine bestimmte [**Befehlsalternative**](command-event.md) zurück.                   |
| [**GetAllItemData**](iagentuserinput--getallitemdata.md)       | Gibt die Daten für alle [**Command-Alternativen**](command-event.md) zurück.                                                                  |



 

 

 