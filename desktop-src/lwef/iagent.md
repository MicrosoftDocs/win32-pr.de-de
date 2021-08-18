---
title: IAgent
description: IAgent
ms.assetid: 35b12006-a938-450c-969a-7b73a3768a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3931c277fbe4a5943ef5881da12cf3669b2e8894c95052f61bc8411e21c7ae3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751425"
---
# <a name="iagent"></a>IAgent

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

**IAgent** definiert eine Schnittstelle, mit der Anwendungen Zeichen laden, Ereignisse empfangen und den aktuellen Status des Microsoft-Agent-Servers überprüfen können. Diese Funktionen sind auch über [**IAgentEx**](iagentex.md)verfügbar.

Die in früheren Versionen enthaltene GetSuspended-Methode ist veraltet und gibt aus Gründen der Abwärtskompatibilität **False** zurück.

**Methoden in Vtable-Reihenfolge**



| IAgent-Methoden                               | Beschreibung                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| [**Laden**](load-method.md)                  | Lädt die Datendatei eines Zeichens.                                |
| [**Entladen**](unload-method.md)              | Entlädt die Datendatei eines Zeichens.                              |
| [**Registrieren**](iagent--register.md)         | Registriert eine Benachrichtigungssenke für den Client.                 |
| [**Unegister**](iagent--unregister.md)      | Aufheben der Registrierung der Benachrichtigungssenke eines Clients.                     |
| [**GetCharacter**](iagent--getcharacter.md) | Gibt die IAgentCharacter-Schnittstelle für ein geladenes Zeichen zurück. |



 

 

 




