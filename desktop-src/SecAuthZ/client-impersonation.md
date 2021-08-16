---
description: Identitätswechsel ist die Fähigkeit eines Threads, mit anderen Sicherheitsinformationen als dem Prozess, der den Thread besitzt, auszuführen.
ms.assetid: a3f74372-bdc9-43eb-b72f-7d00a43e78a8
title: Clientpersonation (Autorisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 454e943b53cffbc4430c71b31e2b172095b999e2201c4cafc08b081bf1782e64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783066"
---
# <a name="client-impersonation-authorization"></a>Clientpersonation (Autorisierung)

[*Identitätswechsel ist*](/windows/desktop/SecGloss/i-gly) die Fähigkeit eines Threads, mit anderen Sicherheitsinformationen als dem Prozess, der den Thread besitzt, auszuführen. In der Regel wird die Identität eines Clients von einem Thread in einer Serveranwendung angenommen. Dadurch kann der Serverthread im Namen dieses Clients auf Objekte auf dem Server zugreifen oder den Zugriff auf die eigenen Objekte des Clients überprüfen.

Die Microsoft Windows-API stellt die folgenden Funktionen bereit, um einen Identitätswechsel zu starten:

-   Eine DDE-Serveranwendung kann die [**DdeImpersonateClient-Funktion**](/windows/win32/api/ddeml/nf-ddeml-ddeimpersonateclient) aufrufen, um die Identität eines Clients zu übernehmen.
-   Ein Named Pipe-Server kann die [**ImpersonateNamedPipeClient-Funktion**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) aufrufen.
-   Sie können die [**Funktion ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) aufrufen, um die Identität des Sicherheitskontexts des Zugriffstokens eines angemeldeten [*Benutzers zu angenommen.*](/windows/desktop/SecGloss/a-gly)
-   Mit [**der ImpersonateSelf-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself) kann ein Thread eine Kopie seines eigenen Zugriffstokens generieren. Dies ist nützlich, wenn eine Anwendung den Sicherheitskontext eines einzelnen Threads ändern muss. Beispielsweise muss manchmal nur ein Thread eines Prozesses eine Berechtigung [*aktivieren.*](/windows/desktop/SecGloss/p-gly)
-   Sie können die [**Funktion SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken) aufrufen, damit der Zielthread im Sicherheitskontext eines angegebenen [*Identitätswechseltokens ausgeführt wird.*](/windows/desktop/SecGloss/i-gly)
-   Eine RPC-Serveranwendung (Microsoft Remote Procedure Call) kann die [**RpcImpersonateClient-Funktion**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) aufrufen, um die Identität eines Clients zu übernehmen.
-   Ein [*Sicherheitspaket oder*](/windows/desktop/SecGloss/s-gly) Anwendungsserver kann die [**ImpersonateSecurityContext-Funktion**](/windows/desktop/api/sspi/nf-sspi-impersonatesecuritycontext) aufrufen, um die Identität eines Clients zu ändern.

Bei den meisten dieser Identitätswechsel kann der Identitätswechselthread auf seinen eigenen Sicherheitskontext zurückwechseln, indem er die [**RevertToSelf-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) aufruft. Die Ausnahme ist der RPC-Identitätswechsel, bei dem die RPC-Serveranwendung [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) oder [**RpcRevertToSelfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoselfex) aufruft, um auf ihren eigenen Sicherheitskontext zurückzuwechseln.

 

 
