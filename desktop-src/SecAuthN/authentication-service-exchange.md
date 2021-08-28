---
description: Der Benutzer beginnt mit der Anmeldung beim Netzwerk, indem er einen Anmeldenamen und ein Kennwort einzugeben. Der Kerberos-Client auf der Arbeitsstation des Benutzers konvertiert das Kennwort in einen Verschlüsselungsschlüssel und speichert das Ergebnis in einer Programmvariablen.
ms.assetid: fcb3b601-9953-474c-9a08-1fa25706f3d7
title: Authentifizierungsdienstaustausch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8480370dd9fe5d7c5fc10e7979de9d4e7f67f99db3e517e1ec6520a3274ef23c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073290"
---
# <a name="authentication-service-exchange"></a>Authentifizierungsdienstaustausch

Der Benutzer beginnt mit der Anmeldung beim Netzwerk, indem er einen Anmeldenamen und ein Kennwort einzugeben. Der [*Kerberos-Client*](/windows/desktop/SecGloss/k-gly) auf der Arbeitsstation des Benutzers konvertiert das Kennwort in einen Verschlüsselungsschlüssel und speichert das Ergebnis in einer Programmvariablen.

Der Client fordert [](/windows/desktop/SecGloss/c-gly) dann Anmeldeinformationen für den Ticket granting Service (TGS) des [*Schlüsselverteilungscenter*](/windows/desktop/SecGloss/k-gly) (KDC) an, indem er dem Authentifizierungsdienst des KDC eine Nachricht vom Typ KRB \_ AS \_ REQ (Kerberos Authentication Service Request) sendet. Im ersten Teil dieser Meldung werden der Benutzer und der angeforderte TGS-Dienst identifiziert. Der zweite Teil dieser Nachricht enthält Daten zur Vorauthentifizierung, die belegen sollen, dass der Benutzer das Kennwort kennt. Dies ist einfach eine Authentatormeldung, die mit dem [*Hauptschlüssel*](/windows/desktop/SecGloss/m-gly) verschlüsselt ist, der vom Anmeldekennwort des Benutzers abgeleitet wird.

Wenn der KDC KRB AS REQ empfängt, sucht er den Benutzer in seiner Datenbank, ruft den Hauptschlüssel des zugeordneten Benutzers ab, entschlüsselt die Vorauthentifizierungsdaten und wertet den Zeitstempel \_ \_ innerhalb aus. Wenn der Zeitstempel gültig ist, kann das KDC sicher sein, dass die Vorauthentifizierungsdaten mit dem Hauptschlüssel des Benutzers verschlüsselt wurden und der Client daher original ist.

Nachdem das KDC die Identität des Benutzers überprüft hat, erstellt es Anmeldeinformationen, die der Client dem TGS wie folgt präsentieren kann:

1.  Das KDC erfindet einen [*Anmeldesitzungsschlüssel*](/windows/desktop/SecGloss/s-gly) und verschlüsselt eine Kopie mit dem Hauptschlüssel des Benutzers.
2.  Das KDC bettet eine weitere Kopie des Anmeldesitzungsschlüssels und der Autorisierungsdaten des Benutzers in ein Ticket-Granting Ticket (TGT) ein und verschlüsselt das TGT mit dem eigenen Hauptschlüssel des KDC.
3.  Das KDC sendet diese Anmeldeinformationen zurück an den Client, indem es mit einer Nachricht vom Typ KRB \_ AS \_ REP (Kerberos Authentication Service Reply) antwortet.
4.  Wenn der Client die Antwort empfängt, verwendet er den vom Kennwort des Benutzers abgeleiteten Schlüssel, um den neuen Anmeldesitzungsschlüssel zu entschlüsseln.
5.  Der Client speichert den neuen Schlüssel im Ticketcache.
6.  Der Client extrahiert das TGT aus der Nachricht und speichert es auch im Ticketcache.

 

 
