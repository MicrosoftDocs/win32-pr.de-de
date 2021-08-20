---
description: Ein Zugriffstoken ist ein Objekt, das den Sicherheitskontext eines Prozesses oder Threads beschreibt.
ms.assetid: 350159c9-2399-427a-ba44-c897a9664299
title: Zugriffstoken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9067df376006f7f7b61dedadc074c23674b2278fb5c311794bbddd12256277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785390"
---
# <a name="access-tokens"></a>Zugriffstoken

Ein [*Zugriffstoken*](/windows/desktop/SecGloss/a-gly) ist ein Objekt, das den [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) eines [*Prozesses*](/windows/desktop/SecGloss/p-gly) oder Threads beschreibt. Die Informationen in einem Token umfassen die Identität und die Berechtigungen des Benutzerkontos, das dem Prozess oder Thread zugeordnet ist. Wenn sich ein Benutzer anmeldet, überprüft das System das Kennwort des Benutzers, indem es es mit den in einer Sicherheitsdatenbank gespeicherten Informationen vergleicht. Wenn das Kennwort [*authentifiziert*](/windows/desktop/SecGloss/a-gly)ist, erzeugt das System ein Zugriffstoken. Jeder Prozess, der im Namen dieses Benutzers ausgeführt wird, verfügt über eine Kopie dieses Zugriffstokens.

Das System verwendet ein Zugriffstoken, um den Benutzer zu identifizieren, wenn ein Thread mit einem [sicherungsfähigen Objekt](securable-objects.md) interagiert oder versucht, eine Systemaufgabe auszuführen, die Berechtigungen erfordert. Zugriffstoken enthalten die folgenden Informationen:

-   Die [Sicherheits-ID](security-identifiers.md) (SID) für das Konto des Benutzers
-   SIDs für die Gruppen, deren Mitglied der Benutzer ist
-   Eine [*Anmelde-SID,*](/windows/desktop/SecGloss/l-gly) die die aktuelle [*Anmeldesitzung*](/windows/desktop/SecGloss/l-gly) identifiziert
-   Eine Liste der [Berechtigungen](privileges.md) des Benutzers oder der Benutzergruppen
-   Eine Besitzer-SID
-   Die SID für die primäre Gruppe
-   Die [Standard-DACL,](access-control-lists.md) die das System verwendet, wenn der Benutzer ein sicherungsfähiges Objekt erstellt, ohne einen [*Sicherheitsdeskriptor*](/windows/desktop/SecGloss/s-gly) anzugeben
-   Die Quelle des Zugriffstokens
-   Gibt an, ob das Token ein [*primäres*](/windows/desktop/SecGloss/p-gly) Token oder [ein Identitätswechseltoken](client-impersonation.md) ist.
-   Eine optionale Liste der [einschränkenden SIDs](restricted-tokens.md)
-   Aktuelle Identitätswechselebenen
-   Andere Statistiken

Jeder Prozess verfügt über ein [*primäres Token,*](/windows/desktop/SecGloss/p-gly) das den [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) des benutzerkontos beschreibt, das dem Prozess zugeordnet ist. Standardmäßig verwendet das System das primäre Token, wenn ein Thread des Prozesses mit einem sicherungsfähigen Objekt interagiert. Darüber hinaus kann ein Thread die Identität eines Clientkontos annehmen. Der Identitätswechsel ermöglicht dem Thread die Interaktion mit sicherungsfähigen Objekten unter Verwendung des Sicherheitskontexts des Clients. Ein Thread, der die Identität eines Clients an sich nimmt, verfügt sowohl über ein primäres Token als auch über ein [*Identitätswechseltoken.*](/windows/desktop/SecGloss/i-gly)

Verwenden Sie die [**OpenProcessToken-Funktion,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) um ein Handle für das primäre Token eines Prozesses abzurufen. Verwenden Sie die [**OpenThreadToken-Funktion,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) um ein Handle für das Identitätswechseltoken eines Threads abzurufen. Weitere Informationen finden Sie unter [Identitätswechsel.](client-impersonation.md)

Sie können die folgenden Funktionen verwenden, um Zugriffstoken zu bearbeiten.



| Funktion                                               | Beschreibung                                                                                                                                                            |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups)         | Ändert die Gruppeninformationen in einem Zugriffstoken.                                                                                                                      |
| [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) | Aktiviert oder deaktiviert die Berechtigungen in einem Zugriffstoken. Es werden keine neuen Berechtigungen gewährt oder vorhandene widerrufen.                                                       |
| [**CheckTokenMembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership)   | Bestimmt, ob eine angegebene SID in einem angegebenen Zugriffstoken aktiviert ist.                                                                                             |
| [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) | Erstellt ein neues Token, das eine eingeschränkte Version eines vorhandenen Tokens ist. Das eingeschränkte Token kann über deaktivierte SIDs, gelöschte Berechtigungen und eine Liste der eingeschränkten SIDs verfügen. |
| [**DuplicateToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)               | Erstellt ein neues Identitätswechseltoken, das ein vorhandenes Token dupliziert.                                                                                                   |
| [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)           | Erstellt ein neues primäres Token oder Identitätswechseltoken, das ein vorhandenes Token dupliziert.                                                                                  |
| [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)     | Ruft Informationen zu einem Token ab.                                                                                                                                   |
| [**IsTokenRestricted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted)         | Bestimmt, ob ein Token über eine Liste einschränkender SIDs verfügt.                                                                                                             |
| [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)           | Ruft ein Handle für das primäre Zugriffstoken für einen Prozess ab.                                                                                                          |
| [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)             | Ruft ein Handle für das Identitätswechselzugriffstoken für einen Thread ab.                                                                                                     |
| [**SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken)               | Weist ein Identitätswechseltoken für einen Thread zu oder entfernt es.                                                                                                                |
| [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation)     | Ändert den Besitzer, die primäre Gruppe oder die Standard-DACL eines Tokens.                                                                                                               |



 

Die Zugriffstokenfunktionen verwenden die folgenden Strukturen, um die Teile eines Zugriffstokens zu beschreiben.



| Struktur                                            | Beschreibung                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**\_TOKENSTEUERELEMENT**](/windows/desktop/api/Winnt/ns-winnt-token_control)              | Informationen, die ein Zugriffstoken identifizieren.                                                          |
| [**\_ \_ TOKENSTANDARD-DACL**](/windows/desktop/api/Winnt/ns-winnt-token_default_dacl)   | Die Standard-DACL, die das System in den Sicherheitsbeschreibungen neuer Objekte verwendet, die von einem Thread erstellt werden. |
| [**\_TOKENGRUPPEN**](/windows/desktop/api/Winnt/ns-winnt-token_groups)                | Gibt die SIDs und Attribute der Gruppen-SIDs in einem Zugriffstoken an.                               |
| [**\_TOKENBESITZER**](/windows/desktop/api/Winnt/ns-winnt-token_owner)                  | Die Standardbesitzer-SID für die Sicherheitsbeschreibungen neuer Objekte.                                    |
| [**\_PRIMÄRE \_ TOKENGRUPPE**](/windows/desktop/api/Winnt/ns-winnt-token_primary_group) | Die standardmäßige primäre Gruppen-SID für die Sicherheitsbeschreibungen neuer Objekte.                            |
| [**\_TOKENPRIVILEGIEN**](/windows/desktop/api/Winnt/ns-winnt-token_privileges)        | Die einem Zugriffstoken zugeordneten Berechtigungen. Bestimmt auch, ob die Berechtigungen aktiviert sind.   |
| [**\_TOKENQUELLE**](/windows/desktop/api/Winnt/ns-winnt-token_source)                | Die Quelle eines Zugriffstokens.                                                                        |
| [**\_TOKENSTATISTIK**](/windows/desktop/api/Winnt/ns-winnt-token_statistics)        | Einem Zugriffstoken zugeordnete Statistiken.                                                           |
| [**\_TOKENBENUTZER**](/windows/desktop/api/Winnt/ns-winnt-token_user)                    | Die SID des Benutzers, der einem Zugriffstoken zugeordnet ist.                                                  |



 

Die Zugriffstokenfunktionen verwenden die folgenden Enumerationstypen.



| Enumerationstyp                                             | Bedeutung                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_ \_ TOKENINFORMATIONSKLASSE**](/windows/desktop/api/Winnt/ne-winnt-token_information_class) | Gibt den Typ der Informationen an, die von einem Zugriffstoken festgelegt oder abgerufen werden. |
| [**\_TOKENTYP**](/windows/desktop/api/Winnt/ne-winnt-token_type)                            | Identifiziert ein Zugriffstoken als primäres Token oder Identitätswechseltoken.                 |



 

 

 
