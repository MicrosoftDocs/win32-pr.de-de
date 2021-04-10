---
title: Registrieren für Änderungs Benachrichtigung
description: Ein Client kann sich registrieren, um Benachrichtigungen über Änderungen an Routing Informationen zu erhalten, die im Routing Tabellen-Manager gespeichert sind. Diese Anforderung kann nur vorgenommen werden, nachdem ein Client beim Routing Tabellen-Manager registriert wurde.
ms.assetid: 90dc98eb-0d0b-4450-848b-c7cedab75a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3a98062fee73c481c1f47c32fa7eeb5465a112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309843"
---
# <a name="registering-for-change-notification"></a>Registrieren für Änderungs Benachrichtigung

Ein Client kann sich registrieren, um Benachrichtigungen über Änderungen an Routing Informationen zu erhalten, die im Routing Tabellen-Manager gespeichert sind. Diese Anforderung kann nur vorgenommen werden, nachdem ein Client beim Routing Tabellen-Manager registriert wurde.

Um sich für die Änderungs Benachrichtigung zu registrieren, muss ein Client [**rtmregisterforchangenotifizierung**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification)aufrufen und die Typen der Änderungen angeben, für die der Client eine Benachrichtigung empfangen muss. Wenn der Client über Änderungen an bestimmten Zielen benachrichtigt werden muss, ruft der Client für jedes Ziel einmal [**rtmmarkdestforchangenotifizierung**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) auf.

Der Client kann die Änderungs Benachrichtigungen durch Aufrufen von [**rtmderegisterfromchangenotifinicht**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification)mehr empfangen.

Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter [registrieren für Änderungs Benachrichtigungen](register-for-change-notification.md).

 

 




