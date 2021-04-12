---
title: Registrieren beim Routing Tabellen-Manager
description: Bevor ein Client auf die Routing Tabelle zugreifen kann, muss er sich zunächst mithilfe der rtmregisterentity-Funktion beim Routing Tabellen-Manager registrieren.
ms.assetid: 9bdbe138-d31b-42bb-9c51-5f1c5e8a4ca7
keywords:
- Routing Table Manager Version 2 RRAS, registrieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ce5a1b350ec5420b3fc32a4e5a68a213a61151
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206685"
---
# <a name="registering-with-the-routing-table-manager"></a>Registrieren beim Routing Tabellen-Manager

Bevor ein Client auf die Routing Tabelle zugreifen kann, muss er sich zunächst mithilfe der [**rtmregisterentity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) -Funktion beim Routing Tabellen-Manager registrieren.

Wenn ein Client registriert wird, übergibt er eine [**RTM- \_ Entitäts \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) Struktur an den Routing Tabellen-Manager. Diese Struktur enthält die Informationen, mit denen ein Client, die Adressfamilie und die Instanz des Routing Tabellen-Managers, mit dem der Client registriert wird, eindeutig identifiziert werden. Ein Client kann auch den [**RTM- \_ Ereignis \_ Rückruf**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) Rückruf einrichten. Der Routing Tabellen-Manager verwendet diesen Rückruf, um den Client über Ereignisse wie Änderungs Benachrichtigungen und Client Registrierungen zu benachrichtigen.

Der Routing Tabellen-Manager schließt die Registrierungs Verarbeitung ab und gibt ein Handle an den Client zurück. Der Client muss dieses Handle für alle nachfolgenden Aufrufe von RTMv2-Funktionen verwenden.

Die in RTMv2 verwendete [**rtmregisterentity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) -Funktion ist analog zur [**rtmregisterclient**](rtmregisterclient.md) -Funktion, die in RTMv1 verwendet wird. Die **rtmregisterclient** -Funktion ist veraltet, außer bei Clients, die IPX verwenden.

Nachdem die Interaktion eines Clients mit dem Routing Tabellen-Manager abgeschlossen ist, muss er [**rtmderegisterentity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity)aufrufen. Der Routing Tabellen-Manager zerstört das Handle, das dem Client zugeordnet ist. Um Speicher Verluste zu vermeiden, muss der Client sicherstellen, dass alle Handles freigegeben werden und alle Routen und nächsten Hops gelöscht werden, die er besitzt, bevor **rtmderegisterentity** aufgerufen wird.

Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter [registrieren beim Routing Tabellen-Manager](register-with-the-routing-table-manager.md) und [Verwenden des Ereignis Benachrichtigungs Rückrufs](use-the-event-notification-callback.md).

 

 




