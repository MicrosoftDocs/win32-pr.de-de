---
description: Zuordnen von Zertifikaten
ms.assetid: 4139f927-54f4-4968-a9eb-020401bb536d
title: Zuordnen von Zertifikaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f671afa6278da49427d0f7b49f78895198333e24d135383207b359846216638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921839"
---
# <a name="mapping-certificates"></a>Zuordnen von Zertifikaten

> [!Note]  
> Die Informationen in diesem Thema gelten nur für Server, die eine Clientauthentifizierung erfordern.

 

Wenn eine Serveranwendung eine Clientauthentifizierung durchführen muss, versucht Schannel automatisch, das vom Client angebotene Zertifikat einem Benutzerkonto zuzuordnen.

Nachdem der [*Sicherheitskontext*](../secgloss/s-gly.md) eingerichtet wurde, kann die Serveranwendung die [**QuerySecurityContextToken-Funktion**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) verwenden, um ein [*Zugriffstoken*](../secgloss/a-gly.md) für das Benutzerkonto abzurufen, dem das [*Clientzertifikat*](../secgloss/c-gly.md) zugeordnet wurde. Außerdem kann der Server die [**ImpersonateSecurityContext-Funktion**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) verwenden, um die Identität des Clients zu annehmen.

Weitere Informationen zur Authentifizierung finden Sie unter [Durchführen der Authentifizierung mithilfe von Schannel](performing-authentication-using-schannel.md).

 

 
