---
title: Kerberos v5-Protokoll
description: Kerberos v5-Protokoll
ms.assetid: a53a1edf-f374-4cbf-8050-7cde45284157
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50a1b739aac67a7a30918e78fa3bb364506ade7dfd720c390db1cc37909f2fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992460"
---
# <a name="kerberos-v5-protocol"></a>Kerberos v5-Protokoll

Das Kerberos v5-Authentifizierungsprotokoll verfügt über den Authentifizierungsdienstbezeichner RPC \_ C \_ AUTHN \_ GSS \_ KERBEROS. Das Kerberos-Protokoll definiert, wie Clients mit einem Netzwerkauthentifizierungsdienst interagieren und wurde im September 1993 von der Internet Engineering Task Force (IETF) im Dokument [RFC 1510 standardisiert.](https://www.ietf.org/rfc/rfc1510.txt) Clients erhalten Tickets vom Kerberos Key Distribution Center (KDC), die sie beim Herstellen einer Verbindung an den Server übergeben. Kerberos-Tickets stellen die Netzwerkanmeldeinformationen des Clients dar.

Wie NTLM verwendet das Kerberos-Protokoll den Domänennamen, Benutzernamen und das Kennwort, um die Identität des Clients zu repräsentieren. Das anfängliche Kerberos-Ticket, das beim Anmelden des Benutzers vom KDC erhalten wurde, basiert auf einem verschlüsselten Hash des Benutzerkennworts. Dieses anfängliche Ticket wird zwischengespeichert. Wenn der Benutzer versucht, eine Verbindung mit einem Server herzustellen, überprüft das Kerberos-Protokoll den Ticketcache auf ein gültiges Ticket für diesen Server. Wenn kein Ticket verfügbar ist, wird das anfängliche Ticket für den Benutzer zusammen mit einer Anforderung für ein Ticket für den angegebenen Server an das KDC gesendet. Dieses Sitzungsticket wird dem Cache hinzugefügt und kann verwendet werden, um eine Verbindung mit demselben Server herzustellen, bis das Ticket abläuft.

Wenn ein Server [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) mithilfe des Kerberos-Protokolls aufruft, werden der Domänenname und der Benutzername des Clients zurückgegeben. Wenn ein Server [**CoImpersonateClient aufruft,**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)wird das Token des Clients zurückgegeben. Diese Verhaltensweisen sind identisch mit denen bei verwendung von NTLM.

Das Kerberos-Protokoll funktioniert computerübergreifend. Die Client- und Servercomputer müssen sich beide in Domänen befinden, und diese Domänen müssen eine Vertrauensstellung haben.

Das Kerberos-Protokoll erfordert gegenseitige Authentifizierung und unterstützt es remote. Der Client muss den Prinzipalnamen des Servers angeben, und die Identität des Servers muss genau mit diesem Prinzipalnamen übereinstimmen. Wenn der Client NULL **für** den Prinzipalnamen des Servers angibt oder wenn der Prinzipalname nicht mit dem Server übereinstimmen soll, kann der Aufruf nicht ausgeführt werden.

Mit dem Kerberos-Protokoll können die Identitätswechselebenen identify, impersonate und delegate verwendet werden. Wenn ein Server [**CoImpersonateClient aufruft,**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)ist das zurückgegebene Token für einen Zeitraum zwischen 5 Minuten und 8 Stunden vom Computer gültig. Nach diesem Zeitpunkt kann es nur auf dem Servercomputer verwendet werden. Wenn ein Server als Aktivator ausgeführt wird und die Aktivierung mit dem Kerberos-Protokoll erfolgt, läuft das Token des Servers zwischen 5 Minuten und 8 Stunden nach der Aktivierung ab.

Das kerberos v5-Authentifizierungsprotokoll, das von Windows implementiert wird, unterstützt [das Versischen von](cloaking.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM- und Sicherheitspakete](com-and-security-packages.md)
</dt> </dl>

 

 




