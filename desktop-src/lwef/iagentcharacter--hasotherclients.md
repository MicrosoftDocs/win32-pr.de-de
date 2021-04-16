---
title: Iagentcharacter hasotherclients
description: Iagentcharacter hasotherclients
ms.assetid: ee74fa9b-2842-43ac-8493-bc69b480581e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32380e31e63278f4181cfd854ecaada1775a4fd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516118"
---
# <a name="iagentcharacterhasotherclients"></a>Iagentcharacter:: hasotherclients

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT HasOtherClients(
   long * plNumOtherClients  // address of variable for number of clients 
);                           // for character 
```

Ruft ab, ob ein Zeichen über andere Clients verfügt.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plNumOtherClients"></span><span id="plnumotherclients"></span><span id="PLNUMOTHERCLIENTS"></span>*plnumotherclients*
</dt> <dd>

Adresse einer Variablen, die die Anzahl anderer verbundener Clients für das Zeichen empfängt (Gesamtzahl der Clients abzüglich des Clients).

</dd> </dl>

 

 




