---
title: Steuern der Clientauthentifizierung
description: Die beste Methode zum Authentifizieren eines Clients ist die Installation einer Sicherheitsrückruffunktion mithilfe der RpcServerRegisterIf2- oder RpcServerRegisterIfEx-Funktion. beide akzeptiert eine Sicherheitsrückruffunktion als Argument.
ms.assetid: 3e858a71-9190-44a3-bc63-08cfbd02d443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb00a03740d99b137f97b085525e4c7232483dc15db487daf486ad51560b4427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931237"
---
# <a name="controlling-client-authentication"></a>Steuern der Clientauthentifizierung

Die beste Methode zum Authentifizieren eines Clients ist die Installation einer Sicherheitsrückruffunktion mithilfe der [**RpcServerRegisterIf2-**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) oder [**RpcServerRegisterIfEx-Funktion.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) beide akzeptiert eine Sicherheitsrückruffunktion als Argument. Wenn die Sicherheitsrückruffunktion aufgerufen wird, nehmen Sie die erforderlichen Überprüfungen vor. Die Attribute für die Verbindung, die Identität des Aufrufers oder beides können überprüft werden. Rufen Sie die [**Funktion RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) oder [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) auf, um die Attribute einer Verbindung zu überprüfen. Dies ermöglicht das Filtern von Clients, die nicht authentifiziert sind, Clients, die einen bestimmten Sicherheitsanbieter verwenden, oder Clients, die nicht stark genug Schutz verwenden (z. B. Datenschutz).

Verwenden Sie [**RpcGetAuthorizationContextForClient,**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient)um den Zugriff auf eine Teilmenge der authentifizierten Benutzer zuzulassen. Diese Funktion gibt einen Autorhz-Clientkontext zurück, der verwendet werden kann, um sehr komplexe Zugriffsüberprüfungen durchzuführen. Diese Methode kann z. B. verwendet werden, um den Zugriff nur für die Vice Presidents in einer Organisation während der normalen Geschäftszeiten und für den CEO während einer stundelangen Verwendung von Active Directory-Diensten zuzulassen, um ihrem Titel einen Benutzernamen zuzuordnen. Die Identität des Benutzers kann angenommen und sein Name abgerufen werden. Sobald ihre Identität bekannt ist, können alle gewünschten Überprüfungen durchgeführt werden.

 

 




