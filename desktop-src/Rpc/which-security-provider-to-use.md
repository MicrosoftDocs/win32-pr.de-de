---
title: Zu verwendende Sicherheitsanbieter
description: Alle anderen Dinge, die gleich sind, verwenden RPC \_ c \_ authn \_ GSS \_ Kerberos oder RPC \_ c \_ authn \_ GSS \_ Aushandlungen.
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33248d989031390b1b57730c637829922d15166a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710571"
---
# <a name="which-security-provider-to-use"></a><span data-ttu-id="fd7f5-103">Zu verwendende Sicherheitsanbieter</span><span class="sxs-lookup"><span data-stu-id="fd7f5-103">Which Security Provider to Use</span></span>

<span data-ttu-id="fd7f5-104">Alle anderen Dinge, die gleich sind, verwenden RPC \_ c \_ authn \_ GSS \_ Kerberos oder RPC \_ c \_ authn \_ GSS \_ Aushandlungen.</span><span class="sxs-lookup"><span data-stu-id="fd7f5-104">All other things being equal, use RPC\_C\_AUTHN\_GSS\_KERBEROS or RPC\_C\_AUTHN\_GSS\_NEGOTIATE.</span></span> <span data-ttu-id="fd7f5-105">Jeder stellt den skalierbaren und sichersten Dienst bereit.</span><span class="sxs-lookup"><span data-stu-id="fd7f5-105">Each provides the most scalable and secure service.</span></span> <span data-ttu-id="fd7f5-106">Wenn Sie die RPC \_ \_ -C-authn- \_ GSS- \_ Aushandlung auf dem Server verwenden, können Downlevelclients, z. b. NTLM-Clients, eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="fd7f5-106">If you use RPC\_C\_AUTHN\_GSS\_NEGOTIATE on the server, this allows down-level clients, such as NTLM clients, to connect to your server.</span></span> <span data-ttu-id="fd7f5-107">Wenn dies nicht erwünscht ist, beschränken Sie die Auswahl nur auf RPC \_ C \_ authn \_ GSS \_ Kerberos, oder wenden Sie [**rpcbindinginqauthclientex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) an, um zu bestimmen, welcher Sicherheitsanbieter vom Client verwendet wird, und verweigern Sie den Zugriff auf Clients mithilfe von NTLM.</span><span class="sxs-lookup"><span data-stu-id="fd7f5-107">If that is undesirable, either limit the choice to RPC\_C\_AUTHN\_GSS\_KERBEROS only, or call [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) to determine which security provider the client is using, and deny access to clients using NTLM.</span></span> <span data-ttu-id="fd7f5-108">Die bevorzugte Methode zum Einrichten des Sicherheits Anbieters, den der Client verwendet, ist die Funktion [**rpcserverinqcallattributs**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) .</span><span class="sxs-lookup"><span data-stu-id="fd7f5-108">The preferred method of establishing which security provider the client is using is the [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) function.</span></span>

 

 




