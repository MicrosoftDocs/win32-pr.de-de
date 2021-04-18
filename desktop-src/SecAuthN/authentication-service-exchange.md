---
description: Der Benutzer beginnt, sich am Netzwerk anzumelden, indem er einen Anmelde Namen und ein Kennwort eingegeben hat. Der Kerberos-Client auf der Arbeitsstation des Benutzers konvertiert das Kennwort in einen Verschlüsselungsschlüssel und speichert das Ergebnis in einer Programmvariablen.
ms.assetid: fcb3b601-9953-474c-9a08-1fa25706f3d7
title: Authentifizierungsdienstaustausch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c14121ed33ae0ac169c590b03dfb0b395306d11f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368004"
---
# <a name="authentication-service-exchange"></a>Authentifizierungsdienstaustausch

Der Benutzer beginnt, sich am Netzwerk anzumelden, indem er einen Anmelde Namen und ein Kennwort eingegeben hat. Der [*Kerberos*](/windows/desktop/SecGloss/k-gly) -Client auf der Arbeitsstation des Benutzers konvertiert das Kennwort in einen Verschlüsselungsschlüssel und speichert das Ergebnis in einer Programmvariablen.

Der Client fordert dann [*Anmelde*](/windows/desktop/SecGloss/c-gly) Informationen für den TGS (Ticket-Gewährung Service, TGS) des [*Schlüsselverteilungscenter*](/windows/desktop/SecGloss/k-gly) (KDC) an, indem er den Authentifizierungsdienst des KDC \_ als \_ req-Nachricht (Kerberos-Authentifizierungsdienst Anforderung) sendet. Der erste Teil dieser Meldung identifiziert den Benutzer und den TGS-Dienst, der angefordert wird. Der zweite Teil dieser Nachricht enthält vorauthentifizierungs Daten, mit denen nachgewiesen werden soll, dass der Benutzer das Kennwort kennt. Dies ist einfach eine authentifikatornachricht, die mit dem [*Hauptschlüssel*](/windows/desktop/SecGloss/m-gly) verschlüsselt ist, der aus dem Anmelde Kennwort des Benutzers abgeleitet wurde.

Wenn der KDC krb \_ als \_ req empfängt, sucht er den Benutzer in seiner Datenbank, Ruft den Hauptschlüssel des zugeordneten Benutzers ab, entschlüsselt die vorauthentifizierungs Daten und wertet den Zeitstempel in aus. Wenn der Zeitstempel gültig ist, kann der KDC sicher sein, dass die vorauthentifizierungs Daten mit dem Hauptschlüssel des Benutzers verschlüsselt wurden und somit der Client echt ist.

Nachdem der KDC die Identität des Benutzers überprüft hat, erstellt er die Anmelde Informationen, die der Client dem TGS wie folgt zur Verfügung stellen kann:

1.  Der KDC erschließt einen Anmelde [*Sitzungsschlüssel*](/windows/desktop/SecGloss/s-gly) und verschlüsselt eine Kopie mit dem Hauptschlüssel des Benutzers.
2.  Der KDC bettet eine andere Kopie des Anmelde Sitzungsschlüssels und die Autorisierungs Daten des Benutzers in ein Ticket-Zustellungs Ticket (TGT) ein und verschlüsselt das TGT mit dem eigenen Hauptschlüssel des KDC.
3.  Der KDC sendet diese Anmelde Informationen zurück an den Client, indem er mit einer Nachricht vom Typ krb \_ als \_ Rep (Kerberos-Authentifizierungsdienst Antwort) antwortet.
4.  Wenn der Client die Antwort empfängt, verwendet er den Schlüssel, der aus dem Kennwort des Benutzers abgeleitet wurde, um den neuen Anmelde Sitzungsschlüssel zu entschlüsseln.
5.  Der neue Schlüssel wird vom Client in seinem Ticket Cache gespeichert.
6.  Der Client extrahiert das TGT aus der Nachricht und speichert dieses ebenfalls im Ticket Cache.

 

 
