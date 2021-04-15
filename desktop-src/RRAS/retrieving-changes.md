---
title: Abrufen von Änderungen
description: Nachdem ein Client sich für Benachrichtigungen über bestimmte Änderungen registriert hat und eine oder mehrere dieser Änderungen auftreten, empfängt der Client eine Benachrichtigung vom Routing Tabellen-Manager.
ms.assetid: 5ddebf2d-e3cb-451c-b082-708d2c7d0f79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ccf66d8a1df671cbd9059c444cf26321911bb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515620"
---
# <a name="retrieving-changes"></a>Abrufen von Änderungen

Nachdem ein Client sich für Benachrichtigungen über bestimmte Änderungen registriert hat und eine oder mehrere dieser Änderungen auftreten, empfängt der Client eine Benachrichtigung vom Routing Tabellen-Manager. Der Routing Tabellen-Manager verwendet den [**RTM- \_ Ereignis \_ Rückruf**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) Rückruf, der in einem vorherigen Aufrufen von [**rtmregisterentity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)angegeben wurde. Der Routing Tabellen-Manager gibt an, dass ein RTM- \_ Änderungs \_ Benachrichtigungs Ereignis aufgetreten ist.

Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter [Verwenden des Ereignis Benachrichtigungs Rückrufs](use-the-event-notification-callback.md).

 

 




