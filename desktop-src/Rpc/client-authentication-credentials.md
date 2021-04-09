---
title: Anmelde Informationen zur Client Authentifizierung
description: Jeder authentifizierte Client muss Anmelde Informationen für die Authentifizierung für den Server bereitstellen.
ms.assetid: d567e944-8d68-4d95-be6a-840e30f57ba9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3704663411fc33340a462d8e3b356041b6061468
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037539"
---
# <a name="client-authentication-credentials"></a>Anmelde Informationen zur Client Authentifizierung

Jeder authentifizierte Client muss Anmelde Informationen für die Authentifizierung für den Server bereitstellen. Unter RPC speichert der Client seine Anmelde Informationen für die Authentifizierung in der Bindung zwischen dem Client und dem Server. Hierzu ruft der Client [**rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) oder [**rpcbindingsetauthinfoex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)auf.

Es gibt zwei Arten von Anmelde Informationen – implizit und explizit:

-   Wenn der Client Benutzername, Kennwort und Domäne angibt, sind explizite Anmelde Informationen vorhanden.
-   Implizite Anmelde Informationen sind vorhanden, wenn der Client Anmelde Informationen aus dem Thread oder Prozess Token verwendet, die die Funktionen **rpcbindingsetauthinfo** oder **rpcbindingsetauthinfoex** aufrufen.

Clients sollten keine expliziten Anmelde Informationen bereitstellen, da das Speichern, bearbeiten und Abrufen eines Benutzer Kennworts eine Sicherheitslücke in einem verteilten System darstellen kann, wenn explizite Anmelde Informationen verwendet werden.

Um implizite Anmelde Informationen zu verwenden, ruft der Client **rpcbindingsetauthinfo**(*Ex*) auf. Das Sicherheitssystem und RPC erhalten Anmelde Informationen aus dem Thread-oder Prozess Token für die Verwendung in der Authentifizierungs Sitzung.

Wenn der Client explizite Anmelde Informationen verwendet, ist der fünfte Parameter dieser beiden Funktionen vom Typ [**RPC \_ auth \_ Identity \_ handle**](rpc-auth-identity-handle.md). Dabei handelt es sich um einen flexiblen Typ, der ein Zeiger auf eine Datenstruktur ist. Der Inhalt der Datenstruktur kann sich je nach Authentifizierungsdienst unterscheiden. Derzeit erfordern die von RPC unterstützten SSPs, dass Ihre Anwendung das RPC-Authentifizierungs **\_ \_ Identitäts \_ handle** so festlegen muss, dass es auf eine [**Sek. \_ Winnt \_ auth- \_ Identitäts**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) Struktur verweist. Die **Identitäts Struktur "sec \_ Winnt \_ auth \_** " enthält Felder für einen Benutzernamen, eine Domäne und ein Kennwort.

 

 




