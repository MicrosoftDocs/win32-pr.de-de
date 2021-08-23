---
title: Welcher Sicherheitsanbieter verwendet werden soll
description: Wenn alles andere gleich ist, verwenden Sie RPC \_ C \_ AUTHN \_ GSS \_ KERBEROS oder RPC C \_ \_ AUTHN \_ GSS \_ NEGOTIATE.
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b89bdb10eb95952183b2a992fd12a668e79b0716f3c453f597d2241323c4ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010448"
---
# <a name="which-security-provider-to-use"></a>Welcher Sicherheitsanbieter verwendet werden soll

Wenn alles andere gleich ist, verwenden Sie RPC \_ C \_ AUTHN \_ GSS \_ KERBEROS oder RPC C \_ \_ AUTHN \_ GSS \_ NEGOTIATE. Jede bietet den skalierbarsten und sichersten Dienst. Wenn Sie RPC C AUTHN GSS NEGOTIATE auf dem Server verwenden, ermöglicht dies, dass Downlevelclients, z. B. \_ \_ \_ \_ NTLM-Clients, eine Verbindung mit Ihrem Server herstellen können. Wenn dies nicht erwünscht ist, beschränken Sie entweder die Auswahl auf RPC C AUTHN GSS KERBEROS, oder rufen Sie \_ \_ \_ \_ [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) auf, um zu bestimmen, welchen Sicherheitsanbieter der Client verwendet, und den Zugriff auf Clients mit NTLM zu verweigern. Die bevorzugte Methode zum Festlegen des Vom Client verwendeten Sicherheitsanbieters ist die [**RpcServerInqCallAttributes-Funktion.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa)

 

 




