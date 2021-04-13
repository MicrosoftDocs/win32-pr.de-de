---
title: Spogo
description: Bei spogo, dessen Authentifizierungsdienst Bezeichner RPC \_ C \_ authn \_ GSS \_ aushandelt ist, werden tatsächlich keine Authentifizierungsdienste bereitgestellt.
ms.assetid: 2087a84c-d302-4511-9f02-2d20ee9e0d8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676b6428d6b7e79893214c2d234dcfc43992e190
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391052"
---
# <a name="snego"></a>Spogo

Bei spogo, dessen Authentifizierungsdienst Bezeichner RPC \_ C \_ authn \_ GSS \_ aushandelt ist, werden tatsächlich keine Authentifizierungsdienste bereitgestellt. Stattdessen wird eine Liste der Authentifizierungsdienste verwendet, und es wird ein Dienst ausgehandelt, der zwischen Client und Server funktioniert. Die Authentifizierungs Parameter werden von spogo nicht verwendet, sondern an den ausgewählten Authentifizierungsdienst weitergeleitet, der die tatsächliche Authentifizierung durchführt. "Snego" wurde von der Internet Engineering Task Force (IETF) im Dezember 1998 im Dokument [RFC 2478](https://www.ietf.org/rfc/rfc2478.txt)standardisiert.

"Snego" ist nützlich, wenn Sie nicht wissen, welche Authentifizierungsdienste der Remote Computer bereitstellen kann.

Zum Verwenden von "spogo" müssen sowohl der Client als auch der Server "snego" als Authentifizierungsdienst angeben. Der Server gibt RPC- \_ C- \_ authn- \_ GSS- \_ Aushandlung als **dwauthnsvc** -Member einer der [**einzigen \_ Authentifizierungs \_ Dienst**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) Strukturen im *asAuthSvc* -Array Parameter an, die an [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)übergeben werden. Der Client kann spogo angeben, indem er [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) aufruft und RPC \_ C \_ authn \_ GSS \_ Aushandlungen als *dwauthnsvc* -Parameter übergibt. Der Client sollte außerdem eine Liste der möglichen Authentifizierungsdienste für "snego" über das **PackageList** -Element der SEC-Struktur "s [**\_ Winnt \_ auth \_ Identity \_ Ex**](/windows/desktop/api/sspi/ns-sspi-_sec_winnt_auth_identity_exa) " bereitstellen, das im Aufrufen von **CoSetProxyBlanket** an den *pAuthInfo* -Parameter übergeben wird. Wenn *pAuthInfo* **null** ist, wird von snego eine Liste der Authentifizierungsdienste von den auf dem Computer installierten Sicherheitspaketen verfasst. Anschließend sendet snego die Liste der Authentifizierungsdienste an den Server, vergleicht die Liste mit den verfügbaren Authentifizierungsdiensten des Servers und wählt einen Authentifizierungsdienst aus, der für die Verbindung verwendet werden soll.

> [!Note]  
> SChannel kann nicht in der Liste der Authentifizierungsdienste enthalten sein, die von snego verwendet werden.

 

Clients können beim Aufrufen von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)auch spogo angeben. Die Parameter *dwauthnsvc* und *pAuthInfo* von [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) werden Member einer [**einzigen \_ Authentifizierungs \_ Informations**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) Struktur, die über den *pauthlist* -Parameter an **CoInitializeSecurity** übergeben wird. Die Details der Werte dieser Member entsprechen den Werten, die im vorherigen Abschnitt beschrieben wurden.

Wenn "snego" verwendet wird, wird "spogo" von Aufrufen an [**coqueryproxyblanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket) oder [**coqueryclientblanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) als Authentifizierungsdienst und nicht als der tatsächliche Authentifizierungsdienst zurückgegeben, den Sie zum Herstellen der Verbindung ausgewählt haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-und Sicherheitspakete](com-and-security-packages.md)
</dt> </dl>

 

 