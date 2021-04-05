---
title: Verwenden von Transport-Level Sicherheit auf dem Client
description: Der Client gibt an, wie der Server die Identität des Clients annimmt, wenn der Client die Zeichen folgen Bindung herstellt.
ms.assetid: 0d02b7f2-4dcb-41e8-829c-6942dfdcd4c6
keywords:
- Remote Prozedur Aufruf RPC, Tasks, mit Sicherheit auf Transport Ebene auf dem Client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10360d5b8d11640803e31ee1d1d0490a6edfdf7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949037"
---
# <a name="using-transport-level-security-on-the-client"></a><span data-ttu-id="0b3f8-104">Verwenden von Transport-Level Sicherheit auf dem Client</span><span class="sxs-lookup"><span data-stu-id="0b3f8-104">Using Transport-Level Security on the Client</span></span>

<span data-ttu-id="0b3f8-105">Der Client gibt an, wie der Server die Identität des Clients annimmt, wenn der Client die Zeichen folgen Bindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-105">The client specifies how the server impersonates the client when the client establishes the string binding.</span></span> <span data-ttu-id="0b3f8-106">Diese QoS-Informationen werden als Endpunkt Option in der Zeichen folgen Bindung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-106">This QOS information is provided as an endpoint option in the string binding.</span></span> <span data-ttu-id="0b3f8-107">Der Client kann die Ebene des Identitäts Wechsels, die dynamische oder statische Nachverfolgung und das Flag für die effektive Festlegung angeben.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-107">The client can specify the level of impersonation, dynamic or static tracking, and the effective-only flag.</span></span>

<span data-ttu-id="0b3f8-108">**So stellen Sie Quality of Service-Informationen für den Server bereit**</span><span class="sxs-lookup"><span data-stu-id="0b3f8-108">**To supply quality-of-service information for the server**</span></span>

1.  <span data-ttu-id="0b3f8-109">Der Client ruft [**rpcstringbindingcompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) auf, um die Komponenten Zeichenfolgen (einschließlich Endpunkt Optionen) im richtigen Zeichen folgen Bindungs Kontext zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-109">The client calls [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) to create the component strings, including endpoint options, in the correct string-binding context.</span></span>
2.  <span data-ttu-id="0b3f8-110">Der Client ruft [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) auf, um ein neues Bindungs Handle zu erhalten und die Quality of Service-Informationen für den Client anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-110">The client calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to obtain a new binding handle and to apply the quality-of-service information for the client.</span></span>
3.  <span data-ttu-id="0b3f8-111">Der Client führt Remote Prozedur Aufrufe mit dem Handle aus.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-111">The client makes remote procedure calls using the handle.</span></span>

<span data-ttu-id="0b3f8-112">Microsoft RPC unterstützt Windows-Sicherheitsfeatures nur auf [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) und [**Ncalrpc**](/windows/desktop/Midl/ncalrpc).</span><span class="sxs-lookup"><span data-stu-id="0b3f8-112">Microsoft RPC supports Windows security features only on [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) and [**ncalrpc**](/windows/desktop/Midl/ncalrpc).</span></span> <span data-ttu-id="0b3f8-113">Sicherheitsoptionen für andere Transporte werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-113">Security options for other transports are ignored.</span></span>

<span data-ttu-id="0b3f8-114">Der Client kann die folgenden Sicherheitsparameter der Bindung für den Named Pipe-Transport [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) oder [**Ncalrpc**](/windows/desktop/Midl/ncalrpc)zuordnen:</span><span class="sxs-lookup"><span data-stu-id="0b3f8-114">The client can associate the following security parameters to the binding for the named-pipe transport [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) or [**ncalrpc**](/windows/desktop/Midl/ncalrpc):</span></span>

-   <span data-ttu-id="0b3f8-115">Identifizierung, Identitätswechsel oder anonym.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-115">Identification, Impersonation, or Anonymous.</span></span> <span data-ttu-id="0b3f8-116">Gibt den verwendeten Sicherheitstyp an.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-116">Specifies the type of security used.</span></span> <span data-ttu-id="0b3f8-117">Der Standardwert ist der Identitätswechsel.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-117">The default is Impersonation.</span></span>
-   <span data-ttu-id="0b3f8-118">Dynamisch oder statisch.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-118">Dynamic or Static.</span></span> <span data-ttu-id="0b3f8-119">Bestimmt, ob einem Thread zugeordnete Sicherheitsinformationen eine Kopie der Sicherheitsinformationen sind, die zu dem Zeitpunkt erstellt werden, zu dem der Remote Prozedur Aufruf erfolgt (statisch), oder ein Zeiger auf die Sicherheitsinformationen (dynamisch).</span><span class="sxs-lookup"><span data-stu-id="0b3f8-119">Determines whether security information associated with a thread is a copy of the security information created at the time the remote procedure call is made (static) or a pointer to the security information (dynamic).</span></span>

    <span data-ttu-id="0b3f8-120">Statische Sicherheitsinformationen werden nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-120">Static security information does not change.</span></span> <span data-ttu-id="0b3f8-121">Die dynamische Einstellung gibt die aktuellen Sicherheitseinstellungen an, einschließlich der Änderungen, die nach dem Ausführen des Remote Prozedur Aufrufes vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-121">The dynamic setting reflects the current security settings, including changes made after the remote procedure call is made.</span></span> <span data-ttu-id="0b3f8-122">Bei [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np)ist die Standardeinstellung für Remote Named Pipe Verbindungen statisch, für lokale Named Pipe Verbindungen der Standardwert Dynamic.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-122">For [**ncacn\_np**](/windows/desktop/Midl/ncacn-np), the default for remote named pipe connections is static, for local named pipe connections the default is dynamic.</span></span>

-   <span data-ttu-id="0b3f8-123">**True** oder **false**.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-123">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="0b3f8-124">Gibt den Wert des Flag für die effektive Gültigkeit an.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-124">Specifies the value of the effective-only flag.</span></span> <span data-ttu-id="0b3f8-125">Der Wert **true** gibt an, dass nur tokenprivilegien, die zum Zeitpunkt des Aufrufes auf ON festgelegt sind, wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-125">A value of **TRUE** indicates that only token privileges set to on at the time of the call are effective.</span></span> <span data-ttu-id="0b3f8-126">Der Wert **false** gibt an, dass alle Berechtigungen verfügbar sind und dass Sie von der Anwendung geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-126">A value of **FALSE** indicates that all privileges are available and that the application can modify them.</span></span>

<span data-ttu-id="0b3f8-127">Eine beliebige Kombination dieser Einstellungen kann der Bindung zugewiesen werden, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="0b3f8-127">Any combination of these settings can be assigned to the binding, as shown in the following example:</span></span>

``` syntax
"Security=Identification Dynamic True"
"Security=Anonymous Static True"
"Security=Impersonation Static False"
```

<span data-ttu-id="0b3f8-128">Standardeinstellungen für Sicherheitsparameter variieren je nach Transportprotokoll.</span><span class="sxs-lookup"><span data-stu-id="0b3f8-128">Default security-parameter settings vary according to the transport protocol.</span></span>

<span data-ttu-id="0b3f8-129">Weitere Informationen zur Syntax der Endpunkt Optionen finden Sie unter [EndPoint](/windows/desktop/Midl/endpoint).</span><span class="sxs-lookup"><span data-stu-id="0b3f8-129">For additional information about the syntax of the endpoint options, see [endpoint](/windows/desktop/Midl/endpoint).</span></span>

 

 