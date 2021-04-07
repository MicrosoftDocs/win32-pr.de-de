---
description: Zuordnung von Zertifikaten
ms.assetid: 4139f927-54f4-4968-a9eb-020401bb536d
title: Zuordnung von Zertifikaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a9ef8822d4f191ae37cdb998166fa54c2b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758257"
---
# <a name="mapping-certificates"></a>Zuordnung von Zertifikaten

> [!Note]  
> Die Informationen in diesem Thema gelten nur für Server, für die eine Client Authentifizierung erforderlich ist.

 

Wenn eine Serveranwendung eine Clientauthentifizierung durchführen muss, versucht Schannel automatisch, das vom Client angebotene Zertifikat einem Benutzerkonto zuzuordnen.

Nachdem der [*Sicherheitskontext*](../secgloss/s-gly.md) eingerichtet wurde, kann die Serveranwendung die [**querysecuritycontexttoken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) -Funktion verwenden, um ein [*Zugriffs Token*](../secgloss/a-gly.md) für das Benutzerkonto abzurufen, dem das [*Client Zertifikat*](../secgloss/c-gly.md) zugeordnet wurde. Der Server kann die Identität des Clients auch mit der Identität [**atesecuritycontext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) -Funktion annehmen.

Weitere Informationen zur Authentifizierung finden Sie unter [Durchführen der Authentifizierung mithilfe von SChannel](performing-authentication-using-schannel.md).

 

 
