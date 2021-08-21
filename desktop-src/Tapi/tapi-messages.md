---
description: Nachrichten werden verwendet, um die Anwendung über asynchrone Ereignisse zu benachrichtigen. Alle diese Nachrichten werden über den Nachrichtenbenachrichtigungsmechanismus, den die Anwendung in lineInitializeEx angegeben hat, an die Anwendung gesendet.
ms.assetid: d302819e-c522-470a-be5e-52625c9223a4
title: TAPI-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd0a73a5ed845901d3cbe937a366a357c149541e8973a423310345dc241b92d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002728"
---
# <a name="tapi-messages"></a>TAPI-Nachrichten

Nachrichten werden verwendet, um die Anwendung über asynchrone Ereignisse zu benachrichtigen. Alle diese Nachrichten werden über den Nachrichtenbenachrichtigungsmechanismus, den die Anwendung in [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)angegeben hat, an die Anwendung gesendet.

Die Nachricht enthält immer ein Handle für das relevante Objekt (Telefon, Zeile oder Anruf), mit dem die Anwendung den Nachrichtentyp bestimmen kann.

Bestimmte Nachrichten werden verwendet, um die Anwendung über eine Änderung des Status eines Objekts zu benachrichtigen. Diese Meldungen stellen das Objekthandle bereit und geben einen Hinweis darauf, welches Statuselement geändert wurde. Die Anwendung kann die entsprechende Funktion "Status abrufen" des Objekts aufrufen, um den vollständigen Status des Objekts abzurufen.

Wenn ein Ereignis auftritt, können Nachrichten an 0 (null), eine oder mehrere Anwendungen gesendet werden. Die Zielanwendungen für eine Nachricht werden durch eine Reihe verschiedener Faktoren bestimmt, z. B. die Bedeutung der Nachricht, die Berechtigung der Anwendung für das Objekt, ob die Anwendung die Anforderung initiiert hat, für die die Nachricht ein direktes Ergebnis ist, und die Nachrichtenmaskierung, die von der Anwendung festgelegt wurde. Beachten Sie die folgenden Punkte zu Nachrichten:

-   Asynchrone Antwortnachrichten werden nur an die Anwendung gesendet, von der die Anforderung stammt, und können nicht maskiert werden.
-   Nachrichten, die den Abschluss der Ziffern- oder Tongenerierung oder das Sammeln von Ziffern signalisieren, werden nur an die Anwendung gesendet, die die Ziffern- oder Tongenerierung angefordert hat.
-   Nachrichten, die auf Änderungen des Zeilen- oder Adresszustands hinweisen, werden an alle Anwendungen gesendet, die die Zeile geöffnet haben, solange die Nachricht über [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)aktiviert wurde.
-   Nachrichten, die Aufschluss über Änderungen des Aufrufzustands und der Aufrufinformationen geben, werden an alle Anwendungen gesendet, die über ein Handle für den Aufruf verfügen.
-   Nachrichten, die eine Ziffernerkennung, Tonerkennung oder Medientyperkennung signalisieren, werden an die Anwendungen gesendet, die die Überwachung dieses Ereignisses angefordert haben.

Dieser Abschnitt enthält die Referenzinformationen für die folgenden TAPI-Meldungen:

-   [Unterstützte Telefonienachrichten](assisted-telephony-messages.md)
-   [Callcenternachrichten](call-center-messages.md)
-   [Formatierte Fehlermeldungen](formatted-error-messages.md)
-   [Zeilengerätemeldungen](line-device-messages.md)
-   [Telefon Gerätenachrichten](phone-device-messages.md)

 

 



