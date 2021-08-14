---
title: Registrieren für Änderungsbenachrichtigungen
description: Ein Client kann sich registrieren, um Benachrichtigungen über Änderungen an Routinginformationen zu erhalten, die im Routingtabellen-Manager gespeichert sind. Diese Anforderung kann nur ausgeführt werden, nachdem sich ein Client beim Routingtabellen-Manager registriert hat.
ms.assetid: 90dc98eb-0d0b-4450-848b-c7cedab75a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7049478a5be834b08b7bb17ad9ebfb0fdf70736837f27d53e7900bf7bfdc88dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788619"
---
# <a name="registering-for-change-notification"></a>Registrieren für Änderungsbenachrichtigungen

Ein Client kann sich registrieren, um Benachrichtigungen über Änderungen an Routinginformationen zu erhalten, die im Routingtabellen-Manager gespeichert sind. Diese Anforderung kann nur ausgeführt werden, nachdem sich ein Client beim Routingtabellen-Manager registriert hat.

Um sich für änderungsbenachrichtigungen zu registrieren, muss ein Client [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification)aufrufen und die Arten von Änderungen angeben, für die der Client Benachrichtigungen empfangen muss. Wenn der Client über Änderungen an bestimmten Zielen benachrichtigt werden muss, ruft der Client [**rtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) einmal für jedes Ziel auf.

Der Client kann den Empfang von Änderungsbenachrichtigungen beenden, indem [**er RtmDeregisterFromChangeNotification aufruft.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification)

Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter [Registrieren für Änderungsbenachrichtigungen.](register-for-change-notification.md)

 

 




