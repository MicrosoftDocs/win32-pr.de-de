---
description: Nachrichten werden verwendet, um die Anwendung über asynchrone Ereignisse zu benachrichtigen. Alle diese Nachrichten werden über den Nachrichten Benachrichtigungs Mechanismus, der von der Anwendung in lineinitializeex angegeben wurde, an die Anwendung gesendet.
ms.assetid: d302819e-c522-470a-be5e-52625c9223a4
title: TAPI-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58307a0230b76c6ad98c57f4590098f0dcf6b236
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368946"
---
# <a name="tapi-messages"></a>TAPI-Nachrichten

Nachrichten werden verwendet, um die Anwendung über asynchrone Ereignisse zu benachrichtigen. Alle diese Nachrichten werden über den Nachrichten Benachrichtigungs Mechanismus, der von der Anwendung in [**lineinitializeex**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)angegeben wurde, an die Anwendung gesendet.

Die Meldung enthält immer ein Handle für das relevante Objekt (Telefon, Zeile oder Anruf), das die Anwendung verwenden kann, um den Nachrichtentyp zu bestimmen.

Bestimmte Nachrichten werden verwendet, um die Anwendung über eine Änderung des Status eines Objekts zu benachrichtigen. Diese Nachrichten stellen das Objekt Handle bereit und geben Aufschluss darüber, welches Status Element geändert wurde. Die Anwendung kann die entsprechende "Get Status"-Funktion des-Objekts abrufen, um den vollständigen Status des Objekts abzurufen.

Wenn ein Ereignis auftritt, können Nachrichten an NULL, eine oder mehrere Anwendungen gesendet werden. Die Zielanwendungen für eine Nachricht werden durch eine Reihe unterschiedlicher Faktoren bestimmt. dazu gehören die Bedeutung der Nachricht, die Berechtigung der Anwendung für das Objekt, ob die Anwendung die Anforderung initiiert hat, für die die Nachricht ein direktes Ergebnis ist, und die Nachrichten Maskierung, die von der Anwendung festgelegt wurde. Beachten Sie die folgenden Punkte zu Nachrichten:

-   Asynchrone Antwort Nachrichten werden nur an die Anwendung gesendet, von der die Anforderung stammt, und können nicht maskiert werden.
-   Nachrichten, die den Abschluss der Ziffern-oder Tongenerierung oder die Erfassung von Ziffern signalisieren, werden nur an die Anwendung gesendet, die die Ziffern-oder Tongenerierung angefordert hat.
-   Nachrichten, die Zeilen-oder Adress Zustandsänderungen angeben, werden an alle Anwendungen gesendet, die die Zeile geöffnet haben, solange die Nachricht durch [**linesetstatusmessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)aktiviert wurde.
-   Nachrichten, die auf den Ansichts-und den Rückruf von Informationen hinweisen, werden an alle Anwendungen gesendet, die ein Handle für den-Befehl haben
-   Nachrichten, die eine Ziffern Erkennung, eine Ton Erkennung oder eine Medientyp Erkennung signalisieren, werden an die Anwendungen gesendet, die die Überwachung dieses Ereignisses angefordert haben.

Dieser Abschnitt enthält die Referenzinformationen für die folgenden TAPI-Meldungen:

-   [Unterstützte telefonienachrichten](assisted-telephony-messages.md)
-   [Callcentermeldungen](call-center-messages.md)
-   [Formatierte Fehlermeldungen](formatted-error-messages.md)
-   [Zeilen Geräte Meldungen](line-device-messages.md)
-   [Geräte Nachrichten per Telefon](phone-device-messages.md)

 

 



