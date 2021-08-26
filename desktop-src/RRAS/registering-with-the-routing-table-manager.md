---
title: Registrieren beim Routingtabellen-Manager
description: Bevor ein Client auf die Routingtabelle zugreifen kann, muss er sich zunächst mithilfe der RtmRegisterEntity-Funktion beim Routingtabellen-Manager registrieren.
ms.assetid: 9bdbe138-d31b-42bb-9c51-5f1c5e8a4ca7
keywords:
- Routing Table Manager Version 2 RRAS , registrieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 088072fac8679d9b2f87729b67a826ac850e77109f18b28fef3c2dc33c433f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028290"
---
# <a name="registering-with-the-routing-table-manager"></a>Registrieren beim Routingtabellen-Manager

Bevor ein Client auf die Routingtabelle zugreifen kann, muss er sich zunächst mithilfe der [**RtmRegisterEntity-Funktion**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) beim Routingtabellen-Manager registrieren.

Wenn ein Client registriert wird, übergibt er eine [**RTM \_ ENTITY \_ INFO-Struktur**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) an den Routingtabellen-Manager. Diese Struktur enthält die Informationen, die einen Client, die Adressfamilie und die Instanz des Routingtabellen-Managers eindeutig identifizieren, bei dem der Client registriert wird. Ein Client kann auch den RÜCKRUF FÜR [**\_ \_ RTM-EREIGNISSE**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) einrichten. Der Routingtabellen-Manager verwendet diesen Rückruf, um den Client über Ereignisse wie Änderungsbenachrichtigungen und Clientregistrierungen zu benachrichtigen.

Der Routingtabellen-Manager schließt die Registrierungsverarbeitung ab und gibt ein Handle an den Client zurück. Der Client muss dieses Handle für alle nachfolgenden Aufrufe von RTMv2-Funktionen verwenden.

Die in RTMv2 verwendete [**RtmRegisterEntity-Funktion entspricht**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) der [**RtmRegisterClient-Funktion,**](rtmregisterclient.md) die in RTMv1 verwendet wird. Die **RtmRegisterClient-Funktion** ist veraltet, mit Ausnahme von Clients, die IPX verwenden.

Sobald ein Client die Interaktion mit dem Routingtabellen-Manager abgeschlossen hat, muss er [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity)aufrufen. Der Routingtabellen-Manager zerstört das dem Client zugeordnete Handle. Um Speicherverluste zu vermeiden, muss der Client sicherstellen, dass er alle Handles freigibt und alle Routen und nächsten Hops löscht, die er besitzt, bevor **er RtmDeregisterEntity aufruft.**

Beispielcode zur Verwendung dieser Funktionen finden Sie unter [Registrieren beim Routingtabellen-Manager](register-with-the-routing-table-manager.md) und [Verwenden des Ereignisbenachrichtigungsrückrufs.](use-the-event-notification-callback.md)

 

 




