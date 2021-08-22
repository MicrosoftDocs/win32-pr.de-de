---
title: Transportsicherheit
description: Obwohl dies nicht die bevorzugte Methode ist, können Sie die Sicherheitseinstellungen des Named Pipe-Transports verwenden, um Ihrer verteilten Anwendung Sicherheitsfeatures hinzuzufügen.
ms.assetid: faf48049-807c-4155-aa01-1947a0311a71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d92a0c9f0b31392d265c1c60bd201d088af8e8ff0b10ac4e09e274da92d2a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011208"
---
# <a name="transport-security"></a>Transportsicherheit

Obwohl dies nicht die bevorzugte Methode ist, können Sie die Sicherheitseinstellungen des Named Pipe-Transports verwenden, um Ihrer verteilten Anwendung Sicherheitsfeatures hinzuzufügen. Diese Sicherheitseinstellungen werden mit den Microsoft RPC-Funktionen verwendet, die mit den Präfixen [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) und [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)beginnen, und den Funktionen [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) und [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).

> [!Note]  
> Wenn Sie eine Anwendung ausführen, die ein Dienst ist, und NTLM aus Sicherheitsgründen verwenden, müssen Sie eine explizite Dienstabhängigkeit für Ihre Anwendung hinzufügen. Der Secur32.dll ruft den Dienststeuerungs-Manager (Service Control Manager, SCM) auf, um den NTLM-Sicherheitspaketdienst zu starten. Eine RPC-Anwendung, die ein Dienst ist und als System ausgeführt wird, muss sich jedoch auch an den SC wenden, es sei denn, sie stellt eine Verbindung mit einem anderen Dienst auf demselben Computer her.

 

 

 




