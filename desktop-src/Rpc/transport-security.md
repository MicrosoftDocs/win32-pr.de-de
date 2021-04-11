---
title: Transportsicherheit
description: Obwohl dies nicht die bevorzugte Methode ist, können Sie die Sicherheitseinstellungen verwenden, die der Named Pipe-Transport anbietet, um der verteilten Anwendung Sicherheitsfeatures hinzuzufügen.
ms.assetid: faf48049-807c-4155-aa01-1947a0311a71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d129b5a373ed7304c142c66dd0e8b2d4e9035416
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310779"
---
# <a name="transport-security"></a><span data-ttu-id="564ad-103">Transportsicherheit</span><span class="sxs-lookup"><span data-stu-id="564ad-103">Transport Security</span></span>

<span data-ttu-id="564ad-104">Obwohl dies nicht die bevorzugte Methode ist, können Sie die Sicherheitseinstellungen verwenden, die der Named Pipe-Transport anbietet, um der verteilten Anwendung Sicherheitsfeatures hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="564ad-104">Although this is not the preferred method, you can use the security settings that the named-pipe transport offers to add security features to your distributed application.</span></span> <span data-ttu-id="564ad-105">Diese Sicherheitseinstellungen werden mit den Microsoft RPC-Funktionen verwendet, die mit den Präfixen [**rpcserveruseprotabf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) und [**rpcserveruseallprotsqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)beginnen, und den Funktionen [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) und [**rpkrevertdeself**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).</span><span class="sxs-lookup"><span data-stu-id="564ad-105">These security settings are used with the Microsoft RPC functions that start with the prefixes [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) and [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), and the functions [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) and [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).</span></span>

> [!Note]  
> <span data-ttu-id="564ad-106">Wenn Sie eine Anwendung ausführen, bei der es sich um einen Dienst handelt, und Sie NTLM für die Sicherheit verwenden, müssen Sie eine explizite Dienst Abhängigkeit für die Anwendung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="564ad-106">If you are running an application that is a service and you are using NTLM for security, you must add an explicit service dependency for your application.</span></span> <span data-ttu-id="564ad-107">Der Secur32.dll ruft den Dienststeuerungs-Manager (SCM) auf, um den NTLM-Sicherheitspaket Dienst zu starten.</span><span class="sxs-lookup"><span data-stu-id="564ad-107">The Secur32.dll will call the Service Control Manager (SCM) to begin the NTLM security package service.</span></span> <span data-ttu-id="564ad-108">Eine RPC-Anwendung, bei der es sich um einen Dienst handelt, der als System ausgeführt wird, muss auch den SC kontaktieren, es sei denn, es wird eine Verbindung mit einem anderen Dienst auf demselben Computer hergestellt.</span><span class="sxs-lookup"><span data-stu-id="564ad-108">However, an RPC application that is a service and is running as a system, must also contact the SC unless it is connecting to another service on the same computer.</span></span>

 

 

 




