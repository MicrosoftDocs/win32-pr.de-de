---
description: Ein eingeschränktes Token ist ein primäres Zugriffstoken oder Identitätswechsel-Zugriffstoken, das von der CreateRestrictedToken-Funktion geändert wurde.
ms.assetid: 06580ab9-ff58-4aa9-bf88-9536a2e1981d
title: Eingeschränkte Token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f63402997d9e1304ca75ca117554ce52c3aa727f44b3b8316c28e1ecfcea45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912008"
---
# <a name="restricted-tokens"></a>Eingeschränkte Token

Ein eingeschränktes Token ist ein [*primäres*](/windows/desktop/SecGloss/p-gly) Zugriffstoken oder [*Identitätswechsel-Zugriffstoken,*](/windows/desktop/SecGloss/a-gly) das von der [**CreateRestrictedToken-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) geändert wurde. Ein [*Prozess*](/windows/desktop/SecGloss/p-gly) oder Thread, der im [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) eines eingeschränkten Tokens ausgeführt wird, ist in seiner Fähigkeit eingeschränkt, auf sicherungsfähige Objekte zuzugreifen oder privilegierte Vorgänge auszuführen. Die **CreateRestrictedToken-Funktion** kann ein Token auf folgende Weise einschränken:

-   Entfernen Sie [Berechtigungen](privileges.md) aus dem Token.
-   Wenden Sie das attribut deny-only auf SIDs im Token an, damit sie nicht für den Zugriff auf geschützte Objekte verwendet werden können. Weitere Informationen zum Attribut "Nur verweigern" finden Sie unter [SID-Attribute in einem Zugriffstoken.](sid-attributes-in-an-access-token.md)
-   Geben Sie eine Liste der einschränkenden SIDs an, die den Zugriff auf sicherungsfähige Objekte einschränken können.

Das System verwendet die Liste der einschränkenden SIDs, wenn es den Zugriff des Tokens auf ein sicherungsfähiges Objekt überprüft. Wenn ein eingeschränkter Prozess oder Thread versucht, auf ein sicherungsfähiges Objekt zuzugreifen, führt das System zwei Zugriffsüberprüfungen durch: eine mit den aktivierten SIDs des Tokens und eine andere mithilfe der Liste der einschränkenden SIDs. Der Zugriff wird nur gewährt, wenn beide Zugriffsüberprüfungen die angeforderten Zugriffsrechte zulassen. Weitere Informationen zu Zugriffsüberprüfungen finden Sie unter Steuern des Zugriffs auf ein Objekt durch [DACLs.](how-dacls-control-access-to-an-object.md)

Sie können ein eingeschränktes [*primäres Token*](/windows/desktop/SecGloss/p-gly) in einem Aufruf der [**CreateProcessAsUser-Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) verwenden. In der Regel muss der Prozess, der **CreateProcessAsUser** aufruft, über die SE \_ ASSIGNPRIMARYTOKEN \_ NAME-Berechtigung verfügen, die in der Regel nur von Systemcode oder von Diensten, die im LocalSystem-Konto ausgeführt werden, gehalten wird. Wenn der **CreateProcessAsUser-Aufruf** jedoch eine eingeschränkte Version des primären Tokens des Aufrufers angibt, ist diese Berechtigung nicht erforderlich. Dadurch können normale Anwendungen eingeschränkte Prozesse erstellen.

Sie können auch ein eingeschränktes primäres Token oder [*Identitätswechseltoken*](/windows/desktop/SecGloss/i-gly) in der [**Funktion ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) verwenden.

Um zu bestimmen, ob ein Token über eine Liste einschränkender SIDs verfügt, rufen Sie die [**IsTokenRestricted-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted) auf.

> [!Note]  
> Anwendungen, die eingeschränkte Token verwenden, sollten die eingeschränkte Anwendung auf anderen Desktops als dem Standarddesktop ausführen. Dies ist erforderlich, um einen Angriff einer eingeschränkten Anwendung mit **SendMessage** oder **PostMessage** auf uneingeschränkte Anwendungen auf dem Standarddesktop zu verhindern. Wechseln Sie bei Bedarf für Ihre Anwendung zwischen Desktops.

 

 

 
