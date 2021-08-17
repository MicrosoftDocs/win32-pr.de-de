---
description: Nachdem ein Ticket-Granting Ticket (TGT) und ein Sitzungsschlüssel für den Client eingerichtet wurden, kann der Client einen separaten Sitzungsschlüssel und ein Ticket für den Dienst anfordern.
ms.assetid: b4f63642-9282-4e11-b40c-eec406b2dd2b
title: Ticket-Granting-Dienstaustausch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a691235b3e7f0faed68f38f0663c7792e381666f441399397f7e653bbb550080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786568"
---
# <a name="ticket-granting-service-exchange"></a>Ticket-Granting-Dienstaustausch

Nachdem ein Ticket-Granting Ticket (TGT) und ein Sitzungsschlüssel für den Client eingerichtet wurden, kann der Client einen separaten Sitzungsschlüssel und ein Ticket für den Dienst anfordern. [](../secgloss/s-gly.md)

**So fordern Sie ein Ticket für einen anderen Dienst an**

1.  Der Kerberos-Client auf der Arbeitsstation des Benutzers fordert Anmeldeinformationen für den Dienst an, indem er eine Nachricht vom Typ KRB [](../secgloss/c-gly.md) TGS [](../secgloss/k-gly.md) \_ \_ REQ (Kerberos Ticket-Granting Service Request) an den Schlüsselverteilungscenter (KDC) sendet. Diese Nachricht besteht aus der Identität des Diensts, für den der Client Anmeldeinformationen an fordert, einer Authentisierungsmeldung, die mit dem neuen Anmeldesitzungsschlüssel des Benutzers verschlüsselt [*ist,*](../secgloss/s-gly.md)und dem TGT, das vom Authentifizierungsdienst für [Exchange.](authentication-service-exchange.md)
2.  Wenn das KDC einen KRB TGS REQ empfängt, entschlüsselt das KDC das TGT mit seinem geheimen Schlüssel und extrahiert den \_ \_ Anmeldesitzungsschlüssel des Benutzers.
3.  Das KDC verwendet [](../secgloss/s-gly.md) den Anmeldesitzungsschlüssel, um die Authentatormeldung des Benutzers zu entschlüsseln und auswerten. Wenn der Authentator den Test besteht, extrahiert das KDC die Autorisierungsdaten des Benutzers aus dem TGT und erfindet einen Sitzungsschlüssel, den der Benutzer für den angeforderten Server freigeben kann.
4.  Das KDC verschlüsselt eine Kopie des Dienstsitzungsschlüssels mit dem Anmeldesitzungsschlüssel des Benutzers.
5.  Das KDC bettet eine weitere Kopie des Dienstsitzungsschlüssels zusammen mit den Autorisierungsdaten des Benutzers in ein Ticket ein und verschlüsselt das Ticket mit dem [*Hauptschlüssel des Servers.*](../secgloss/m-gly.md)
6.  Das KDC sendet diese Anmeldeinformationen zurück an den Client, indem es mit einer Nachricht vom Typ KRB \_ TGS \_ REP (Kerberos Ticket-Granting Service Reply) antwortet.
7.  Wenn der Client die Antwort empfängt, entschlüsselt er den Dienstsitzungsschlüssel mit dem Anmeldesitzungsschlüssel des Benutzers und speichert den Dienstsitzungsschlüssel im Ticketcache.
8.  Der Client extrahiert das Ticket auf den Server und speichert es im Ticketcache.

 

 
