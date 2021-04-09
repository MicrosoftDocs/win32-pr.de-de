---
title: MSMQ-Sicherheitsdienste
description: Synchrone RPC-Nachrichten können beliebige Sicherheitsfunktionen verwenden, die zur RPC-Laufzeit verfügbar sind. Weitere Informationen finden Sie unter Sicherheit.
ms.assetid: 0f4d45c4-7457-4449-8736-e141a95f6930
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd2e12cd9f32a571088de769adb079327caab9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101986"
---
# <a name="msmq-security-services"></a><span data-ttu-id="062df-104">MSMQ-Sicherheitsdienste</span><span class="sxs-lookup"><span data-stu-id="062df-104">MSMQ Security Services</span></span>

<span data-ttu-id="062df-105">Synchrone RPC-Nachrichten können beliebige Sicherheitsfunktionen verwenden, die zur RPC-Laufzeit verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="062df-105">Synchronous RPC messages can use any of the security features available from the RPC run time.</span></span> <span data-ttu-id="062df-106">Weitere Informationen finden Sie unter [Sicherheit](security.md) .</span><span class="sxs-lookup"><span data-stu-id="062df-106">See [Security](security.md) for more details.</span></span>

<span data-ttu-id="062df-107">Asynchrone \[ [Nachrichten](/windows/desktop/Midl/message) \] Aufrufe können keine RPC-Sicherheit verwenden, da kein Handshake zwischen Client und Server vorliegt.</span><span class="sxs-lookup"><span data-stu-id="062df-107">Asynchronous \[ [message](/windows/desktop/Midl/message)\] calls cannot use RPC security because there is no handshake between client and server.</span></span> <span data-ttu-id="062df-108">Tatsächlich wird der Server möglicherweise nicht einmal zum Zeitpunkt des Aufrufes ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="062df-108">In fact, the server may not even be running at the time of the call.</span></span> <span data-ttu-id="062df-109">Um auf die von Message Queuing Services (MSMQ) bereitgestellten Sicherheitsdienste zuzugreifen, sollte die Client Anwendung [**rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) aufrufen, um den Grad der Authentifizierung und den Datenschutz für Ihre Aufrufe an den Server zu steuern.</span><span class="sxs-lookup"><span data-stu-id="062df-109">To access the security services provided by Message Queuing Services (MSMQ), the client application should call [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) to control the level of authentication and privacy for its calls to the server.</span></span>

<span data-ttu-id="062df-110">Die Serveranwendung kann [**rpcbindinginqauthclient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) innerhalb eines Remote Prozedur Aufrufes aufzurufen, um die Sicherheitsstufe für diesen-Befehl zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="062df-110">The server application can call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) from within a remote procedure call to determine the security level for that call.</span></span> <span data-ttu-id="062df-111">Die Zuordnung zwischen den RPC-Sicherheits Konstanten und der MSMQ-Sicherheit ist in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="062df-111">The mapping between RPC security constants and MSMQ security is shown in the following table.</span></span>



| <span data-ttu-id="062df-112">RPC-Sicherheitsstufe</span><span class="sxs-lookup"><span data-stu-id="062df-112">RPC security level</span></span>                | <span data-ttu-id="062df-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="062df-113">Description</span></span>                                                                                |
|-----------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="062df-114">RPC \_ authn \_ Level \_ None</span><span class="sxs-lookup"><span data-stu-id="062df-114">RPC\_AUTHN\_LEVEL\_NONE</span></span>           | <span data-ttu-id="062df-115">Der-Befehl wird weder authentifiziert noch verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="062df-115">The call is not authenticated or encrypted.</span></span>                                                |
| <span data-ttu-id="062df-116">Pkt-Integrität der RPC- \_ authn- \_ Ebene \_ \_</span><span class="sxs-lookup"><span data-stu-id="062df-116">RPC\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> | <span data-ttu-id="062df-117">Der-Rückruf wird mithilfe der MSMQ-Sicherheit authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="062df-117">The call is authenticated using MSMQ security.</span></span>                                             |
| <span data-ttu-id="062df-118">Datenschutz auf RPC- \_ authn- \_ Ebene \_ Pkt \_</span><span class="sxs-lookup"><span data-stu-id="062df-118">RPC\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   | <span data-ttu-id="062df-119">Der-Rückruf wird bei der Übertragung zwischen der Client-und der Server Warteschlange authentifiziert und verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="062df-119">The call is authenticated and encrypted as it travels between the client and server queue.</span></span> |



 

<span data-ttu-id="062df-120">Der Server kann auch die Aufruf Authentifizierung und-Verschlüsselung erzwingen, indem er [**rpcserveruseprotseqepex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) aufruft \_ und \_ \_ \_ in der Struktur der RPC-Richtlinie den Wert für RPC-c MQ authn Level \_ None, RPC c MQ authn Level \_ \_ \_ \_ \_ Pkt \_ Integrity und RPC \_ c \_ MQ \_ authn \_ Level \_ Pkt- \_ [**\_**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) datenschutzkennzeichen festlegt.</span><span class="sxs-lookup"><span data-stu-id="062df-120">The server can also force call authentication and encryption by calling [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) and setting the RPC\_C\_MQ\_AUTHN\_LEVEL\_NONE, RPC\_C\_MQ\_AUTHN\_LEVEL\_PKT\_INTEGRITY and RPC\_C\_MQ\_AUTHN\_LEVEL\_PKT\_PRIVACY flags in the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure.</span></span>

 

 