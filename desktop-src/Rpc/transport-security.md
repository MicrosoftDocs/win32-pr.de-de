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
# <a name="transport-security"></a>Transportsicherheit

Obwohl dies nicht die bevorzugte Methode ist, können Sie die Sicherheitseinstellungen verwenden, die der Named Pipe-Transport anbietet, um der verteilten Anwendung Sicherheitsfeatures hinzuzufügen. Diese Sicherheitseinstellungen werden mit den Microsoft RPC-Funktionen verwendet, die mit den Präfixen [**rpcserveruseprotabf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) und [**rpcserveruseallprotsqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)beginnen, und den Funktionen [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) und [**rpkrevertdeself**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).

> [!Note]  
> Wenn Sie eine Anwendung ausführen, bei der es sich um einen Dienst handelt, und Sie NTLM für die Sicherheit verwenden, müssen Sie eine explizite Dienst Abhängigkeit für die Anwendung hinzufügen. Der Secur32.dll ruft den Dienststeuerungs-Manager (SCM) auf, um den NTLM-Sicherheitspaket Dienst zu starten. Eine RPC-Anwendung, bei der es sich um einen Dienst handelt, der als System ausgeführt wird, muss auch den SC kontaktieren, es sei denn, es wird eine Verbindung mit einem anderen Dienst auf demselben Computer hergestellt.

 

 

 




