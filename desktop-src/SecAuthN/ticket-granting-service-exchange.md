---
description: Nachdem ein Ticket Erteilungs Ticket (TGT) und ein Sitzungsschlüssel für den Client eingerichtet wurden, kann der Client einen separaten Sitzungsschlüssel und ein Ticket für den Dienst anfordern.
ms.assetid: b4f63642-9282-4e11-b40c-eec406b2dd2b
title: Ticket-Granting-Dienstaustausch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b227ee551d762abd145ca56c6cced110b6a2dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343803"
---
# <a name="ticket-granting-service-exchange"></a>Ticket-Granting-Dienstaustausch

Nachdem ein Ticket Erteilungs Ticket (TGT) und ein [*Sitzungsschlüssel*](../secgloss/s-gly.md) für den Client eingerichtet wurden, kann der Client einen separaten Sitzungsschlüssel und ein Ticket für den Dienst anfordern.

**So fordern Sie ein Ticket für einen anderen Dienst an**

1.  Der Kerberos-Client auf der Arbeitsstation des Benutzers fordert [*Anmelde*](../secgloss/c-gly.md) Informationen für den Dienst an, indem er an den [*Schlüsselverteilungscenter*](../secgloss/k-gly.md) (KDC) sendet, eine Nachricht vom Typ krb \_ TGS \_ req (Kerberos Ticket-Granting Service Request). Diese Nachricht besteht aus der Identität des Diensts, für den der Client Anmelde Informationen anfordert, einer Authentifikator-Nachricht, die mit dem neuen Anmelde [*Sitzungsschlüssel*](../secgloss/s-gly.md)des Benutzers verschlüsselt ist, und dem TGT, der vom [Authentifizierungsdienst Austausch](authentication-service-exchange.md)abgerufen wurde.
2.  Wenn der KDC ein krb- \_ TGS- \_ req empfängt, entschlüsselt der KDC den TGT mit seinem geheimen Schlüssel und extrahiert den Anmelde Sitzungsschlüssel des Benutzers.
3.  Der KDC verwendet den Anmelde [*Sitzungsschlüssel*](../secgloss/s-gly.md) zum Entschlüsseln der Authentifikator-Nachricht des Benutzers und wertet ihn aus. Wenn der Authentifikator den Test übergibt, extrahiert der KDC die Autorisierungs Daten des Benutzers aus dem TGT und gibt einen Sitzungsschlüssel aus, den der Benutzer für den angeforderten Server freigeben muss.
4.  Der KDC verschlüsselt eine Kopie des Dienst Sitzungsschlüssels mit dem Anmelde Sitzungsschlüssel des Benutzers.
5.  Der KDC bettet eine andere Kopie des Dienst Sitzungsschlüssels in ein Ticket zusammen mit den Autorisierungs Daten des Benutzers ein und verschlüsselt das Ticket mit dem [*Hauptschlüssel*](../secgloss/m-gly.md)des Servers.
6.  Der KDC sendet diese Anmelde Informationen zurück an den Client, indem er mit einer Nachricht vom Typ krb \_ TGS \_ Rep (Kerberos-Ticket-Granting Dienst Antwort) antwortet.
7.  Wenn der Client die Antwort empfängt, entschlüsselt er den Dienst Sitzungsschlüssel mit dem Anmelde Sitzungsschlüssel des Benutzers und speichert den Dienst Sitzungsschlüssel im Ticket Cache.
8.  Der Client extrahiert das Ticket auf den Server und speichert dieses im Ticket Cache.

 

 
