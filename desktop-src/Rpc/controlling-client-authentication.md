---
title: Steuern der Client Authentifizierung
description: Die beste Methode zum Authentifizieren eines Clients besteht darin, eine Sicherheits Rückruffunktion mithilfe der RpcServerRegisterIf2-oder RpcServerRegisterIfEx-Funktion zu installieren. akzeptiert eine Sicherheits Rückruffunktion als Argument.
ms.assetid: 3e858a71-9190-44a3-bc63-08cfbd02d443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3508e99b351cd57fb67a3727710b60562ffe25dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856004"
---
# <a name="controlling-client-authentication"></a>Steuern der Client Authentifizierung

Die beste Methode zum Authentifizieren eines Clients besteht darin, eine Sicherheits Rückruffunktion mithilfe der [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) -oder [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) -Funktion zu installieren. akzeptiert eine Sicherheits Rückruffunktion als Argument. Wenn die Sicherheits Rückruffunktion aufgerufen wird, nehmen Sie die erforderlichen Überprüfungen vor. Die Attribute für die Verbindung, die Identität des Aufrufers oder beides können geprüft werden. Um die Attribute einer Verbindung zu überprüfen, rufen Sie die [**rpcserverinqcallattribute**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) -oder [**rpcbindinginqauthclient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) -Funktion auf. Dadurch wird das Filtern von Clients ermöglicht, die nicht authentifiziert sind, Clients, die einen bestimmten Sicherheitsanbieter verwenden, oder Clients, die keinen sicheren Schutz verwenden (z. b. Datenschutz).

Um den Zugriff auf eine Teilmenge der authentifizierten Benutzer zuzulassen, verwenden Sie [**rpcgetauthorizationcontextforclient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient). Diese Funktion gibt einen Authz-Client Kontext zurück, der verwendet werden kann, um sehr ausgereifte Zugriffs Überprüfungen durchzuführen. Diese Methode kann z. b. verwendet werden, um den Zugriff nur für die Vizepräsidenten in einer Organisation während der normalen Geschäftszeiten zuzulassen, und für den CEO während einer beliebigen Stunde, indem Active Directory Services verwendet wird, um dem Titel einen Benutzernamen zuzuordnen. Der Benutzer kann einen Identitätswechsel durchgeführt werden, und der zugehörige Name wird abgerufen. Nachdem Ihre Identität bekannt ist, können alle gewünschten Überprüfungen vorgenommen werden.

 

 




