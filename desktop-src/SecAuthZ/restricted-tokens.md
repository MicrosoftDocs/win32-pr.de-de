---
description: Ein eingeschränktes Token ist ein primäres Token oder ein Identitätswechsel-Zugriffs Token, das von der Funktion "| aterestrictedtoken" geändert wurde.
ms.assetid: 06580ab9-ff58-4aa9-bf88-9536a2e1981d
title: Eingeschränkte Token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee8e6c89915e3edd0a9206f84a0d3d5697a3cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129912"
---
# <a name="restricted-tokens"></a>Eingeschränkte Token

Ein eingeschränktes Token ist ein [*Primäres*](/windows/desktop/SecGloss/p-gly) Token oder ein Identitätswechsel- [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly) , das von der Funktion "| [**aterestrictedtoken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) " geändert wurde. Ein [*Prozess*](/windows/desktop/SecGloss/p-gly) oder der Identitätswechsel in einem Thread, der im [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) eines eingeschränkten Tokens ausgeführt wird, ist darauf beschränkt, auf Sicherungs fähige Objekte zuzugreifen oder privilegierte Vorgänge auszuführen. Die **Funktion "** Funktion" kann ein Token auf folgende Weise einschränken:

-   Entfernen Sie [Berechtigungen](privileges.md) aus dem Token.
-   Wenden Sie das Attribut Deny auf SIDs im Token an, damit Sie nicht für den Zugriff auf gesicherte Objekte verwendet werden können. Weitere Informationen zum Deny-only-Attribut finden Sie unter [SID-Attribute in einem Zugriffs Token](sid-attributes-in-an-access-token.md).
-   Geben Sie eine Liste mit einschränkenden SIDs an, die den Zugriff auf Sicherungs fähige Objekte einschränken kann.

Das System verwendet die Liste der einschränkenden SIDs, wenn der Zugriff des Tokens auf ein Sicherungs fähiges Objekt überprüft wird. Wenn ein eingeschränkter Prozess oder Thread versucht, auf ein Sicherungs fähiges Objekt zuzugreifen, führt das System zwei Zugriffs Überprüfungen durch: einen, der die aktivierten SIDs des Tokens verwendet, und einen anderen, der die Liste der einschränkenden SIDs verwendet. Der Zugriff wird nur gewährt, wenn beide Zugriffs Überprüfungen die angeforderten Zugriffsrechte zulassen. Weitere Informationen zu Zugriffs Überprüfungen finden [Sie Untersteuern des Zugriffs auf ein Objekt durch DACLs](how-dacls-control-access-to-an-object.md).

Sie können ein eingeschränktes [*primäres Token*](/windows/desktop/SecGloss/p-gly) in einem aufzurufenden Befehl an die Funktion "| [**ateprocessasuser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) " verwenden. In der Regel muss der Prozess, der " **itateprocessasuser** " aufruft, die namens Berechtigung "SE zuweist" \_ \_ , die in der Regel nur durch Systemcode oder Dienste, die im Konto "LocalSystem" ausgeführt werden, enthalten. Wenn der Aufruf von "| **ateprocessasuser** " jedoch eine eingeschränkte Version des primären Tokens des Aufrufers angibt, ist dieses Privileg nicht erforderlich. Dadurch können normale Anwendungen eingeschränkte Prozesse erstellen.

Sie können in der Identität [**ateloggedonuser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) -Funktion auch ein eingeschränktes primär-oder Identitäts [*Token*](/windows/desktop/SecGloss/i-gly) verwenden.

Um zu ermitteln, ob ein Token über eine Liste mit einschränkenden SIDs verfügt, müssen Sie die [**istokenrestricted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted) -Funktion aufzurufen.

> [!Note]  
> Anwendungen, die eingeschränkte Token verwenden, sollten die eingeschränkte Anwendung auf Desktops außer dem Standard Desktop ausführen. Dies ist erforderlich, um Angriffe durch eine eingeschränkte Anwendung, die **SendMessage** oder **PostMessage**, an unbeschränkte Anwendungen auf dem Standard Desktop zu verhindern. Wechseln Sie ggf. zwischen den Desktops für Ihre Anwendung.

 

 

 
