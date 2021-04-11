---
title: Iagent
description: Iagent
ms.assetid: 35b12006-a938-450c-969a-7b73a3768a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12900a4288b9917d695dd25d4b81362b67c93587
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310051"
---
# <a name="iagent"></a>Iagent

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

**Iagent** definiert eine Schnittstelle, die es Anwendungen ermöglicht, Zeichen zu laden, Ereignisse zu empfangen und den aktuellen Status des Microsoft-Agent-Servers zu überprüfen. Diese Funktionen sind auch über [**iagentex**](iagentex.md)verfügbar.

Die in früheren Versionen enthaltene getangeh-Methode ist veraltet und gibt aus Gründen der Abwärtskompatibilität **false** zurück.

**Methoden in Vtable-Reihenfolge**



| Iagent-Methoden                               | BESCHREIBUNG                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| [**Laden**](load-method.md)                  | Lädt die Datendatei eines Zeichens.                                |
| [**Entladen**](unload-method.md)              | Entlädt die Datendatei eines Zeichens.                              |
| [**Registrieren**](iagent--register.md)         | Registriert eine Benachrichtigungs Senke für den Client.                 |
| [**Unegiester**](iagent--unregister.md)      | Hebt die Registrierung der Benachrichtigungs Senke eines Clients auf.                     |
| [**Getcharacter**](iagent--getcharacter.md) | Gibt die iagentcharacter-Schnittstelle für ein geladenes Zeichen zurück. |



 

 

 




