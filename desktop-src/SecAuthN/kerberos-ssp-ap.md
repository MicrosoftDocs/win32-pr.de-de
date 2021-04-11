---
description: Das Kerberos-Authentifizierungs Paket wird bei der Anmeldung bei einem Netzwerk verwendet. lokale Anmeldungen werden von MSV1 0 verarbeitet \_ .
ms.assetid: 43970c99-53f1-43c1-9d9f-65573572f731
title: Kerberos SSP/AP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d14565c8c6526d9cab34d7b9ddec9a0a04ff8de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042383"
---
# <a name="kerberos-sspap"></a>Kerberos SSP/AP

Das [*Kerberos*](../secgloss/k-gly.md) -Authentifizierungs Paket wird bei der Anmeldung bei einem Netzwerk verwendet. lokale Anmeldungen werden von MSV1 0 verarbeitet \_ .

Wenn ein Benutzer sich mit einem Netzwerk Konto anmeldet, versucht Kerberos standardmäßig, eine Verbindung mit dem Kerberos- [*Schlüsselverteilungscenter*](../secgloss/k-gly.md) (KDC) auf dem Domänen Controller herzustellen und ein Ticket Erstellungs Ticket (TGT) zu erhalten, indem die vom Benutzer bereitgestellten Anmeldedaten verwendet werden.

Wenn ein Kerberos-KDC nicht verfügbar ist, verwendet Windows MSV1 \_ 0 und die Passthrough-Authentifizierung, wie unter [MSV1 \_ 0 Authentication Package](msv1-0-authentication-package.md)beschrieben.

Das Kerberos-Authentifizierungs Paket unterstützt Version 5, Revision 6 des Kerberos-Protokolls. Dieses Protokoll basiert auf Internet [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt). Weitere Informationen finden Sie auf der IETF-Website:

[https://www.ietf.org](https://www.ietf.org/)

Weitere Informationen zu Kerberos finden Sie unter [Microsoft Kerberos](microsoft-kerberos.md).

## <a name="kerberos-credential-formats"></a>Kerberos-Anmelde Informationsformate

Die Benutzer [*Anmelde*](../secgloss/c-gly.md) Informationen, die nach einem erfolgreichen Anmeldeversuch vom Kerberos-Authentifizierungs Paket zugewiesen werden, sind ein Ticket und ein temporärer Verschlüsselungsschlüssel, der häufig als [*Sitzungsschlüssel*](../secgloss/s-gly.md)bezeichnet wird. Das Ticket enthält sowohl eine verschlüsselte Kopie der Anmelde Informationen des Clients als auch den Sitzungsschlüssel.

 

 
