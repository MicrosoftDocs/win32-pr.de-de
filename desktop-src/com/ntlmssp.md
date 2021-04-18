---
title: NTLMSSP
description: NTLMSSP
ms.assetid: ae434165-4429-4ef0-b083-60abdfc50de0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706c788f103d3d616b5a3087522b5f06b417e972
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337265"
---
# <a name="ntlmssp"></a>NTLMSSP

NTLMSSP, dessen Authentifizierungsdienst Bezeichner RPC \_ C \_ authn \_ Winnt ist, ist eine Security Support Provider, die in allen Versionen von DCOM verfügbar ist. Er verwendet das NTLM-Protokoll für die Authentifizierung. NTLM überträgt das Kennwort des Benutzers bei der Authentifizierung nie an den Server. Daher kann der Server das Kennwort beim Identitätswechsel nicht verwenden, um auf Netzwerkressourcen zuzugreifen, auf die der Benutzer Zugriff hat. Nur auf lokale Ressourcen kann zugegriffen werden.

NTLM funktioniert sowohl lokal als auch Computer übergreifend. Das heißt, wenn sich der Client und der Server auf unterschiedlichen Computern befinden, kann NTLM weiterhin sicherstellen, dass der Client seine Ansprüche anfordert.

Bei NTLM wird die Identität des Clients durch einen Domänen Namen, einen Benutzernamen und ein Kennwort oder Token repräsentiert. Wenn ein Server [**coqueryclientblanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)aufruft, werden der Domänen Name und der Benutzername des Clients zurückgegeben. Wenn jedoch ein Server " [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)" aufruft, wird das Token des Clients zurückgegeben. Wenn keine Vertrauensstellung zwischen Client und Server besteht und der Server über ein lokales Konto mit dem gleichen Namen und Kennwort wie der Client verfügt, wird dieses Konto zur Darstellung des Clients verwendet.

NTLM unterstützt die gegenseitige Authentifizierung für Thread übergreifende und prozessübergreifende Authentifizierung (nur lokal). Wenn der Client den Prinzipal Namen des Servers im Formular Domänen \\ Benutzer in einem [**IClientSecurity:: setblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)-Befehl angibt, muss die Identität des Servers mit dem Prinzipal Namen übereinstimmen, andernfalls tritt ein Fehler auf. Wenn der Client **null** angibt, wird die Identität des Servers nicht geprüft.

NTLM unterstützt zusätzlich die delegatidentitäts Wechsel-Ebene Thread übergreifend und Prozess übergreifend (nur lokal).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-und Sicherheitspakete](com-and-security-packages.md)
</dt> </dl>

 

 