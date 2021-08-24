---
title: IAgentCharacter HasOtherClients
description: IAgentCharacter HasOtherClients
ms.assetid: ee74fa9b-2842-43ac-8493-bc69b480581e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6469c289d846cb34e14c6afabbed72647e6e786fbda273baaf70532d4ad6578c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665750"
---
# <a name="iagentcharacterhasotherclients"></a>IAgentCharacter::HasOtherClients

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT HasOtherClients(
   long * plNumOtherClients  // address of variable for number of clients 
);                           // for character 
```

Ruft ab, ob ein Zeichen über andere Clients verfügt.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plNumOtherClients"></span><span id="plnumotherclients"></span><span id="PLNUMOTHERCLIENTS"></span>*plNumOtherClients*
</dt> <dd>

Adresse einer Variablen, die die Anzahl anderer verbundener Clients für das Zeichen empfängt (Gesamtzahl der Clients abzüglich Ihres Clients).

</dd> </dl>

 

 




