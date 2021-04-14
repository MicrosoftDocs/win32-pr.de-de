---
title: Iagentuserinput
description: Iagentuserinput
ms.assetid: 59ce7337-6031-4449-8b29-fd0c6737c3e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37d195d6b5d1294c071a1b73d1da95548cb7a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390237"
---
# <a name="iagentuserinput"></a>Iagentuserinput

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Wenn vom Server der Eingabe-aktiv-Client mit dem [**Befehl iagentnotifysink::**](iagentnotifysink--command.md)benachrichtigt wird, werden Informationen über das [**iagentuserinput**](/windows/desktop/lwef/iagentuserinput) -Objekt zurückgegeben. **Iagentuserinput** definiert eine Schnittstelle, die es Anwendungen ermöglicht, diese Werte abzufragen.

**Methoden in Vtable-Reihenfolge**



| Iagentuserinput-Methoden                                         | BESCHREIBUNG                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCount**](iagentuserinput--getcount.md)                   | Gibt die Anzahl der Befehls Alternativen zurück, die in einem [**Befehls**](command-event.md) Ereignis zurückgegeben werden.                                         |
| [**GetItemID**](iagentuserinput--getitemid.md)                 | Gibt die ID für eine bestimmte [**Befehls**](command-event.md) Alternative zurück.                                                              |
| [**Getitemconfidence**](iagentuserinput--getitemconfidence.md) | Gibt den Wert der [**Confidence**](confidence-property.md) -Eigenschaft für eine bestimmte [**Befehls**](command-event.md) Alternative zurück. |
| [**GetItemText**](iagentuserinput--getitemtext.md)             | Gibt den Wert von [**voicetext für**](voice-property.md) eine bestimmte [**Befehls**](command-event.md) Alternative zurück.                   |
| [**Getallitemdata**](iagentuserinput--getallitemdata.md)       | Gibt die Daten für alle [**Befehls**](command-event.md) Alternativen zurück.                                                                  |



 

 

 