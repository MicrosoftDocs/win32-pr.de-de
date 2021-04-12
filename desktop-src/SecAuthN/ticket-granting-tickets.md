---
description: Da das Kerberos-Protokoll ursprünglich entworfen wurde, wurde ein Hauptschlüssel für einen Benutzer von einem vom Benutzer bereitgestellten Kennwort abgeleitet.
ms.assetid: b8fcb68d-751e-4495-ab92-8b70c96aaa7a
title: Ticket-Granting Tickets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39dff161ba2d905f676fe6b6b5e7e7d5289ee550
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129313"
---
# <a name="ticket-granting-tickets"></a>Ticket-Granting Tickets

Da das [*Kerberos-Protokoll*](../secgloss/k-gly.md) ursprünglich entworfen wurde, wurde ein Hauptschlüssel für einen Benutzer von einem vom Benutzer bereitgestellten Kennwort abgeleitet. Wenn ein Benutzer sich angemeldet hat, hat der Kerberos-Client auf der Arbeitsstation des Benutzers das Kennwort vom Benutzer akzeptiert und in einen Verschlüsselungsschlüssel konvertiert, indem der Text über eine unidirektionale [*Hash*](../secgloss/h-gly.md) Funktion übergeben wurde. Der resultierende Hash war der [*Hauptschlüssel*](../secgloss/m-gly.md)des Benutzers. Der Client hat diesen *Hauptschlüssel* zum Entschlüsseln von [*Sitzungs Schlüsseln*](../secgloss/s-gly.md) verwendet, die von KDC empfangen wurden.

Das Problem mit dem ursprünglichen Kerberos-Entwurf besteht darin, dass der Client den Hauptschlüssel des Benutzers jedes Mal benötigt, wenn er einen Sitzungsschlüssel aus dem KDC entschlüsselt. Dies bedeutet, dass der Client den Benutzer zum Anfang jedes Client/Server-Austauschs auffordern muss, oder der Client muss den Benutzerschlüssel auf der Arbeitsstation speichern. Häufige Unterbrechungen des Benutzers sind zu stark aufdringlich. Wenn Sie den Schlüssel auf der Arbeitsstation speichern, riskieren Sie die Gefährdung eines Schlüssels, der vom Benutzer Kennwort abgeleitet ist.

Die Lösung des Kerberos-Protokolls für dieses Problem besteht darin, dass der Client einen temporären Schlüssel vom KDC erhält. Dieser temporäre Schlüssel eignet sich nur für diese [*Anmelde Sitzung*](../secgloss/l-gly.md). Wenn sich ein Benutzer anmeldet, fordert der Client ein Ticket für den KDC an, so wie er ein Ticket für jeden anderen Dienst anfordern würde. Der KDC antwortet, indem er einen Anmelde Sitzungsschlüssel und ein Ticket für einen speziellen Server erstellt, den vollständigen Ticket Erteilungs Dienst des KDC. Eine Kopie des Anmelde Sitzungsschlüssels ist in das Ticket eingebettet, und das Ticket wird mit dem Hauptschlüssel des KDC verschlüsselt. Eine andere Kopie des Anmelde Sitzungsschlüssels wird mit dem Hauptschlüssel des Benutzers verschlüsselt, der aus dem Anmelde Kennwort des Benutzers abgeleitet wurde. Sowohl das Ticket als auch der verschlüsselte Sitzungsschlüssel werden an den Client gesendet.

Wenn der Client die KDC-Antwort erhält, entschlüsselt er den Anmelde Sitzungsschlüssel mit dem Hauptschlüssel des Benutzers, der aus dem Kennwort des Benutzers abgeleitet wurde. Der Client benötigt nicht mehr den Schlüssel, der aus dem Kennwort des Benutzers abgeleitet wurde, da der Client nun den Anmelde Sitzungsschlüssel verwendet, um seine Kopie eines beliebigen Server Sitzungsschlüssels zu entschlüsseln, der vom KDC abgerufen wird. Der Client speichert den Anmelde Sitzungsschlüssel in seinem Ticket Cache zusammen mit dem Ticket für den vollständigen Ticket Erteilungs Dienst des KDC.

Das Ticket für den vollständigen Ticket Erteilungs Dienst wird als Ticket Erteilungs Ticket (TGT) bezeichnet. Wenn der Client die KDC nach einem Ticket an einen Server anfordert, werden die [*Anmelde*](../secgloss/c-gly.md) Informationen in Form einer Authentifikator-Nachricht und eines Tickets angezeigt – in diesem Fall ein TGT –, so wie es Anmelde Informationen für jeden anderen Dienst darstellen würde. Der Ticket Erteilungs Dienst öffnet den TGT mit dem Hauptschlüssel, extrahiert den Anmelde Sitzungsschlüssel für diesen Client und verwendet den Anmelde Sitzungsschlüssel, um die Client Kopie eines Sitzungsschlüssels für den Server zu verschlüsseln.

 

 
