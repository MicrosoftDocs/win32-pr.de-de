---
title: Anmeldeinformationen für die Clientauthentifizierung
description: Jeder authentifizierte Client muss Authentifizierungsanmeldeinformationen für den Server bereitstellen.
ms.assetid: d567e944-8d68-4d95-be6a-840e30f57ba9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2410b073886ffd70409cd749ea90305faa8d4635754e8f9596547c47bb976800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932186"
---
# <a name="client-authentication-credentials"></a>Anmeldeinformationen für die Clientauthentifizierung

Jeder authentifizierte Client muss Authentifizierungsanmeldeinformationen für den Server bereitstellen. Unter RPC speichert der Client seine Authentifizierungsanmeldeinformationen in der Bindung zwischen dem Client und dem Server. Hierzu ruft der Client [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) oder [**RpcBindingSetAuthInfoEx auf.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)

Es gibt zwei Arten von Anmeldeinformationen: implizit und explizit:

-   Explizite Anmeldeinformationen sind vorhanden, wenn der Client Benutzername, Kennwort und Domäne anfing.
-   Implizite Anmeldeinformationen sind vorhanden, wenn der Client Anmeldeinformationen aus dem Thread oder Prozesstoken verwendet, die die **RpcBindingSetAuthInfo-** oder **RpcBindingSetAuthInfoEx-Funktionen** aufrufen.

Clients sollten von der Bereitstellung expliziter Anmeldeinformationen absehen, da das Speichern, Bearbeiten und Abrufen eines Benutzerkennworts zu einem Sicherheitsrisiko in einem verteilten System führen kann, wenn explizite Anmeldeinformationen verwendet werden.

Um implizite Anmeldeinformationen zu verwenden, ruft der Client **RpcBindingSetAuthInfo**(*z. B.*) auf. Das Sicherheitssystem und rpc beziehen Anmeldeinformationen aus dem Thread oder Prozesstoken für die Verwendung in der Authentifizierungssitzung.

Wenn der Client explizite Anmeldeinformationen verwendet, ist der fünfte Parameter dieser beiden Funktionen vom Typ [**RPC \_ AUTH \_ IDENTITY \_ HANDLE**](rpc-auth-identity-handle.md). Dies ist ein flexibler Typ, der ein Zeiger auf eine Datenstruktur ist. Der Inhalt der Datenstruktur kann sich je nach Authentifizierungsdienst unterscheiden. Derzeit erfordern die SSPs, die RPC unterstützt, dass Ihre Anwendung **RPC \_ AUTH \_ IDENTITY \_ HANDLE** so festgelegt, dass sie auf eine [**SEC \_ WINNT \_ AUTH \_ IDENTITY-Struktur**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) verweisen kann. Die **SEC \_ WINNT \_ AUTH \_ IDENTITY-Struktur** enthält Felder für einen Benutzernamen, eine Domäne und ein Kennwort.

 

 




