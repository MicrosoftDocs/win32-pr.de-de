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
# <a name="which-security-provider-to-use"></a>Zu verwendende Sicherheitsanbieter

Alle anderen Dinge, die gleich sind, verwenden RPC \_ c \_ authn \_ GSS \_ Kerberos oder RPC \_ c \_ authn \_ GSS \_ Aushandlungen. Jeder stellt den skalierbaren und sichersten Dienst bereit. Wenn Sie die RPC \_ \_ -C-authn- \_ GSS- \_ Aushandlung auf dem Server verwenden, können Downlevelclients, z. b. NTLM-Clients, eine Verbindung mit dem Server herstellen. Wenn dies nicht erwünscht ist, beschränken Sie die Auswahl nur auf RPC \_ C \_ authn \_ GSS \_ Kerberos, oder wenden Sie [**rpcbindinginqauthclientex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) an, um zu bestimmen, welcher Sicherheitsanbieter vom Client verwendet wird, und verweigern Sie den Zugriff auf Clients mithilfe von NTLM. Die bevorzugte Methode zum Einrichten des Sicherheits Anbieters, den der Client verwendet, ist die Funktion [**rpcserverinqcallattributs**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) .

 

 




