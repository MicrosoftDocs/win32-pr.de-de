---
title: Kerberos V5-Protokoll
description: Kerberos V5-Protokoll
ms.assetid: a53a1edf-f374-4cbf-8050-7cde45284157
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68d78c4bdc457007c04ad66163e2ebfd7f5397f9
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "106340481"
---
# <a name="kerberos-v5-protocol"></a>Kerberos V5-Protokoll

Das Kerberos V5-Authentifizierungsprotokoll verfügt über einen Authentifizierungsdienst Bezeichner von RPC \_ C \_ authn \_ GSS \_ Kerberos. Das Kerberos-Protokoll definiert, wie Clients mit einem Netzwerk Authentifizierungsdienst interagieren und von der Internet Engineering Task Force (IETF) im September 1993 im Dokument [RFC 1510](https://www.ietf.org/rfc/rfc1510.txt)standardisiert wurden. Clients erhalten Tickets vom Kerberos Key Distribution Center (KDC), die sie beim Herstellen einer Verbindung an den Server übergeben. Kerberos-Tickets stellen die Netzwerkanmeldeinformationen des Clients dar.

Wie NTLM verwendet das Kerberos-Protokoll den Domänen Namen, Benutzernamen und das Kennwort zur Darstellung der Identität des Clients. Das anfängliche Kerberos-Ticket, das bei der Anmeldung des Benutzers vom KDC abgerufen wird, basiert auf einem verschlüsselten Hash des Benutzer Kennworts. Dieses anfängliche Ticket wird zwischengespeichert. Wenn der Benutzer versucht, eine Verbindung mit einem Server herzustellen, überprüft das Kerberos-Protokoll den Ticket Cache auf ein gültiges Ticket für diesen Server. Wenn eine solche nicht verfügbar ist, wird das Anfangs Ticket für den Benutzer zusammen mit einer Anforderung für ein Ticket für den angegebenen Server an den KDC gesendet. Das Sitzungs Ticket wird dem Cache hinzugefügt und kann verwendet werden, um eine Verbindung mit dem gleichen Server herzustellen, bis das Ticket abläuft.

Wenn ein Server [**coqueryclientblanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) mithilfe des Kerberos-Protokolls aufruft, werden der Domänen Name und der Benutzername des Clients zurückgegeben. Wenn ein Server " [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)" aufruft, wird das Token des Clients zurückgegeben. Diese Verhalten sind identisch mit der Verwendung von NTLM.

Das Kerberos-Protokoll funktioniert über Computer Grenzen hinweg. Die Client-und Server Computer müssen sich in Domänen befinden, und diese Domänen müssen eine Vertrauensstellung aufweisen.

Das Kerberos-Protokoll erfordert die gegenseitige Authentifizierung und unterstützt es Remote. Der Client muss den Prinzipal Namen des Servers angeben, und die Identität des Servers muss genau mit dem Prinzipal Namen übereinstimmen. Wenn der Client für den Prinzipal Namen des Servers **null** angibt oder wenn der Prinzipal Name nicht mit dem Server identisch ist, tritt ein Fehler auf.

Mithilfe des Kerberos-Protokolls können die Identitätswechsel Ebenen identifiziert, angenommen und Delegat verwendet werden. Wenn von einem Server " [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)" aufgerufen wird, ist das zurückgegebene Token für einen Zeitraum von 5 Minuten bis 8 Stunden außerhalb des Computers gültig. Nach dieser Zeit kann Sie nur auf dem Server Computer verwendet werden. Wenn ein Server "Ausführen als Aktivator" ist und die Aktivierung mit dem Kerberos-Protokoll erfolgt, läuft das Token des Servers zwischen 5 Minuten und 8 Stunden nach der Aktivierung ab.

Das Kerberos V5-Authentifizierungsprotokoll, das von Windows implementiert wird, unterstützt das [Cloaking](cloaking.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-und Sicherheitspakete](com-and-security-packages.md)
</dt> </dl>

 

 




