---
title: Snego
description: Snego, dessen Authentifizierungsdienstbezeichner RPC \_ C \_ AUTHN \_ GSS \_ NEGOTIATE lautet, stellt eigentlich keine Authentifizierungsdienste selbst bereit.
ms.assetid: 2087a84c-d302-4511-9f02-2d20ee9e0d8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a82f8da58cc77ebfd4debd0763ad4af6e1c96d3e88d9ede69ff82a28e3d8a5ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129812"
---
# <a name="snego"></a>Snego

Snego, dessen Authentifizierungsdienstbezeichner RPC \_ C \_ AUTHN \_ GSS \_ NEGOTIATE lautet, stellt eigentlich keine Authentifizierungsdienste selbst bereit. Stattdessen wird eine Liste der Authentifizierungsdienste verwendet und ein Dienst ausgehandelt, der zwischen Client und Server funktioniert. Die Authentifizierungsparameter werden nicht von Snego verwendet, sondern an den ausgewählten Authentifizierungsdienst übergeben, der die eigentliche Authentifizierung übernimmt. Snego wurde von der Internet Engineering Task Force (IETF) im Dezember 1998 im Dokument [RFC 2478](https://www.ietf.org/rfc/rfc2478.txt)standardisiert.

Snego ist nützlich, wenn Sie nicht wissen, welche Authentifizierungsdienste der Remotecomputer bereitstellen kann.

Um Snego verwenden zu können, müssen sowohl der Client als auch der Server Snego als Authentifizierungsdienst angeben. Der Server gibt RPC \_ C \_ AUTHN \_ GSS \_ NEGOTIATE als **dwAuthnSvc-Member** einer der [**SOLE AUTHENTICATION \_ \_ SERVICE-Strukturen**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) im *asAuthSvc-Arrayparameter* an, der an [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)übergeben wird. Der Client kann Snego angeben, indem [**er CoSetProxyBlanket aufruft**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) und RPC \_ C \_ AUTHN \_ GSS \_ NEGOTIATE als *dwAuthnSvc-Parameter* übergibt. Der Client sollte auch eine Liste möglicher Authentifizierungsdienste für Snego über den **PackageList-Member** der [**SEC \_ WINNT \_ AUTH \_ IDENTITY \_ EX-Struktur**](/windows/desktop/api/sspi/ns-sspi-_sec_winnt_auth_identity_exa) bereitstellen, die im Aufruf von **CoSetProxyBlanket** an den *pAuthInfo-Parameter* übergeben wird. Wenn *pAuthInfo* **NULL** ist, erstellt Snego eine Liste der Authentifizierungsdienste aus den auf dem Computer installierten Sicherheitspaketen. Anschließend sendet Snego die Liste der Authentifizierungsdienste an den Server, vergleicht die Liste mit den verfügbaren Authentifizierungsdiensten des Servers und wählt einen Authentifizierungsdienst aus, der für die Verbindung verwendet werden soll.

> [!Note]  
> Schannel kann nicht in der Liste der von Snego verwendeten Authentifizierungsdienste enthalten sein.

 

Clients können auch Snego angeben, wenn sie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)aufrufen. Die *Parameter dwAuthnSvc* und *pAuthInfo* von [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) werden Mitglieder einer [**SOLE AUTHENTICATION \_ \_ INFO-Struktur,**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) die über den *pAuthList-Parameter* an **CoInitializeSecurity** übergeben wird. Die Details der Werte dieser Elemente sind identisch mit den im vorherigen Absatz beschriebenen Werten.

Wenn Snego verwendet wird, geben Aufrufe von [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket) oder [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) Snego als Authentifizierungsdienst zurück, anstatt den tatsächlichen Authentifizierungsdienst, den Snego zum Herstellen der Verbindung ausgewählt hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM- und Sicherheitspakete](com-and-security-packages.md)
</dt> </dl>

 

 