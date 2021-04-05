---
title: Auflisten registrierter Entitäten
description: Nachdem ein Client registriert wurde, kann der Client eine Liste aller anderen Clients abrufen, die beim Routing Tabellen-Manager registriert wurden. Einige Clients müssen bestimmte Vorgänge ausführen, wenn ein bestimmter Clienttyp erkannt wird.
ms.assetid: d94de573-7c1e-4179-a41f-5836d2c5d44a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac92ccf89336d3fbca378209b9e79877d9b426a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037013"
---
# <a name="enumerating-registered-entities"></a>Auflisten registrierter Entitäten

Nachdem ein Client registriert wurde, kann der Client eine Liste aller anderen Clients abrufen, die beim Routing Tabellen-Manager registriert wurden. Einige Clients müssen bestimmte Vorgänge ausführen, wenn ein bestimmter Clienttyp erkannt wird.

Der Client kann die Funktion [**rtmgetregisteredentities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) aufzurufen. Ein Puffer von [**RTM- \_ Entitäts \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) Strukturen wird zurückgegeben. Nachdem der Client diese Informationen verarbeitet hat, sollte der Client [**rtmreleaseentities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) aufgerufen werden, um die Handles in den **RTM- \_ Entitäts \_ Informations** Strukturen freizugeben.

Wenn der Routing Tabellen-Manager-Client im Aufrufen von [**rtmregisterentity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)eine Rückruffunktion bereitgestellt hat, wird der Client benachrichtigt, wenn sich andere Clients registrieren oder die Registrierung aufheben.

Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter Auflisten [der registrierten Entitäten](enumerate-the-registered-entities.md) und [Verwenden des Ereignis Benachrichtigungs Rückrufs](use-the-event-notification-callback.md).

 

 




