---
description: Ein Zugriffstoken ist ein Objekt, das den Sicherheitskontext eines Prozesses oder Threads beschreibt.
ms.assetid: 350159c9-2399-427a-ba44-c897a9664299
title: Zugriffstoken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0993c1f5aebab797ab28e61b36f59507e4d2f1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866003"
---
# <a name="access-tokens"></a>Zugriffstoken

Ein [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly) ist ein Objekt, das den [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) eines [*Prozesses*](/windows/desktop/SecGloss/p-gly) oder Threads beschreibt. Die Informationen in einem Token enthalten die Identität und die Berechtigungen des dem Prozess oder Thread zugeordneten Benutzerkontos. Wenn sich ein Benutzer anmeldet, überprüft das System das Kennwort des Benutzers, indem es mit in einer Sicherheitsdatenbank gespeicherten Informationen vergleicht. Wenn das Kennwort [*authentifiziert*](/windows/desktop/SecGloss/a-gly)ist, erstellt das System ein Zugriffs Token. Jeder Prozess, der für diesen Benutzer ausgeführt wird, verfügt über eine Kopie dieses Zugriffs Tokens.

Das System verwendet ein Zugriffs Token, um den Benutzer zu identifizieren, wenn ein Thread mit einem Sicherungs [fähigen Objekt](securable-objects.md) interagiert oder versucht, eine System Aufgabe auszuführen, für die Berechtigungen erforderlich sind. Zugriffs Token enthalten die folgenden Informationen:

-   Die [Sicherheits](security-identifiers.md) -ID (SID) für das Konto des Benutzers.
-   SIDs für die Gruppen, in denen der Benutzer Mitglied ist
-   Eine [*Anmelde-SID*](/windows/desktop/SecGloss/l-gly) zur Identifizierung der aktuellen [*Anmelde Sitzung*](/windows/desktop/SecGloss/l-gly) .
-   Eine Liste der [Berechtigungen](privileges.md) , die der Benutzer oder die Benutzergruppen innehat.
-   Eine Besitzer-SID
-   Die sid für die primäre Gruppe
-   Die Standard- [DACL](access-control-lists.md) , die das System verwendet, wenn der Benutzer ein Sicherungs fähiges Objekt erstellt, ohne eine [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) anzugeben.
-   Die Quelle des Zugriffs Tokens.
-   Ob das Token ein [*Primäres*](/windows/desktop/SecGloss/p-gly) Token [oder Identitäts](client-impersonation.md) Wechsel Token ist
-   Eine optionale Liste mit [einschränkenden SIDs](restricted-tokens.md) .
-   Aktuelle Identitätswechsel Ebenen
-   Weitere Statistiken

Jeder Prozess verfügt über ein [*primäres Token*](/windows/desktop/SecGloss/p-gly) , das den [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) des Benutzerkontos beschreibt, das dem Prozess zugeordnet ist. Standardmäßig verwendet das System das primäre Token, wenn ein Thread des Prozesses mit einem Sicherungs fähigen Objekt interagiert. Darüber hinaus kann ein Thread die Identität eines Client Kontos annehmen. Der Identitätswechsel ermöglicht es dem Thread, mit Sicherungs fähigen Objekten zu interagieren, indem er den Sicherheitskontext des Clients verwendet. Ein Thread, der die Identität eines Clients annimmt, verfügt sowohl über ein primäres Token als auch über ein Identitäts [*Token*](/windows/desktop/SecGloss/i-gly).

Verwenden Sie die [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) -Funktion, um ein Handle für das primäre Token eines Prozesses abzurufen. Verwenden Sie die [**openthletotokenfunktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) , um ein Handle für das Identitätswechsel Token eines Threads abzurufen. Weitere Informationen finden Sie unter Identitäts [Wechsel.](client-impersonation.md)

Sie können die folgenden Funktionen verwenden, um Zugriffs Token zu bearbeiten.



| Funktion                                               | BESCHREIBUNG                                                                                                                                                            |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Leistungsgruppen"**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups)         | Ändert die Gruppeninformationen in einem Zugriffs Token.                                                                                                                      |
| [**"AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) | Aktiviert oder deaktiviert die Berechtigungen in einem Zugriffs Token. Es werden keine neuen Berechtigungen gewährt, und vorhandene Berechtigungen werden nicht widerrufen.                                                       |
| [**Checkeinkenmitgliedschaft**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership)   | Bestimmt, ob eine angegebene SID in einem angegebenen Zugriffs Token aktiviert ist.                                                                                             |
| [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) | Erstellt ein neues Token, bei dem es sich um eine eingeschränkte Version eines vorhandenen Tokens handelt. Das eingeschränkte Token kann über deaktivierte SIDs, gelöschte Berechtigungen und eine Liste eingeschränkter SIDs verfügen. |
| [**Duplicatetoken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)               | Erstellt ein neues Identitätswechsel Token, das ein vorhandenes Token dupliziert.                                                                                                   |
| [**Duplialisietokenex**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)           | Erstellt ein neues primäres Token oder Identitäts Token, das ein vorhandenes Token dupliziert.                                                                                  |
| [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)     | Ruft Informationen zu einem Token ab.                                                                                                                                   |
| [**Istokenrestricted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted)         | Bestimmt, ob ein Token über eine Liste mit einschränkenden SIDs verfügt.                                                                                                             |
| [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)           | Ruft ein Handle für das primäre Zugriffs Token für einen Prozess ab.                                                                                                          |
| [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)             | Ruft ein Handle für das Identitätswechsel-Zugriffs Token für einen Thread ab.                                                                                                     |
| [**SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken)               | Weist ein Identitätswechsel Token für einen Thread zu oder entfernt es.                                                                                                                |
| [**Setdekeninformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation)     | Ändert den Besitzer, die primäre Gruppe oder die standarddacl eines Tokens.                                                                                                               |



 

Die zugriffstokenfunktionen verwenden die folgenden Strukturen, um die Teile eines Zugriffs Tokens zu beschreiben.



| Struktur                                            | BESCHREIBUNG                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**\_tokensteuerelement**](/windows/desktop/api/Winnt/ns-winnt-token_control)              | Informationen, mit denen ein Zugriffs Token identifiziert wird.                                                          |
| [**\_standardmäßige \_ DACL für Token**](/windows/desktop/api/Winnt/ns-winnt-token_default_dacl)   | Die Standard-DACL, die das System in den Sicherheits Beschreibungen neuer, von einem Thread erstellten Objekte verwendet. |
| [**\_Tokengruppen**](/windows/desktop/api/Winnt/ns-winnt-token_groups)                | Gibt die SIDs und Attribute der Gruppen-SIDs in einem Zugriffs Token an.                               |
| [**\_Tokenbesitzer**](/windows/desktop/api/Winnt/ns-winnt-token_owner)                  | Die standardmäßige Besitzer-SID für die Sicherheits Deskriptoren neuer Objekte.                                    |
| [**\_primäre \_ Tokengruppe**](/windows/desktop/api/Winnt/ns-winnt-token_primary_group) | Die Standard-primäre Gruppen-sid für die Sicherheits Deskriptoren neuer Objekte.                            |
| [**\_Tokenberechtigungen**](/windows/desktop/api/Winnt/ns-winnt-token_privileges)        | Die einem Zugriffs Token zugeordneten Berechtigungen. Bestimmt außerdem, ob die Berechtigungen aktiviert sind.   |
| [**\_tokenquelle**](/windows/desktop/api/Winnt/ns-winnt-token_source)                | Die Quelle eines Zugriffs Tokens.                                                                        |
| [**\_tokenstatistik**](/windows/desktop/api/Winnt/ns-winnt-token_statistics)        | Einem Zugriffs Token zugeordnete Statistiken.                                                           |
| [**\_tokenbenutzer**](/windows/desktop/api/Winnt/ns-winnt-token_user)                    | Die SID des Benutzers, der einem Zugriffs Token zugeordnet ist.                                                  |



 

Die zugriffstokenfunktionen verwenden die folgenden Enumerationstypen.



| Enumerationstyp                                             | Bedeutung                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_tokeninformationsklasse \_**](/windows/desktop/api/Winnt/ne-winnt-token_information_class) | Identifiziert den Typ der Informationen, die von einem Zugriffs Token festgelegt oder abgerufen werden. |
| [**\_Tokentyp**](/windows/desktop/api/Winnt/ne-winnt-token_type)                            | Identifiziert ein Zugriffs Token als primäres oder Identitäts Token.                 |



 

 

 
