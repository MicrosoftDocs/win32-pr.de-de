---
title: Aufzählen registrierter Entitäten
description: Nachdem ein Client registriert wurde, kann er eine Liste aller anderen Clients abrufen, die beim Routingtabellen-Manager registriert wurden. Einige Clients müssen bestimmte Vorgänge ausführen, wenn ein bestimmter Clienttyp erkannt wird.
ms.assetid: d94de573-7c1e-4179-a41f-5836d2c5d44a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1d67a810806c1bc29f8f18c4cdea9f3a36e5b5a95922e8f66a943a99923ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674160"
---
# <a name="enumerating-registered-entities"></a>Aufzählen registrierter Entitäten

Nachdem ein Client registriert wurde, kann er eine Liste aller anderen Clients abrufen, die beim Routingtabellen-Manager registriert wurden. Einige Clients müssen bestimmte Vorgänge ausführen, wenn ein bestimmter Clienttyp erkannt wird.

Der Client kann die [**RtmGetRegisteredEntities-Funktion**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) aufrufen. Ein Puffer von [**RTM \_ ENTITY \_ INFO-Strukturen**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) wird zurückgegeben. Nachdem der Client diese Informationen verarbeitet hat, sollte der Client [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) aufrufen, um die Handles in den **RTM \_ ENTITY \_ INFO-Strukturen frei** zu geben.

Wenn der Routingtabellen-Manager-Client im Aufruf von [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)eine Rückruffunktion bereitgestellt hat, wird der Client benachrichtigt, wenn sich andere Clients registrieren oder die Registrierung aufheben.

Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter [Aufzählen](enumerate-the-registered-entities.md) der registrierten Entitäten und Verwenden [des Ereignisbenachrichtigungsrückrufs.](use-the-event-notification-callback.md)

 

 




