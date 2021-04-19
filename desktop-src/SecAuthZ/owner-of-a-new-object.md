---
description: Ein Objektbesitzer hat implizit Schreib \_ Zugriff auf das Objekt. Dies bedeutet, dass der Besitzer die Objekte der freigegebenen Zugriffs Steuerungs Liste (DACL) ändern und somit den Zugriff auf das Objekt steuern kann.
ms.assetid: 16144f38-3416-4594-b5e4-ca84fcbdddc9
title: Besitzer eines neuen Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f16124d84e17a075c78c676465ad753fcc12db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364064"
---
# <a name="owner-of-a-new-object"></a>Besitzer eines neuen Objekts

Der Besitzer eines Objekts hat implizit Schreib \_ Zugriff auf das Objekt. Dies bedeutet, dass der Besitzer die [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) des Objekts ändern kann und somit den Zugriff auf das Objekt steuern kann.

Der Besitzer eines neuen Objekts ist die Standard- [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID) des Besitzers aus dem [*primären*](/windows/desktop/SecGloss/p-gly) Token oder dem Identitätswechsel [*Token*](/windows/desktop/SecGloss/i-gly) des Erstellungs [*Prozesses*](/windows/desktop/SecGloss/p-gly). Um den Standard Besitzer in einem [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly)abzurufen oder festzulegen, müssen Sie die [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) -oder [**settokeninformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) -Funktion mit der tokenbesitzerstruktur aufrufen. [**\_**](/windows/desktop/api/Winnt/ns-winnt-token_owner) Das System lässt nicht zu, dass der Standard Besitzer eines Tokens auf eine ungültige sid festgelegt wird, z. b. die SID des Kontos eines anderen Benutzers.

Ein Prozess, bei dem die SE \_ Take \_ Ownership-Berechtigung aktiviert ist, kann sich selbst als Besitzer eines Objekts festlegen. Ein Prozess, bei dem die Berechtigung "SE \_ Restore \_ Name" aktiviert ist, oder mit dem Schreib \_ Besitzer Zugriff auf das Objekt kann eine beliebige gültige Benutzer-oder Gruppen-SID als Besitzer eines Objekts festlegen.

 

 
